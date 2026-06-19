# 🔧 Configuración de GitHub

Esta carpeta contiene la configuración de GitHub Actions y documentación del flujo de trabajo.

## 📁 Contenido

### Workflows (`.github/workflows/`)

#### `deploy.yml` - Despliegue a Producción
- **Trigger**: Push a `main`
- **Acción**: Despliega a GitHub Pages
- **Duración**: ~2 minutos
- **URL**: https://rubaanxd.github.io/ChronoMap/

#### `dev-ci.yml` - Validación de Desarrollo
- **Trigger**: Push a `dev` o PR a `dev`
- **Acción**: Valida estructura y sintaxis
- **Checks**:
  - ✅ Archivos esenciales presentes
  - ✅ Sintaxis HTML válida
  - ✅ CDNs configurados
  - ✅ Estructura del proyecto

### Documentación

#### `BRANCH_STRATEGY.md`
Estrategia completa de branching:
- Descripción de ramas (`main`, `dev`, `feature/*`, `hotfix/*`)
- Workflows por tipo de cambio
- Reglas de oro
- Versionado semántico
- Estados de las ramas

## 🚀 Uso Rápido

### Crear Nueva Feature
```bash
git checkout dev
git pull origin dev
git checkout -b feature/mi-funcionalidad
# ... desarrollar ...
git push origin feature/mi-funcionalidad
```

### Release a Producción
```bash
git checkout main
git merge dev
git tag -a v1.4.0 -m "Release v1.4.0"
git push origin main --tags
```

### Hotfix Urgente
```bash
git checkout main
git checkout -b hotfix/bug-critico
# ... arreglar ...
git checkout main
git merge hotfix/bug-critico
git push origin main
```

## 📊 Estado Actual

- **Rama de producción**: `main` (v1.3.0)
- **Rama de desarrollo**: `dev`
- **Features activas**: 0
- **Próximo release**: v1.4.0

## 🔗 Enlaces Útiles

- [CONTRIBUTING.md](../CONTRIBUTING.md) - Guía de contribución completa
- [BRANCH_STRATEGY.md](BRANCH_STRATEGY.md) - Estrategia de ramas
- [GitHub Actions](https://github.com/rubaanxd/ChronoMap/actions) - Ver workflows

---

**Última actualización**: 2026-06-19
