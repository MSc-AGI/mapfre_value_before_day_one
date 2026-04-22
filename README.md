# MAPFRE Espana | AI Strategy Advisory Deck

**Proof-of-value deck** dirigido al CDO de MAPFRE Espana. Analiza la madurez AI de la compania, identifica gaps criticos frente a competidores europeos (Allianz, AXA), y propone un roadmap de 12 meses para transformar 150+ pilotos AI en impacto real sobre el P&L.

> Todo el contenido fue construido desde **fuentes publicas y market research**. No se utilizaron datos internos, confidenciales o propietarios de MAPFRE.

---

## Contexto del proyecto

MAPFRE Espana opera en un momento critico: el EU AI Act entra en vigor en agosto 2026 para sistemas de alto riesgo, la compania tiene un gap de 2.6 puntos porcentuales en combined ratio frente al grupo (95.8% vs 92.2%), y mas de 150 use cases de AI permanecen en fase piloto sin escalar a produccion.

Este deck articula el problema, cuantifica la oportunidad, y propone un plan de accion concreto con deliverables medibles.

---

## Estructura del deck (25 slides)

### Portada
El deck abre con la propuesta de valor: advisory para el CDO de MAPFRE Espana enfocado en AI strategy.

### Capitulo 1: Analisis Situacional (10 slides)
Diagnostico completo del posicionamiento de MAPFRE en AI usando frameworks de estrategia:

- **Porter's Five Forces** aplicado al sector seguros vs disrupcion AI
- **BCG Growth-Share Matrix** para clasificar el portfolio de 150+ use cases
- **5 Vectores de Disrupcion**: Pricing, Claims, Fraude, Distribucion, Compliance
- **Cascade Estrategico**: de la vision corporativa al plan de ejecucion local
- **Gap Combined Ratio**: IBERIA 95.8% vs Grupo 92.2%, el gap que AI puede cerrar
- **Pilot Purgatory**: 150+ use cases sin produccion a escala
- **EU AI Act Timeline**: deadline regulatorio Agosto 2026
- **Bridge Operativo**: gap entre estrategia Group y ejecucion local
- **Fault Line Politica**: dinamica de doble reporte (Group CTDO vs CEO IBERIA)

### Capitulo 2: Plan de Ataque (8 slides)
Roadmap de 12 meses con 5 fases y work packages detallados:

- **Roadmap Overview**: Gantt de 12 meses con Fase 4 (EU AI Act) como workstream transversal
- **Fase 0 (M1-M2)**: Triage del portfolio AI, de 150+ use cases a clasificacion BCG
- **Fase 1 (M2-M5)**: Priorizacion por P&L + clasificacion de riesgo EU AI Act
- **Fase 2 (M4-M7)**: Governance Design con Decision Rights sistematizados
- **Fase 3 (M6-M10)**: Cuantificacion via Combined Ratio Bridge (waterfall) y AI P&L Dashboard
- **Fase 4 (M1-M12)**: EU AI Act Readiness como stream paralelo con deadline en Agosto 2026
- **Impact Summary**: Before/After en tres dimensiones (Combined Ratio, Portfolio, Governance)

### Capitulo 3: Back-ups (6 slides)
Material de soporte para la audiencia:

- **B1**: Organigrama MAPFRE post-reorganizacion Dic 2025
- **B2**: EU AI Act requisitos clave (Articulos 9, 11, 14)
- **B3**: Benchmark competitivo Allianz y AXA en AI
- **B4**: Glosario de terminos (Combined Ratio, Loss Ratio, Expense Ratio, Pilot Purgatory)
- **B5**: Fuentes publicas y metodologia del analisis

---

## GitHub Pages

Este repositorio incluye una pagina web interactiva donde se pueden navegar todos los slides en el navegador.

**Funcionalidades de la pagina:**
- Navegacion por capitulos con sticky header
- Thumbnails de cada slide con preview en iframe
- Visor fullscreen con navegacion por teclado (flechas, Escape)
- Responsive para mobile y desktop

Para activar GitHub Pages: Settings > Pages > Source: main branch > / (root).

---

## Stack tecnico

El deck fue producido con un pipeline custom que convierte HTML/SVG en PPTX de alta resolucion:

```
HTML (SVG inline, 960x540)
        |
   Playwright (headless Chromium)
   viewport: 1920x1080, deviceScaleFactor: 2
        |
   PNG screenshots (@2x resolution)
        |
   python-pptx (widescreen 16:9)
   13.333 x 7.5 inches
        |
   .pptx (image-based slides)
```

**Ventajas de este approach:**
- Pixel-perfect rendering: cada slide es una imagen de alta resolucion
- Sin dependencia de fuentes o temas PowerPoint
- Edicion facil del contenido via HTML/SVG
- Versionable en git (los slides son archivos de texto)

**Dependencias:**
- Python 3.10+
- playwright (con chromium)
- python-pptx
- Node.js (para Playwright)

---

## Paleta de colores

| Elemento | Color | Hex |
|---|---|---|
| Fondo principal | Navy oscuro | `#0F1A2E` |
| Fondo cards | Navy medio | `#1A2744` |
| Fase 0 / Acento principal | Teal | `#3A9DBF` |
| Fase 1 / Positivo | Verde | `#38A169` |
| Fase 2 / Warning | Gold | `#D69E2E` |
| Fase 3 / Premium | Purple | `#805AD5` |
| Fase 4 / Critico | Rojo | `#C53030` |
| Texto primario | Blanco | `#FFFFFF` |
| Texto secundario | Gris azul | `#8895A7` |

---

## Estructura de archivos

```
.
├── index.html                              # Landing page (GitHub Pages)
├── README.md
├── MAPFRE_FullDeck_260422_1705.pptx        # Deck completo (25 slides)
└── slides/
    ├── 00-titulo/
    │   └── 00_portada.html
    ├── 01-analisis-situacional/
    │   ├── 00_divider.html
    │   ├── 01_porter_five_forces.html
    │   ├── 02_bcg_matrix.html
    │   ├── 03_cinco_vectores.html
    │   ├── 04_cascade_estrategico.html
    │   ├── 05_gap_combined_ratio.html
    │   ├── 06_pilot_purgatory.html
    │   ├── 07_eu_ai_act_timeline.html
    │   ├── 08_bridge_operativo.html
    │   └── 09_fault_line_politica.html
    ├── 02-plan-de-ataque/
    │   ├── 00_divider.html
    │   ├── 01_roadmap_overview.html
    │   ├── 02_fase0_triage.html
    │   ├── 03_fase1_priorizacion.html
    │   ├── 04_fase2_governance.html
    │   ├── 05_fase3_cuantificacion.html
    │   ├── 06_fase4_eu_ai_act.html
    │   └── 07_impact_summary.html
    └── 03-backups/
        ├── 00_divider.html
        ├── 01_organigrama.html
        ├── 02_eu_ai_act_requisitos.html
        ├── 03_benchmark_allianz_axa.html
        ├── 04_glosario.html
        └── 05_fuentes_metodologia.html
```

---

## Metricas clave del analisis

| Metrica | Valor |
|---|---|
| Combined Ratio IBERIA | 95.8% |
| Combined Ratio Grupo | 92.2% |
| Gap | 2.6 pp |
| Target post-AI (estimado) | 93.9% |
| Use cases en piloto | 150+ |
| Use cases target produccion | 30-40 |
| AI Maturity MAPFRE | 35.5 / 100 |
| AI Maturity Allianz | 61.5 / 100 |
| AI Maturity AXA | 63 / 100 |
| Deadline EU AI Act (high-risk) | Agosto 2026 |

---

## Fuentes

- MAPFRE Informe Anual e Integrado 2024
- MAPFRE Plan Estrategico 2024-2026
- Allianz Annual Report 2024
- AXA Universal Registration Document 2024
- EU AI Act (Regulation (EU) 2024/1689)
- EIOPA AI Governance Guidelines
- McKinsey Global Insurance Report 2025
- Perfiles profesionales publicos (LinkedIn)

---

## Autor

**Marcelo Caballero**
AI Strategy Advisory
Abril 2026

---

*Este repositorio es privado y contiene material de advisory. No distribuir sin autorizacion.*
