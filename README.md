# ChronoMap - Línea de Tiempo Operativa 🚀

<div align="center">

![ChronoMap](https://img.shields.io/badge/version-1.4.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/Tailwind-38B2AC?logo=tailwind-css&logoColor=white)

**ChronoMap** es una aplicación web interactiva y moderna para crear y gestionar líneas de tiempo operativas. Visualiza actividades, gestiona dependencias, filtra por estado y comparte con un solo click.

[🌐 Demo en Vivo](https://rubaanxd.github.io/ChronoMap/) • [📖 Documentación](https://github.com/Rubaanxd/ChronoMap/wiki) • [🐛 Reportar Bug](https://github.com/Rubaanxd/ChronoMap/issues)

</div>

---

## ✨ Características Principales

### 🎨 **Interfaz Moderna**
- **Modo Oscuro** 🌙: Toggle persistente con paleta optimizada
- **Pan Inteligente** 🖐️: Navega arrastrando el espacio vacío, cursor contextual
- **Zoom Progresivo** 🔍: Detalle adaptativo (5, 10, 15, 30 min) según nivel de zoom
- **Diseño Responsivo**: Interfaz limpia con Tailwind CSS y Phosphor Icons

### 📊 **Gestión de Actividades**
- **Crear y Editar**: Modal completo con todos los detalles
- **Arrastrar y Soltar**: Mueve actividades horizontalmente y verticalmente
- **Redimensionar**: Extiende duración desde los bordes
- **Subcarriles Dinámicos**: Detección automática de solapamientos
- **Copiar/Pegar**: Atajos de teclado (Ctrl+C/V) y menú contextual
- **Estado y Prioridad**: Marca actividades como pendientes, en progreso o completadas

### 🔗 **Sistema de Dependencias**
- Define relaciones entre actividades (predecesoras y sucesoras)
- Visualización gráfica con flechas SVG en el timeline
- Detección automática de conflictos de tiempo
- Indicadores visuales: rojo (conflictos) vs gris (válidas)
- Gestión completa desde el modal de propiedades

### 🔍 **Búsqueda y Filtros**
- **Búsqueda en Tiempo Real**: Encuentra actividades por nombre
- **Filtros por Área**: Selecciona múltiples áreas con checkboxes
- **Filtros por Estado**: Pendiente, En Progreso, Completado
- **Filtros por Prioridad**: Baja, Media, Alta
- **Badge Contador**: Muestra cantidad de filtros activos
- **Filtros Combinables**: Lógica AND para búsqueda precisa

### 🌐 **Compartir y Exportar**
- **Compartir con Link** 🔗: URL comprimida en Base64, modo readonly automático
- **Exportar HTML** 📄: Archivo standalone sin dependencias
- **Exportar JSON** 💾: Guarda tu progreso
- **Exportar PNG** 🖼️: Imagen de alta calidad
- **Modal Elegante**: Copia al portapapeles con un click

### 👁️ **Modo de Solo Vista**
- **Modo Readonly**: Visualiza sin editar desde URL (`?view=readonly`)
- **Modo Presentación**: Toggle interno para presentaciones
- **Controles Deshabilitados**: Drag & drop y edición bloqueados
- **Badge Visual**: Indica el modo activo
- **Ideal para Compartir**: Links y HTML exportado en modo readonly

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

### Versión 1.4.0 (Actual) 🆕
- ✅ **Modo Oscuro**: Toggle persistente con paleta optimizada
- ✅ **Pan Inteligente**: Navegación arrastrando espacio vacío
- ✅ **Zoom Progresivo**: Detalle adaptativo según nivel de zoom
- ✅ **Búsqueda en Tiempo Real**: Filtrado instantáneo por nombre
- ✅ **Sistema de Filtros**: Por área, estado y prioridad
- ✅ **Compartir con Link**: URL comprimida en Base64
- ✅ **Exportar HTML**: Archivo standalone sin dependencias
- ✅ **Modo de Solo Vista**: Readonly y presentación
- ✅ **Estado y Prioridad**: Campos en actividades
- ✅ **Cursor Contextual**: Grab en espacio, move en nodos

### Versión 1.3
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

### Próximas Funcionalidades (Roadmap v1.5+)
- [ ] **Tags Personalizados**: Etiquetas customizables por actividad
- [ ] **Ruta Crítica**: Critical Path Method automático
- [ ] **Validación de Dependencias**: Detección de ciclos
- [ ] **Ajuste Automático**: Tiempos según dependencias
- [ ] **Undo/Redo**: Historial de cambios (Ctrl+Z/Y)
- [ ] **Múltiples Timelines**: Varios proyectos en uno
- [ ] **Plantillas**: Timelines predefinidos
- [ ] **Exportar PDF**: Documentos imprimibles
- [ ] **Colaboración**: Edición en tiempo real
- [ ] **Responsive Mobile**: Optimización para móviles

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
git clone https://github.com/rubaanxd/ChronoMap.git
cd ChronoMap
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
   - URL: `https://tu-usuario.github.io/ChronoMap/`
   - El despliegue toma ~2 minutos

**Archivos importantes para GitHub Pages:**
- `index.html` - Página de bienvenida
- `.nojekyll` - Evita procesamiento Jekyll
- `CNAME` - Para dominio personalizado (opcional)
- `.github/workflows/deploy.yml` - Automatización del despliegue

### 📖 Guía de Uso

#### Gestión Básica
1. **Agregar Actividad**: Click en "Nueva Actividad"
2. **Editar Actividad**: Doble click para abrir modal de propiedades
3. **Mover Actividad**: Arrastra horizontalmente
4. **Cambiar Subcarril**: Arrastra verticalmente dentro del área
5. **Extender Duración**: Arrastra desde los bordes

#### Navegación
6. **Pan (Mano)**: Arrastra el espacio vacío para desplazarte
7. **Zoom**: Usa los controles +/- o Ctrl+Scroll del mouse
8. **Modo Oscuro**: Toggle en el header (persistente)
9. **Colapsar Panel**: Click en botón de flecha en panel de áreas

#### Búsqueda y Filtros
10. **Buscar**: Escribe en la barra de búsqueda (tiempo real)
11. **Filtrar**: Click en "Filtros" para abrir panel
    - Selecciona áreas, estados y prioridades
    - Badge muestra cantidad de filtros activos
    - Click "Limpiar Filtros" para resetear

#### Gestión Avanzada
12. **Estado y Prioridad**: Configura en modal de propiedades
    - Estado: Pendiente, En Progreso, Completado
    - Prioridad: Baja, Media, Alta
13. **Dependencias**:
    - Abre el modal de propiedades (doble click)
    - Sección "Predecesoras": Actividades previas
    - Sección "Sucesoras": Actividades siguientes
    - Conflictos se marcan en rojo automáticamente
    - Flechas en el timeline muestran relaciones
14. **Copiar/Pegar**: Selecciona y usa Ctrl+C / Ctrl+V
15. **Menú Contextual**: Click derecho para más opciones

#### Compartir y Exportar
16. **Compartir Link**: Click en "Compartir"
    - Se copia automáticamente al portapapeles
    - Link comprimido en Base64
    - Abre en modo readonly
17. **Exportar HTML**: Archivo standalone sin dependencias
18. **Exportar JSON**: Guarda tu progreso
19. **Exportar PNG**: Imagen de alta calidad
20. **Importar**: Carga archivo JSON previamente guardado

#### Modo Presentación
21. **Toggle Presentación**: Click en botón "Presentación"
    - Oculta controles de edición
    - Ideal para mostrar a otros
    - Click "Editar" para volver

## 📁 Estructura del Proyecto

```
ChronoMap/
├── ChronoMap.html              # Aplicación principal (todo en un archivo)
├── index.html                  # Página de bienvenida para GitHub Pages
├── README.md                   # Documentación del proyecto
├── CONTRIBUTING.md             # Guía de contribución
├── .gitignore                  # Archivos ignorados por Git
├── .nojekyll                   # Configuración para GitHub Pages
├── CNAME                       # Dominio personalizado (opcional)
└── .github/
    ├── README.md               # Documentación de workflows
    ├── BRANCH_STRATEGY.md      # Estrategia de branches
    └── workflows/
        ├── deploy.yml          # Despliegue automático a GitHub Pages
        └── dev-ci.yml          # CI para rama dev
```

## 🤝 Contribución

¡Las contribuciones son bienvenidas! Por favor lee [CONTRIBUTING.md](CONTRIBUTING.md) para más detalles.

### Flujo de Trabajo
1. **Fork** el proyecto
2. **Crea una rama** para tu feature (`git checkout -b feature/NuevaFuncionalidad`)
3. **Commit** tus cambios (`git commit -m 'feat: Agrega nueva funcionalidad'`)
4. **Push** a la rama (`git push origin feature/NuevaFuncionalidad`)
5. **Abre un Pull Request** a la rama `dev`

### Estrategia de Branches
- `main`: Producción (GitHub Pages)
- `dev`: Desarrollo activo
- `feature/*`: Nuevas funcionalidades
- `fix/*`: Correcciones de bugs

Ver [.github/BRANCH_STRATEGY.md](.github/BRANCH_STRATEGY.md) para más detalles.

## 📝 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 👥 Autores

- **Rubaanxd** - [GitHub](https://github.com/Rubaanxd)

## 🙏 Agradecimientos

- [Tailwind CSS](https://tailwindcss.com/) - Framework CSS
- [Phosphor Icons](https://phosphoricons.com/) - Biblioteca de iconos
- [html2canvas](https://html2canvas.hertzen.com/) - Exportación a PNG

---

<div align="center">

**Versión 1.4.0** - Modo Oscuro, Búsqueda y Filtros, Compartir con Link, Exportar HTML

Hecho con ❤️ por [Rubaanxd](https://github.com/Rubaanxd)

[⬆ Volver arriba](#chronomap---línea-de-tiempo-operativa-)

</div>
