# Gestor de Informes — Contrato CPS No. 1681 de 2026

**Gobernación de Casanare — Dirección de Talento Humano**
Contratista: LELIO EDUARDO ACERO PINTO · Supervisora: NINI JHOANA MARIÑO BERNAL

Aplicación web (un solo archivo `index.html`) para preparar los informes mensuales del contrato: se registran las 11 obligaciones, se cargan los documentos de soporte y se generan los tres entregables con el formato oficial.

**App en línea:** https://lelioacero315-ui.github.io/gestor-informes/

---

## Qué genera

| Archivo | Contenido |
|---|---|
| `INFORME_ACTIVIDADES_NoN_CTO1681_2026.xlsx` | Informe de actividades (pestaña "INF. No. 1", logo CONTRACTUS, escala 55 %) |
| `INFORME_ACTIVIDADES_NoN_CTO1681_2026.docx` | Carta a la Secretaria General con la tabla ACTIVIDADES / ANEXOS |
| `ACTA_RESUMEN_FO-GD-11_NoN_CTO1681_2026.docx` | Acta FO-GD-11 V.05 con las imágenes de evidencia incrustadas por obligación |

## Cómo se usa

1. **⚙️ Config:** número de informe, fechas del período y fecha de radicación. Guardar.
2. **📎 Docs:** arrastrar o seleccionar los soportes (se pueden cargar varios a la vez) y asignar cada uno a una o varias obligaciones.
3. **✍️ Actividades:** en cada obligación, pulsar **✨ Generar**. La descripción sale del texto del Informe No. 1 con los datos del período nuevo. Lo que no se pudo sacar de los documentos queda entre corchetes, por ejemplo `[FECHA_COMITE]`; se completa a mano y luego se pulsa **💾 Guardar actividad**.
4. **📅 Bitácora** (opcional): registro diario de actividades con su soporte.
5. **⚡ Generar:** descargar el Excel, el Word Carta y el Acta FO-GD-11.

## Archivos que acepta

- **PDF** (digital o escaneado): hasta 6 páginas como imagen y extracción de texto
- **Imágenes:** JPG, PNG, WEBP, GIF y BMP (se reducen automáticamente). Las fotos HEIC del iPhone se deben exportar primero como JPG.
- **Excel:** XLSX, XLSM, XLS, ODS y CSV (la tabla se convierte en imagen)
- **Word:** DOCX (texto e imágenes pegadas) y DOC (texto)
- **TXT**

## Dónde quedan los datos

Todo se guarda **en el navegador del equipo**: los datos de las actividades en localStorage y las imágenes y el texto de los documentos en IndexedDB. No se envía nada a ningún servidor.
- Si se borran los datos de navegación, se pierde la información. Conviene descargar los informes al terminar cada período.
- Los datos no pasan de un navegador a otro (Edge ↔ Chrome) ni de un equipo a otro.

---

## Cómo actualizar la app en GitHub

1. Entrar a https://github.com/lelioacero315-ui/gestor-informes
2. Pulsar **Add file → Upload files**.
3. Arrastrar el `index.html` nuevo (y este `README.md`). GitHub reemplaza los archivos que tengan el mismo nombre.
4. Escribir un mensaje, por ejemplo `v40 — carga de todo tipo de archivos`, y pulsar **Commit changes**.
5. Esperar 1–2 minutos a que GitHub Pages publique (pestaña **Actions** → en verde ✓).
6. Abrir la app y pulsar **Ctrl + Shift + R** en Edge para forzar la versión nueva.

Para confirmar que se cargó la versión nueva: clic derecho → *Ver código fuente*. Debe aparecer `<!-- v40-carga-archivos-2026-10-20 -->` cerca del inicio.

> Si GitHub Pages no está activo: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.

## Requisitos técnicos

- Edge o Chrome actualizados
- Conexión a internet al cargar documentos: PDF.js, SheetJS y Mammoth se descargan de cdnjs, con jsdelivr como respaldo
- Las plantillas (Excel, Word Carta, FO-GD-11) y los logos van incluidos dentro de `index.html`

## Versión

**v40 (2026-10-20)**
- Corregido el bloqueo al cargar archivos: las imágenes se guardaban en localStorage y lo llenaban.
- Ahora se cargan PDF, imágenes, Excel, Word y TXT.
- El generador de descripción trabaja sobre el texto exacto del Informe No. 1 y deja entre corchetes los datos que faltan.
- En el Acta FO-GD-11, las imágenes conservan su proporción real.
