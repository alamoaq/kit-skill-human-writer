# Catálogo de señales de redacción generada

**Regla de lectura:** una señal aislada casi nunca importa. Lo que delata es el cluster: varias señales en el mismo tramo, o la misma señal repetida en varias secciones. Excepción: la raya larga, que se marca siempre.

Severidad base: **C** crítico · **A** alto · **M** medio · **B** bajo. Sube un nivel si forma cluster.

Los problemas de hechos y fuentes (cifras sin respaldo, atribuciones vagas, causalidad no demostrada) no están aquí: los revisa `verificador-factual`.

## Contenido

1. Capa A: residuos de herramienta
2. Capa C: patrones semánticos
3. Capa D: estilo y estructura
4. Capa F: ritmo y voz
5. No cuentan como señal
6. Pruebas operativas

## Capa A: residuos de herramienta (C)

Prueban que una herramienta de IA pasó por el proceso. Casi nunca tienen explicación humana. Se borran siempre.

| ID | Señal | Ejemplos |
|---|---|---|
| A1 | Conversación del chatbot pegada | "Claro, aquí tienes…", "Espero que te sirva", "¿Quieres que también…?", "Basado en la información proporcionada" |
| A2 | Códigos de cita internos | `oaicite`, `turn0search0`, `contentReference`, `[cite: 1]`, `start_span`, `grok_card` |
| A3 | URL con rastro de la herramienta | `utm_source=chatgpt.com`, `utm_source=openai`, `utm_source=copilot.com`, `referrer=grok.com` |
| A4 | Placeholders olvidados | `[INSERTAR FUENTE]`, `[Nombre de empresa]`, `XX%`, `202X`, `PASTE_URL_HERE` |
| A5 | Instrucciones o descargos del modelo | "Escribe un artículo de 800 palabras…", "como modelo de lenguaje", "hasta mi última actualización", "(mantener tono neutral)" |
| A6 | Formato que el canal no interpreta | `##` o `**` visibles en un correo, un post de LinkedIn o un documento que no renderiza Markdown |

Revisa también los enlaces y las notas al pie, no solo el cuerpo.

## Capa C: patrones semánticos

Lo que hace predecible a un texto de LLM es esta secuencia: **hecho → interpretación → importancia → contexto amplio → cierre positivo.** Pesa más que la superficie.

| ID | Señal | Cómo reconocerla | Sev |
|---|---|---|---|
| C1 | Importancia inflada | "marca un punto de inflexión", "desempeña un papel fundamental", "redefine la industria", "es un testimonio de", sin dato que lo sostenga | M |
| C2 | Contexto grandilocuente | Un dato pequeño termina "reflejando la evolución del ecosistema latinoamericano" | M |
| C3 | Gerundio interpretativo | "…, demostrando / reflejando / consolidando / fortaleciendo / posicionando…" cierra la frase con una conclusión no demostrada | M |
| C4 | Hecho → moraleja | El párrafo no termina en el dato: agrega "esto demuestra…", "lo que pone de manifiesto…" | M |
| C5 | Tono promocional | líder, potente, de vanguardia, revolucionario, referente, en texto informativo y sin fuente | M |
| C6 | Cierre optimista forzado | "A pesar de estos desafíos, el sector sigue avanzando hacia…" | B |
| C7 | Notoriedad vacía | "ampliamente reconocido", "con fuerte presencia en medios" sin quién ni cuándo | M |
| C8 | Exhaustividad falsa | Historia, beneficios, desafíos, tendencias y futuro, cada uno con generalidades | M |
| C9 | Abstracción creciente | El párrafo empieza concreto y termina en "valor, eficiencia, transformación" | M |
| C10 | Baja densidad factual | Párrafo de 100 palabras con un solo hecho verificable | M |
| C11 | Frase intercambiable | Cambias la marca, el producto o el país y el párrafo sigue funcionando igual | M |
| C12 | Ejemplo genérico puntual | "una empresa podría usar IA para automatizar tareas" | B |
| C13 | Ausencia total de casos | Ni un mecanismo ni una situación tangible de principio a fin | A |
| C14 | Balance artificial / opinión tibia | ventajas → desafíos → "depende de diversos factores", sin postura | M |
| C15 | Falta de jerarquía | Lo central y lo accesorio ocupan el mismo espacio | M |
| C16 | Misma idea en varias secciones | Intro, beneficios, cómo funciona y cierre repiten el concepto con otras palabras | M |
| C17 | Redundancia semántica | "mejora la productividad y permite trabajar de manera más eficiente"; la misma idea tres veces con sinónimos | B |

## Capa D: estilo y estructura

| ID | Señal | Cómo reconocerla | Sev |
|---|---|---|---|
| D1 | **Raya larga (—)** | Se marca siempre, aunque sea una. Se reemplaza por punto, coma, dos puntos o paréntesis | B (siempre) |
| D2 | Contraste prefabricado | "No es X, es Y", "no solo X sino Y", "más que X", "ya no se trata de", "el verdadero valor está en" | M si >1 |
| D3 | "Lo que antes…, ahora…" | "Lo que antes tomaba horas, ahora se resuelve en minutos" | B |
| D4 | Tríos perfectos | Tres adjetivos, tres verbos o "tres claves" en cada sección | M si se repite |
| D5 | Frases simétricas | "Menos complejidad. Más resultados." | B |
| D6 | Pregunta retórica + respuesta | "¿La mejor parte? …" | B |
| D7 | Frases cortas dramáticas en cadena | "Y aquí cambia todo. Literalmente." | B |
| D8 | Falso rango | "desde startups hasta grandes corporaciones" | B |
| D9 | Conectores encadenados | además, asimismo, por otro lado, en este sentido, finalmente, en párrafos seguidos | M |
| D10 | Muletillas prescindibles | "cabe destacar", "es importante tener en cuenta", "vale la pena señalar" | B |
| D11 | Transición de curso online | "Ahora que entendemos X, veamos Y", "con esto en mente" | B |
| D12 | Pegamento | "esto permite", "de esta manera", "de este modo", más de 3 veces | B |
| D13 | Verbos inflados | "se posiciona como", "se erige como", "cuenta con", "lleva a cabo", "hace uso de" donde basta es, tiene, hace, usa | B |
| D14 | Sustantivización corporativa | "la implementación de la optimización de la gestión" | B |
| D15 | Vocabulario de piloto automático | fundamental, crucial, clave, robusto, integral, innovador, estratégico, significativo, potenciar, aprovechar, transformar, abordar, facilitar, panorama, ecosistema. Densidad, no presencia | M si 6+ en 3 párrafos |
| D16 | Sinónimos rotados | empresa → compañía → organización → firma | M |
| D17 | Marketing genérico | "desbloquea tu potencial", "lleva tu negocio al siguiente nivel", "revoluciona la forma en que…" | M |
| D18 | Metáfora sobreexplicada | Una imagen estirada por varios párrafos | B |
| D19 | Introducción vacía | "En un mundo cada vez más digital", "Hoy más que nunca", "En este artículo veremos" | M |
| D20 | Cierre que repite la intro | Mismas ideas con sinónimos | M |
| D21 | Párrafos que siempre cierran | La última frase de cada párrafo resume o eleva | M |
| D22 | Topic sentence escolar | Cada párrafo anuncia lo que va a decir | B |
| D23 | Misma plantilla por sección | heading → definición → tres bullets → beneficio → mini conclusión, repetido | M |
| D24 | Headings clonados | "Cómo mejorar X / Cómo mejorar Y / Cómo mejorar Z" | B |
| D25 | Exceso de headings | Una idea simple convertida en ebook | B |
| D26 | Bullets clonados | Misma longitud, mismo verbo inicial, misma sintaxis | B |
| D27 | Infinitivos sueltos como lista | "Analizar datos. Optimizar campañas." en toda la sección | B |
| D28 | Enumeración de manual en prosa | "Primero… Segundo… Finalmente…" en cada bloque | B |
| D29 | Negritas mecánicas | "**Término:** descripción" diez veces fuera de fichas | B |
| D30 | Title Case en español | "Cómo Reducir Los Costos" | B |
| D31 | Emojis como viñetas | ✅ 🚀 💡 en contenido que no es informal | B |
| D32 | Heading que promete y no entrega | El subtítulo promete región, caso o cifra y la sección sigue genérica | A |
| D33 | CTA duplicado | Dos llamados casi iguales a pocas líneas | M |
| D34 | Fuente citada y abandonada | Un vocero o experto aparece una vez al inicio y desaparece | M |
| D35 | Repetir la pregunta antes de responder | "Sí, puedes conectar X con Y. Esto permite…" | B |

## Capa F: ritmo y voz

| ID | Señal | Cómo reconocerla | Sev |
|---|---|---|---|
| F1 | Ritmo uniforme | Todas las oraciones con longitud y cadencia parecidas | B |
| F2 | Sin voz del sector | Vocabulario neutro que no usaría alguien que trabaja en el tema | B |
| F3 | Explicar lo obvio | Definir "tasa de conversión" a un equipo de marketing | B |
| F4 | Registro mezclado | "tienes" y "tenés", o "tú" y "usted", en la misma pieza | M |

## No cuentan como señal

- Gramática perfecta, tono formal o un conector aislado. Nunca se "arreglan" metiendo errores.
- Falta de fuente por sí sola: eso es del verificador.
- Markdown que el destino sí renderiza.
- Lo que exige el formato de la pieza: definiciones obligatorias, headings en pregunta en contenido SEO, listas numeradas de pasos, etiquetas repetidas en fichas comparativas, repetir el nombre de la marca al inicio de cada sección para que se entienda sola.

## Pruebas operativas

Se aplican a cada párrafo o afirmación importante:

1. **Información nueva:** ¿la frase agrega un dato, mecanismo, argumento o matiz? Si no, se corta.
2. **Intercambiabilidad:** ¿sirve igual cambiando la marca por otra o el país por otro? Falta especificidad.
3. **Pegado en otros veinte artículos:** ¿podría ir sin cambios en cualquier blog del sector? Falta especificidad.
4. **Abstracción:** para cada término abstracto, ¿qué significa concretamente aquí?
5. **Cluster:** ¿cuántas señales hay en el mismo párrafo? Tres o más es cluster.
