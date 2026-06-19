# 🌿 Estrategia de Ramas - ChronoMap

## Estructura de Branching

```
┌─────────────────────────────────────────────────────────┐
│                         main                            │
│  (Producción - GitHub Pages - Solo merge desde dev)    │
└─────────────────────────────────────────────────────────┘
                            ▲
                            │ merge cuando esté estable
                            │
┌─────────────────────────────────────────────────────────┐
│                          dev                            │
│     (Desarrollo - Integración de features)              │
└─────────────────────────────────────────────────────────┘
                            ▲
                            │ merge cuando feature esté completa
                            │
        ┌───────────────────┴───────────────────┐
        │                                       │
┌───────────────────┐                  ┌───────────────────┐
│  feature/nombre   │                  │   hotfix/nombre   │
│  (Nueva feature)  │                  │  (Bug urgente)    │
└───────────────────┘                  └───────────────────┘
```

## 📋 Descripción de Ramas

### `main` - Rama de Producción
- **Estado**: Siempre estable y deployable
- **Despliegue**: Automático a GitHub Pages
- **Protección**: ⛔ No hacer commits directos
- **Merge desde**: Solo desde `dev` después de testing completo
- **Tags**: Versiones de release (v1.3.0, v1.4.0, etc.)

### `dev` - Rama de Desarrollo
- **Estado**: Integración continua de features
- **Propósito**: Testing antes de producción
- **Base para**: Todas las ramas `feature/*`
- **CI/CD**: Validación automática con GitHub Actions
- **Merge a main**: Solo cuando esté completamente testeado

### `feature/*` - Ramas de Funcionalidades
- **Naming**: `feature/nombre-descriptivo`
- **Base**: Siempre desde `dev`
- **Duración**: Corta (días, no semanas)
- **Merge a**: `dev` cuando esté completa
- **Ejemplos**:
  - `feature/ruta-critica`
  - `feature/modo-oscuro`
  - `feature/validacion-circular`
  - `feature/undo-redo`

### `hotfix/*` - Correcciones Urgentes
- **Naming**: `hotfix/descripcion-bug`
- **Base**: Desde `main` (producción)
- **Merge a**: `main` Y `dev` (ambas)
- **Tag**: Incrementa PATCH (v1.3.0 → v1.3.1)
- **Ejemplos**:
  - `hotfix/exportacion-png-error`
  - `hotfix/dependencias-circulares`

## 🔄 Workflows por Tipo de Cambio

### 1️⃣ Nueva Funcionalidad (Feature)

```bash
# 1. Actualizar dev
git checkout dev
git pull origin dev

# 2. Crear feature branch
git checkout -b feature/mi-funcionalidad

# 3. Desarrollar y commitear
git add .
git commit -m "feat: Descripción del cambio"

# 4. Push de la feature
git push origin feature/mi-funcionalidad

# 5. Cuando esté lista, merge a dev
git checkout dev
git pull origin dev
git merge feature/mi-funcionalidad

# 6. Push dev
git push origin dev

# 7. Limpiar (opcional)
git branch -d feature/mi-funcionalidad
git push origin --delete feature/mi-funcionalidad
```

### 2️⃣ Release a Producción

```bash
# 1. Asegurar que dev está testeado
git checkout dev
git pull origin dev

# 2. Merge a main
git checkout main
git pull origin main
git merge dev

# 3. Tag de versión
git tag -a v1.4.0 -m "Release v1.4.0: Ruta crítica y optimizaciones"

# 4. Push con tags
git push origin main --tags

# 5. GitHub Pages se despliega automáticamente
```

### 3️⃣ Hotfix Urgente

```bash
# 1. Desde main
git checkout main
git pull origin main
git checkout -b hotfix/bug-critico

# 2. Arreglar el bug
git add .
git commit -m "fix: Corregir bug crítico en exportación"

# 3. Merge a main
git checkout main
git merge hotfix/bug-critico

# 4. Tag de patch
git tag -a v1.3.1 -m "Hotfix v1.3.1: Bug en exportación PNG"

# 5. Push main
git push origin main --tags

# 6. Merge también a dev
git checkout dev
git merge hotfix/bug-critico
git push origin dev

# 7. Limpiar
git branch -d hotfix/bug-critico
```

## 🎯 Reglas de Oro

### ✅ DO (Hacer)
- ✅ Siempre crear features desde `dev`
- ✅ Hacer commits pequeños y frecuentes
- ✅ Testear antes de merge a `dev`
- ✅ Usar mensajes de commit descriptivos
- ✅ Actualizar `dev` antes de crear feature
- ✅ Eliminar branches después de merge
- ✅ Usar tags para releases

### ❌ DON'T (No Hacer)
- ❌ Nunca commit directo a `main`
- ❌ No crear features desde `main`
- ❌ No hacer merge sin testing
- ❌ No pushear código roto
- ❌ No dejar features abiertas por semanas
- ❌ No hacer force push a `main` o `dev`
- ❌ No mezclar múltiples features en una rama

## 🚦 Estados de las Ramas

### main (Producción)
```
Estado: 🟢 ESTABLE
Versión: v1.3.0
Último deploy: 2026-06-19
URL: https://rubaanxd.github.io/ChronoMap/
```

### dev (Desarrollo)
```
Estado: 🟡 EN DESARROLLO
Features activas: 0
Próximo release: v1.4.0
```

## 📊 Versionado

Seguimos [Semantic Versioning](https://semver.org/):

```
MAJOR.MINOR.PATCH
  │     │     │
  │     │     └─ Bug fixes (v1.3.1)
  │     └─────── Nuevas features (v1.4.0)
  └───────────── Breaking changes (v2.0.0)
```

### Historial de Versiones

- **v1.3.0** (Actual) - Sistema de dependencias
- **v1.2.0** - Modal de propiedades y UX
- **v1.1.0** - Subcarriles dinámicos
- **v1.0.0** - Release inicial

### Próximas Versiones

- **v1.4.0** - Ruta crítica y validación circular
- **v1.5.0** - Undo/Redo
- **v2.0.0** - Múltiples timelines

## 🔧 Configuración de Protección

### Recomendaciones para GitHub

1. **Proteger `main`**:
   - Settings → Branches → Add rule
   - Branch name pattern: `main`
   - ✅ Require pull request reviews
   - ✅ Require status checks to pass
   - ✅ Include administrators

2. **Proteger `dev`** (opcional):
   - Settings → Branches → Add rule
   - Branch name pattern: `dev`
   - ✅ Require status checks to pass

## 📞 Soporte

¿Dudas sobre el flujo de trabajo?
- 📖 Lee `CONTRIBUTING.md`
- 💬 Abre un issue
- 📧 Contacta al equipo

---

**Última actualización**: 2026-06-19
**Versión del documento**: 1.0
