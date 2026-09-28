# Criptografía y LaTeX

Trabajo de investigación sobre **criptografía clásica** que incluye, además,
una guía práctica de **LaTeX** con la parte matemática de los distintos cifrados.

- **Autora:** Marina Fabregat Expósito
- **Tutor:** Artur Arroyo
- **Curso:** 2019–2020
- **Centro:** Colegio Sant Josep Obrer
- **Idioma del documento:** español (`babel` con opción `spanish`)

## Documento principal

El documento se genera a partir de [`TR.tex`](TR.tex). El PDF compilado está
incluido en el repositorio como `TR.pdf`, para que pueda consultarse sin
necesidad de instalar TeX.

## Compilar

Se necesita una distribución de TeX Live con `latexmk` y `bibtex`:

```bash
latexmk -pdf TR.tex     # compila (ejecuta pdflatex y bibtex tantas veces como haga falta)
latexmk -pdf -c TR.tex  # elimina los archivos auxiliares
```

De forma manual, la secuencia es `pdflatex` → `bibtex` → `pdflatex` → `pdflatex`,
es decir, **tres** ejecuciones de `pdflatex`: la primera genera los archivos
auxiliares, `bibtex` procesa la bibliografía y las dos siguientes resuelven las
referencias cruzadas con los datos definitivos.

```bash
pdflatex TR.tex
bibtex   TR
pdflatex TR.tex
pdflatex TR.tex
```

## Contenido del documento

1. Definición de criptografía.
2. Clasificación histórica de los criptosistemas.
3. Herramientas de la criptografía clásica.
4. Cifrado por transposición.
5. Cifrado por sustitución.
6. Marco práctico.
7. Conclusiones.

Tras esas secciones, el documento incorpora una **guía de LaTeX** como material
de apoyo, que cubre el preámbulo, las listas, las tablas, las figuras, las
fórmulas matemáticas y la bibliografía.

## Estructura del repositorio

| Ruta | Contenido |
| --- | --- |
| `TR.tex` | Documento principal: preámbulo y cuerpo |
| `TR.pdf` | Documento ya compilado |
| `libreria.bib` | Bibliografía en formato BibTeX |
| `imagenes/` | Imágenes referenciadas desde el documento |
| `Proves/` | Pruebas y ejercicios sueltos de LaTeX |
| `Beamer/` | Ejemplos y material para presentaciones Beamer |
| `presentación.tex` | Presentación independiente |
| `pract.1.tex` | Práctica independiente |
| `P. con fondos.tex`, `Pautas P.tex` | Pautas y ejercicios de apoyo |
| `build/` | Archivos auxiliares de compilación (ignorados por git) |

## Requisitos

- **TeX Live**, probado con la instalación completa de TeX Live 2023.
- Herramientas: `latexmk`, `pdflatex` y `bibtex`.
- Paquetes: `babel` (español), `amsmath`, `amssymb`, `graphicx`, `xcolor`,
  `tikz`, `hyperref`, `multicol`, `geometry`, `parskip`, `ragged2e`,
  `multirow`, `wrapfig` y `tocbibind`.

## Licencia

Ver el archivo [LICENSE](LICENSE).
