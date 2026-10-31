# Guías de configuración · Placas NFC — NORTH DRIVE

Sitio web estático con la guía de configuración (PDF descargable) y el video de cada
modelo de placa de North Drive. Cada modelo tiene su propia página, para que el código QR
de cada publicación lleve directo a la guía correcta.

## Páginas (links para los códigos QR)

| Modelo | Ruta | Archivo |
|---|---|---|
| Placa en inglés + QR programable | `/` | `index.html` |
| Placa de reseñas en español (solo NFC) | `/espanol` | `espanol.html` |
| Placa de menú NFC | `/menu` | `menu.html` |

`vercel.json` activa `cleanUrls`, así que `/espanol` y `/menu` funcionan sin la extensión `.html`.

## Contenido

```
sitio-web/
├─ index.html · espanol.html · menu.html   # una página por modelo (HTML/CSS/JS embebidos)
├─ vercel.json
├─ guia/    # PDFs de configuración (uno por modelo)
├─ video/   # videos de configuración optimizados (MP4, 720p)
└─ img/     # logo, fotos de las placas, portadas y miniaturas
```

## Ver en local

El navegador bloquea `file://`, así que sirve la carpeta con un servidor local:

```bash
python -m http.server 8000
```

Luego abre http://localhost:8000 (en local usa `/espanol.html` y `/menu.html`).

## Publicar en Vercel

Con el repositorio importado en Vercel, cada `git push` a `main` actualiza el sitio.
Framework Preset: **Other**, sin build command, Output Directory `.`.

---

> **Contenido exclusivo de NORTH DRIVE.** Prohibida su copia, reproducción o distribución
> sin autorización. Todos los derechos reservados.
