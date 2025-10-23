# 📚 Escáner de Libros - PWA

Aplicación web progresiva (PWA) para escanear códigos ISBN de libros y compararlos automáticamente con tu base de datos personal.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Características

- 📸 **Escaneo con cámara** - Escanea códigos de barras ISBN directamente con tu móvil
- ✅ **Comparación inteligente** - Compara automáticamente con tu base de datos usando IA
- 📂 **Sistema de carpetas** - Organiza libros en "Coincidencias" y "No Coincidencias"
- 💾 **Exportación CSV** - Exporta tus resultados con estadísticas completas
- 📱 **Instalable** - Instálala como app nativa en tu móvil
- 🔒 **100% privado** - Todos los datos se guardan localmente en tu dispositivo
- 🌐 **Funciona offline** - Una vez cargada, funciona sin conexión a internet*

*_La búsqueda de información de libros nuevos requiere conexión_

## 🚀 Instalación

### Opción 1: GitHub Pages (Recomendado)

1. **Fork este repositorio**
   - Haz clic en "Fork" arriba a la derecha
   
2. **Activa GitHub Pages**
   - Ve a Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main` / `(root)`
   - Haz clic en "Save"
   
3. **Accede a tu app**
   - URL: `https://tu-usuario.github.io/nombre-del-repo`
   - Ejemplo: `https://juanperez.github.io/escaner-libros`

### Opción 2: Descargar y Usar Localmente

1. **Descarga el repositorio**
   ```bash
   git clone https://github.com/tu-usuario/escaner-libros.git
   cd escaner-libros
   ```

2. **Abre en tu navegador**
   - Simplemente abre `index.html` con tu navegador
   - O usa un servidor local:
   ```bash
   python -m http.server 8000
   # Luego abre: http://localhost:8000
   ```

## 📱 Instalar como App en tu Móvil

### iPhone/iPad (Safari)

1. Abre la app en Safari
2. Toca el botón de **Compartir** (cuadrado con flecha)
3. Desplázate y selecciona **"Añadir a pantalla de inicio"**
4. Dale un nombre y toca **"Añadir"**
5. ¡Listo! Ahora tienes un icono en tu pantalla

### Android (Chrome)

1. Abre la app en Chrome
2. Toca el menú (⋮) en la esquina superior derecha
3. Selecciona **"Añadir a pantalla de inicio"** o **"Instalar aplicación"**
4. Confirma tocando **"Añadir"**
5. ¡Listo! La app aparecerá en tu pantalla de inicio

## 🎯 Uso

### 1️⃣ Cargar tu Base de Datos

Prepara un archivo CSV con este formato:

```csv
Autor/a,Título,Editorial,Año
Gabriel García Márquez,Cien años de soledad,Sudamericana,1967
Isabel Allende,La casa de los espíritus,Plaza & Janés,1982
Mario Vargas Llosa,La ciudad y los perros,Seix Barral,1963
```

**Importante:**
- Primera línea: encabezados (Autor/a, Título, Editorial, Año)
- Separador: comas (`,`)
- Si hay comas en el texto, usa comillas: `"García Márquez, Gabriel"`

**Cargar el CSV en la app:**
1. Abre la app
2. Toca "Seleccionar archivo CSV"
3. Elige tu archivo
4. Verás: "✅ Base de datos cargada: X libros"

### 2️⃣ Escanear Libros

1. **Activa la cámara**
   - Toca "📸 Activar Cámara"
   - Permite acceso a la cámara cuando te lo pida

2. **Escanea el código**
   - Apunta al código de barras ISBN del libro
   - Centra el código en el recuadro verde
   - Mantén el móvil estable
   - ¡BEEP! → El código fue detectado

3. **Revisa el resultado**
   - ✅ **Verde**: Coincidencia exacta en tu base de datos
   - ⚠️ **Amarillo**: Posibles coincidencias similares
   - ❌ **Rojo**: No encontrado en tu base de datos

4. **Archiva el libro**
   - "📂 Coincide" → Si está en tu base de datos
   - "❌ No Coincide" → Si NO está en tu base de datos
   - "⏭️ Siguiente" → Para escanear otro sin archivar

### 3️⃣ Revisar Historial

1. Toca el icono de "Historial" en la barra inferior
2. Verás todos los libros escaneados con:
   - Portada del libro
   - Título y autor
   - Estado (Coincide / No Coincide / Pendiente)
   - ISBN escaneado

### 4️⃣ Exportar Resultados

1. Ve a "Historial"
2. Toca "💾 Exportar Resultados"
3. Se descargará un CSV con:
   - Estado de cada libro
   - Información completa
   - Estadísticas del escaneo

## 💡 Consejos para Mejores Escaneos

### ✅ Hacer
- Usa **buena iluminación** (natural o artificial brillante)
- Mantén el móvil **estable** con ambas manos
- **Centra** el código en el recuadro verde
- Mantén **distancia de 10-15cm**
- **Espera 1-2 segundos** para que detecte

### ❌ Evitar
- Reflejos en el código de barras
- Códigos dañados o borrosos
- Movimiento excesivo del móvil
- Iluminación muy tenue
- Demasiado cerca o lejos

## 🔧 Solución de Problemas

### "Error al acceder a la cámara"

**Solución:**
1. Ve a configuración de tu navegador
2. Busca "Permisos del sitio" o "Camera"
3. Permite acceso a la cámara para este sitio
4. Recarga la página

### "No detecta el código"

**Posibles causas:**
- Código de barras dañado
- Iluminación insuficiente
- Código muy pequeño o muy grande
- No es un ISBN válido

**Solución:**
- Mejora la iluminación
- Limpia la cámara del móvil
- Ajusta la distancia
- Intenta con otro libro para verificar

### "La app no se instala"

**iPhone:**
- Asegúrate de usar Safari (no Chrome)
- Verifica que iOS esté actualizado

**Android:**
- Usa Chrome (versión reciente)
- Verifica que Android esté actualizado

## 🛠️ Tecnologías Utilizadas

- **React 18** - Framework de interfaz
- **QuaggaJS** - Escaneo de códigos de barras
- **Google Books API** - Información de libros
- **Open Library API** - Información alternativa de libros
- **PWA** - Progressive Web App
- **Service Worker** - Funcionamiento offline
- **LocalStorage** - Almacenamiento local

## 📊 Tipos de ISBN Soportados

✅ ISBN-13 (13 dígitos) - Ej: 9788420412146  
✅ ISBN-10 (10 dígitos) - Ej: 8420412147  
✅ EAN-13 (Códigos europeos)  
✅ UPC (Códigos americanos)

## 🔒 Privacidad

- **100% privado**: Todos los datos se guardan localmente
- **Sin seguimiento**: No se envía información a servidores externos
- **Sin cuentas**: No necesitas registrarte
- **Control total**: Puedes borrar todos los datos cuando quieras

## 📄 Estructura del Proyecto

```
book-scanner-app/
├── index.html          # Aplicación principal
├── styles.css          # Estilos CSS
├── manifest.json       # Configuración PWA
├── sw.js              # Service Worker
├── icon-192.png       # Icono 192x192
├── icon-512.png       # Icono 512x512
└── README.md          # Este archivo
```

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 🙏 Agradecimientos

- [QuaggaJS](https://github.com/ericblade/quagga2) por el escaneo de códigos
- [Google Books API](https://developers.google.com/books) por la información de libros
- [Open Library](https://openlibrary.org/) por la API alternativa

## 📮 Contacto

¿Preguntas? ¿Sugerencias? Abre un [Issue](https://github.com/tu-usuario/escaner-libros/issues) en GitHub.

---

⭐ Si te gusta este proyecto, ¡dale una estrella en GitHub!

Hecho con ❤️ y ☕