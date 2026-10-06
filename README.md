# Portafolio — Juan Pablo Valdebenito

Sitio personal estático (HTML + CSS + JS puro, sin frameworks ni build step) con tema oscuro/claro, animaciones al hacer scroll y CV descargable en PDF.

## Estructura

```
index.html          Página principal
cv.html              Versión HTML del CV (fuente para el PDF)
css/style.css        Estilos y temas (oscuro/claro)
js/main.js           Toggle de tema, menú móvil, animaciones al hacer scroll
assets/
  favicon.svg
  profile.svg                          Avatar placeholder (reemplázalo por tu foto)
  CV_Juan_Pablo_Valdebenito.pdf         CV generado desde cv.html
```

## Reemplazar la foto de perfil

1. Copia tu foto a `assets/profile.jpg` (o `.png`).
2. En `index.html`, busca la línea `<img src="assets/profile.svg" ...>` (dentro de `<div class="avatar-ring">`) y cambia el `src` por `assets/profile.jpg`.

## Actualizar el CV

1. Edita el contenido en `cv.html`.
2. Vuelve a generar el PDF con Edge en modo headless (o imprime desde el navegador con Ctrl+P → Guardar como PDF):

```powershell
& "C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" --headless --disable-gpu --no-pdf-header-footer --print-to-pdf="assets\CV_Juan_Pablo_Valdebenito.pdf" "file:///RUTA/COMPLETA/cv.html"
```

## Ver el sitio en local

Simplemente abre `index.html` en el navegador, o si prefieres un servidor local:

```powershell
python -m http.server 5500
```

y visita `http://localhost:5500`.

## Despliegue gratuito

### Opción A — GitHub Pages
1. Sube este proyecto a un repositorio en GitHub (por ejemplo `Juan-Valdebenito/portafolio`).
2. En el repo: **Settings → Pages → Source: Deploy from a branch → main / (root)**.
3. Tu sitio quedará en `https://juan-valdebenito.github.io/portafolio/`.
4. (Opcional) Puedes solicitar un subdominio gratuito tipo `jpvaldebenito.is-a.dev` en https://github.com/is-a-dev/register apuntando a GitHub Pages.

### Opción B — Vercel
1. Ve a https://vercel.com, conecta tu cuenta de GitHub.
2. Importa el repositorio (sin configuración adicional, es un sitio estático).
3. Vercel te da una URL tipo `portafolio-juanpablo.vercel.app` al instante.

### Opción C — Netlify
1. Ve a https://app.netlify.com/drop y arrastra la carpeta del proyecto directamente (sin necesidad de GitHub).
2. Netlify publica el sitio al instante con una URL propia.

## Pendientes sugeridos

- [ ] Reemplazar `assets/profile.svg` por una foto real.
- [ ] Agregar perfil de LinkedIn cuando lo tengas (en `index.html`, sección hero y contacto).
- [x] Actualizar el link de FullFragance cuando el dominio `FullFragance.cl` esté activo.
