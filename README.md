# Sonrisa Imperial — landing page

Página estática de una sola vista. Todo el CSS y el JS van dentro de `index.html`;
la única dependencia externa son las tipografías de Google Fonts.

```
index.html    la página entera
vercel.json   URLs limpias + cabeceras de seguridad
```

## Desplegar en Vercel

### Opción A — CLI (requiere Node.js)

```bash
npm i -g vercel
vercel login
vercel --prod
```

Ejecuta los comandos desde esta carpeta. `vercel login` abre el navegador
para autenticarte; no puede hacerse de forma desatendida.

### Opción B — GitHub

1. Crea un repositorio vacío en GitHub.
2. Desde esta carpeta:

```bash
git init && git add . && git commit -m "Landing page Sonrisa Imperial"
git branch -M main
git remote add origin https://github.com/USUARIO/REPO.git
git push -u origin main
```

3. En vercel.com → **Add New → Project** → importa el repositorio.
   Framework Preset: **Other**. Sin build command ni output directory.
   Cada `git push` a `main` vuelve a desplegar.

## Antes de que sea público

Los datos de la página son de relleno y hay que sustituirlos:

- Teléfono `+34 912 34 56 78` y email `citas@sonrisaimperial.es`
- Dirección `Calle Velázquez, 118` y el horario
- El testimonio de "Marina G."
- Las cifras de la fila de confianza: primera visita sin coste,
  financiación a 12 meses, respuesta en 2 horas
- El formulario **no envía nada todavía**: hay que conectarlo a un correo,
  un CRM o un gestor de citas

La página lleva `<meta name="robots" content="noindex, nofollow">` y un
`robots.txt` que bloquea a los buscadores. Se puede visitar y compartir por
enlace, pero no aparecerá en Google. **Quita las dos cosas** cuando el
contenido sea real.
