# AdaptIA

**Aplicación:** https://fborrasumh.github.io/adaptia/

**Asistente de envío a revista.** Adapta un artículo científico a las normas de la revista elegida **sin tocar la ciencia**: construye el perfil editorial de la revista, compara el manuscrito con él, propone solo los cambios necesarios con un *diff científico* que el autor acepta o rechaza, convierte las referencias verificándolas en Crossref y prepara el paquete de envío. Aplicación de un solo fichero (`index.html`), sin servidor ni cuenta, con el diseño de la familia Forja.

## Principio: forma frente a contenido

| Transformación editorial · permitida | Transformación científica · requiere permiso |
|---|---|
| Estructura y títulos de sección, longitud, resumen, palabras clave, estilo, formato de referencias, declaraciones | Cifras, tamaños muestrales, valores p, métodos, resultados, conclusiones, fuerza de las afirmaciones, referencias |

## Recorrido

1. **Manuscrito** (Word, PDF o texto): reconocimiento de secciones (en inglés y en español), corregible, y recuentos.
2. **Revista**: búsqueda en OpenAlex y **perfil editorial** extraído de las normas para autores. Cada regla lleva la frase literal de las normas, comprobada con código. Los perfiles se guardan, se exportan e importan.
3. **Diagnóstico**: tabla de cumplimiento calculada con código antes de tocar nada, más la coherencia entre citas y referencias. Tres niveles: Formato, Edición y Paquete de envío.
4. **Adaptación con siete agentes**: analista editorial, analista del manuscrito, verificador de cumplimiento, editor científico, redactor, editor de referencias y auditor final.
5. **Revisión**: diff palabra a palabra de cada cambio, con aceptar, rechazar o editar.
6. **Resultado**: lista de comprobación recalculada, pendientes del autor, manuscrito en Word, informe de cambios, paquete de envío (carta, puntos destacados, declaraciones, plantilla de respuesta a revisores y lista de comprobación) y perfil de la revista.

## El auditor

Cada propuesta se compara con el original **con código** y, con clave, también con un segundo modelo:

- ⛔ **Rojo** (no se aplica sin confirmación expresa): cifras que no están en el manuscrito, citas añadidas, redacción más categórica (p. ej., de *may reduce* a *reduces*), paso de asociación a causalidad.
- ⚠ **Ámbar**: cifras eliminadas, matices de prudencia perdidos, citas quitadas, palabras clave que no aparecen en el texto.

Las declaraciones obligatorias que faltan se añaden como plantillas con `[COMPLETAR]`: la app nunca inventa comités de ética, financiación ni registros.

## Referencias

Cada referencia se busca en **Crossref** (por DOI o por su texto) y se formatea en **Vancouver, AMA, APA o Harvard** con los datos oficiales. Las citas del texto se convierten entre formato numérico y autor-año, y se renumeran por orden de primera aparición. Las referencias no encontradas se dejan como estaban y se marcan.

## Límites

- Las normas para autores deben pegarse o subirse: un navegador no puede descargar webs de terceros, y así se usan las vigentes para el tipo de artículo concreto.
- Tablas y figuras se conservan como marcadores en el Word.
- Reducir el número de referencias, tablas o figuras queda como decisión del autor.
- La responsabilidad del contenido y del envío es de los autores.

## Privacidad

El manuscrito se procesa en el navegador. Con clave (`ia_openai_key`, compartida con el resto del catálogo), los fragmentos necesarios viajan a OpenAI. Las referencias se consultan en Crossref y la revista en OpenAlex. Los perfiles de revista se guardan en `localStorage`.

Forma parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT © 2026 Fernando Borrás Rocher · Universidad Miguel Hernández de Elche.
