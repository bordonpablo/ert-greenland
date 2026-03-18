# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## info about the projet

El objetivo de este proyecto es adaptar un ejemplo de uso de la libreria open source pygimli donde se realiza una inversion de datos ERT con topografìa, haciendolo funcionar sobre datos que provienen del sensor IRIS Syscal Pro Switch Multi-electrode geoelectrical equipment with 10 m electrode spacing cables. 

El archivo de datos del ejemplo y el archivo de datos de trabajo difieren en su estructura y la idea es hacer un pre-proceso al cargar el dataContairnerERT para que el proceso subsiguiente funcione

El script de ejemplo de partida esta en examples/plot_02_ert_field_data.py
El archivo con datos que espera este ejemplo es: examples/slagdump.ohm
El archivo de trabajo sobre el que hay que editar, el responsable de hacer la adaptacion es src/inversion_WS48.py
El archivo con datos para el script de trabajo esta en data/greenland/WS-48-16.dat

La estructura del repo es la siguiente:

├── CLAUDE.md
├── data
│   ├── greenland
│   │   ├── WS_05_xx.bin
│   │   ├── WS_05_xx_cor.dat
│   │   ├── WS_3_20.bin
│   │   ├── WS_3_20_cor.dat
│   │   ├── WS-48-16.bin
│   │   └── WS-48-16.dat
│   └── Mitterberg
│       ├── P2_Höhe.txt
│       ├── WS-5-42.dat
│       └── WS-5-42_topo.dat
├── doc
│   └── INSTALL.md
├── examples
│   ├── plot_02_ert_field_data.ipynb
│   ├── plot_02_ert_field_data.py
│   └── slagdump.ohm
├── img
│   ├── 01_electrodos.png
│   ├── 02_pseudoseccion.png
│   ├── 03_errores.png
│   ├── 04_resultado_y_ajuste.png
│   └── 05_modelo_resistividad.png
├── README.md
└── src
    └── inversion_WS48.py (archivo principal)


## Development Guidelines for Claude

### Working Style

- *Incremental Changes Only*: Make small, focused modifications to single functions or files
- *No Bulk Refactoring*: Avoid large-scale changes or restructuring without explicit permission
- *Preserve Existing Logic*: Maintain current implementation patterns unless specifically asked to change
- *Step-by-Step Approach*: Break complex tasks into small, reviewable steps
- *Explicit Scope*: Only modify files/functions explicitly mentioned in the request

### Code Modification Rules

1. *Single Responsibility*: Each change should address one specific issue or feature
2. *Minimal Impact*: Prefer the smallest possible change that solves the problem
3. *Ask Before Expanding*: If a change requires touching multiple files, ask for confirmation first
4. *Preserve Comments*: Keep existing comments and TODOs unless specifically addressing them
5. *No Unsolicited Improvements*: Don't optimize or refactor code unless that's the specific request