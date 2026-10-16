---
name: revisor-consistencia
description: Revisa la consistencia de redacción de un texto largo antes de publicarlo: un término por concepto, nombres y marcas escritos igual, formato de números, fechas y monedas, promesas de la intro o del título contra lo que entrega el cuerpo, tabla ↔ texto ↔ FAQ ↔ meta description, fichas y listas parejas, siglas, registro (tú/vos/usted) y concordancia. También comprueba que una reescritura de estilo no cambió cifras ni afirmaciones. Úsala cuando pidan "revisar consistencia", "revisar inconsistencias", "copyedit", "corrección de estilo", "que todo cuadre" o como paso después de human-writer y human-reviewer. No revisa hechos ni tics de IA. Parte del Kit Human Writer.
---

# Revisor de consistencia

Tercera mirada sobre el texto. Responde una sola pregunta: **¿el texto dice lo mismo de la misma forma, de principio a fin?**

| Skill | Pregunta que responde |
|---|---|
| human-writer | ¿Cómo lo escribo bien? |
| human-reviewer | ¿Qué tics de IA tiene y dónde? |
| **revisor-consistencia** (esta) | ¿Dice lo mismo de la misma forma de principio a fin? |
| verificador-factual (después de esta) | ¿Cada afirmación dice lo que su fuente permite? |

**Entrada:** el texto. Si existen, también: el glosario o guía de estilo del usuario, otras piezas ya publicadas de la misma marca y la tabla "Cambios de human-writer".
**Salida:** un informe con hallazgos. **Propone; aplica cambios solo si se lo piden.** Nunca deja notas dentro del texto.

## Antes de empezar

- Si el usuario tiene glosario, guía de estilo o manual de marca, esa es la fuente de verdad para los términos. Pídelo si no está a la vista y la pieza es de una marca.
- Si no hay glosario, el criterio es: el término que más se usa en el propio texto, salvo que sea incorrecto. Los casos dudosos van como "decisión pendiente", no se eligen.

## Comprobaciones

Cada hallazgo se cita textualmente. Si una comprobación no encuentra nada, no se menciona.

### 1. Términos

- **Dentro de la pieza:** un concepto escrito de dos formas ("email" y "correo", "clientes" y "usuarios" para lo mismo, "app" y "aplicación"). Se corrige al glosario o se marca como decisión pendiente.
- **Entre piezas de la misma marca:** si hay otras piezas publicadas a la vista, el mismo concepto escrito distinto. Solo se reporta.
- **Nombres propios y marcas:** misma grafía siempre (WhatsApp, Mercado Pago, YouTube, iPhone).

### 2. Números, fechas y unidades

- Un solo separador de miles y decimales en toda la pieza, el del país del lector (1.200 o 1,200; 3,5 o 3.5). Un mismo número con dos formatos es hallazgo.
- Porcentajes siempre igual ("12%" o "12 %", no ambos).
- Monedas con el símbolo o código en la misma posición, y aclaradas si el lector puede confundirlas ($ en México no es $ en Argentina).
- Fechas y horas con un solo formato. Meses y días en minúscula.
- Números en cifra o en letra con un criterio parejo.

### 3. Promesa vs entrega

- El título, la intro, el resumen o una transición anuncian algo ("cinco errores", "al final verás un ejemplo", "comparamos precios") → comprobar que el cuerpo lo cumple, en todos los casos.
- El conteo del título y de las listas cuadra ("7 herramientas" y hay 7).
- Cada heading entrega lo que promete. Si el subtítulo dice "caso real" y la sección es genérica, es hallazgo.

### 4. Coherencia entre partes de la pieza

- Tabla ↔ texto: el mismo dato con la misma forma ("No disponible" en la tabla y "no especificado" en el texto es hallazgo).
- Cuerpo ↔ FAQ: la FAQ no dice más ni menos que el cuerpo sobre lo mismo.
- Título ↔ meta description ↔ primer párrafo: misma promesa, mismo país, mismo público.
- Enlace ↔ texto del enlace: el ancla describe la página de destino.
- Dos cifras o plazos distintos para lo mismo en dos partes de la pieza: hallazgo alto.

### 5. Fichas y listas

- Fichas repetidas (productos, herramientas, planes) con las mismas etiquetas y en el mismo orden. Si un campo no aplica, va con "No aplica" o "No especificado", no desaparece.
- Cada etiqueta contiene lo que dice ("Precio:" tiene un precio, no una descripción).
- Bullets de una misma lista con la misma estructura (todos empiezan con verbo conjugado, o todos con sustantivo).
- Puntuación de listas pareja: todos con punto final o ninguno.

### 6. Arranques que dependen del heading

En piezas que se leen por fragmentos (SEO, FAQ, documentación), la primera oración de cada sección debe entenderse sin leer el título. Se marcan arranques como "Es la herramienta…", "Porque…", "Depende…", "Esto…" sin sujeto. En FAQ, "Sí." o "No." se admiten si la oración siguiente nombra el sujeto.

En piezas que se leen de corrido (newsletter, ensayo, guion) esta comprobación no aplica.

### 7. Siglas

- Toda sigla se desarrolla la primera vez, salvo las que el lector conoce (SMS, PDF, IA, CRM en un público de negocios).
- Una vez desarrollada, se usa siempre igual.

### 8. Gramática y registro

- Un solo registro: tuteo, voseo o usted, sin mezclar "tienes" y "tenés".
- Concordancia de género y número, sobre todo en tablas y en listas largas.
- Mayúsculas según la RAE: sin Title Case en headings, sin mayúscula después de dos puntos salvo cita o nombre propio.
- Verbos intransitivos usados como transitivos ("crecer las ventas" → "hacer crecer las ventas", "aumentar las ventas").

### 9. Control de la reescritura de estilo

Si existe la tabla "Cambios de human-writer": ¿algún cambio tocó una cifra, un alcance ("hasta", "más de"), una cita, un nombre o lo que algo hace? Si sí, es hallazgo **alto** y se propone revertir. Las secciones marcadas con más del 20% de oraciones cambiadas se pasan a `verificador-factual` para que las relea enteras.

## Severidad

- **Alto:** cambia el significado o contradice otra parte de la pieza (tabla ≠ texto, FAQ ≠ cuerpo, promesa incumplida, dos cifras para lo mismo, reescritura que tocó un dato).
- **Medio:** término del glosario incumplido, mezcla de términos, formato numérico de otro país, ficha con campos distintos, arranque que depende del heading, sigla sin desarrollar, registro mezclado.
- **Bajo:** puntuación, mayúsculas, estructura de bullets.

Si hay más de 15 hallazgos, los bajos van agrupados en una línea.

## Informe

```
## Revisión de consistencia
País / variante: … | Glosario: [sí, cuál | no]

| Sev | # | Ubicación | Texto citado | Problema | Corrección |

Decisiones pendientes: [concepto → formas encontradas]
Inconsistencias con otras piezas de la marca: [pieza → término] o "no revisado"
Control de la reescritura: [OK | cambios a revertir]
```

## Qué NO hacer

- No reescribir por estilo: eso es de `human-writer`.
- No corregir hechos, cifras ni fuentes: se reportan para `verificador-factual`.
- No elegir un término que el glosario o el usuario no decidió.
- No editar piezas ya publicadas: sus inconsistencias solo se reportan.

---
Parte del **Kit Human Writer** de **Sebastian Avila AI**.
