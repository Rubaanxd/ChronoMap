# ChronoMap - Línea de Tiempo Operativa

ChronoMap es una aplicación web interactiva para crear y gestionar líneas de tiempo operativas. Permite visualizar actividades en un formato de timeline con funcionalidades de arrastrar, zoom, importación/exportación y más.

## 🚀 Características

- **Gestión de Actividades**: Agrega, edita y elimina actividades en la línea de tiempo
- **Interactividad**: Arrastra actividades para moverlas, usa los bordes para extender su duración
- **Zoom**: Controles de zoom para visualizar diferentes escalas de tiempo
- **Importación/Exportación**:
  - Importar proyectos desde archivos JSON
  - Exportar a JSON para guardar el progreso
  - Exportar a PNG para compartir visualizaciones
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

### Versión 1.0 (Actual)
- ✅ Interfaz básica de línea de tiempo
- ✅ Agregar y editar actividades
- ✅ Arrastrar y redimensionar actividades
- ✅ Controles de zoom
- ✅ Importación/Exportación JSON
- ✅ Exportación a PNG
- ✅ Panel de áreas organizativas

### Próximas Funcionalidades (Roadmap)
- [ ] Persistencia local (localStorage)
- [ ] Múltiples timelines en un mismo proyecto
- [ ] Colaboración en tiempo real
- [ ] Plantillas predefinidas
- [ ] Modo oscuro
- [ ] Atajos de teclado
- [ ] Historial de cambios (undo/redo)
- [ ] Filtros y búsqueda avanzada
- [ ] Integración con calendarios externos

## 🚀 Instalación y Uso

### Requisitos
- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- Conexión a internet (para cargar CDNs)

### Instalación
1. Clona el repositorio:
```bash
git clone <repository-url>
cd Timelines
```

2. Abre el archivo `ChronoMap.html` en tu navegador:
- Doble clic en el archivo, o
- Arrastra el archivo a tu navegador, o
- Usa un servidor local (opcional)

### Uso
1. **Agregar Actividad**: Click en "Nueva Actividad"
2. **Mover Actividad**: Arrastra la actividad horizontalmente
3. **Extender Duración**: Arrastra desde los bordes de la actividad
4. **Zoom**: Usa los controles + y - en la barra superior
5. **Exportar**: Usa los botones JSON o PNG para guardar tu trabajo
6. **Importar**: Click en "Importar" para cargar un archivo JSON previamente guardado

## 📁 Estructura del Proyecto

```
Timelines/
├── ChronoMap.html    # Aplicación principal (todo en un archivo)
├── README.md         # Documentación
└── .gitignore        # Archivos ignorados por Git
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

**Versión 1.0** - Primera versión estable con funcionalidades core de gestión de timelines.
