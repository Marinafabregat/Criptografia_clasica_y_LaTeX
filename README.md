# Criptografía y \TeX

Trabajo de investigación sobre **criptografía clásica** y una guía práctica de
**\LaTeX**, que incluye la parte matemática de los distintos cifrados.

- **Autora:** Marina Fabregat Expósito
- **Tutor:** Artur Arroyo
- **Curso:** 2019–2020
- **Centre:** Colegio Sant Josep Obrer

## Documento principal

El documento que se compila es [`TR.tex`](TR.tex), que genera el PDF final.

## Compilar

Necesitas una distribución de TeX Live con `latexmk` y `babel` en español:

```bash
latexmk -pdf TR.tex     # compila (ejecuta pdflatex + bibtex las veces necesarias)
latexmk -pdf -c TR.tex  # limpia los ficheros auxiliares
```

O de forma manual, en dos passes para que las referencias cruzadas se resuelvan:

```bash
pdflatex TR.tex
bibtex   TR
pdflatex TR.tex
pdflatex TR.tex
```

## Estructura

| Ruta | Contenido |
| --- | --- |
| `TR.tex` | Documento principal (preámbulo + cuerpo) |
| `libreria.bib` | Bibliografía en formato BibTeX |
| `imagenes/` | Imágenes referenciadas desde el documento |
| `Proves/` | Pruebas y ejercicios sueltos de \LaTeX |
| `Beamer/` | Ejemplos y material de presentaciones Beamer |
| `build/` | Salida de compilación (ignorada por git) |
| `pract.1.tex`, `presentación.tex` | Trabajos y presentaciones independientes |

## Contenido del documento

1. Definición de criptografía.
2. Clasificación histórica de criptosistemas.
3. Herramientas de la criptografía clásica.
4. Cifrado por transposición.
5. Cifrado por sustitución.
6. Marco práctico.
7. Conclusiones.

Además, el documento incluye una **guía de \LaTeX** como material de apoyo
(secciones de preámbulo, listas, tablas, figuras, matemáticas y bibliografía).

## Requisitos

- `TeX Live` (probado con la instalación completa de TeX Live 2023)
- `latexmk`, `pdflatex` y `bibtex`
- Paquetes: `babel` (español), `amsmath`, `amssymb`, `graphicx`, `xcolor`,
  `tikz`, `hyperref`, `multicol`, `geometry`, `parskip`, `ragged2e`,
  `multirow`, `wrapfig`, `tocbibind`
