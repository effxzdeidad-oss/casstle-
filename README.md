# Casstle Command Dashboard

Dashboard estático de documentación de comandos. No contiene panel de control, login, invitación ni conexión con el token del bot: únicamente muestra comandos, descripciones, categorías y alias.

## Archivos
- `index.html`: página principal.
- `style.css`: diseño responsive.
- `app.js`: búsqueda, filtros, selección y panel de detalle.
- `commands.json`: catálogo extraído de la lista de ayuda de Casstle.

## Probar localmente
Abre una terminal en esta carpeta y ejecuta:
```bash
python -m http.server 8000
```
Después abre `http://localhost:8000`. Como usa `fetch()` para leer `commands.json`, no abras `index.html` directamente como archivo.

## Publicar gratis
1. Crea un repositorio público en GitHub.
2. Sube los cuatro archivos manteniendo sus nombres y la misma carpeta.
3. En Settings → Pages, selecciona Deploy from a branch, `main` y `/ (root)`.
4. Cuando GitHub Pages publique la web, configura el dominio personalizado desde Settings → Pages → Custom domain.
5. En el proveedor del dominio configura los registros DNS que GitHub Pages indique.

## Importante
El catálogo se ha generado a partir de las categorías y descripciones del centro de ayuda incluidas en el código entregado. Los comandos creados dinámicamente o fuera de esas categorías podrían requerir añadirlos a `commands.json`. Revisa el catálogo antes de publicarlo. El prefijo mostrado es una muestra; el prefijo real depende del servidor.
