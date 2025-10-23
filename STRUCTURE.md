# 📁 Estructura del Proyecto

```
book-scanner-app/
│
├── 📄 index.html              # ⭐ Aplicación principal (React PWA)
├── 🎨 styles.css              # Estilos CSS
├── ⚙️ manifest.json           # Configuración de la PWA
├── 🔧 sw.js                   # Service Worker (funcionalidad offline)
│
├── 🎨 generate-icons.html     # Generador de iconos (úsalo primero)
├── 🖼️ icon-192.png            # Icono 192x192 (genera con generate-icons.html)
├── 🖼️ icon-512.png            # Icono 512x512 (genera con generate-icons.html)
│
├── 📖 README.md               # Documentación principal
├── 🚀 INSTALL.md              # Guía rápida de instalación
├── 📋 STRUCTURE.md            # Este archivo
│
├── 📜 LICENSE                 # Licencia MIT
└── 🚫 .gitignore              # Archivos a ignorar en Git
```

## 🎯 Descripción de Archivos

### Archivos Principales

| Archivo | Descripción | ¿Necesario? |
|---------|-------------|-------------|
| `index.html` | La aplicación React completa | ✅ Obligatorio |
| `styles.css` | Todos los estilos CSS | ✅ Obligatorio |
| `manifest.json` | Configuración PWA (nombre, iconos, etc.) | ✅ Obligatorio |
| `sw.js` | Service Worker para offline | ✅ Obligatorio |

### Archivos de Iconos

| Archivo | Descripción | ¿Necesario? |
|---------|-------------|-------------|
| `generate-icons.html` | Genera los iconos automáticamente | ⚠️ Úsalo una vez |
| `icon-192.png` | Icono pequeño (192x192px) | ✅ Obligatorio |
| `icon-512.png` | Icono grande (512x512px) | ✅ Obligatorio |

### Archivos de Documentación

| Archivo | Descripción | ¿Necesario? |
|---------|-------------|-------------|
| `README.md` | Documentación completa | 📚 Recomendado |
| `INSTALL.md` | Guía de instalación | 📚 Recomendado |
| `STRUCTURE.md` | Esta guía de estructura | 📚 Opcional |
| `LICENSE` | Licencia MIT | 📚 Recomendado |
| `.gitignore` | Archivos que Git ignora | 📚 Recomendado |

## 🔄 Orden de Configuración

### 1️⃣ Generar Iconos (Primera vez)
```bash
# Abre en tu navegador:
generate-icons.html
# → Descarga icon-192.png
# → Descarga icon-512.png
```

### 2️⃣ Verificar Archivos
Asegúrate de tener estos archivos:
- ✅ index.html
- ✅ styles.css
- ✅ manifest.json
- ✅ sw.js
- ✅ icon-192.png
- ✅ icon-512.png

### 3️⃣ Subir a GitHub
```bash
git init
git add .
git commit -m "Primera versión"
git remote add origin https://github.com/TU-USUARIO/escaner-libros.git
git push -u origin main
```

### 4️⃣ Activar GitHub Pages
1. Settings → Pages
2. Source: Deploy from a branch
3. Branch: main / (root)
4. Save

### 5️⃣ Acceder
```
https://TU-USUARIO.github.io/escaner-libros
```

## 📦 Tamaño de Archivos

| Archivo | Tamaño Aprox. |
|---------|---------------|
| index.html | ~35 KB |
| styles.css | ~12 KB |
| manifest.json | ~1 KB |
| sw.js | ~2 KB |
| icon-192.png | ~5-10 KB |
| icon-512.png | ~15-25 KB |
| **Total** | **~70 KB** |

## 🌐 URLs Externas (CDN)

La app carga estos recursos desde CDN:
- React 18 (production)
- React DOM 18 (production)
- Babel Standalone
- QuaggaJS (escáner de códigos)

**Total adicional:** ~400 KB (se cachean después de la primera carga)

## 🔐 Datos del Usuario

### Se guardan localmente (LocalStorage):
- `bookDatabase` - Tu CSV de libros cargado
- `scannedBooks` - Historial de escaneos

### NO se envían a ningún servidor:
- ✅ 100% privado
- ✅ Sin tracking
- ✅ Sin cookies de terceros

## 📝 Modificar la App

### Cambiar colores:
Edita `styles.css`:
```css
/* Gradiente principal */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Cambiar nombre:
Edita `manifest.json`:
```json
{
  "name": "Tu Nombre Aquí",
  "short_name": "Nombre Corto"
}
```

### Cambiar iconos:
1. Edita `generate-icons.html` (función `drawIcon`)
2. Regenera los iconos
3. Reemplaza `icon-192.png` y `icon-512.png`

## ❓ ¿Qué archivo debo editar si...?

| Quiero cambiar... | Edita este archivo |
|-------------------|-------------------|
| Colores o estilos | `styles.css` |
| Funcionalidad | `index.html` (sección `<script>`) |
| Nombre de la app | `manifest.json` |
| Iconos | `generate-icons.html` → regenera |
| Documentación | `README.md` |
| Cache offline | `sw.js` |

## 🎓 Para Desarrolladores

### Estructura del Código (index.html)

```javascript
BookScannerApp
├── Estados (useState)
│   ├── database
│   ├── scannedBooks
│   ├── currentBook
│   ├── scanning
│   └── ...
│
├── Funciones
│   ├── handleFileUpload()
│   ├── startScanner()
│   ├── fetchBookInfo()
│   ├── findMatches()
│   └── ...
│
└── Componentes
    ├── ScannerView
    ├── ResultView
    └── HistoryView
```

### Modificar Service Worker

Si añades nuevos archivos, actualiza `sw.js`:
```javascript
const urlsToCache = [
  './',
  './index.html',
  './styles.css',
  './tu-nuevo-archivo.js',  // ← Añade aquí
  // ...
];
```

Y cambia la versión:
```javascript
const CACHE_NAME = 'book-scanner-v2';  // ← Incrementa
```

## 🚀 Deploy Alternativo

### Vercel
```bash
npm i -g vercel
vercel
```

### Netlify
Arrastra la carpeta a [netlify.com/drop](https://app.netlify.com/drop)

### GitHub Pages (Ya cubierto en INSTALL.md)
Settings → Pages → Deploy from branch

---

📚 ¿Preguntas? Lee el [README.md](README.md) o el [INSTALL.md](INSTALL.md)