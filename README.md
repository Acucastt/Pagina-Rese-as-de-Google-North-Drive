# Guía de Configuración · Placa de Reseñas de Google — NORTH DRIVE

Sitio web estático de instrucciones para configurar la placa NFC + QR de reseñas de Google
que vende **North Drive**. Incluye la guía descargable en PDF, un video demostrativo,
información del producto y dinámicas para conseguir más reseñas.

## Contenido

```
sitio-web/
├─ index.html          # Página única (HTML/CSS/JS embebidos, sin dependencias)
├─ guia/               # Guía de configuración en PDF (descargable)
├─ video/              # Video demostrativo optimizado (MP4)
└─ img/                # Logo, foto de la placa y miniaturas
```

## Ver en local

Como el navegador bloquea `file://`, sirve la carpeta con un servidor local:

```bash
# Python
python -m http.server 8000
# o Node
npx serve .
```

Luego abre http://localhost:8000

## Publicar en Vercel

1. Sube este repositorio a GitHub.
2. En [vercel.com](https://vercel.com) → **Add New → Project** → importa el repo.
3. Framework Preset: **Other** (sitio estático). No requiere build.
   - Build Command: *(vacío)*
   - Output Directory: `.` (raíz)
4. **Deploy**. Vercel te dará la URL pública para el código QR.

---

> **Contenido exclusivo de NORTH DRIVE.** Prohibida su copia, reproducción o distribución
> sin autorización. Todos los derechos reservados.
