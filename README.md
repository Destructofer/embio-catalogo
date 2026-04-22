# EMBIO Portafolio Web · Versión "Menú de Restaurante"

Al escanear el QR, el usuario ve **directamente el catálogo** desplazándose como si fuera un menú. Sin intermediarios, sin pantallas extra. Un botón flotante "Déjanos tus datos" aparece siempre visible abajo, y al final del catálogo hay formulario + contactos directos.

---

## 📦 Contenido del paquete

```
embio-landing/
├── index.html                        ← La página (ábrela en tu navegador para ver)
├── catalogo-embio.pdf                ← PDF original (descarga opcional)
├── embio-logo-horizontal.webp        ← Logo para el QR
├── embio-icon.webp                   ← Solo el ícono (cruz) para el QR
├── embio-full-logo.png               ← Logo completo con texto descriptivo
└── pages-web/                        ← 24 páginas del catálogo en WebP (~2 MB total)
    ├── page-01.webp
    ├── ...
    └── page-24.webp
```

El primer `page-01.webp` (~126 KB) se precarga, así que aparece al instante al escanear el QR. Las demás páginas cargan solas conforme la persona hace scroll (lazy load).

---

## 🚀 Paso 1 · Configurar el formulario (elige UNA opción)

### Opción A · Netlify Forms (más fácil, gratis)

El formulario ya viene preparado con `data-netlify="true"`. Solo:

1. Abre `index.html` en cualquier editor
2. Busca esta línea del `<form>`:
   ```
   action="https://formspree.io/f/REEMPLAZA_CON_TU_ENDPOINT"
   ```
3. **Elimínala** (deja el form sin `action`)
4. Guarda

Los leads llegan al dashboard de Netlify: `Sites → tu-sitio → Forms`. Activa notificaciones por email en `Site settings → Forms → Form notifications → Add notification`.

### Opción B · Formspree (funciona en cualquier hosting)

1. Crea cuenta gratis en https://formspree.io
2. Crea un nuevo form, copia el endpoint
3. En `index.html`, reemplaza `REEMPLAZA_CON_TU_ENDPOINT` por tu código
4. Plan gratis = 50 envíos/mes

---

## 🌐 Paso 2 · Desplegar (3 minutos)

### Netlify Drop (drag & drop)
1. Ve a https://app.netlify.com/drop
2. **Arrastra la carpeta `embio-landing/` completa** (no solo el HTML — necesita las imágenes)
3. URL lista en ~30 segundos
4. (Opcional) Cambia el nombre del sitio: `Site settings → Change site name`

### Alternativas
- **Vercel**: `npx vercel --prod` desde la terminal dentro de la carpeta
- **GitHub Pages**: sube a un repo y activa Pages

---

## 📱 Paso 3 · Generar el QR

**Recomendado:** https://www.qrcode-monkey.com

**Configuración sugerida:**
- URL: tu URL de Netlify
- Color del QR: `#0e2747` (navy EMBIO)
- Logo al centro: sube `embio-icon.webp`
- Error correction: **H (30%)** — obligatorio si llevas logo
- Descarga mínima: **1500x1500 px**

**Para imprimir en la expo:**
- Tamaño mínimo: 5 cm × 5 cm
- Ideal para stand: 8-12 cm
- Texto debajo: "Escanea para ver nuestro portafolio"

---

## ✅ Checklist pre-expo

- [ ] Configuré el formulario
- [ ] Envié un lead de prueba — me llegó el email
- [ ] Probé escanear el QR desde 2-3 celulares distintos
- [ ] Al tocar los números → abre el dialer
- [ ] Al tocar los emails → abre el cliente de correo
- [ ] Imprimí el QR en alta calidad
- [ ] Tengo capturas del sitio como respaldo por si falla el internet
- [ ] Precargué el sitio en el WiFi del venue

---

## ⚡ Tips para la expo

- **Precarga en el venue**: al llegar, escanea el QR 3-4 veces desde distintos dispositivos — el sitio queda cacheado.
- **Monitoreo en tiempo real**: deja abierto el dashboard de Netlify/Formspree durante la expo.
- **Follow-up rápido**: responde leads en menos de 1 hora — es cuando están más interesados.
- **Plan B físico**: lleva tarjetas impresas por si el WiFi del venue falla.
