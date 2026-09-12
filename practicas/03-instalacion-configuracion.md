
## Práctica 3: Instalación y Configuración de Entornos de Desarrollo

**Objetivo:** Instalar y configurar todas las herramientas del curso: kits de desarrollo (.NET 10 SDK, JDK 25), Git, Oh My Posh, y los IDEs JetBrains Rider, IntelliJ IDEA y Visual Studio Code con tema, fuente y ligaduras unificados.

**Requisito de Documentación:** Realizar **capturas de pantalla de cada paso crucial** de instalación y configuración.

---

### PARTE I: Instalación de Plataformas Base

#### 1. Instalación de .NET 10 SDK

El SDK de .NET es fundamental para el desarrollo en C# y es especialmente relevante para **JetBrains Rider**, nuestro IDE principal.

**Pasos a realizar (con captura):**
1. Descargue e instale el SDK de **.NET 10** desde https://dotnet.microsoft.com/download
2. Verifique la instalación ejecutando en la terminal:
   ```bash
   dotnet --version
   ```
3. **[CAPTURAR]** La línea de comandos mostrando la versión de .NET instalada.

#### 2. Instalación de JDK 25 (Java Development Kit)

El JDK es necesario para desarrollar aplicaciones Java. Se usa en **IntelliJ IDEA** para proyectos Java/Kotlin.

**Pasos a realizar (con captura):**
1. Descargue el instalador de **JDK 25** desde la fuente oficial (Oracle, Adoptium, etc.).
2. Ejecute el instalador y siga el asistente.
3. Verifique la instalación:
   ```bash
   java --version
   javac --version
   ```
4. **[CAPTURAR]** La ventana que confirma la versión del JDK instalado.

#### 3. Instalación de Git

**Git** es esencial para el control de versiones. VS Code incluye soporte Git integrado de fábrica.

**Pasos a realizar (con captura):**
1. Descargue e instale Git desde https://git-scm.com/download/win
2. Acepte las opciones por defecto (añadir al PATH).
3. **[CAPTURAR]** La ventana de confirmación final de la instalación.

#### 4. Instalación de Oh My Posh

**Oh My Posh** personaliza la terminal con información visual (branch de Git, etc.).

**Pasos a realizar (con captura):**
1. Instale Oh My Posh:
   ```powershell
   winget install JanDeDobbeleer.OhMyPosh
   ```
2. Configure un tema (ej. *Agnoster* o *agnoster*) en su perfil de PowerShell.
3. **[CAPTURAR]** La terminal con el tema de Oh My Posh aplicado.

---

### PARTE II: Instalación de IDEs

#### 5. Instalación de JetBrains Toolbox App

La Toolbox App gestiona todas las actualizaciones de los IDEs JetBrains.

**Pasos a realizar (con captura):**
1. Descargue e instale la **JetBrains Toolbox App** desde https://www.jetbrains.com/toolbox-app/
2. **[CAPTURAR]** La interfaz de la Toolbox App con los IDEs disponibles.

#### 6. Instalación de JetBrains Rider (IDE Principal)

**Pasos a realizar (con captura):**
1. Use la Toolbox App para instalar **JetBrains Rider**.
2. Si está en Windows, seleccione la opción de añadir los ejecutables de Rider a las **exclusiones de Windows Defender** (mejora el tiempo de arranque).
3. **[CAPTURAR]** La pantalla principal de Rider.

#### 7. Instalación de IntelliJ IDEA (IDE Secundario)

**Pasos a realizar (con captura):**
1. Use la Toolbox App para instalar **IntelliJ IDEA Community** (gratuita).
2. **[CAPTURAR]** La pantalla de bienvenida de IntelliJ IDEA.

#### 8. Instalación de Visual Studio Code

**Pasos a realizar (con captura):**
1. Descargue VS Code desde https://code.visualstudio.com/
2. Ejecute el instalador y acepte las opciones por defecto.
3. **[CAPTURAR]** La pantalla principal de VS Code.

---

### PARTE III: Configuración Unificada de Apariencia

El objetivo es lograr la máxima similitud visual en los tres IDEs.

#### 9. Instalación de Plugins y Fuentes

##### 9.1. Plugins de Apariencia
- **Rider / IntelliJ IDEA:** `File → Settings → Plugins` → busque e instale el tema deseado (Material Theme o Dracula)
- **VS Code:** Vista Extensiones (`Ctrl+Shift+X`) → busque e instale el mismo tema

##### 9.2. Fuente Fira Code
1. Descargue **Fira Code** desde https://github.com/tonsky/FiraCode
2. Instale la fuente en su sistema operativo.

##### 9.3. Gestión de Plugins: Instalación y Eliminación (CCEE b)

El CCEE b) exige demostrar que sabes **añadir y eliminar módulos** en el entorno de desarrollo.

**En Rider / IntelliJ IDEA:**
1. Instale el plugin **Key Promoter X** desde Settings → Plugins
2. Verifique que funciona (aparecen notificaciones al usar atajos)
3. Desinstale el plugin desde Settings → Plugins → Installed → Key Promoter X → Uninstall
4. Reinicie el IDE
5. Verifique que las notificaciones ya no aparecen

**En VS Code:**
1. Instale la extensión **Python** desde Extensiones (`Ctrl+Shift+X`)
2. Verifique que aparece en la lista de extensiones instaladas
3. Desactívela (Disable) desde el menú de la extensión
4. Desinstalela (Uninstall) completamente
5. Verifique que ya no aparece

**[CAPTURAR]** Antes y después de instalar/desinstalar en cada IDE.

##### 9.4. Sistema de Actualizaciones (CCEE d)

El CCEE d) exige demostrar que sabes configurar el sistema de actualizaciones.

**En Rider / IntelliJ IDEA:**
1. `Help → Check for Updates` — verifique si hay actualizaciones
2. `Settings → Appearance & Behavior → System Settings → Updates` — configure el canal a "Stable"
3. Marque "Check for updates automatically"

**En VS Code:**
1. Verifique la versión actual: `Help → About`
2. Compruebe si hay actualizaciones: el badge de notificación en la esquina inferior derecha
3. Configure: `Settings → Search "update"` → `"update.mode": "manual"` o `"default"`

**[CAPTURAR]** El proceso de verificación de actualizaciones en cada IDE.

#### 10. Configuración de Tema, Fuente y Ligaduras

##### 10.1. Configuración de JetBrains Rider
1. `File → Settings` (`Ctrl+Alt+S`)
2. **Appearance:** Aplique el tema oscuro elegido
3. **Editor → Font:** Seleccione **Fira Code** y active **Ligatures**
4. **[CAPTURAR]** Editor de Rider con tema oscuro, Fira Code y ligaduras

##### 10.2. Configuración de IntelliJ IDEA
1. `File → Settings` (`Ctrl+Alt+S`)
2. Aplique el **mismo tema** que en Rider
3. **Editor → Font:** Seleccione **Fira Code** y active **Ligatures**
4. **[CAPTURAR]** Editor de IntelliJ con la misma configuración

##### 10.3. Configuración de VS Code
1. `Ctrl+,` (Settings)
2. Aplique el **mismo tema**
3. `editor.fontFamily`: **Fira Code**
4. `editor.fontLigatures`: **true**
5. **[CAPTURAR]** Editor de VS Code con la misma configuración

#### 11. Instalación de Extensiones Esenciales en VS Code

| Extensión | Función |
|-----------|---------|
| **C#** | Soporte C#, .NET |
| **Extension Pack for Java** | Soporte Java |
| **ReSharper** | Análisis de código C# |
| **GitLens** | Visualización avanzada de Git |
| **Python** | Soporte Python |
| **Prettier** | Formateo automático |

**[CAPTURAR]** La vista de extensiones instaladas en VS Code.

#### 12. Captura Final

**[CAPTURAR]** Los **tres IDEs** abiertos simultáneamente mostrando la apariencia unificada (mismo tema, misma fuente, mismas ligaduras).

---

### PARTE IV: Configuración Avanzada

#### 13. Snippets Personalizados en VS Code

Cree al menos 3 snippets en `settings.json`:
- Uno para `Console.WriteLine` (C#)
- Uno para `System.out.println` (Java)
- Uno para un bucle `for`

**[CAPTURAR]** El archivo `settings.json` con los snippets configurados.

#### 14. Dotfiles y Configuración Reproducible

Cree un archivo `.editorconfig` en la raíz de un proyecto con:
- `indent_style = space`
- `indent_size = 4`
- `end_of_line = lf`
- `charset = utf-8`

**[CAPTURAR]** El contenido del archivo `.editorconfig`.

#### 15. Script de Configuración Post-Instalación

Cree un script `setup.ps1` (PowerShell) que instale automáticamente:
```powershell
# Herramientas base
winget install Microsoft.VisualStudioCode
winget install Git.Git
winget install JanDeDobbeleer.OhMyPosh

# Extensiones VS Code
code --install-extension ms-dotnettools.csharp
code --install-extension vscjava.vscode-java-pack
code --install-extension JetBrains.ReSharper
code --install-extension ms-python.python
code --install-extension eamodio.gitlens
```

**[CAPTURAR]** El script ejecutándose correctamente.

---

**Formato de entrega:** PDF con capturas de pantalla de cada paso documentado, organizadas por partes (I, II, III, IV). Incluir el script setup.ps1 y el archivo .editorconfig creados.
