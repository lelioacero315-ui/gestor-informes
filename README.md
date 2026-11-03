# Gestor de Informes — Contrato CPS No. 1681 de 2026

**Gobernación de Casanare — Dirección de Talento Humano**
Contratista: LELIO EDUARDO ACERO PINTO · Supervisora: NINI JHOANA MARIÑO BERNAL

Aplicación web (un solo archivo `index.html`) para preparar los informes mensuales del contrato: se registran las 11 obligaciones, se cargan los documentos de soporte y se generan los tres entregables con el formato oficial.

**App en línea:** https://lelioacero315-ui.github.io/gestor-informes/

**Versión vigente: v47 · 03/11/2026** — Adición y Prórroga No. 1 (ver [Versión](#versión))

---

## Datos del contrato

| Concepto | Valor |
|---|---|
| Contrato | SECOP II CAS-GEN-CDPSP-0120-2026 · No. interno 1681 de 2026-08-03 |
| Acta de inicio | 4 de agosto de 2026 |
| Valor inicial | $13.119.321,00 (3 cuotas de $4.373.107,00) |
| Adición y Prórroga No. 1 | $6.559.660,50 · 1 mes y 15 días · CDP 2604061 del 27-10-2026 |
| Valor total | $19.678.981,50 |
| Terminación | 18 de diciembre de 2026 (antes: 3 de noviembre de 2026) |

| Informe | Periodo | Valor del acta | Pagado acumulado | Ejecución |
|---|---|---|---|---|
| No. 1 | 04/08 – 03/09/2026 | $4.373.107,00 | $4.373.107,00 | 33,33 % |
| No. 2 | 04/09 – 03/10/2026 | $4.373.107,00 | $8.746.214,00 | 66,67 % |
| No. 3 | 04/10 – 03/11/2026 | $4.373.107,00 | $13.119.321,00 | 66,67 % (sobre el valor con la adición) |
| No. 4 | 04/11 – 03/12/2026 | $4.373.107,00 | $17.492.428,00 | 88,89 % |
| No. 5 | 04/12 – 18/12/2026 | $2.186.553,50 | $19.678.981,50 | 100 % |

---

## Qué genera

| Archivo | Contenido |
|---|---|
| `INFORME ACTIVIDADES No. N.xlsx` | Informe de actividades (pestaña "INF. No. N", logo CONTRACTUS, escala 55 %) |
| `INFORME ACTIVIDADES No. N.docx` | Carta a la Secretaria General con la tabla ACTIVIDADES / ANEXOS |
| `ACTA RESUMEN FO-GD-11 No.N.docx` | Acta FO-GD-11 V.05 con las imágenes de evidencia incrustadas por obligación |

## Cómo se usa

1. **⚙️ Config:** número de informe, fechas del período y fecha de radicación. Guardar.
2. **📎 Docs:** arrastrar o seleccionar los soportes (se pueden cargar varios a la vez) y asignar cada uno a una o varias obligaciones.
3. **✍️ Actividades:** en cada obligación, pulsar **✨ Generar**. La descripción se redacta en prosa con el contenido de cada soporte asignado a esa obligación (radicados, fechas, personas, cifras); los avisos en ámbar indican qué revisar. Luego se pulsa **💾 Guardar actividad**.
4. **📅 Bitácora** (opcional): registro diario de actividades con su soporte.
5. **⚡ Generar:** descargar el Excel, el Word Carta y el Acta FO-GD-11.
6. **Al terminar el informe:** **➕ Nuevo informe** (descarga un respaldo, archiva el informe y deja la app lista para el próximo periodo).

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
4. Escribir un mensaje, por ejemplo `v47 — Adición y Prórroga No. 1`, y pulsar **Commit changes**.
5. Esperar 1–2 minutos a que GitHub Pages publique (pestaña **Actions** → en verde ✓).
6. Abrir la app y pulsar **Ctrl + Shift + R** en Edge para forzar la versión nueva.

Para confirmar que se cargó la versión nueva: mira la etiqueta de versión arriba a la izquierda (ej. **v47 · 03/11/2026**). Si aparece en amarillo «⬆ Hay versión nueva», pulsa **🔄 Actualizar**. También puedes hacer clic derecho → *Ver código fuente*. Debe aparecer `<!-- v47-adicion-prorroga-1-2026-11-03 -->` cerca del inicio.

> Si GitHub Pages no está activo: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.

## Requisitos técnicos

- Edge o Chrome actualizados
- Conexión a internet al cargar documentos: PDF.js, SheetJS y Mammoth se descargan de cdnjs, con jsdelivr como respaldo
- Las plantillas (Excel, Word Carta, FO-GD-11) y los logos van incluidos dentro de `index.html`

## Versión

**v47 (2026-11-03)** — Adición y Prórroga No. 1
- Valor del contrato: $13.119.321,00 + adición $6.559.660,50 = $19.678.981,50 (CDP 2604061 del 27-10-2026). Nueva terminación: 18 de diciembre de 2026.
- Estado financiero del Word: fila ADICIONAL, total, valor pagado y por ejecutar con la adición desde el Informe No. 3 (los informes 1 y 2 conservan el valor inicial). Los valores muestran centavos.
- Ejecución automática = valor pagado ÷ valor total: 33,33 % / 66,67 % / 66,67 % / 88,89 % / 100 %.
- Periodos: Informe 4 del 04/11 al 03/12 y Informe 5 del 04/12 al 18/12 (medio mes, $2.186.553,50). No se crea un informe después del 18/12.

**v46 (2026-11-03)** — Descripción a partir de cada soporte
- Cada actividad relata en prosa todos los soportes que tiene asignados (ya no repite textos del informe anterior ni lista nombres de archivo).
- Lee formatos nuevos: correo de la Registraduría (oficio, reporte, solicitud de complemento, fechas y plazo), CETIL, planillas de aportes «Planilla Resumen», libros de auditoría de nómina, actualización de aportante (ICBF/SENA) y respuestas de fondos de pensiones anexas a los oficios.
- Actividades 5 y 6 sin frases fijas del Banco de Maquinaria cuando los soportes no son de esa nómina.
- Avisos nuevos: .zip que no se leen, libros de auditoría sin valores calculados y soportes con fecha fuera del período.

**v45 (2026-11-02)** — Redacción de descripciones
- El botón ✨ Generar redacta cada actividad con las frases del Informe No. 1, pero solo con los párrafos que tienen datos en los soportes: ya no quedan `[CORCHETES]` en el texto.
- Lee el reporte de la Registraduría, los certificados de estado de cédula, oficios y memorandos (con su asunto), la nómina, la liquidación, la planilla PILA y los libros de retención por procedimiento 1.
- Los avisos (archivos de otro mes, diferencias entre nómina, PILA, liquidación y retención) salen en ámbar debajo del botón, no dentro del texto.
- La columna ANEXOS del Word y del Excel usa la descripción de cada soporte (ya no «Soporte»).

**v44 (2026-10-21)** — Marca de versión
- Etiqueta con la versión y la fecha en el encabezado (ej. «v44 · 21/10/2026»).
- Si hay una versión más nueva publicada en GitHub, la etiqueta se pone en amarillo y avisa que hay que pulsar 🔄 Actualizar.

**v43 (2026-10-21)** — Acta igual al original e informes archivados
- Acta FO-GD-11 idéntica al formato de la entidad: TEMA, LUGAR, OBJETIVO, AGENDA/ACTIVIDADES y DESARROLLO como lista numerada (sin filas adicionales).
- Selector **Informe** en la barra superior: muestra número y mes de cada informe (en curso o archivado) y botón **➕ Nuevo informe**.
- Informes archivados en **solo lectura**: se pueden revisar actividades y soportes y descargar el Excel, el Word y el Acta, pero no modificarlos.
- Config → **Mes del informe** (automático según el periodo, editable).

**v42 (2026-10-21)** — Guardar, actualizar y siguiente informe
- Botón **💾 Guardar** en el encabezado y autoguardado mientras se escribe (también al cerrar u ocultar la app).
- Botón **🔄 Actualizar**: guarda y recarga la app con la última versión publicada.
- Config → **Descargar respaldo / Restaurar respaldo**: copia completa en un archivo .json (actividades, configuración y soportes con sus imágenes).
- Config → **Iniciar siguiente informe**: descarga un respaldo, archiva el informe actual en «Contratos guardados» y deja la app limpia con el periodo siguiente.

**v41 (2026-10-21)** — Formatos idénticos a los originales
- Acta Resumen sobre el formato oficial FO-GD-11 (encabezado, márgenes 2 cm, Arial 11, tabla, Compromisos, ASISTENTES y pie), con el contenido al estilo del Acta No. 1: sección por obligación, evidencia documental y pies «Ilustración N» numerados por Word.
- Word del informe sobre el INFORME ACTIVIDADES No. 1: el estado financiero ahora es una tabla con los valores de cada pago.
- Excel sobre el INFORME ACTIVIDADES No. 2: conserva tildes, ajusta el alto de filas y nombra la hoja «INF. No. N».
- Los archivos abren en Word y Excel sin reparación.
- Nuevos campos: pie de ilustración, páginas que van al Acta y obligación donde se muestra cada evidencia; anexos por actividad; contenido del Acta (tema, objetivo, metodología, hallazgos, compromisos); % de ejecución física.

**v40 (2026-10-20)**
- Corregido el bloqueo al cargar archivos: las imágenes se guardaban en localStorage y lo llenaban.
- Ahora se cargan PDF, imágenes, Excel, Word y TXT.
- El generador de descripción trabaja sobre el texto exacto del Informe No. 1 y deja entre corchetes los datos que faltan.
- En el Acta FO-GD-11, las imágenes conservan su proporción real.
