---
name: verificador-factual
description: Revisión factual de un texto antes de publicarlo: extrae cada afirmación verificable (cifras, fechas, capacidades de un producto, datos de competidores, normas, estudios, citas, relaciones de causa) y la contrasta con su fuente. Marca lo que no tiene fuente, lo que la fuente no dice, lo que el texto afirma con más fuerza que la fuente, lo que está fuera de alcance, las inferencias presentadas como hecho, la causalidad no demostrada, las atribuciones vagas ("según expertos") y los datos desactualizados. Úsala cuando pidan "fact-check", "verificar fuentes", "revisar datos", "chequear claims", "¿esto es cierto?" o como último paso del Kit Human Writer antes de publicar. No revisa estilo ni consistencia de términos.
---

# Verificador factual

El último filtro antes de publicar. Responde una sola pregunta: **¿cada afirmación dice exactamente lo que su fuente permite, ni más ni menos?**

Existe porque una pasada de estilo no detecta este problema. Un texto puede no tener un solo tic de IA y aun así decir "certificado" donde la fuente dice "declara", o "gracias a X" donde solo hay una coincidencia en el tiempo.

| Skill | Pregunta que responde |
|---|---|
| human-writer | ¿Cómo lo escribo bien? |
| human-reviewer | ¿Qué tics de IA tiene y dónde? |
| revisor-consistencia | ¿Dice lo mismo de la misma forma de principio a fin? |
| **verificador-factual** (esta) | ¿Cada afirmación dice lo que su fuente permite? |

**Entrada:** el texto. Si existen, también: las fuentes o notas que usó el autor, la información oficial de la marca (web, ficha de producto, manual, brief), y la tabla "Cambios de human-writer".
**Salida:** un informe. **Propone; aplica cambios solo si se lo piden.** Nunca deja notas dentro del texto.

## Fuentes de verdad

Antes de empezar, identifica qué cuenta como fuente:

1. **Sobre la marca del autor** (qué hace su producto, sus cifras, sus clientes): lo que el usuario entregue (brief, web oficial, ficha, manual). Si no hay nada a la vista y el texto afirma capacidades o cifras propias, pide la fuente. Mientras tanto, esas afirmaciones quedan como **"confirmar con el autor"**, no como OK.
2. **Sobre terceros** (competidores, mercado, normas, estudios): la fuente original, abierta y leída.

Jerarquía para datos externos: regulador o gobierno → documentación oficial → estudio o caso primario → publicación especializada → prensa general → blog o fuente secundaria. Si solo hay una fuente débil para un dato importante, se reporta y se sugiere una mejor.

## Escalera de evidencia

| Nivel | Qué es | Uso |
|---|---|---|
| E1 | Caso propio con cliente o cohorte + métrica + punto de partida + periodo | Ideal para afirmaciones principales |
| E2 | Métrica interna con metodología, sin cliente nombrado | Válida |
| E3 | Fuente primaria externa: regulador, organismo, estadística oficial | Ideal para contexto |
| E4 | Publicación especializada reconocida | Aceptable |
| E5 | Afirmación de una empresa sobre sí misma, sin metodología | Solo atribuida ("según su sitio") |
| E6 | Afirmación sin fuente | No es evidencia: brecha |

## Proceso

1. **Inventario.** Recorre todo el texto (cuerpo, tablas, fichas, FAQ, títulos, meta description, pies de imagen) y extrae cada afirmación verificable: cifras, fechas, capacidades de un producto, datos de terceros, normas y su alcance, estudios, citas textuales, relaciones de causa. Las opiniones marcadas como tales y las recomendaciones de método ("conviene empezar por…") no entran.
2. **Contraste.** Para cada afirmación: fuente → qué dice la fuente → nivel de evidencia → veredicto.
3. **Enlaces.** Si tienes herramienta de búsqueda o lectura web, abre cada enlace y comprueba que exista, que el autor, la entidad y la fecha coincidan, y que diga lo atribuido. Sin herramienta: **"no verificado"**, nunca "OK". Que un enlace abra no prueba que respalde la frase.
4. **Secciones reescritas.** Si la tabla de `human-writer` marca secciones con más del 20% de oraciones cambiadas, relee esas secciones enteras contra las fuentes.
5. **Informe.** Solo los veredictos distintos de OK, más el conteo total.

## Veredictos

| Veredicto | Qué significa | Severidad |
|---|---|---|
| OK | La fuente dice lo mismo, con la misma fuerza | Ninguna |
| **Sin fuente** | No hay fuente a la vista ni se encuentra | Crítico si es una cifra o capacidad propia, una norma o una cita; Alto si es contexto |
| **Referencia inventada** | El estudio, informe, autor o enlace no existe, o apunta a otra cosa | Crítico |
| **Fuente no lo dice** | La fuente existe pero no contiene la afirmación | Crítico |
| **Más fuerte que la fuente** | La fuente dice "puede", "declara", "en algunos casos", "hasta", y el texto dice "garantiza", "es", "siempre", "certificado" | Alto |
| **Fuera de alcance** | La fuente es real, pero habla de otro país, sector, público, periodo o sujeto | Alto |
| **Inferencia como hecho** | Conclusión del autor redactada como dato ("esto demuestra que…") | Alto |
| **Causalidad no demostrada** | "Gracias a X, Y", "lo que permitió", cuando la fuente solo muestra secuencia o correlación | Alto |
| **Atribución vaga** | "Los expertos coinciden", "diversos estudios", "según analistas" sin nombre, lugar ni fecha | Alto |
| **Precisión falsa** | Cifra demasiado conveniente o redonda sin metodología ("ahorra 20 horas", "mejora un 30%") | Alto |
| **Desactualizado** | Dato que cambia con el tiempo (precios, funciones de un competidor, normas, estadísticas) sin fecha o con más de un año | Medio |
| **Confirmar con el autor** | Afirmación sobre la propia marca sin fuente a la vista | Medio (bloquea publicar hasta confirmar) |

## Comprobaciones específicas

### Capacidades de un producto (propio o ajeno)

- Cada verbo se compara con la fuente. Un sinónimo puede ser una capacidad nueva: "registra" no es "audita", "se conecta con" no es "se integra de forma nativa", "sugiere" no es "decide".
- Si la fuente dice lo que el producto **no** hace, una frase que lo contradiga es crítica.
- Certificaciones y cumplimiento: "declara cumplir ISO 27001" o "según su sitio", nunca "certificado" salvo que se haya visto el certificado.

### Cifras

- Cifra, unidad, población y periodo iguales a la fuente. El texto no puede agregar población ("en todas las empresas"), periodo ("en un mes") ni causa que la fuente no tiene.
- "Hasta 40%" no es "40%". "Más de 1.000" no es "1.000".

### Clientes y testimonios

- Un cliente nombrado necesita fuente pública o autorización del autor.
- Una cita textual va igual a la fuente, con nombre y cargo correctos. Si se parafraseó, no lleva comillas.

### Competidores y terceros

- Cada dato lleva "según su sitio", "declara" o equivalente, con enlace y fecha de consulta.
- Si se comparan opciones para un país, cada opción tiene que operar en ese país según su fuente.
- Las debilidades atribuidas a un competidor se apoyan en lo que su fuente dice o no dice, no en suposiciones.

### Normas y leyes

- Nombre exacto, organismo y enlace oficial.
- **A quién aplica:** una norma para bancos no se extiende a comercios; una ley de un país no aplica en otro.
- **Qué exige exactamente:** "documentar los acuerdos" no es "grabar cada llamada". Las buenas prácticas se presentan como tales, no como obligación.
- Plazos, montos y horarios copiados de la fuente oficial, no de la prensa.

### Datos de mercado y estudios

- Preferir el organismo oficial o el estudio original a la nota de prensa que lo cita.
- Revisar quién hizo el estudio: un informe de una empresa sobre su propio mercado es E5, no E3.

## Informe

```
## Revisión factual
Afirmaciones revisadas: N (marca propia: n, terceros: n, normas: n, mercado: n) | Enlaces abiertos: n de n

| Sev | Ubicación | Afirmación (cita) | Fuente | Qué dice la fuente | Veredicto | Corrección |

No verificado (sin herramienta o fuente caída): [lista]
Para confirmar con el autor: [afirmación → dónde aparece]
Secciones releídas por reescritura: [lista o "ninguna"]
```

Si hay más de 15 hallazgos, los medios van agrupados en una línea.

La corrección propuesta siempre es una de estas: atribuir ("según…"), bajar la fuerza ("puede", "hasta", "en algunos casos"), acotar el alcance (país, periodo, público), marcar como opinión, o quitar la frase.

## Qué NO hacer

- No dar por buena una afirmación porque "suena razonable" o porque el enlace abre.
- No inventar una fuente de reemplazo. Si no existe, la afirmación se suaviza o se quita.
- No resolver un hueco sobre la marca con una inferencia: va a "confirmar con el autor".
- No subir la fuerza de una frase para que coincida con el título.
- No reescribir por estilo ni unificar términos (eso es de `human-writer` y `revisor-consistencia`).

---
Parte del **Kit Human Writer** de **Sebastian Avila AI**. Capa factual basada en parte en la guía "Signs of AI writing" de Wikipedia (WikiProject AI Cleanup).
