# ChronoMap - Línea de Tiempo Operativa

ChronoMap es una aplicación web interactiva para crear y gestionar líneas de tiempo operativas. Permite visualizar actividades en un formato de timeline con funcionalidades de arrastrar, zoom, importación/exportación y más.

## 🚀 Características

- **Gestión de Actividades**: Agrega, edita y elimina actividades en la línea de tiempo
- **Interactividad**: Arrastra actividades para moverlas, usa los bordes para extender su duración
- **Modal de Propiedades**: Doble click en actividad abre modal flotante con todos los detalles
- **Sistema de Dependencias** ✨ NUEVO:
  - Define relaciones entre actividades (predecesoras y sucesoras)
  - Visualización gráfica con flechas en el timeline
  - Detección automática de conflictos de tiempo
  - Indicadores visuales de conflictos (rojo) vs dependencias válidas (gris)
  - Gestión completa desde el modal de propiedades
- **Subcarriles Dinámicos**: 
  - Detección automática de actividades solapadas
  - Reorganización manual arrastrando verticalmente
  - Altura de carriles ajustable según necesidad
- **Diferenciador Visual de Áreas**:
  - Fondo de color suave en cada carril
  - Etiqueta con nombre del área visible
  - Selector de color personalizable
- **Panel Colapsable**: Panel de áreas colapsable para más espacio
- **Copiar/Pegar**: 
  - Atajos de teclado (Ctrl+C / Ctrl+V)
  - Menú contextual (click derecho)
  - Duplicar actividades rápidamente
- **Zoom Avanzado**: 
  - Controles de zoom (0.5x - 10x)
  - Ctrl+Scroll para zoom intuitivo
- **Limpiar Lienzo**: Botón para limpiar todas las actividades con confirmación
- **Importación/Exportación**:
  - Importar proyectos desde archivos JSON
  - Exportar a JSON para guardar el progreso
  - Exportar a PNG de alta calidad (con padding mejorado)
- **Áreas Organizativas**: Organiza actividades en diferentes áreas/categorías
- **Interfaz Moderna**: Diseño limpio con Tailwind CSS y Phosphor Icons

## 🛠️ Tecnologías

El proyecto ha migrado de una arquitectura basada en Node.js a **HTML y JavaScript puro**, eliminando dependencias de backend y simplificando el despliegue.

### Stack Actual
- **HTML5**: Estructura semántica
- **JavaScript (ES6+)**: Lógica de la aplicación
- **Tailwind CSS (CDN)**: Estilos y diseño responsivo
- **Phosphor Icons (CDN)**: Biblioteca de iconos
- **html2canvas (CDN)**: Exportación a imágenes PNG

### Cambios Importantes
- ✅ Eliminadas dependencias de Node.js
- ✅ Migración a arquitectura cliente-side pura
- ✅ Uso de CDNs para bibliotecas externas
- ✅ No requiere servidor ni instalación de paquetes
- ✅ Funciona directamente en el navegador

## 📋 Roadmap

### Versión 1.3 (Actual) 🆕
- ✅ Sistema de dependencias entre actividades
- ✅ Visualización de relaciones con flechas SVG
- ✅ Detección de conflictos de tiempo
- ✅ Gestión de predecesoras y sucesoras en modal
- ✅ Exportación PNG mejorada (sin texto cortado)
- ✅ Limpieza automática de dependencias huérfanas

### Versión 1.2
- ✅ Modal de propiedades (doble click)
- ✅ Diferenciador visual de áreas (fondo + etiqueta)
- ✅ Panel de áreas colapsable
- ✅ Zoom con Ctrl+Scroll (0.5x - 10x)
- ✅ Botón limpiar lienzo con confirmación
- ✅ Selector de color para áreas

### Versión 1.1
- ✅ Sistema de subcarriles dinámicos
- ✅ Copiar/Pegar actividades (Ctrl+C/V)
- ✅ Menú contextual (click derecho)
- ✅ Duplicar actividades
- ✅ Arrastre vertical entre subcarriles
- ✅ Altura de carriles ajustable

### Versión 1.0
- ✅ Interfaz básica de línea de tiempo
- ✅ Agregar y editar actividades
- ✅ Arrastrar y redimensionar actividades
- ✅ Controles de zoom
- ✅ Importación/Exportación JSON
- ✅ Exportación a PNG
- ✅ Panel de áreas organizativas

### Próximas Funcionalidades (Roadmap v1.4+)
- [ ] Ruta crítica automática (Critical Path Method)
- [ ] Validación de dependencias circulares
- [ ] Ajuste automático de tiempos según dependencias
- [ ] UI para undo/redo (Ctrl+Z / Ctrl+Y)
- [ ] Múltiples timelines en un mismo proyecto
- [ ] Plantillas predefinidas
- [ ] Modo oscuro
- [ ] Más atajos de teclado
- [ ] Filtros y búsqueda avanzada
- [ ] Exportar a PDF

## 🚀 Instalación y Uso

### 🌐 Demo en Vivo
Prueba ChronoMap directamente en tu navegador:
👉 **[https://rubaanxd.github.io/ChronoMap/](https://rubaanxd.github.io/ChronoMap/)**

### Requisitos
- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- Conexión a internet (para cargar CDNs)

### Instalación Local
1. Clona el repositorio:
```bash
git clone https://github.com/rubaanxd/Timelines.git
cd Timelines
```

2. Abre el archivo `ChronoMap.html` en tu navegador:
- Doble clic en el archivo, o
- Arrastra el archivo a tu navegador, o
- Usa un servidor local (opcional)

### 🚀 Despliegue en GitHub Pages

Este proyecto está configurado para desplegarse automáticamente en GitHub Pages:

1. **Fork o clona el repositorio**
2. **Habilita GitHub Pages**:
   - Ve a Settings → Pages
   - Source: GitHub Actions
   - El workflow `.github/workflows/deploy.yml` se ejecutará automáticamente
3. **Accede a tu sitio**:
   - URL: `https://tu-usuario.github.io/Timelines/`
   - El despliegue toma ~2 minutos

**Archivos importantes para GitHub Pages:**
- `index.html` - Página de bienvenida
- `.nojekyll` - Evita procesamiento Jekyll
- `CNAME` - Para dominio personalizado (opcional)
- `.github/workflows/deploy.yml` - Automatización del despliegue

### Uso
1. **Agregar Actividad**: Click en "Nueva Actividad"
2. **Editar Actividad**: Doble click en actividad para abrir modal de propiedades
3. **Mover Actividad**: Arrastra la actividad horizontalmente
4. **Cambiar Subcarril**: Arrastra la actividad verticalmente dentro del área
5. **Extender Duración**: Arrastra desde los bordes de la actividad
6. **Gestionar Dependencias**:
   - Abre el modal de propiedades (doble click)
   - Sección "Predecesoras": Actividades que deben completarse antes
   - Sección "Sucesoras": Actividades que dependen de esta
   - Conflictos se marcan en rojo automáticamente
   - Las flechas en el timeline muestran las relaciones
7. **Copiar/Pegar**: Selecciona actividad y usa Ctrl+C / Ctrl+V
8. **Menú Contextual**: Click derecho sobre actividad para más opciones
9. **Zoom**: Usa los controles +/- o Ctrl+Scroll del mouse
10. **Colapsar Panel**: Click en botón de flecha en panel de áreas
11. **Limpiar Lienzo**: Click en botón "Limpiar" (con confirmación)
12. **Exportar**: Usa los botones JSON o PNG para guardar tu trabajo
13. **Importar**: Click en "Importar" para cargar un archivo JSON previamente guardado

## 📁 Estructura del Proyecto

```
Timelines/
├── ChronoMap.html              # Aplicación principal (todo en un archivo)
├── index.html                  # Página de bienvenida para GitHub Pages
├── README.md                   # Documentación del proyecto
├── .gitignore                  # Archivos ignorados por Git
├── .nojekyll                   # Configuración para GitHub Pages
├── CNAME                       # Dominio personalizado (opcional)
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions para despliegue automático
└── .context/                   # Documentación técnica (excluida de Git)
    ├── TECHNICAL.md
    ├── ARCHITECTURE.md
    ├── DEVELOPMENT_GUIDE.md
    ├── PROJECT_STATUS.md
    └── AI_CONTEXT.md
```

## 🤝 Contribución

Las contribuciones son bienvenidas. Por favor:
1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/NuevaFuncionalidad`)
3. Commit tus cambios (`git commit -m 'Agrega nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/NuevaFuncionalidad`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto está bajo la Licencia MIT.

## 👥 Autores

- Desarrollado por el equipo de ChronoMap

---

**Versión 1.3** - Sistema de Dependencias: relaciones entre actividades, visualización con flechas, detección de conflictos, exportación PNG mejorada.
