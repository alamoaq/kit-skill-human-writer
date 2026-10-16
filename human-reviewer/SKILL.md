---
name: human-reviewer
description: Audita un texto ya escrito y lista sus señales de escritura generada por IA, frase por frase y por severidad: residuos de la herramienta, patrones semánticos (moraleja, importancia inflada, frase intercambiable, cero casos concretos), estilo (raya larga, "no es X sino Y", tríos, conectores de manual) y ritmo. Úsala siempre que pidan revisar, auditar o pasar por filtro un texto, pidan la lista de errores o tics de IA, digan "suena a ChatGPT", "qué lo delata", o peguen un blog, artículo o copy largo para saber qué corregir. También como paso después de human-writer. No reescribe salvo que se lo pidan. Parte del Kit Human Writer.
---

# Human Reviewer

Audita un texto terminado y reporta qué señales de IA tiene, dónde están y qué tan graves son. **Detecta y reporta; no reescribe** salvo que se lo pidan (para reescribir, la herramienta es `human-writer`).

| Skill | Pregunta que responde |
|---|---|
| human-writer | ¿Cómo lo escribo bien? |
| **human-reviewer** (esta) | ¿Qué tics de IA tiene y dónde? |
| revisor-consistencia | ¿Dice lo mismo de la misma forma de principio a fin? |
| verificador-factual | ¿Cada afirmación dice lo que su fuente permite? |

## Principios

- **Es un catálogo de indicios, no una prueba.** Los modelos aprendieron de textos humanos, así que una señal aislada no demuestra nada. Lo que pesa es la densidad: varias señales en el mismo tramo, o la misma repetida en varias secciones.
- **Excepción: la raya larga (—) se marca siempre**, aunque sea una sola.
- **No hay veredicto "es IA / no es IA".** Hay severidades y lugares donde se concentran los problemas.
- **No se acusa al autor.** Se describen patrones del texto, no cómo se produjo.
- **El fondo pesa más que la superficie.** Un texto sin un solo tic puede seguir siendo genérico, sin casos y sin postura. Eso se revisa primero.

## Proceso

1. **Lee el texto completo** antes de marcar nada.
2. **Pregunta o deduce el contexto:** canal (blog, newsletter, landing, guion), audiencia y si el formato tiene reglas propias (SEO, fichas, estructura fija). Lo que el formato exige no es una señal.
3. **Recorre las capas en este orden**, con el catálogo de `references/catalogo-senales.md`:
   - **Capa A:** residuos de la herramienta.
   - **Capa C:** patrones semánticos (fondo).
   - **Capa D:** estilo y estructura (superficie).
   - **Capa F:** ritmo y voz.
4. **Aplica las pruebas operativas** del catálogo a la intro, al primer párrafo de cada sección y al cierre.
5. **Si una frase parece un problema de hecho** (una cifra sin fuente, una causa no demostrada, "los expertos dicen"), no la evalúes aquí: anótala en "Para el verificador". Los hechos los revisa `verificador-factual`.
6. **Clasifica** cada hallazgo con la escala de abajo y **reporta**.
7. **Corrige solo si te lo piden.** Orden: crítico → fondo → superficie. Sigue las reglas de `human-writer` si está instalada.

## Escala de severidad

- **CRÍTICO:** cualquier señal de la capa A (residuo de herramienta).
- **ALTO:** tres o más señales de la capa C en el mismo tramo; heading que promete y no entrega; ausencia total de casos concretos en toda la pieza.
- **MEDIO:** capa D en cluster, o un mismo patrón de C repetido en varias secciones.
- **BAJO:** una señal aislada (una "crucial", un trío suelto). La raya larga es BAJO pero se reporta siempre.

Sube un nivel si la señal forma cluster con otras.

## Formato del informe

Una entrada por instancia, no solo por patrón. Es lo accionable: cada línea se puede tachar o reescribir.

```
## Revisión de tics de IA
Texto: [título o primeras palabras] | Canal: … | Audiencia: …

[SEVERIDAD · capa · ID] "frase citada" → señal → por qué delata

### Resumen
1. Patrones que se repiten y dónde forman cluster (párrafo o sección).
2. Nivel general según la escala (sin decir "es IA").
3. Para el verificador: [frases con posible problema de hecho, o "nada"].
4. Orden sugerido de corrección.
```

Si hay más de 20 hallazgos, los BAJO se agrupan por señal en una línea ("D9 conectores: 6 casos en §2 y §4").

Hay un ejemplo de informe completo en `references/ejemplo-informe.md`.

## Lo que NO cuenta como señal

- Gramática perfecta o tono formal.
- Un conector aislado ("además", "sin embargo").
- Falta de fuentes por sí sola (eso es del verificador).
- Markdown que el destino sí muestra bien (negritas o tablas en un blog).
- Lo que exige el formato: una definición obligatoria, headings en pregunta en un artículo SEO, listas numeradas de pasos, campos repetidos en fichas.

## Cautelas

- Muchos patrones vienen de guías en inglés. En español pesa más la estructura que la palabra exacta.
- Los modelos nuevos ya evitan varios tics viejos ("En conclusión", "Es importante señalar"). Que no aparezcan no dice nada.
- No inventes hallazgos para llenar el informe. Si una capa está limpia, dilo en una línea.

---
Parte del **Kit Human Writer** de **Sebastian Avila AI**. Catálogo basado en parte en la guía "Signs of AI writing" de Wikipedia (WikiProject AI Cleanup), adaptada al español.
