# 🚀 Guía Rápida de Instalación

## 📱 Instalar en tu Móvil (5 minutos)

### Paso 1: Genera los Iconos
1. Abre `generate-icons.html` en tu navegador
2. Descarga ambos iconos:
   - `icon-192.png`
   - `icon-512.png`
3. Guárdalos en la misma carpeta que `index.html`

### Paso 2: Sube a GitHub

#### Opción A: GitHub Desktop (Fácil)
1. Descarga [GitHub Desktop](https://desktop.github.com/)
2. Crea un nuevo repositorio
3. Arrastra todos los archivos
4. Haz commit y push

#### Opción B: Línea de Comandos
```bash
# Inicializa el repositorio
git init
git add .
git commit -m "Primera versión del escáner de libros"

# Crea el repositorio en GitHub y súbelo
git remote add origin https://github.com/TU-USUARIO/escaner-libros.git
git branch -M main
git push -u origin main
```

### Paso 3: Activa GitHub Pages
1. Ve a tu repositorio en GitHub
2. Click en **Settings** (⚙️)
3. En el menú lateral, click en **Pages**
4. En "Source":
   - Selecciona: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
5. Click en **Save**
6. Espera 1-2 minutos
7. Refresca la página
8. Verás tu URL: `https://TU-USUARIO.github.io/escaner-libros`

### Paso 4: Instala la App

#### iPhone/iPad:
1. Abre tu URL en **Safari**
2. Toca el botón **Compartir** (□↑)
3. Baja y selecciona **"Añadir a pantalla de inicio"**
4. Toca **"Añadir"**
5. ✅ ¡Listo! La app está en tu pantalla de inicio

#### Android:
1. Abre tu URL en **Chrome**
2. Toca el menú **⋮** (arriba a la derecha)
3. Selecciona **"Añadir a pantalla de inicio"**
4. Toca **"Añadir"**
5. ✅ ¡Listo! La app está en tu pantalla de inicio

## 🎯 Primera Vez Usando la App

1. **Prepara tu CSV**
   ```csv
   Autor/a,Título,Editorial,Año
   Gabriel García Márquez,Cien años de soledad,Sudamericana,1967
   ```

2. **Abre la app** desde tu pantalla de inicio

3. **Carga tu CSV**
   - Toca "Seleccionar archivo CSV"
   - Elige tu archivo
   - Verás: "✅ Base de datos cargada: X libros"

4. **¡Empieza a escanear!**
   - Toca "📸 Activar Cámara"
   - Permite acceso a la cámara
   - Apunta al código ISBN
   - ¡BEEP! → Libro detectado

## ❓ Problemas Comunes

### "No puedo ver mi app en GitHub Pages"
- Espera 2-3 minutos después de activar Pages
- Verifica que el Branch sea `main` y la carpeta `/ (root)`
- Asegúrate de que `index.html` esté en la raíz del repositorio

### "Los iconos no aparecen"
- Verifica que `icon-192.png` y `icon-512.png` estén en la raíz
- Verifica que los nombres sean exactamente esos
- Haz commit y push de los iconos a GitHub

### "La cámara no funciona"
- Verifica que diste permisos de cámara
- Usa HTTPS (GitHub Pages usa HTTPS automáticamente)
- En iPhone, usa Safari (no Chrome)
- En Android, usa Chrome

### "No puedo instalar la app"
- En iPhone: Asegúrate de usar Safari
- En Android: Asegúrate de usar Chrome
- Verifica que estés usando HTTPS
- Intenta desde el navegador, no desde la app ya instalada

## 📞 ¿Necesitas Ayuda?

Abre un [Issue en GitHub](https://github.com/TU-USUARIO/escaner-libros/issues) describiendo:
1. Qué dispositivo usas (iPhone, Android, etc.)
2. Qué navegador usas
3. Qué error ves
4. Captura de pantalla (si es posible)

## ✅ Checklist de Instalación

- [ ] Generar iconos con `generate-icons.html`
- [ ] Subir todos los archivos a GitHub
- [ ] Activar GitHub Pages
- [ ] Esperar 2-3 minutos
- [ ] Abrir la URL en el navegador móvil
- [ ] Añadir a pantalla de inicio
- [ ] Abrir la app instalada
- [ ] Cargar CSV con libros
- [ ] Probar escanear un libro

¡Disfruta escaneando tus libros! 📚✨