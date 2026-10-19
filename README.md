# Gestor de Informes — Contrato CPS No. 1681 de 2026

Herramienta web para la gestión, documentación y generación de informes del **Contrato de Prestación de Servicios Profesionales No. SECOP II CAS-GEN-CDPSP-0120-2026 No. interno 1681**, ejecutado en la **Dirección de Talento Humano de la Gobernación de Casanare**.

---

## ¿Qué hace?

Gestiona las **11 obligaciones de la Cláusula 3** del contrato y genera automáticamente los tres documentos institucionales requeridos para el cobro mensual:

| Formato | Archivo generado |
|---|---|
| 📊 Excel | `INFORME_ACTIVIDADES_No1_CTO1681_2026.xlsx` |
| 📋 Word Carta | `INFORME_ACTIVIDADES_No1_CARTA_CTO1681_2026.docx` |
| 📋 Word Acta | `ACTA_RESUMEN_FO-GD-11_No1_CTO1681_2026.docx` |

---

## Funcionalidades

- **11 obligaciones** de la Cláusula 3 con el texto exacto de la minuta del contrato
- **Carga de documentos** — PDF, JPG, PNG, Excel, Word: todos se convierten a imagen automáticamente
- **Carga múltiple** — selecciona varios archivos a la vez; el modal de asignación se abre en secuencia
- **Asignación flexible** — un mismo documento puede asignarse a 1, 2 o 3 obligaciones simultáneamente
- **Bitácora diaria** — registra lo que haces cada día; las entradas se acumulan automáticamente en la obligación correspondiente
- **Imágenes incrustadas** en el Acta Resumen FO-GD-11 — cada imagen queda embebida en la sección DESARROLLO de la obligación asignada
- **Multi-contrato** — crea contratos independientes; los anteriores quedan guardados para consulta
- **Respaldo automático** — doble backup en `localStorage` + `sessionStorage`; si el navegador borra los datos, se recuperan automáticamente
- **Porcentaje manual** — ingresa libremente el porcentaje de ejecución por obligación

---

## Formatos institucionales

Los tres archivos generados son **idénticos a los formatos oficiales** de la Gobernación de Casanare:

- **Excel**: tab `INF. No. 1`, logo CONTRACTUS, escala 55%, portrait, área de impresión `$A$1:$D$18`
- **Word Carta**: dirigida a la Secretaria General, tabla ACTIVIDADES | ANEXOS, estado financiero del contrato, logo Gobernación
- **Word Acta FO-GD-11**: estructura TEMA / LUGAR / OBJETIVO / AGENDA/ACTIVIDADES / DESARROLLO / METODOLOGÍA DE REVISIÓN / HALLAZGOS Y RESULTADOS / Compromisos / ASISTENTES

---

## Uso

Abre la aplicación en:

```
https://lelioacero315-ui.github.io/gestor-informes/
```

No requiere instalación ni registro. Todos los datos se guardan localmente en el navegador.

---

## Contrato

| Campo | Valor |
|---|---|
| Contratista | LELIO EDUARDO ACERO PINTO |
| C.C. | 1.118.564.051 de Yopal |
| Entidad | Gobernación de Casanare |
| Dependencia | Dirección de Talento Humano |
| Supervisora | Nini Jhoana Mariño Bernal |
| Valor | $13.119.321,00 |
| Plazo | 3 meses — 2026-08-04 al 2026-11-03 |
| Objeto | Apoyar a la DTH en procesos de nómina, prestaciones sociales, gestión de historias laborales y actualización/validación/depuración en PASIVOCOL |

---

*Gobernación de Casanare · Dirección de Talento Humano · Yopal, Casanare*
