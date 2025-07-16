# 📋 Sistema MOVES III - Formulario Automatizado

![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-deployed-brightgreen)
![Version](https://img.shields.io/badge/version-4.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

> Sistema de procesamiento automatizado para solicitudes del programa MOVES III con integración completa con Google Apps Script.

## 🚀 **DEMO EN VIVO**

**🔗 Formulario**: [https://tu-usuario.github.io/sistema-moves-iii/](https://tu-usuario.github.io/sistema-moves-iii/)

*Reemplaza `tu-usuario` con tu nombre de usuario de GitHub*

## ✨ **Características Principales**

- ✅ **Formulario HTML Responsive** - Compatible con todos los dispositivos
- ✅ **Subida Múltiple de Archivos** - Drag & drop con validación automática
- ✅ **Integración Google Apps Script** - Procesamiento automático en la nube
- ✅ **Generación Automática de Documentos** - PDFs de solicitud, autorización y declaración
- ✅ **Notificaciones por Email** - Confirmaciones automáticas al cliente y administrador
- ✅ **Sistema de Métricas** - Monitoreo en tiempo real del rendimiento
- ✅ **Respaldos Automáticos** - Seguridad de datos garantizada
- ✅ **HTTPS Nativo** - Seguridad completa con GitHub Pages

## 🛠️ **Tecnologías Utilizadas**

| Tecnología | Propósito | Versión |
|------------|-----------|---------|
| **HTML5 + CSS3** | Interfaz de usuario | Latest |
| **JavaScript ES6+** | Lógica del cliente | Latest |
| **Google Apps Script** | Backend y automatización | v4.0 |
| **Google Drive API** | Almacenamiento de archivos | v3 |
| **Google Sheets API** | Base de datos | v4 |
| **GitHub Pages** | Hosting estático | Latest |

## 📁 **Estructura del Proyecto**

```
sistema-moves-iii/
├── README.md                 # ← Este archivo
├── index.html               # ← Formulario principal
├── assets/
│   ├── images/
│   │   └── logo.png         # ← Logo de Innonea Lab
│   └── docs/
│       └── manual.pdf       # ← Manual de usuario
├── google-apps-script/
│   ├── codigo-principal.js  # ← Script principal v4.0
│   ├── optimizaciones.js    # ← Módulos de optimización
│   └── configuracion.md     # ← Guía de configuración
└── docs/
    ├── implementacion.md     # ← Guía de implementación
    ├── api-reference.md      # ← Referencia de API
    └── troubleshooting.md    # ← Solución de problemas
```

## 🚀 **Guía de Configuración Rápida**

### **Paso 1: Clonar el Repositorio**

```bash
# Opción A: Usando GitHub Desktop (Recomendado)
1. Abrir GitHub Desktop
2. File → Clone Repository
3. URL: https://github.com/tu-usuario/sistema-moves-iii.git

# Opción B: Usando Git CLI
git clone https://github.com/tu-usuario/sistema-moves-iii.git
cd sistema-moves-iii
```

### **Paso 2: Configurar Google Apps Script**

1. **Ir a [script.google.com](https://script.google.com)**
2. **Crear nuevo proyecto** → Nombrar: "Sistema MOVES III v4.0"
3. **Copiar el código** desde `google-apps-script/codigo-principal.js`
4. **Configurar variables**:
   ```javascript
   const CONFIG = {
     SPREADSHEET_ID: 'TU_SPREADSHEET_ID',
     PLANTILLA_AUTORIZACION_MOVES: 'TU_PLANTILLA_ID',
     // ... resto de configuración
   };
   ```
5. **Publicar como Web App**:
   - Implementar → Nueva implementación
   - Tipo: Aplicación web
   - Ejecutar como: Yo
   - Acceso: Cualquier persona
   - **Copiar la URL generada**

### **Paso 3: Actualizar el Formulario**

En `index.html`, buscar y actualizar:

```html
<!-- Línea 350 aproximadamente -->
<form id="movesForm" action="TU_URL_DE_GOOGLE_APPS_SCRIPT_AQUI" method="POST" enctype="multipart/form-data">
```

### **Paso 4: Activar GitHub Pages**

1. **Ir a Settings** de tu repositorio
2. **Scroll hasta "Pages"**
3. **Source**: Deploy from a branch
4. **Branch**: main / (root)
5. **Save**
6. **Esperar 2-3 minutos**
7. **Tu formulario estará disponible en**: `https://tu-usuario.github.io/sistema-moves-iii/`

## 📊 **Panel de Control y Monitoreo**

### **Métricas Disponibles**

El sistema incluye un panel de métricas accesible desde Google Apps Script:

```javascript
// Ejecutar en Google Apps Script Console
metricas.obtenerReporte();
```

**Métricas incluidas**:
- 📈 Formularios procesados
- 📎 Archivos subidos
- ⏱️ Tiempo promedio de procesamiento
- 🎯 Tasa de éxito
- ❌ Errores registrados

### **Funciones de Diagnóstico**

```javascript
// Verificar estado del sistema
diagnosticarSistemaHTML();

// Generar reporte completo
generarReporteCompleto();

// Limpiar archivos temporales
limpiezaAutomatica();
```

## 🔧 **Configuración Avanzada**

### **Variables de Entorno**

El sistema detecta automáticamente que está siendo ejecutado desde GitHub Pages y ajusta su comportamiento:

```javascript
// Detección automática del entorno
if (window.location.hostname.includes('github.io')) {
    console.log('🌐 Ejecutándose desde GitHub Pages');
    // Optimizaciones específicas para GitHub Pages
}
```

### **Personalización del Tema**

Puedes personalizar los colores editando las variables CSS en `index.html`:

```css
:root {
    --primary-color: #667eea;      /* Color principal */
    --secondary-color: #764ba2;    /* Color secundario */
    --success-color: #28a745;      /* Color de éxito */
    --warning-color: #ffc107;      /* Color de advertencia */
    --danger-color: #dc3545;       /* Color de error */
}
```

## 📱 **Compatibilidad**

| Plataforma | Estado | Notas |
|------------|--------|-------|
| **Chrome 90+** | ✅ Completo | Recomendado |
| **Firefox 88+** | ✅ Completo | Completamente compatible |
| **Safari 14+** | ✅ Completo | Compatible con iOS/macOS |
| **Edge 90+** | ✅ Completo | Chromium-based |
| **Mobile Chrome** | ✅ Completo | Responsive design |
| **Mobile Safari** | ✅ Completo | Compatible con iOS |

## 🚨 **Solución de Problemas**

### **Problema: Los archivos no se suben**

```bash
1. Verificar que la URL de Google Apps Script sea correcta
2. Comprobar que el script esté publicado como "Cualquier persona"
3. Validar que los archivos sean menores a 25MB
4. Verificar tipos de archivo permitidos: PDF, JPG, PNG, DOC, DOCX
```

### **Problema: Error 403 o CORS**

```bash
1. Verificar que tanto GitHub Pages como Google Apps Script usen HTTPS
2. Redeployar la aplicación web en Google Apps Script
3. Limpiar caché del navegador
```

### **Problema: No se generan documentos**

```bash
1. Verificar IDs de plantillas en CONFIG
2. Comprobar permisos de acceso a Google Drive
3. Verificar cuota disponible en Google Drive
```

## 📞 **Soporte y Contacto**

### **Desarrollado por Innonea Lab**

- 📧 **Email**: innonea.lab@gmail.com
- 🌐 **Web**: [Sitio web de Innonea Lab]
- 📱 **Soporte**: Disponible de Lunes a Viernes, 9:00 - 18:00 CET

### **Reportar Problemas**

Si encuentras algún problema:

1. **Abrir un Issue** en este repositorio
2. **Incluir información**:
   - Navegador y versión
   - Pasos para reproducir el problema
   - Capturas de pantalla si es posible
   - Logs de la consola del navegador

### **Contribuir al Proyecto**

¡Las contribuciones son bienvenidas! 

1. **Fork** el repositorio
2. **Crear rama** para tu feature: `git checkout -b feature/nueva-funcionalidad`
3. **Commit** tus cambios: `git commit -m 'Añadir nueva funcionalidad'`
4. **Push** a la rama: `git push origin feature/nueva-funcionalidad`
5. **Abrir Pull Request**

## 📄 **Licencia**

Este proyecto está bajo la Licencia MIT. Ver archivo `LICENSE` para más detalles.

## 🎯 **Roadmap**

### **v4.1 (Próximo)**
- [ ] Dashboard web de administración
- [ ] Notificaciones push
- [ ] Integración con SMS
- [ ] Firma digital de documentos

### **v4.2 (Futuro)**
- [ ] App móvil nativa
- [ ] API REST pública
- [ ] Machine Learning para validación
- [ ] OCR para extracción automática de datos

## 📈 **Estadísticas del Proyecto**

- ⭐ **Stars**: Si te gusta el proyecto, ¡dale una estrella!
- 🍴 **Forks**: Contribuciones de la comunidad
- 🐛 **Issues**: Problemas reportados y resueltos
- 📊 **Commits**: Historial de desarrollo

## 🔄 **Changelog**

### **v4.0 - Actual**
- ✅ Soporte completo para GitHub Pages
- ✅ Interfaz rediseñada y responsive
- ✅ Sistema de métricas avanzado
- ✅ Optimizaciones de rendimiento
- ✅ Mejor manejo de errores

### **v3.0**
- ✅ Integración con Google Apps Script
- ✅ Generación automática de documentos
- ✅ Sistema de notificaciones

### **v2.0**
- ✅ Formulario HTML básico
- ✅ Validación de archivos

### **v1.0**
- ✅ Prototipo inicial

---

**⚡ Desarrollado con pasión por automatización por [Innonea Lab](mailto:innonea.lab@gmail.com)**

*¿Te gusta este proyecto? ¡Dale una ⭐ en GitHub!*
