# Web de escritura académica · Grupo LyS

Web hecha con [Hugo](https://gohugo.io/) y publicada con GitHub Pages en
https://escrituracademica-grupolys.github.io/

## Ver la web en tu ordenador
```
hugo server
```
Abre http://localhost:1313 (se actualiza al guardar). Para pararlo: `Ctrl + C`.

## Publicar cambios
```
git pull
git add .
git commit -m "Describe el cambio"
git push
```
En 1-2 minutos GitHub construye y publica la web (pestaña **Actions** para ver el progreso).

## Dónde está cada cosa
| Qué | Dónde |
|---|---|
| Textos de cada sección | `content/<sección>/_index.md` (español) y `_index.en.md` (inglés) |
| Un proyecto nuevo | `hugo new proyectos/nombre.md` y su versión inglesa `nombre.en.md` |
| Una persona del equipo | `hugo new equipo/nombre-apellido.md` (cambia `draft: true` a `false`) |
| Un evento | `hugo new eventos/nombre.md` (cambia `draft: true` a `false`) |
| Financiación y logos | `data/financiacion.yaml` y logos en `static/logos/` |
| Imágenes | `static/img/` (se usan como `/img/archivo.jpg`) |
| Menú e idiomas | `hugo.toml` |
| Textos fijos de la interfaz | `i18n/es.yaml` y `i18n/en.yaml` |
| Colores y tipografía | `assets/css/main.css` (variables al principio) |

Los comentarios `<!-- COMPLETAR ... -->` marcan lo que falta por rellenar.
Una página sin versión en inglés (`.en.md`) solo aparece en español.

## Añadir otro idioma (p. ej. gallego)
En `hugo.toml` copia el bloque `[languages.en]` como `[languages.gl]`, traduce el menú,
crea `i18n/gl.yaml` y añade archivos `.gl.md` junto a los `.md`.
