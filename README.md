# AdaptIA

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23068186.svg)](https://doi.org/10.5281/zenodo.23068186)

**Aplicación:** https://fborrasumh.github.io/adaptia/

**Tu artículo, adaptado a la revista sin tocar la ciencia.** Pegas tu manuscrito y las normas para autores de la revista; la IA propone solo cambios de forma y el código comprueba que no cambian cifras, citas ni la fuerza de lo que afirmas. Tú aceptas o rechazas cada cambio y descargas el manuscrito en Word. Aplicación de un solo fichero (`index.html`), sin servidor ni cuenta, en español, inglés y portugués, con el diseño de la familia Forja.

La versión 2 es una simplificación de la 1: tres pasos, pensados para que la use cualquier investigador sin formación previa. La versión 1.0.1 (perfiles de revista, siete agentes, referencias con Crossref y paquete de envío) sigue archivada en Zenodo.

## Cómo se usa

1. **Tus dos textos.** Pega o sube (Word, PDF o texto) el manuscrito y las normas para autores. Los títulos de sección (Abstract, Introduction, Methods…, también en español y portugués) deben ir cada uno en su línea; la app muestra las secciones que reconoce.
2. **Revisa cada cambio.** Ves las normas que ha extraído la IA, la tabla de cumplimiento calculada con código (antes y después) y cada cambio propuesto con un *diff* palabra a palabra y su semáforo. Aceptas o rechazas.
3. **Descarga** el manuscrito adaptado y un informe de cambios, ambos en Word.

El botón **Ver un ejemplo** recorre todo el proceso sin clave de IA.

## La IA propone, el código comprueba

- **Normas:** cada norma lleva la frase literal de la revista en la que se basa. El código comprueba que esa frase existe en el texto pegado; si no aparece, la norma se marca con ⚠ y no se usa. Los límites (palabras del resumen, del texto principal, número de palabras clave) solo cuentan si su número aparece en una frase verificada. Los títulos de sección exigidos solo cuentan si aparecen en las normas.
- **Cumplimiento:** recuentos de palabras, palabras clave y secciones calculados con código sobre tu original y sobre la versión con los cambios aceptados.
- **Semáforo de cada cambio**, comparando con tu original:
  - ⛔ **Rojo** (pide confirmación expresa): cifras que no están en el manuscrito, citas añadidas, redacción más categórica (p. ej., de *may reduce* a *reduces*).
  - ⚠ **Ámbar**: cifras o citas que desaparecen, matices de prudencia perdidos.
  - ✓ **Verde**: solo forma.

## Privacidad

Todo se guarda en el navegador. A tu proveedor de IA (OpenAI, Google Gemini o Anthropic Claude, con tu propia clave) salen las normas y las secciones del manuscrito, con correos y teléfonos enmascarados; el título, los autores y las referencias no salen. Antes del primer envío ves lo que sale. Se hace una petición para las normas y una por sección.

## Límites

- No formatea las referencias: usa tu gestor bibliográfico (Zotero, Mendeley…) con el estilo de la revista.
- No toca tablas ni figuras, no redacta declaraciones (ética, financiación, conflictos) ni envía nada a la revista.
- El Word de salida es texto con títulos de sección: el formato fino (tablas, figuras, estilos de la revista) lo completas tú.
- El auditor detecta por código cifras, citas y expresiones de certeza o prudencia frecuentes en inglés, español y portugués; no sustituye la lectura de cada cambio.
- Las normas se pegan o se suben: un navegador no puede descargar webs de terceros.
- La responsabilidad del contenido y del envío es de los autores.

## Autoría

- Fernando Borrás Rocher · Universidad Miguel Hernández de Elche · ORCID [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)
- Alejandro Ruiz Picazo · Universidad Miguel Hernández de Elche · ORCID [0000-0003-1281-8208](https://orcid.org/0000-0003-1281-8208)

## Cómo citar

Borrás Rocher, F. y Ruiz Picazo, A. (2026). *AdaptIA* (versión 2.0.0) [Software]. Universidad Miguel Hernández de Elche. https://doi.org/10.5281/zenodo.23068186

El DOI es el de concepto: apunta siempre a la última versión. GitHub ofrece la cita en APA y BibTeX con el botón *Cite this repository*, a partir de `CITATION.cff`.

Forma parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT © 2026 Fernando Borrás Rocher y Alejandro Ruiz Picazo · Universidad Miguel Hernández de Elche.
