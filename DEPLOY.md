# 🚀 Guía de Despliegue en GitHub Pages

## Pasos para Publicar ChronoMap

### 1️⃣ Preparar el Repositorio

Si aún no has subido el código a GitHub:

```bash
# Inicializar Git (si no está inicializado)
git init

# Agregar todos los archivos
git add .

# Hacer commit
git commit -m "Initial commit: ChronoMap v1.3"

# Crear repositorio en GitHub y conectarlo
git remote add origin https://github.com/TU-USUARIO/Timelines.git

# Subir código
git push -u origin main
```

### 2️⃣ Habilitar GitHub Pages

1. Ve a tu repositorio en GitHub
2. Click en **Settings** (⚙️)
3. En el menú lateral, click en **Pages**
4. En **Source**, selecciona: **GitHub Actions**
5. ¡Listo! El workflow se ejecutará automáticamente

### 3️⃣ Verificar el Despliegue

1. Ve a la pestaña **Actions** en tu repositorio
2. Verás el workflow "Deploy to GitHub Pages" ejecutándose
3. Espera ~2 minutos hasta que aparezca ✅
4. Tu sitio estará disponible en:
   ```
   https://TU-USUARIO.github.io/Timelines/
   ```

### 4️⃣ Actualizaciones Automáticas

Cada vez que hagas `git push` a la rama `main`, el sitio se actualizará automáticamente:

```bash
# Hacer cambios en ChronoMap.html
git add .
git commit -m "feat: Nueva funcionalidad"
git push

# GitHub Pages se actualizará automáticamente en ~2 minutos
```

## 🌐 Dominio Personalizado (Opcional)

Si tienes un dominio propio:

1. Edita el archivo `CNAME`:
   ```
   chronomap.tudominio.com
   ```

2. Configura DNS en tu proveedor:
   - Tipo: `CNAME`
   - Nombre: `chronomap` (o el subdominio que quieras)
   - Valor: `TU-USUARIO.github.io`

3. En GitHub Settings → Pages → Custom domain:
   - Ingresa: `chronomap.tudominio.com`
   - Click en **Save**

## 📊 Monitoreo

### Ver Logs del Despliegue
1. Ve a **Actions** en GitHub
2. Click en el workflow más reciente
3. Click en el job "deploy"
4. Revisa los logs de cada step

### Solución de Problemas

**El sitio no carga:**
- Verifica que el workflow haya terminado exitosamente (✅)
- Espera 2-3 minutos después del despliegue
- Limpia caché del navegador (Ctrl+Shift+R)

**Error 404:**
- Verifica que `index.html` esté en la raíz del repositorio
- Verifica que `.nojekyll` exista
- Revisa que la rama sea `main` (no `master`)

**Cambios no se reflejan:**
- Verifica que el commit se haya pusheado: `git log --oneline`
- Revisa el workflow en Actions
- Limpia caché del navegador

## 🔧 Archivos Importantes

| Archivo | Propósito |
|---------|-----------|
| `index.html` | Página de bienvenida |
| `ChronoMap.html` | Aplicación principal |
| `.nojekyll` | Evita procesamiento Jekyll |
| `CNAME` | Dominio personalizado |
| `.github/workflows/deploy.yml` | Automatización del despliegue |

## 📱 Compartir tu Proyecto

Una vez desplegado, puedes compartir:

```
🌐 Demo en vivo: https://TU-USUARIO.github.io/Timelines/
📦 Código fuente: https://github.com/TU-USUARIO/Timelines
```

## 🎯 Próximos Pasos

1. ✅ Personaliza `index.html` con tu información
2. ✅ Actualiza el link del repositorio en `index.html`
3. ✅ Agrega screenshots al README
4. ✅ Comparte en redes sociales
5. ✅ Recibe feedback y mejora

---

**¿Necesitas ayuda?** Abre un issue en el repositorio o consulta la [documentación de GitHub Pages](https://docs.github.com/pages).
