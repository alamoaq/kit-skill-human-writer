# Kit Human Writer: escribir, auditar y verificar textos para que no suenen a IA

Cuatro skills en español para Claude (adaptables a otros asistentes) que cubren todo el proceso de un texto largo antes de publicarlo: blogs, newsletters, artículos, copy de landing, guiones, posts largos.

No usan trucos contra detectores. Hacen lo que hace un buen equipo editorial: alguien escribe, alguien revisa el estilo, alguien revisa que todo cuadre y alguien verifica los hechos.

Creado por **Sebastian Avila AI**.

> ¿Solo quieres una skill simple que escriba y reescriba? Usa **[human-writer](https://github.com/alamoaq/human-writer)**. Instala uno u otro, no los dos: ambos traen una skill llamada `human-writer`.

## Las cuatro skills

| Paso | Skill | Pregunta que responde |
|---|---|---|
| 1 | `human-writer` | ¿Cómo lo escribo bien? Redacta o reescribe con voz propia y datos concretos |
| 2 | `human-reviewer` | ¿Qué tics de IA quedaron y dónde? Lista frase por frase, con severidad |
| 3 | `revisor-consistencia` | ¿Dice lo mismo de la misma forma? Términos, números, fechas, títulos que prometen algo, tablas vs texto |
| 4 | `verificador-factual` | ¿Cada afirmación dice lo que su fuente permite? Datos sin fuente, exageraciones, "según expertos", causas no demostradas |

## Flujo recomendado para una pieza que vas a publicar

1. **Escribe o reescribe** con `human-writer`. Dale el ángulo, el público y al menos un dato o caso real.
2. **Audita** con `human-reviewer`. Te devuelve la lista de tics frase por frase.
3. **Corrige** pidiéndole a `human-writer` que aplique el informe. Pídele la tabla de cambios: las skills siguientes la usan para comprobar que la reescritura no cambió datos.
4. **Revisa la consistencia** con `revisor-consistencia`. Si tienes un glosario o guía de estilo, dáselo.
5. **Verifica los hechos** con `verificador-factual`. Va al final porque cualquier reescritura de estilo puede cambiar sin querer un dato o una afirmación. Dale tus fuentes y la información oficial de tu marca.

Para un texto corto o informal, con los pasos 1 y 2 alcanza.

### Ejemplo de conversación

> **Tú:** Escribe un artículo sobre por qué los carritos se abandonan en el checkout. Público: tiendas online en Colombia. Dato real: en mi tienda, el 60% abandona cuando aparece el costo de envío.
>
> **Tú:** Ahora pásalo por human-reviewer.
>
> **Tú:** Aplica las correcciones y dame la tabla de cambios.
>
> **Tú:** Revisa la consistencia.
>
> **Tú:** Verifica los datos. La fuente del 60% es mi Google Analytics de septiembre.

### Por qué cuatro skills y no una

- Quien escribe no es buen juez de su propio texto. Separar escritura y auditoría da una segunda mirada.
- Una pasada de estilo no detecta que "declara" se convirtió en "certificado". Eso lo ve solo el verificador.
- Cada una sirve sola: el verificador sirve para textos que no escribiste tú, el revisor de consistencia para cualquier documento largo.

## Qué detecta

- La raya larga (—), siempre.
- "No es X, es Y", tríos perfectos, frases simétricas ("Menos complejidad. Más resultados.").
- Conectores de manual en cadena: "además", "asimismo", "por otro lado", "cabe destacar".
- Introducciones vacías, moralejas al final del párrafo, importancia inflada, opinión tibia.
- Textos sin un solo ejemplo concreto de principio a fin.
- Restos del chat pegados: "Claro, aquí tienes…", `utm_source=chatgpt.com`.
- Un mismo concepto escrito de dos formas, números con formatos distintos, títulos que prometen "7 herramientas" y traen 6.
- Cifras sin fuente, "según expertos", "gracias a X creció Y" sin prueba, afirmaciones más fuertes que su fuente.

## Cómo instalar

### En Claude.ai (web o app de escritorio)

1. Descarga este repositorio: botón verde **Code → Download ZIP**, y descomprímelo.
2. Adentro hay cuatro carpetas, una por skill, cada una con su `SKILL.md`.
3. Comprime **cada carpeta por separado** en un `.zip` (en Windows o Mac: clic derecho → Comprimir).
4. En Claude.ai, ve a **Configuración → Capacidades** (sección Skills) y sube los cuatro `.zip`, uno por uno.

Necesitas tener activadas las Skills en tu cuenta. Si no ves la opción, revisa que tu plan las incluya.

### En Claude Code

```bash
git clone https://github.com/alamoaq/kit-skill-human-writer.git
cd kit-skill-human-writer
cp -r human-writer human-reviewer revisor-consistencia verificador-factual ~/.claude/skills/
```

En Windows la ruta es `C:\Users\TU_USUARIO\.claude\skills\`. Para usarlas solo en un proyecto, cópialas a `.claude/skills/` dentro del proyecto.

### En ChatGPT, Gemini u otros

No tienen el mismo sistema de skills. Puedes crear un GPT personalizado o un Gem por skill, pegando el contenido de su `SKILL.md` como instrucciones y subiendo los archivos de `references/` como conocimiento.

## Lo que estas skills no hacen

- No meten errores a propósito ni caracteres invisibles para "engañar" detectores.
- No inventan datos, clientes, estudios ni citas. Si falta algo, te dicen qué falta.
- No garantizan pasar un detector de IA. Están hechas para que el texto sea mejor, no para esconder cómo se escribió.

## Créditos y licencia

Creado por **Sebastian Avila AI**.

Parte del catálogo de señales está basado en la guía ["Signs of AI writing"](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) del WikiProject AI Cleanup de Wikipedia, adaptada al español y ampliada.

Licencia [CC BY-SA 4.0](LICENSE): puedes usar, modificar y compartir estas skills, incluso con fines comerciales, siempre que des crédito a Sebastian Avila AI y compartas tus versiones con la misma licencia.
