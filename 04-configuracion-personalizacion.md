- [4. Plugins, Configuración y Personalización del Entorno](#4-plugins-configuración-y-personalización-del-entorno)
  - [4.1. Gestión de Plugins y Extensiones (Modularidad)](#41-gestión-de-plugins-y-extensiones-modularidad)
    - [4.1.1. Gestión en IntelliJ IDEA y JetBrains Rider (JetBrains)](#411-gestión-en-intellij-idea-y-jetbrains-rider-jetbrains)
    - [4.1.2. Gestión en Visual Studio Code (VS Code)](#412-gestión-en-visual-studio-code-vs-code)
  - [4.2. Personalización Visual y de Uso](#42-personalización-visual-y-de-uso)
      - [4.2.1. Acceso a la Configuración General](#421-acceso-a-la-configuración-general)
      - [4.2.2. Temas, Apariencia y Configuración de Archivos](#422-temas-apariencia-y-configuración-de-archivos)
      - [4.2.3. Configuraciones Específicas del Proyecto (VS Code)](#423-configuraciones-específicas-del-proyecto-vs-code)
      - [4.2.4. Refactorización (Mejora de Código)](#424-refactorización-mejora-de-código)
  - [4.3. Automatización y Configuración Reproducible](#43-automatización-y-configuración-reproducible)
  - [4.4. Actualización y Mantenimiento del Entorno](#44-actualización-y-mantenimiento-del-entorno)


> 💡 **Punto de partida:** ¿Por qué dos programadores con el mismo IDE pueden tener experiencias tan diferentes? Porque uno personaliza su entorno y el otro no.

> 💡 **¿Por qué me importa?**
> Un IDE bien configurado se adapta a tu forma de trabajar y te ahorra tiempo. Los plugins correctos pueden duplicar tu productividad. La personalización no es un lujo: es una inversión en eficiencia.
> 
> 🔗 **Conexión con otros puntos:** El Punto 02 instalaste las herramientas. Este punto las personalizas. El Punto 04.3 verás cómo mantenerlas actualizadas.

En el Punto 02 instalaste las herramientas. Ahora veremos cómo personalizar y configurar los IDEs: temas, plugins, extensiones y opciones de actualización.

**Objetivos de aprendizaje:**

- Instalar y gestionar plugins/extensiones en JetBrains y VS Code
- Personalizar temas, fuentes y atajos de teclado
- Configurar opciones de guardado automático y formato
- Entender la jerarquía de configuración en VS Code
- Configurar el sistema de actualización del entorno

# 4. Plugins, Configuración y Personalización del Entorno

La personalización es vital, ya que el programador pasa mucho tiempo en el entorno, que debe ser agradable y disponer de todas las funcionalidades necesarias. Todo entorno de desarrollo dispone de un panel donde se puede cambiar la configuración, incluyendo el aspecto visual, las conexiones de red y la asignación de teclas.

> 💡 **Analogía:** Un IDE es como tu puesto de trabajo. Puedes mover los monitores, organizar los cajones, poner una foto en el escritorio... Lo importante es que estés cómodo y productivo.

## 4.1. Gestión de Plugins y Extensiones (Modularidad)

Un *plugin* es un complemento que agrega una función nueva y específica a la aplicación principal.

### 4.1.1. Gestión en JetBrains Rider y IntelliJ IDEA (JetBrains)

Los IDEs de JetBrains utilizan *plugins* para ampliar sus capacidades.

- **Acceso al gestor:** Se realiza desde **`File -> Settings`** o utilizando el atajo **Ctrl+Alt+S**.

```mermaid
graph LR
    A[Settings] --> B[Plugins]
    B --> C[Marketplace]
    B --> D[Installed]
    B --> E[Updates]

    C --> F[Buscar plugin]
    F --> G[Install]
    G --> H[Restart IDE]

    style A fill:#2196F3,color:#fff
    style B fill:#4CAF50,color:#fff
    style C fill:#FF9800,color:#fff
```

- **Instalación:** Dentro de la sección *Plugins*, se hace clic en *Install JetBrains plugins* para realizar búsquedas por nombre o categoría. Tras la instalación, es necesario **reiniciar el IDE**.

> 📝 **Plugins esenciales JetBrains:**
> | Plugin | Utilidad |
> |--------|----------|
> | **Key Promoter X** | Aprende atajos mientras trabajas |
> | **Lombok** | Anotaciones para reducir boilerplate |
> | **Rainbow Brackets** | Colorea los paréntesis anidados |
> | **String Manipulation** | Manipulación de texto avanzada |

- **Eliminación/Desactivación:** Un módulo se puede **desactivar** (sigue instalado, pero inactivo) o **desinstalar** (se elimina físicamente).

> 💡 **Consejo:** Desactivar en lugar de desinstalar es más seguro. Si el plugin causa problemas, puedes activarlo nuevamente.

### 4.1.2. Gestión en Visual Studio Code (VS Code)

VS Code permite añadir soporte para lenguajes, depuradores y herramientas a través de extensiones, disponible en el *Visual Studio Marketplace*.

- **Vista de Extensiones:** La gestión se realiza desde la **vista Extensiones** (*Extensions view*) en la *Activity Bar*.

> 💡 **Atajo rápido:** `Ctrl+Shift+X` abre directamente la vista de extensiones.

- **Instalación:** El usuario busca la extensión deseada (ej. *Python*), la selecciona y pulsa **Install**.

**Extensiones VS Code por tecnología:**

| Categoría | Extensión | Valoración |
|-----------|-----------|------------|
| **Java** | Extension Pack for Java | ⭐⭐⭐⭐⭐ |
| **Python** | Python (Microsoft) | ⭐⭐⭐⭐⭐ |
| **C#** | C# (Microsoft) | ⭐⭐⭐⭐⭐ |
| **C#** | ReSharper (JetBrains) | ⭐⭐⭐⭐⭐ |
| **HTML/CSS** | Live Server | ⭐⭐⭐⭐⭐ |
| **Git** | GitLens | ⭐⭐⭐⭐⭐ |
| **Formato** | Prettier | ⭐⭐⭐⭐⭐ |

> 📝 **Instalación rápida desde comandos:**
> ```bash
> # Instalar extensión desde línea de comandos
> code --install-extension ms-python.python
> code --install-extension esbenp.prettier-vscode
> code --install-extension eamodio.gitlens
> ```

## 4.2. Personalización Visual y de Uso

#### 4.2.1. Acceso a la Configuración General

- **Rider / IntelliJ IDEA:** Se accede mediante **Ctrl+Alt+S** o `File -> Settings`. El panel de opciones está dividido en un panel de navegación a la izquierda (árbol de directorios como Apariencia, Plugins, Control de Versiones) y un área de presentación a la derecha.

```mermaid
graph TD
    A[Settings Structure] --> B[Appearance]
    A --> C[Editor]
    A --> D[Plugins]
    A --> E[Version Control]
    A --> F[Build Tools]
    A --> G[Languages]
    A --> H[Tools]

    B --> B1[Theme]
    B --> B2[Font]
    B --> B3[Layout]

    C --> C1[Font]
    C --> C2[Colors]
    C --> C3[Keymap]

    style A fill:#2196F3,color:#fff
    style B fill:#4CAF50,color:#fff
    style C fill:#FF9800,color:#fff
```

- **Visual Studio Code:** La configuración se abre presionando **Ctrl+,** (Windows/Linux). Se utiliza un cuadro de búsqueda para filtrar la lista de ajustes.

> 💡 **Truco VS Code:** La configuración se guarda en JSON. Puedes editar `settings.json` directamente para configuraciones avanzadas.

#### 4.2.2. Temas, Apariencia y Configuración de Archivos

- **Temas y Apariencia (Rider / IntelliJ IDEA):** Al arrancar el IDE por primera vez, se le pide al usuario que **elija un tema** para la apariencia.

| Tema | Fondo | Uso recomendado |
|------|-------|-----------------|
| **Light** | Blanco | Presentaciones, printing |
| **Dark** | Negro | Programación prolongada |
| **Darcula** | Gris oscuro | Predeterminado, popular |

- **Fuentes y Colores:** Se puede modificar los colores, las fuentes, el color de fondo y los iconos de advertencia del editor de texto.

**Configuración de fuente recomendada:**
```
Font: JetBrains Mono o Fira Code
Size: 14-16
Line spacing: 1.2
Enable ligatures: ✓
```

- **Atajos de Teclado:** Es posible configurar los atajos del teclado para modificar las acciones que se realizan con más frecuencia. VS Code permite instalar **extensiones Keymap** para usar atajos de otros editores (Sublime Text, Atom, Vim).

> 📝 **Extensión Keymap para VS Code:**
> - "JetBrains Keybindings" - Atajos de JetBrains en VS Code
> - "Vim" - Modo Vim emulado
> - "Sublime Text Keybindings" - Atajos de Sublime

- **VS Code: Selecciones Múltiples:** Se pueden añadir cursores con **Alt+Click** (Windows/Linux), o con atajos como `Ctrl+Alt+Down`. Para cambiar la tecla modificadora a **Ctrl+Click** (Windows/Linux), se usa la configuración `editor.multiCursorModifier`.

```json
// settings.json
{
    "editor.fontFamily": "JetBrains Mono",
    "editor.fontSize": 14,
    "editor.lineHeight": 1.6,
    "editor.fontLigatures": true,
    "editor.multiCursorModifier": "ctrlCmd",
    "editor.formatOnSave": true,
    "editor.wordWrap": "on"
}
```

#### 4.2.3. Configuraciones Específicas del Proyecto (VS Code)

En VS Code, las configuraciones se dividen por alcance:

- **Configuración de Usuario (*User settings*):** Se aplican a todos los *workspaces*.
- **Configuración del Workspace (*Workspace settings*):** Se aplican solo al *workspace* actual y **anulan** las de usuario.

> 💡 **Jerarquía de configuración:**
> ```
> 1. Default (valores del IDE)
> 2. User (tu configuración personal)
> 3. Workspace (configuración del proyecto)
> 4. Folder (carpeta específica)
> 
> Cada nivel anula el anterior
> ```

- **Guardado Automático (*Auto Save*):** Se puede activar en `File > Auto Save` o configurando `files.autoSave` con valores como `afterDelay` (por defecto 1000 ms), `onFocusChange`, u `onWindowChange`.

```json
// Configuración de Auto Save
{
    "files.autoSave": "afterDelay",
    "files.autoSaveDelay": 1000
}
```

#### 4.2.4. Refactorización (Mejora de Código)

La **refactorización** es la parte del mantenimiento del código que busca **mejorar la facilidad de comprensión**.

> 💡 **Regla de oro:** "No modificar funcionalidad, solo estructura". El comportamiento del programa debe ser idéntico antes y después de refactorizar.

- **Implementación (Rider / IntelliJ IDEA):** Ambos IDEs disponen de opciones específicas para la refactorización. En los IDEs JetBrains, se puede acceder a la lista contextual de refactorizaciones mediante **Ctrl+Alt+Shift+T** (*Refactor This*).

**Refactorizaciones comunes:**

| Refactorización | Atajo | Descripción |
|-----------------|-------|-------------|
| **Rename** | `Shift+F6` | Renombrar variable/método/clase |
| **Extract Method** | `Ctrl+Alt+M` | Crear método desde código duplicado |
| **Inline** | `Ctrl+Alt+N` | Sustituir llamada por su contenido |
| **Change Signature** | `Ctrl+F6` | Modificar parámetros |
| **Safe Delete** | `Alt+Delete` | Eliminar sin romper referencias |
| **Move** | `F6` | Mover a otra clase/paquete |

- **Configuración:** Se puede ajustar la configuración de refactorización en `Settings | Editor | Code Editing | Refactorings`.

- **Resolución de Conflictos:** Si Rider encuentra problemas durante una refactorización, muestra un diálogo con conflictos, dando la opción de ignorarlos (*Refactor Anyway*) o gestionarlos en la ventana *Find*.

- **Limpieza de Código (Rider):** JetBrains Rider permite aplicar la limpieza de código para aplicar reglas de estilo mediante **Ctrl+R, C**.

## 4.3. Automatización y Configuración Reproducible

> 💡 **Punto de partida:** ¿Y si pudieras configurar tu entorno de una sola vez y que se aplique automáticamente en cualquier ordenador? Eso es la automatización: configurar una vez, usar siempre.

> 💡 **¿Por qué me importa?**
> En el ámbito profesional, los desarrolladores trabajan en múltiples máquinas (local, oficina, nube). La automatización permite tener el mismo entorno en todas partes sin configurar cada vez manualmente.

### Dotfiles: Tu configuración como código

Los **dotfiles** son archivos de configuración que empiezan por punto (`.settings.json`, `.editorconfig`). Guardarlos en un repositorio Git permite sincronizar tu configuración entre dispositivos.

**Ejemplo de `.editorconfig`** (estándar de formato):

```ini
root = true

[*]
indent_style = space
indent_size = 4
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

[*.{csproj,slnx,xml}]
indent_size = 2

[*.md]
trim_trailing_whitespace = false
```

### Snippets Personalizados

Los **snippets** son plantillas de código que se expanden con un atajo. Ahorra tiempo escribiendo código repetitivo.

**Crear un snippet en VS Code** (`settings.json`):

```json
{
  "snippets": {
    "Console.WriteLine": {
      "prefix": "cw",
      "body": [
        "Console.WriteLine(\"$1\");"
      ],
      "description": "Imprime en consola"
    },
    "For Loop": {
      "prefix": "for",
      "body": [
        "for (int ${1:i} = 0; ${1:i} < ${2:length}; ${1:i}++)",
        "{",
        "\t$0",
        "}"
      ],
      "description": "Bucle for"
    }
  }
}
```

### Configuración Sincronizada

**VS Code:** Settings Sync (`Ctrl+Shift+P` → "Settings Sync") sincroniza: extensiones, settings, keybindings, snippets, themes.

**JetBrains:** `Settings Repository` (plugin) o `JetBrains Account` sync.

> 🔧 **Truco:** Crea un script `setup.ps1` (PowerShell) que instale todo automáticamente:
> ```powershell
> # Script de configuración del entorno
> winget install JetBrains.Rider
> winget install Microsoft.VisualStudioCode
> winget install Git.Git
> code --install-extension ms-dotnettools.csharp
> code --install-extension JetBrains.ReSharper
> code --install-extension ms-python.python
> ```

| Herramienta | Uso |
|-------------|-----|
| **Dotfiles** | Configuración persistente en Git |
| **Snippets** | Ahorro de tiempo en código repetitivo |
| **Settings Sync** | Sincronización entre dispositivos |
| **Scripts setup** | Instalación automatizada |
| **`.editorconfig`** | Formato consistente en equipo |

## 4.4. Actualización y Mantenimiento del Entorno

> 💡 **Punto de partida:** Tus IDEs se actualizan constantemente con nuevas funciones y parches de seguridad. ¿Sabes cuándo y cómo actualizar sin romper tu entorno?

### Canales de Actualización

Los IDEs de JetBrains ofrecen diferentes **canales de actualización**:

| Canal | Descripción | Cuándo usarlo |
|-------|-------------|---------------|
| **Stable** | Versión probada y estable | Producción, proyectos importantes |
| **EAP** (*Early Access Program*) | Versiones preliminares con nuevas funciones | Probar novedades, reportar bugs |
| **Nightly** | Builds diarios, inestables | Desarrolladores de plugins |

**Configurar en JetBrains:**
- `Help → Change Settings → Updates`
- Seleccionar canal: "Stable" (recomendado) o "EAP"
- Marcar "Check for updates automatically"

**VS Code** solo tiene un canal (estable), pero permite desactivar actualizaciones automáticas:
- `File → Preferences → Settings → Search "update"`
- `"update.mode": "manual"` para control manual

### Proceso de Actualización

**JetBrains (IntelliJ/Rider):**
1. `Help → Check for Updates`
2. Si hay actualización: descargar e instalar
3. Reiniciar el IDE
4. Verificar: `Help → About` (nueva versión)

**VS Code:**
1. Badge de notificación en la esquina inferior derecha
2. Click en el badge → "Download and Install"
3. Reiniciar

> ⚠️ **Advertencia:** Antes de actualizar, haz commit de tu código. Algunas actualizaciones pueden cambiar configuraciones de proyecto o requerir migración de plugins.

### Rollback: Volver a una Versión Anterior

Si una actualización causa problemas:

**JetBrains:**
1. Desinstalar la versión actual
2. Descargar la versión anterior desde https://www.jetbrains.com/idea/other-releases/
3. Instalar la versión deseada

**VS Code:**
1. Descargar la versión anterior desde https://code.visualstudio.com/updates/v1XX (XX = versión)
2. Instalar (sobreescribe la actual)

> 💡 **Consejo:** JetBrains guarda configuraciones en `~/.IdeaICXXXX.X/` (IntelliJ) o `~/.riderXXXX.X/` (Rider). Si necesitas migrar configuración entre versiones, copia esta carpeta.

### Actualización de Plugins/Extensiones

**JetBrains:** `Settings → Plugins → Updates` → ver actualizaciones pendientes → actualizar una o todas

**VS Code:** `Ctrl+Shift+X` → pestaña "Updates" → actualizar extensiones

> 📝 **Nota:** Las actualizaciones de plugins son independientes del IDE. Un plugin puede actualizar sin actualizar el IDE y viceversa.

---

**Resumen del punto:**

| Concepto | Descripción |
|----------|-------------|
| **Plugins** | Extensiones que añaden funcionalidades al IDE |
| **Marketplace** | Tienda de plugins/extensiones de cada IDE |
| **Temas** | Light, Dark, Darcula (apariencia visual) |
| **Fuentes** | JetBrains Mono, Fira Code (con ligaduras) |
| **Atajos** | Configurables en Settings/Preferences |
| **Auto Save** | Guardado automático configurable |
| **Actualizaciones** | Help → Check for Updates (JetBrains), automático (VS Code) |

En el siguiente punto veremos la operativa básica del IDE: cómo usar el editor, compilar, depurar y gestionar el código en el día a día.
