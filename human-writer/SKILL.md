---
name: human-writer
description: Redacta o reescribe piezas largas para publicar (blogs, artículos, newsletters, publirreportajes, copy de landing, guiones, posts largos) con voz propia, datos concretos y ritmo natural, sin tics de IA. Úsala siempre que pidan escribir, redactar, reescribir, editar o "humanizar" un texto, o pidan que suene humano, natural o menos robótico, aunque no nombren la skill. Es parte del Kit Human Writer: para auditar un texto y listar sus tics usa human-reviewer; para consistencia de términos y formatos, revisor-consistencia; para revisar hechos y fuentes, verificador-factual. No es para respuestas cortas de chat.
---

# Human Writer

Escribe y reescribe textos que suenan a una persona con criterio: específicos, con postura y con ritmo irregular. El objetivo es escribir bien, no engañar a un detector. Un texto concreto y con opinión deja de parecerse al promedio que produce un modelo de lenguaje.

Esta skill **escribe**. Las demás del kit revisan:

| Skill | Pregunta que responde |
|---|---|
| **human-writer** (esta) | ¿Cómo lo escribo bien? |
| human-reviewer | ¿Qué tics de IA tiene y dónde? |
| revisor-consistencia | ¿Dice lo mismo de la misma forma de principio a fin? |
| verificador-factual | ¿Cada afirmación dice lo que su fuente permite? |

## Prioridades, en este orden

1. **Claridad:** se entiende a la primera.
2. **Especificidad:** datos, nombres, casos y cifras reales en vez de abstracciones.
3. **Voz:** postura y vocabulario de alguien que conoce el tema.
4. **Ritmo:** oraciones y párrafos de largos distintos.

## Proceso: redactar desde cero

1. **Pide los insumos que falten:** ángulo, audiencia, canal, país o variante del español, uno o dos datos, casos o anécdotas reales, y las fuentes que se pueden citar. Es lo que más humaniza y lo único que no se puede fabricar.
2. **Escribe el borrador priorizando voz y especificidad.** Puede salir irregular. No escribas con una checklist delante: el texto sale acartonado.
3. **Repasa las reglas de abajo una sola vez**, con el borrador ya hecho.
4. **Entrega** (ver "Entrega").

## Proceso: reescribir un texto existente

1. Lee el texto completo y marca la **zona intocable** (abajo).
2. Si viene un informe de `human-reviewer`, úsalo como mapa. Si no, ubica tú los clusters: dónde se juntan tres o más señales.
3. Edita en este orden:
   1. Cortar relleno, introducciones vacías y moralejas.
   2. Cambiar abstracciones por datos, casos o mecanismos concretos.
   3. Apagar conectores de manual y verbos inflados.
   4. Variar el ritmo.
4. Relee solo las frases cambiadas contra la zona intocable. Si cambió una cifra, un alcance o lo que algo hace, revierte.
5. Si la pieza va a pasar por el resto del kit, deja la tabla de cambios (ver "Entrega").

## Zona intocable

Al reescribir cambia el estilo, no el contenido. No se modifica (salvo el orden de la frase):

- Cifras, porcentajes, fechas y montos, incluidas palabras como "hasta", "más de", "aproximadamente".
- Citas textuales y a quién se atribuyen.
- Nombres propios, marcas, leyes, instituciones.
- Lo que un producto, empresa o persona hace o no hace. Un sinónimo puede ser una afirmación nueva: "registra" no es "audita", "ayuda a" no es "garantiza".
- Enlaces, marcadores de pendiente (`[VALIDAR]`, `[FUENTE]`) y términos que el usuario definió en un glosario.
- Lo que exige el formato: estructura SEO, campos de una ficha, una definición obligatoria, la cantidad de caracteres de un título. Si hay reglas de formato, la estructura gana y solo se corrige la forma.

Si un tic cae dentro de la zona intocable, se deja y se avisa.

## Reglas de escritura

1. **Dato primero.** La interpretación va solo si aporta algo que el lector no vería solo.
2. **Un párrafo puede terminar en el dato,** sin moraleja ni "esto demuestra que…".
3. **Sin introducciones que anuncian** ("en este artículo veremos") **ni cierres que resumen** lo ya dicho.
4. **Concreción.** Al menos un caso, cifra o nombre real por sección. Si no lo hay, quizá la sección sobra.
5. **No infles la importancia.** Nada de "punto de inflexión" ni "papel fundamental" sin un dato que lo sostenga. Sin adjetivos que la fuente no justifique (innovador, líder, robusto).
6. **Verbos simples:** es, tiene, hace, usa. No "se posiciona como", "cuenta con", "lleva a cabo".
7. **Repite el término correcto.** No rotes sinónimos (empresa, compañía, organización, firma) para no repetir: varía la frase.
8. **Contrastes y tríos con dosis.** Un "no es X, sino Y" por pieza, como máximo. Tríos solo cuando hay tres cosas reales.
9. **Sin raya larga (—).** Usa punto, coma, dos puntos o paréntesis.
10. **Varía la forma.** Párrafos de distinto largo, secciones que no comparten la misma plantilla.
11. **Atribuye con nombre o no atribuyas.** "Los expertos dicen" se cambia por quién, dónde y cuándo.
12. **Ninguna afirmación más fuerte que su fuente.** Separa hecho, inferencia y opinión. No escribas "gracias a X, creció Y" si solo sabes que pasaron en ese orden.
13. **Toma postura donde la evidencia lo permite.** Matiza con detalles reales ("en México funcionó, en Colombia no"), no con "depende de diversos factores".
14. **Formato mínimo.** Negritas y viñetas solo cuando ayudan a leer. Headings en formato de oración, sin Title Case. Sin emojis decorativos salvo que el canal los pida.
15. **Cada frase aporta algo nuevo:** un dato, un ejemplo, un argumento o un matiz. Si no, se corta.
16. **Prueba de intercambiabilidad.** Si el párrafo sirve para otra marca o país cambiando solo el nombre, falta especificidad.
17. **Variante del español del lector.** Si no se indica y no se deduce del país, tuteo neutro. Voseo solo si el público es rioplatense. Un mismo registro de principio a fin.

Hay pares de antes y después en `references/ejemplos.md`.

## Si falta un dato

No lo inventes: ni cifras, ni citas, ni estudios, ni clientes, ni fuentes. Escribe alrededor del hueco. Al entregar, di qué dato falta y dónde iría. Si el usuario quiere marcadores dentro del texto, usa `[VALIDAR: qué falta]`.

## Qué no hacer

- No metas errores ortográficos ni caracteres raros para "parecer humano".
- No uses espacios invisibles ni trucos contra detectores.
- No borres todos los recursos retóricos. Un trío o una pregunta retórica en dosis normales son humanos.
- No conviertas la edición en caza de sinónimos. "Fundamental" por "esencial" no arregla la abstracción.
- No sacrifiques claridad por sonar natural.
- No resuelvas un `[VALIDAR]` para que la frase fluya.

## Entrega

- El texto limpio, sin notas dentro. Piezas largas como archivo `.md` o artifact.
- Si el cambio fue grande, 2 o 3 líneas sobre qué ajustaste.
- Lista de datos que faltan, si los hay.
- **Si la pieza sigue por el kit** (o el usuario lo pide), agrega al final, fuera del texto, la tabla de cambios. `revisor-consistencia` y `verificador-factual` la usan para comprobar que la reescritura no cambió hechos:

```
## Cambios de human-writer
| Ubicación | Antes | Después | Motivo |
No tocado (zona intocable): [lista]
Para el verificador: [frases que parecen un problema de hecho, no de estilo]
Secciones con más del 20% de oraciones cambiadas: [lista o "ninguna"]
```

Sugiere el siguiente paso si la pieza se va a publicar: `human-reviewer` para una auditoría independiente, después `revisor-consistencia` y al final `verificador-factual`.

---
Parte del **Kit Human Writer** de **Sebastian Avila AI**.
