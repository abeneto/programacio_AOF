## REQUISITS

- Visual Studio Code
  
- latex: https://www.latex-project.org/get/

- pandoc: https://pandoc.org/installing.html

- plantilla eisvogel:
    - https://github.com/Wandmalfarbe/pandoc-latex-template

## Estructura de carpetes

```
--DEP_INF
    | README.md
    |--img
         |*.png
    |--programacio
            | 
            |--dam
                 | plantillaDAM.md
                 | sge.md
                 |--sge
                     |*.xlsx
                     |*.png
                 |--curs2425
                        |*.pdf
    |--seguiment
    |--memoria

```

## Crear Programació 

El procés per a crear la programació consistirà en confeccionar els arxius `.xlsx` dels mòduls i fer les modificacions necessàries en els arxius `.md`.

Per una banda, tenim una carpeta per a cada cicle i la part comuna del cicle estarà a l'arxiu `plantillaCICLE` (en l'exemple tenim plantillaDAM.md).

Per altra banda, en la carpeta del cicle també hi ha un arxiu .md i una carpeta per mòdul (en l'exemple tenim l'arxiu i la carpeta corresponent al mòdul SGE)

1. Generar la programació general del cicle des de la carpeta DEP_INF/programacio/cicle (en l'exemple:  `DEP_INF/programacio/dam`) executant:

    ```bash
    pandoc plantillaDAM.md -o curs2425/Prog_DAM.pdf --template eisvogel --pdf-engine=lualatex
    ```
2. Generar la programació d'un mòdul (en l'exemple: sge) des de la carpeta DEP_INF/programacio/cicle (en l'exemple:  `DEP_INF/programacio/dam`). Prèviament s'haurà modificat els arxius .xlsx i s'hauran fet les captures necessàries per a incloure-les en l'arxiu .md. A continuació s'executarà:

    ```bash
    pandoc sge.md -o curs2425/sge.pdf --template eisvogel --pdf-engine=lualatex
    ```