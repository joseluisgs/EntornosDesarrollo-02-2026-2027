- [3. Anatomía y Estructura de los IDEs Seleccionados](#3-anatomía-y-estructura-de-los-ides-seleccionados)
  - [3.1. Filosofía JetBrains: Uniformidad de Flujo de Trabajo](#31-filosofía-jetbrains-uniformidad-de-flujo-de-trabajo)
    - [3.1.1. Consistencia de la Interfaz (Rider y IntelliJ IDEA)](#311-consistencia-de-la-interfaz-rider-y-intellij-idea)
    - [3.1.2. Uso de la Terminal integrada](#312-uso-de-la-terminal-integrada)
  - [3.2. Estructura de JetBrains Rider y IntelliJ IDEA](#32-estructura-de-jetbrains-rider-y-intellij-idea)
  - [3.3. Estructura de Visual Studio Code (VS Code)](#33-estructura-de-visual-studio-code-vs-code)


> 💡 **Punto de partida:** Si nunca has abierto el capó de un coche, no sabes qué hay dentro. Lo mismo pasa con un IDE: saber qué hay y para qué sirve cada cosa te convierte en un usuario más eficiente.

> 💡 **¿Por qué me importa?**
> Conocer la anatomía del IDE te permite aprovechar al máximo sus funcionalidades. Es como conocer cada botón del volante: puedes manejar sin ellos, pero es mucho más cómodo y rápido con ellos.
> 
> 🔗 **Conexión con otros puntos:** El Punto 01 introdujo los componentes. Este punto los detalla visualmente. El Punto 05 enseñará a usarlos en la práctica diaria.

En el Punto 02 instalaste las herramientas de desarrollo. Ahora veremos qué hay dentro de los IDEs: cómo se estructuran, para qué sirve cada zona y cómo se organizan las herramientas.

**Objetivos de aprendizaje:**

- Identificar las zonas principales de un IDE JetBrains (Tool Windows, Gutter, Status Bar)
- Conocer la estructura de VS Code (Activity Bar, Editor, Panel)
- Entender la filosofía de uniformidad entre IDEs de JetBrains
- Usar la terminal integrada y la barra de navegación

# 3. Anatomía y Estructura de los IDEs Seleccionados

## 3.1. Filosofía JetBrains: Uniformidad de Flujo de Trabajo

Una característica notable al utilizar IDEs del mismo fabricante, como **JetBrains Rider** e **IntelliJ IDEA**, es la **consistencia de la interfaz** y la **familiaridad del flujo de trabajo**. Esto facilita la transición entre entornos diseñados para diferentes plataformas (.NET en Rider, Java en IDEA).

> 💡 **Ventaja de usar productos JetBrains:** Si aprendes Rider, aprender IntelliJ IDEA es muy fácil. Los atajos, la estructura de menús y la filosofía son idénticas. Tu inversión en aprender una herramienta se transfiere a otras.

> 📌 **Ejemplo real:** Cuando abres Rider por primera vez, verás el Solution Explorer a la izquierda, el editor al centro y la barra de estado abajo. Es exactamente la misma disposición que en IntelliJ IDEA, solo que en vez de ver un proyecto Java, ves un proyecto C# con archivos .cs y una solución .slnx.

### 3.1.1. Consistencia de la Interfaz (Rider y IntelliJ IDEA)

Ambos IDEs comparten una filosofía de diseño basada en:

```mermaid
graph TD
    A[IDE JetBrains] --> B[Tool Windows]
    A --> C[Gutter]
    A --> D[Status Bar]
    A --> E[Editor Area]

    B --> B1[Alt+1: Proyecto]
    B --> B2[Alt+12: Git]
    B --> B3[Alt+F12: Terminal]

    C --> C1[Números de línea]
    C --> C2[Breakpoints]
    C --> C3[Marcadores]

    D --> D1[Línea:Columna]
    D --> D2[Codificación]
    D --> D3[Branch actual]

    style A fill:#2196F3,color:#fff
    style B fill:#4CAF50,color:#fff
    style C fill:#FF9800,color:#fff
    style D fill:#9C27B0,color:#fff
    style E fill:#FF9800,color:#fff
```

- **Ventanas de Herramientas (*Tool Windows*):** Proporcionan funcionalidades complementarias a la edición de código. Por defecto, están acopladas a los lados y al fondo de la ventana principal. Se puede acceder a ellas mediante la barra de iconos laterales o atajos de teclado. Por ejemplo, **Alt+1** abre la ventana de Proyecto/Solución, y **F12** salta desde el editor a la última *Tool Window* activa.

| Atajo | Ventana | Función |
|-------|---------|---------|
| `Alt + 1` | Proyecto | Ver estructura del proyecto |
| `Alt + 2` | Favoritos | Marcadores y breakpoints |
| `Alt + 9` | Git | Control de versiones |
| `Alt + 12` | Database | Base de datos |
| `Alt + F12` | Terminal | Línea de comandos |

- **Gutter:** El panel a la izquierda del editor contiene **iconos de acción** para corregir problemas de código, ejecutar o depurar. También muestra **números de línea, puntos de ruptura (*breakpoints*)** y **marcadores** (*bookmarks*). Permite el plegado de código y marca las líneas modificadas bajo control de versiones.

> 📝 **Partes del Gutter:**
> ```
>  1 | package com.ejemplo;
>  2 |              ← Icono de acción (bombilla)
>  3 | class Main {
>  4 |     // TODO: implementar
>  5 |     ••••           ← Breakpoint
>  6 |     void main() {
>  7 |         System.out.println("Hola");
>  8 |     }
>  9 | }
> ```

- **Barra de Estado (*Status Bar*):** Se encuentra en la parte inferior de la ventana principal.
  - **Mensajes:** En el lado izquierdo, muestra mensajes de eventos recientes y el progreso de las tareas en segundo plano (*Background Tasks*).
  - **Widgets:** En el lado derecho, contiene *widgets* que indican el estado general del proyecto y del IDE. Ejemplos incluyen el número de línea y columna (ej. `52:11`), terminaciones de línea (LF o CRLF), codificación de archivo (UTF-8), y el estilo de sangría (ej. `2 spaces`). Rider también incluye *widgets* para el estado del análisis de la solución y el Análisis Dinámico de Programas (DPA).

### 3.1.2. Uso de la Terminal integrada

La Terminal integrada se presenta como una *Tool Window*.

- El acceso rápido a la Terminal integrada se puede realizar mediante el atajo de teclado **Alt+F12** en ambos IDEs de JetBrains.

```bash
# Comandos útiles en la terminal integrada
cd /ruta/al/proyecto          # Navegar
ls -la                        # Listar archivos
./mvnw clean install          # Maven wrapper
dotnet build                  # .NET build
git status                    # Ver cambios
```

> 💡 **Truco:** La terminal integrada hereda el PATH del sistema, pero también puedes configurarla para usar diferentes shells (PowerShell, CMD, WSL, bash).

## 3.2. Estructura de JetBrains Rider y IntelliJ IDEA

Ambos IDEs comparten elementos de navegación y control en el encabezado (Nueva UI):

![img](./images/intellij-01.png)

![img](./images/rider-01.png)

- **Área del Editor (*Editor*):** Es la zona central para leer, escribir y explorar el código fuente.

```mermaid
graph TD
    A[Área del Editor] --> B[Pestañas]
    A --> C[Barra de navegación]
    A --> D[Gutter]
    A --> E[Contenido]

    B --> B1[Archivos abiertos]
    C --> C1[Navegación breadcrumb]
    D --> D1[Números, breakpoints]
    E --> E1[Código fuente]
```

- **Barra de Navegación (*Navigation Bar*):** Se puede mostrar en la parte superior del IDE o en la barra de estado. Es una alternativa a la vista de Proyecto/Solución para navegar por la estructura del proyecto y saltar a elementos específicos del código. Se accede usando **Alt+Home**.

> 📝 **Uso de la barra de navegación:**
> ```
> com.ejemplo.Main → main() → Variables
> ```
> Permite saltar rápidamente a cualquier clase, método o variable.

- **Barra de Herramientas (*Toolbar*):** Ubicada en el encabezado de la ventana, contiene *widgets* importantes:

| Widget | Icono | Función |
|--------|-------|---------|
| **Project Widget** | 📂 | Abrir proyectos, cambiar entre recientes |
| **VCS Widget** | 🔀 | Rama actual, commit, push, pull |
| **Run Widget** | ▶️ | Ejecutar configuración actual |
| **Build Widget** | 🔨 | Compilar proyecto (Rider) |

## 3.3. Estructura de Visual Studio Code (VS Code)

VS Code es un IDE/editor ligero que organiza el trabajo en torno a un *workspace* (espacio de trabajo), generalmente la carpeta raíz del proyecto.

![img](./images/vscode-01.png)

```mermaid
graph TD
    A[Diseño de VS Code] --> B[Barra de Actividad]
    A --> C[Barra lateral principal]
    A --> D[Área del Editor]
    A --> E[Panel]
    A --> F[Barra de Estado]

    B --> B1[Explorador]
    B --> B2[Búsqueda]
    B --> B3[Git]
    B --> B4[Extensiones]

    D --> D1[Pestañas]
    D --> D2[Divisiones]
    D --> D3[IntelliSense]

    E --> E1[Terminal]
    E --> E2[Salida]
    E --> E3[Problemas]

    style A fill:#2196F3,color:#fff
```

- **Barra de Actividad (*Activity Bar*):** Barra vertical en el extremo izquierdo utilizada para **cambiar entre las diferentes vistas** principales, como el Explorador, Control de Código Fuente y Extensiones. Al pasar el ratón por encima se puede ver el nombre de cada vista y su atajo de teclado.

| Vista | Atajo | Función |
|-------|-------|---------|
| Explorer | `Ctrl+Shift+E` | Explorador de archivos |
| Search | `Ctrl+Shift+F` | Búsqueda global |
| Source Control | `Ctrl+Shift+G` | Git integrado |
| Run and Debug | `Ctrl+Shift+D` | Depuración |
| Extensions | `Ctrl+Shift+X` | Marketplace |

- **Vista de Explorador (*Explorer View*) (Gestor de Ficheros):** Al seleccionarla, se abre la **barra lateral principal (*Primary Side Bar*)** y permite **ver y administrar los archivos y carpetas** dentro del *workspace*.

- **Área del Editor (*Editor*):** Área principal de la ventana para leer, escribir y explorar el código. Permite la edición en múltiples pestañas y visualización lado a lado. Muestra sugerencias de autocompletado (*IntelliSense*) y **resaltado de sintaxis**.

> 💡 **Atajos esenciales del editor VS Code:**
> ```
> Ctrl + P         → Quick Open (buscar archivo)
> Ctrl + Shift + P → Command Palette
> Ctrl + B         → Toggle Sidebar
> Ctrl + `         → Toggle Terminal
> Ctrl + Shift + M → Problems panel
> ```

- **Panel Inferior (*Panel*) y Terminal Integrado:** El panel inferior incluye la **terminal integrada**, cuyo acceso se logra mediante **Ctrl+`** (Windows, Linux).

> 📝 **Configuración de terminal en VS Code:**
> ```
> Ctrl + , → Settings → Terminal → Integrated
> ```

- **Paleta de Comandos (*Command Palette*):** Herramienta central de navegación y ejecución.
  - Se accede mediante **Ctrl+Shift+P** (Windows, Linux).
  - Permite buscar y ejecutar comandos (ej. `move terminal`).
  - Al quitar el símbolo `>` de la paleta, se puede usar directamente para **buscar archivos** en el *workspace*. Utiliza la **coincidencia difusa** (*fuzzy matching*) para encontrar comandos o archivos.

> 💡 **Fuzzy matching ejemplo:** Si buscas "jre", encontrará "JavaRuntimeEnvironment" porque las letras coinciden en orden.

- **Guardado y Hot Exit:** Por defecto, VS Code requiere una acción explícita para guardar (`Ctrl+S`). Sin embargo, se puede activar el **Auto Save** para guardar después de un retardo (por defecto 1000 ms), al perder el foco del editor, o al perder el foco de la ventana. VS Code también recuerda los cambios no guardados al salir (*Hot Exit*).

| Configuración | Valor | Descripción |
|---------------|-------|-------------|
| `files.autoSave` | `off` | Manual (por defecto) |
| `files.autoSave` | `afterDelay` | Auto después de X ms |
| `files.autoSave` | `onFocusChange` | Al cambiar de pestaña |
| `files.autoSave` | `onWindowChange` | Al cambiar de ventana |

> 📝 **Recomendación:** Para principiantes, mantener `off` es mejor para entender el flujo de trabajo. Para productividad, `afterDelay` de 1000ms es ideal.

---

**Resumen del punto:**

| Concepto | JetBrains (IntelliJ/Rider) | VS Code |
|----------|---------------------------|---------|
| **Panel proyecto** | Tool Window (`Alt+1`) | Activity Bar → Explorer |
| **Terminal** | `Alt+F12` | `` Ctrl+` `` |
| **Gutter** | Números, breakpoints, acciones | — |
| **Barra de estado** | Línea, encoding, branch | Línea, encoding, branch |
| **Navegación** | `Ctrl+N` (clases), `Ctrl+Shift+N` (archivos) | `Ctrl+P` (archivos) |
| **Paleta comandos** | `Ctrl+Shift+A` | `Ctrl+Shift+P` |

En el siguiente punto veremos cómo personalizar y configurar estos IDEs: temas, plugins, extensiones y opciones de actualización.
