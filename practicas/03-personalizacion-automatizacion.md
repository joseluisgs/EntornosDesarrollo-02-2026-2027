# Práctica 3: Personalización y Automatización de IDEs

## Tabla de contenidos

- [1. Introducción](#1-introducción)
  - [1.1. Objetivos](#11-objetivos)
  - [1.2. Requisitos previos](#12-requisitos-previos)
- [2. Ejercicio 1: Personalización completa](#2-ejercicio-1-personalización-completa)
  - [2.1. Configurar tema oscuro](#21-configurar-tema-oscuro)
  - [2.2. Cambiar fuente a JetBrains Mono](#22-cambiar-fuente-a-jetbrains-mono)
  - [2.3. Crear snippets personalizados en VS Code](#23-crear-snippets-personalizados-en-vs-code)
  - [2.4. Configurar atajos personalizados](#24-configurar-atajos-personalizados)
  - [2.5. Exportar/sincronizar configuración](#25-exportarsincronizar-configuración)
- [3. Ejercicio 2: Dotfiles](#3-ejercicio-2-dotfiles)
  - [3.1. Crear settings.json personalizado](#31-crear-settingsjson-personalizado)
  - [3.2. Crear script de configuración post-instalación](#32-crear-script-de-configuración-post-instalación)
  - [3.3. Documentar el script](#33-documentar-el-script)
- [4. Tiempo estimado](#4-tiempo-estimado)

---

## 1. Introducción

> 💡 **Punto de partida:** Tu IDE es tu espacio de trabajo. Si lo personalizas bien, serás más productivo y cómodo. En esta práctica vas a configurar aspectos visuales, crear atajos útiles y automatizar la configuración para que siempre tengas tu entorno listo.

### 1.1. Objetivos

- Configurar tema oscuro en IntelliJ y VS Code.
- Cambiar la fuente a JetBrains Mono con ligaduras.
- Crear snippets personalizados en VS Code.
- Configurar atajos de teclado personalizados.
- Exportar la configuración para sincronizarla entre equipos.

### 1.2. Requisitos previos

- IntelliJ IDEA Community instalado (Práctica 1).
- VS Code instalado (Práctica 1).
- Fuente JetBrains Mono instalada (se puede descargar de https://www.jetbrains.com/lp/mono/).

---

## 2. Ejercicio 1: Personalización completa

### 2.1. Configurar tema oscuro

**En IntelliJ IDEA:**

1. Ve a **File → Settings → Appearance & Behavior → Appearance**.
2. En **Theme**, selecciona **Darcula** (tema oscuro por defecto).
3. Haz clic en **Apply** y luego **OK**.
4. Verifica que todo el interfaz cambia a colores oscuros.

**En VS Code:**

1. Abre la paleta de comandos (`Ctrl+Shift+P`).
2. Escribe "Color Theme".
3. Selecciona **Dark+ (default dark)** o **One Dark Pro** (si la tienes instalada).
4. Verifica el cambio inmediato.

📸 **Capturas requeridas:**
- IntelliJ con tema Darcula.
- VS Code con tema oscuro.

### 2.2. Cambiar fuente a JetBrains Mono

**En IntelliJ IDEA:**

1. Ve a **File → Settings → Editor → Font**.
2. En **Font**, selecciona **JetBrains Mono**.
3. Ajusta el tamaño recomendado: **14** o **16**.
4. Marca **Enable ligatures** (ligaduras de programación).
5. Haz clic en **Apply**.

**En VS Code:**

1. Ve a **File → Preferences → Settings** (o `Ctrl+,`).
2. Busca "Font Family".
3. Escribe: `'JetBrains Mono', Consolas, monospace`.
4. Busca "Font Ligatures" y actívalo con `"editor.fontLigatures": true`.
5. Guarda el settings.json.

> 💡 **Consejo:** Las ligaduras son combinaciones de caracteres que se muestran como un solo glifo. Por ejemplo, `!=` puede mostrarse como un solo símbolo con una línea diagonal. Es solo estético, pero muchos programadores lo prefieren.

📸 **Capturas requeridas:**
- IntelliJ con JetBrains Mono y ligaduras activadas.
- VS Code con JetBrains Mono configurado.
- Ejemplo de código mostrando ligaduras.

### 2.3. Crear snippets personalizados en VS Code

Los snippets son plantillas de código que se expanden al escribir un prefijo.

**Snippet 1: Estructura HTML5**

1. Ve a **File → Preferences → User Snippets**.
2. Selecciona **html.json**.
3. Añade este snippet:

```json
{
  "HTML5 Básico": {
    "prefix": "html5",
    "body": [
      "<!DOCTYPE html>",
      "<html lang=\"es\">",
      "<head>",
      "    <meta charset=\"UTF-8\">",
      "    <meta name=\"viewport\" content=\"width=device-width, initial-scale=1.0\">",
      "    <title>$1</title>",
      "</head>",
      "<body>",
      "    $0",
      "</body>",
      "</html>"
    ],
    "description": "Estructura HTML5 completa"
  }
}
```

**Snippet 2: Flexbox en CSS**

1. Abre **css.json** en User Snippets.
2. Añade:

```json
{
  "Flexbox Center": {
    "prefix": "flex-center",
    "body": [
      "display: flex;",
      "justify-content: center;",
      "align-items: center;"
    ],
    "description": "Centra un elemento con Flexbox"
  }
}
```

**Snippet 3: Función en JavaScript**

1. Abre **javascript.json** en User Snippets.
2. Añade:

```json
{
  "Función con params": {
    "prefix": "fn",
    "body": [
      "function $1($2) {",
      "    $0",
      "}"
    ],
    "description": "Función con parámetros"
  }
}
```

**Verificación:**

1. Crea un archivo HTML y escribe `html5` → pulsa Tab.
2. Crea un archivo CSS y escribe `flex-center` → pulsa Tab.
3. Crea un archivo JS y escribe `fn` → pulsa Tab.

📸 **Capturas requeridas:**
- Cada snippet configurado en su JSON.
- Cada snippet expandido con Tab.

### 2.4. Configurar atajos personalizados

**En VS Code:**

1. Ve a **File → Preferences → Keyboard Shortcuts** (o `Ctrl+K Ctrl+S`).
2. Busca un atajo existente o crea uno nuevo haciendo clic en el icono de "+".
3. Configura estos atajos útiles:

| Acción | Atajo sugerido | Comando |
|--------|---------------|---------|
| Abrir terminal | `Ctrl+`` ` | `workbench.action.terminal.toggleTerminal` |
| Formatear documento | `Shift+Alt+F` | `editor.action.formatDocument` |
| Duplicar línea hacia abajo | `Shift+Alt+↓` | `editor.action.copyLinesDownAction` |

**En IntelliJ IDEA:**

1. Ve a **File → Settings → Keymap**.
2. Busca la acción que quieres modificar.
3. Haz clic derecho → **Add Keyboard Shortcut**.
4. Pulsa la combinación de teclas deseada.

### 2.5. Exportar/sincronizar configuración

**En VS Code (Settings Sync):**

1. Abre la paleta de comandos (`Ctrl+Shift+P`).
2. Escribe "Settings Sync: Turn On".
3. Inicia sesión con tu cuenta de GitHub o Microsoft.
4. Selecciona qué quieres sincronizar: Settings, Extensions, Keybindings, Snippets.
5. Confirma.

**En IntelliJ IDEA:**

1. Ve a **File → Manage IDE Settings → Export Settings**.
2. Selecciona qué exportar (tema, keymap, plugins, etc.).
3. Guarda el archivo `.zip` resultante.

> 📝 **Nota:** Settings Sync de VS Code es muy práctico si trabajas en varios equipos. La configuración se sube a la nube y se descarga automáticamente en cada equipo donde inicies sesión.

---

## 3. Ejercicio 2: Dotfiles

### 3.1. Crear settings.json personalizado

Crea un archivo `settings.json` con esta configuración base:

```json
{
    // Apariencia
    "workbench.colorTheme": "One Dark Pro",
    "workbench.iconTheme": "material-icon-theme",
    
    // Editor
    "editor.fontFamily": "'JetBrains Mono', Consolas, monospace",
    "editor.fontSize": 14,
    "editor.fontLigatures": true,
    "editor.minimap.enabled": false,
    "editor.wordWrap": "on",
    "editor.formatOnSave": true,
    "editor.suggestSelection": "first",
    
    // Tabulación
    "editor.tabSize": 4,
    "editor.insertSpaces": true,
    "editor.detectIndentation": true,
    
    // Terminal
    "terminal.integrated.fontSize": 13,
    
    // Archivos
    "files.autoSave": "afterDelay",
    "files.autoSaveDelay": 1000,
    "files.trimTrailingWhitespace": true,
    "files.insertFinalNewline": true,
    
    // Emmet
    "emmet.includeLanguages": {
        "javascript": "javascriptreact"
    },
    
    // JavaScript
    "javascript.updateImportsOnFileMove.enabled": "always",
    
    // Python
    "python.defaultInterpreterPath": "python",
    "[python]": {
        "editor.tabSize": 4
    }
}
```

### 3.2. Crear script de configuración post-instalación

**Para Windows (PowerShell) — `configurar-entorno.ps1`:**

```powershell
# Script de configuración post-instalación para VS Code
# Ejecutar con: .\configurar-entorno.ps1

Write-Host "=== Configurando entorno de desarrollo ===" -ForegroundColor Cyan

# 1. Verificar VS Code
Write-Host "`n[1/5] Verificando VS Code..." -ForegroundColor Yellow
$vscodePath = Get-Command code -ErrorAction SilentlyContinue
if ($vscodePath) {
    Write-Host "  VS Code encontrado: $($vscodePath.Source)" -ForegroundColor Green
} else {
    Write-Host "  VS Code NO encontrado. Instálalo desde https://code.visualstudio.com" -ForegroundColor Red
    exit 1
}

# 2. Instalar extensiones esenciales
Write-Host "`n[2/5] Instalando extensiones..." -ForegroundColor Yellow
$extensions = @(
    "ms-python.python",
    "ms-dotnettools.csharp",
    "dbaeumer.vscode-eslint",
    "esbenp.prettier-vscode",
    "JetBrains.jetbrains-monokai-pro",
    "pkief.material-icon-theme"
)

foreach ($ext in $extensions) {
    Write-Host "  Instalando $ext..." -ForegroundColor Gray
    code --install-extension $ext --force
}

# 3. Copiar settings.json
Write-Host "`n[3/5] Configurando settings.json..." -ForegroundColor Yellow
$settingsDir = "$env:APPDATA\Code\User"
$settingsFile = "$settingsDir\settings.json"

if (Test-Path $settingsFile) {
    $backup = "$settingsFile.backup.$(Get-Date -Format 'yyyyMMdd-HHmmss')"
    Copy-Item $settingsFile $backup
    Write-Host "  Backup creado: $backup" -ForegroundColor Green
}

# Aquí copiarías tu settings.json personalizado
# Copy-Item "settings.json" $settingsFile -Force
Write-Host "  (Configura manualmente o copia tu settings.json)" -ForegroundColor Gray

# 4. Instalar JetBrains Mono
Write-Host "`n[4/5] Verificando JetBrains Mono..." -ForegroundColor Yellow
$fontInstalled = Get-ItemProperty "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts" -Name "JetBrains Mono*" -ErrorAction SilentlyContinue
if ($fontInstalled) {
    Write-Host "  JetBrains Mono ya instalado" -ForegroundColor Green
} else {
    Write-Host "  Descarga JetBrains Mono desde: https://www.jetbrains.com/lp/mono/" -ForegroundColor Yellow
}

# 5. Verificar Git
Write-Host "`n[5/5] Verificando Git..." -ForegroundColor Yellow
$gitPath = Get-Command git -ErrorAction SilentlyContinue
if ($gitPath) {
    Write-Host "  Git encontrado: $($gitPath.Source)" -ForegroundColor Green
} else {
    Write-Host "  Git NO encontrado. Instálalo desde https://git-scm.com" -ForegroundColor Yellow
}

Write-Host "`n=== Configuración completada ===" -ForegroundColor Cyan
Write-Host "Reinicia VS Code para aplicar todos los cambios." -ForegroundColor White
```

### 3.3. Documentar el script

Crea un archivo `README.md` que explique qué hace cada línea del script:

| Sección | Qué hace | Comando clave |
|---------|----------|---------------|
| Verificar VS Code | Comprueba si VS Code está en el PATH | `Get-Command code` |
| Instalar extensiones | Instala extensiones desde la línea de comandos | `code --install-extension` |
| Configurar settings | Copia tu archivo de configuración | `Copy-Item` |
| Verificar fuente | Comprueba si JetBrains Mono está instalado | Registro de Windows |
| Verificar Git | Comprueba si Git está disponible | `Get-Command git` |

> ⚠️ **Advertencia:** Los scripts de configuración deben ejecutarse con precaución. Siempre haz backup de tu configuración anterior antes de ejecutarlos. Nunca ejecutes scripts de fuentes que no conoces.

---

## 4. Tiempo estimado

**Total: 2,5 horas**

| Actividad | Tiempo estimado |
|-----------|----------------|
| Configurar tema oscuro en ambos IDEs | 15 minutos |
| Configurar JetBrains Mono | 15 minutos |
| Crear 3 snippets personalizados | 30 minutos |
| Configurar atajos personalizados | 20 minutos |
| Exportar/sincronizar configuración | 15 minutos |
| Crear settings.json | 20 minutos |
| Crear script de configuración | 30 minutos |
| Documentación y redacción | 15 minutos |
