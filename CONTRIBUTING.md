# 🤝 Guía de Contribución - ChronoMap

## 📋 Flujo de Trabajo con Git

### Estructura de Ramas

```
main (producción)
  ↓
dev (desarrollo)
  ↓
feature/* (nuevas funcionalidades)
  ↓
hotfix/* (correcciones urgentes)
```

### Ramas Principales

#### `main` - Producción
- **Propósito**: Código estable y listo para producción
- **Despliegue**: Automático a GitHub Pages
- **Protección**: Solo merge desde `dev` después de testing
- **Regla**: Nunca hacer commit directo aquí

#### `dev` - Desarrollo
- **Propósito**: Integración de nuevas features
- **Testing**: Pruebas antes de merge a `main`
- **Workflow**: Base para todas las features
- **Regla**: Merge solo cuando la feature esté completa

### Ramas de Trabajo

#### `feature/*` - Nuevas Funcionalidades
```bash
# Crear feature desde dev
git checkout dev
git pull origin dev
git checkout -b feature/nombre-descriptivo

# Ejemplos:
git checkout -b feature/ruta-critica
git checkout -b feature/modo-oscuro
git checkout -b feature/undo-redo
```

#### `hotfix/*` - Correcciones Urgentes
```bash
# Crear hotfix desde main
git checkout main
git pull origin main
git checkout -b hotfix/descripcion-bug

# Ejemplo:
git checkout -b hotfix/exportacion-png-error
```

## 🔄 Workflow Completo

### 1. Iniciar Nueva Feature

```bash
# Actualizar dev
git checkout dev
git pull origin dev

# Crear rama de feature
git checkout -b feature/mi-nueva-funcionalidad

# Trabajar en tu código...
# Hacer commits frecuentes
git add .
git commit -m "feat: Descripción de cambio"
```

### 2. Finalizar Feature

```bash
# Asegurar que dev está actualizado
git checkout dev
git pull origin dev

# Volver a tu feature
git checkout feature/mi-nueva-funcionalidad

# Rebase con dev (opcional pero recomendado)
git rebase dev

# Merge a dev
git checkout dev
git merge feature/mi-nueva-funcionalidad

# Push a dev
git push origin dev

# Eliminar rama local (opcional)
git branch -d feature/mi-nueva-funcionalidad
```

### 3. Release a Producción

```bash
# Cuando dev esté estable y testeado
git checkout main
git pull origin main
git merge dev

# Tag de versión
git tag -a v1.4.0 -m "Release v1.4: Ruta crítica y validación circular"

# Push con tags
git push origin main --tags
```

### 4. Hotfix Urgente

```bash
# Desde main
git checkout main
git checkout -b hotfix/bug-critico

# Arreglar el bug
git add .
git commit -m "fix: Descripción del bug arreglado"

# Merge a main
git checkout main
git merge hotfix/bug-critico

# También merge a dev
git checkout dev
git merge hotfix/bug-critico

# Push ambas ramas
git push origin main
git push origin dev

# Tag de patch
git tag -a v1.3.1 -m "Hotfix: Bug crítico"
git push origin main --tags
```

## 📝 Convenciones de Commits

Usamos [Conventional Commits](https://www.conventionalcommits.org/):

```bash
# Nuevas funcionalidades
git commit -m "feat: Agregar sistema de ruta crítica"

# Corrección de bugs
git commit -m "fix: Corregir cálculo de dependencias circulares"

# Documentación
git commit -m "docs: Actualizar README con nuevas features"

# Refactorización
git commit -m "refactor: Optimizar algoritmo de subcarriles"

# Estilos/formato
git commit -m "style: Mejorar espaciado en modal de propiedades"

# Tests
git commit -m "test: Agregar tests para sistema de dependencias"

# Configuración
git commit -m "chore: Actualizar workflow de GitHub Actions"

# Performance
git commit -m "perf: Optimizar renderizado de timeline"
```

## 🧪 Testing Antes de Merge

Antes de hacer merge a `dev` o `main`:

### Checklist de Testing

- [ ] La aplicación carga sin errores en consola
- [ ] Todas las features existentes funcionan
- [ ] La nueva feature funciona como se esperaba
- [ ] No hay conflictos con otras features
- [ ] El código está limpio y comentado
- [ ] La documentación está actualizada
- [ ] Exportación JSON funciona
- [ ] Exportación PNG funciona
- [ ] LocalStorage persiste correctamente
- [ ] Responsive en mobile/tablet/desktop

### Testing en Diferentes Navegadores

- [ ] Chrome/Edge (Chromium)
- [ ] Firefox
- [ ] Safari (si es posible)

## 🚀 Pull Requests

Si trabajas en un fork:

1. **Crea un PR desde tu fork a `dev`** (no a `main`)
2. **Título descriptivo**: `feat: Agregar modo oscuro`
3. **Descripción completa**:
   ```markdown
   ## Descripción
   Implementa modo oscuro con toggle en header
   
   ## Cambios
   - Nuevo toggle en header
   - Estilos CSS para tema oscuro
   - Persistencia en localStorage
   
   ## Testing
   - ✅ Funciona en Chrome, Firefox
   - ✅ Persiste al recargar
   - ✅ No afecta otras features
   
   ## Screenshots
   [Adjuntar capturas]
   ```
4. **Espera review** antes de merge

## 📊 Versionado Semántico

Seguimos [SemVer](https://semver.org/):

```
v1.3.0
│ │ │
│ │ └─ PATCH: Hotfixes y bugs (v1.3.1)
│ └─── MINOR: Nuevas features (v1.4.0)
└───── MAJOR: Breaking changes (v2.0.0)
```

### Ejemplos:

- `v1.3.0` → `v1.3.1`: Hotfix de exportación PNG
- `v1.3.0` → `v1.4.0`: Nueva feature de ruta crítica
- `v1.3.0` → `v2.0.0`: Cambio completo de arquitectura

## 🛠️ Comandos Útiles

```bash
# Ver todas las ramas
git branch -a

# Ver ramas remotas
git branch -r

# Eliminar rama local
git branch -d feature/mi-feature

# Eliminar rama remota
git push origin --delete feature/mi-feature

# Ver commits de una rama
git log --oneline --graph --all

# Ver diferencias entre ramas
git diff dev..main

# Actualizar todas las ramas
git fetch --all

# Ver estado de todas las ramas
git branch -vv
```

## 🎯 Buenas Prácticas

1. **Commits pequeños y frecuentes**: Mejor 10 commits pequeños que 1 gigante
2. **Mensajes descriptivos**: Explica QUÉ y POR QUÉ, no CÓMO
3. **Pull antes de push**: Siempre `git pull` antes de `git push`
4. **Rebase vs Merge**: Usa rebase para features, merge para integración
5. **No pushear código roto**: Asegura que funciona antes de push
6. **Actualiza dev frecuentemente**: Evita conflictos grandes
7. **Elimina ramas obsoletas**: Mantén el repo limpio

## 📞 ¿Necesitas Ayuda?

- 📖 [Git Documentation](https://git-scm.com/doc)
- 💬 Abre un issue en GitHub
- 📧 Contacta al equipo

---

**¡Gracias por contribuir a ChronoMap!** 🎉
