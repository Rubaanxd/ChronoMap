# ⚡ Quick Start - Publicar en GitHub Pages

## 🎯 Comandos Rápidos

### Si NO tienes el repositorio en GitHub aún:

```bash
# 1. Crear repositorio en GitHub (ve a github.com/new)
#    Nombre sugerido: Timelines
#    NO inicialices con README

# 2. Conectar y subir
git remote add origin https://github.com/TU-USUARIO/Timelines.git
git branch -M main
git push -u origin main
```

### Si YA tienes el repositorio en GitHub:

```bash
# Simplemente push
git push origin main
```

## 🚀 Habilitar GitHub Pages

1. Ve a: `https://github.com/TU-USUARIO/Timelines/settings/pages`
2. En **Source**, selecciona: **GitHub Actions**
3. ¡Listo! Espera 2 minutos

## 🌐 Tu Sitio Estará en:

```
https://TU-USUARIO.github.io/Timelines/
```

## ✅ Checklist Post-Despliegue

- [ ] Actualizar link en `index.html` línea 118:
  ```html
  <a href="https://github.com/TU-USUARIO/Timelines" ...>
  ```

- [ ] Actualizar link en `index.html` línea 14:
  ```html
  <meta property="og:url" content="https://TU-USUARIO.github.io/Timelines/">
  ```

- [ ] Actualizar link en `index.html` línea 19:
  ```html
  <meta property="twitter:url" content="https://TU-USUARIO.github.io/Timelines/">
  ```

- [ ] Hacer commit y push de los cambios:
  ```bash
  git add index.html
  git commit -m "chore: Actualizar links con usuario correcto"
  git push
  ```

## 🎨 Personalización Opcional

### Cambiar colores del index.html:
```css
/* Línea 45-47 en index.html */
background: linear-gradient(135deg, #TU-COLOR-1 0%, #TU-COLOR-2 100%);
```

### Agregar dominio personalizado:
```bash
# Edita CNAME
echo "chronomap.tudominio.com" > CNAME
git add CNAME
git commit -m "chore: Agregar dominio personalizado"
git push
```

## 📊 Verificar Despliegue

1. Ve a: `https://github.com/TU-USUARIO/Timelines/actions`
2. Verifica que el workflow tenga ✅
3. Abre: `https://TU-USUARIO.github.io/Timelines/`

## 🆘 Problemas Comunes

**404 Not Found:**
```bash
# Verifica que .nojekyll existe
ls -la .nojekyll

# Verifica que index.html existe
ls -la index.html
```

**Cambios no aparecen:**
```bash
# Limpia caché del navegador: Ctrl+Shift+R
# O abre en modo incógnito
```

**Workflow falla:**
```bash
# Revisa los logs en Actions
# Verifica permisos en Settings → Actions → General
# Debe estar en "Read and write permissions"
```

## 📱 Compartir

```markdown
🎉 ChronoMap está en vivo!
🌐 Demo: https://TU-USUARIO.github.io/Timelines/
📦 Código: https://github.com/TU-USUARIO/Timelines
```

---

**¿Listo?** Ejecuta los comandos y en 2 minutos tendrás tu sitio en vivo! 🚀
