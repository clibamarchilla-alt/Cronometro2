# Cronometro Congregacion

Contenido
- cronometro.html — la pantalla grande del cronómetro (para proyectar).
- control.html — panel de control (para usar desde el móvil).
- index.html — página de inicio con enlaces y ejemplo de iframe.

Cómo usar en Google Sites
1. Publica el repositorio usando GitHub Pages:
   - Ve a Settings → Pages → Branch: `main` (o `gh-pages`) → / (root) → Save.
   - La URL será: `https://<owner>.github.io/<repo>/` y las páginas individuales: `.../cronometro.html` y `.../control.html`.

2. En Google Sites:
   - Abre tu sitio en Google Sites.
   - Insertar → Incrustar → Por URL → pega `https://<owner>.github.io/<repo>/cronometro.html` (o `control.html`).
   - Si Google Sites no carga la URL por políticas de CORS/embed, usa la opción "Incrustar" → "Código" y pega un iframe:
     `<iframe src="https://<owner>.github.io/<repo>/cronometro.html" width="100%" height="600"></iframe>`

Alternativa rápida sin Pages
- Usa un servicio como https://raw.githack.com/ o https://rawcdn.githack.com/ para generar una URL pública:
  `https://raw.githack.com/<owner>/<repo>/main/cronometro.html`
  (sustituye `main` por la rama correcta). Esta URL puede usarse en el iframe.

Notas
- Recomendado acceder al control.html desde otro dispositivo en la misma red o desde el móvil; ambos usan BroadcastChannel si el navegador lo soporta. Si no, usan localStorage como fallback (funciona cuando ambas pestañas están en el mismo origen).
- Si quieres que el cronómetro inicie con pantalla completa automáticamente al abrir, puedo añadir un botón o un parámetro URL que haga la petición al cargar la página.
