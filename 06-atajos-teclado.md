- [6. Atajos de Teclado Esenciales para la Productividad](#6-atajos-de-teclado-esenciales-para-la-productividad)
  - [6.1. Los 10 Atajos para Sobrevivir (Primeros días)](#61-los-10-atajos-para-sobrevivir-primeros-días)
  - [6.2. Atajos Intermedios (Primeras semanas)](#62-atajos-intermedios-primeras-semanas)
  - [6.3. Atajos Avanzados (Para destacar)](#63-atajos-avanzados-para-destacar)
  - [6.4. Tabla Completa de Referencia](#64-tabla-completa-de-referencia)


# 6. Atajos de Teclado Esenciales para la Productividad

> 💡 **Punto de partida:** Un programador profesional hace miles de acciones al día en el IDE. Si cada acción te lleva 2 segundos más de lo necesario, al día son minutos perdidos. Al año, horas.

> 💡 **¿Por qué me importa?**
> Los atajos de teclado son la diferencia entre ser un usuario lento y un usuario veloz. No necesitas memorizarlos todos: con 10-15 esenciales ya multiplicas tu productividad.
> 
> 🔗 **Conexión con otros puntos:** El Punto 05 viste las operaciones básicas. Este punto las ejecutas más rápido. Son complementarios.

En el Punto 05 viste las operaciones básicas del IDE. Ahora verás los atajos de teclado para ejecutar esas operaciones más rápido. Dominar los atajos es la diferencia entre ser un usuario lento y uno veloz.

> 📌 **Ejemplo real:** Los desarrolladores de GitHub recomienden aprender 10 atajos básicos antes de profundizar. Según sus estudios de productividad, un programador que domina los atajos es un 25% más rápido que uno que usa el ratón para todo.

**Objetivos de aprendizaje:**

- Memorizar los atajos más importantes de JetBrains Rider (IDE principal)
- Memorizar los atajos más importantes de IntelliJ IDEA (IDE secundario)
- Memorizar los atajos más importantes de VS Code
- Personalizar atajos según las necesidades del proyecto

```mermaid
graph LR
    A[Básico: 10 atajos] --> B[Intermedio: +15 atajos]
    B --> C[Avanzado: +5 atajos]
    C --> D[Productividad total]
    
    style A fill:#4CAF50,color:#fff
    style B fill:#2196F3,color:#fff
    style C fill:#9C27B0,color:#fff
    style D fill:#FF9800,color:#fff
```

Dominar los atajos de teclado es fundamental para ser un programador eficiente. Estudios demuestran que usar atajos puede aumentar la productividad hasta un 50%.

> 💡 **Dato:** Un programador profesional hace miles de acciones al día. Cada segundo ahorrado en cada acción se multiplica por miles.

## 6.1. Los 10 Atajos para Sobrevivir (Primeros días)

> 💡 **Punto de partida:** No necesitas memorizar 200 atajos. Empieza con estos 10 y serás más rápido que el 80% de los usuarios.

| Atajo | Rider/IntelliJ | VS Code | Para qué sirve |
|-------|----------------|---------|----------------|
| **Paleta comandos** | `Ctrl+Shift+A` | `Ctrl+Shift+P` | Buscar cualquier acción |
| **Buscar archivo** | `Ctrl+Shift+N` | `Ctrl+P` | Abrir archivo rápido |
| **Buscar texto** | `Ctrl+F` | `Ctrl+F` | Buscar en el archivo |
| **Reemplazar** | `Ctrl+R` | `Ctrl+H` | Buscar y reemplazar |
| **Guardar** | `Ctrl+S` | `Ctrl+S` | Guardar archivo |
| **Deshacer** | `Ctrl+Z` | `Ctrl+Z` | Deshacer último cambio |
| **Ejecutar** | `Shift+F10` | `F5` | Ejecutar proyecto |
| **Depurar** | `Shift+F9` | `F9` | Ejecutar en modo depuración |
| **Terminal** | `Alt+F12` | `` Ctrl+` `` | Abrir terminal |
| **Navegación** | `Ctrl+N` / `Ctrl+Shift+N` | `Ctrl+P` | Ir a clase/archivo |

> 🔧 **Truco:** Practica estos 10 durante una semana. No busques más hasta que estos sean automáticos.

### Mini-ejercicio 1: Memoria muscular
1. Abre tu IDE
2. Sin usar el ratón, ejecuta estos 5 pasos solo con atajos:
   - Abrir la paleta de comandos (`Ctrl+Shift+A` o `Ctrl+Shift+P`)
   - Buscar el archivo `Program.cs` o `Main.java`
   - Abrir la terminal
   - Escribir `dotnet --version` (o `java --version`)
   - Cerrar la terminal
3. Cronometra cuánto tardas. Repite hasta hacerlo en menos de 15 segundos.

## 6.2. Atajos Intermedios (Primeras semanas)

Una vez dominas los 10 básicos, estos te harán productivo:

### Navegación Avanzada

| Atajo | Rider/IntelliJ | VS Code | Para qué sirve |
|-------|----------------|---------|----------------|
| **Ir a implementación** | `Ctrl+Alt+B` | `F12` | Ver el código de una función/método |
| **Ir a definición** | `Ctrl+B` | `Ctrl+F12` | Ir donde se define un símbolo |
| **Usos de un símbolo** | `Alt+F7` | `Shift+F12` | Buscar todos los usos |
| **Historial** | `Ctrl+Alt+←` | `Alt+←` | Volver a la posición anterior |
| **Terraza** | `Ctrl+E` | `Ctrl+Tab` | Ver archivos abiertos recientemente |

### Edición Eficiente

| Atajo | Rider/IntelliJ | VS Code | Para qué sirve |
|-------|----------------|---------|----------------|
| **Duplicar línea** | `Ctrl+D` | `Ctrl+Shift+K` | Copiar línea actual |
| **Eliminar línea** | `Ctrl+Y` | `Ctrl+Shift+K` | Borrar línea actual |
| **Mover línea** | `Alt+↑/↓` | `Alt+↑/↓` | Subir/bajar línea |
| **Comentar** | `Ctrl+/` | `Ctrl+/` | Comentar/descomentar |
| **Selección múltiple** | `Alt+J` | `Ctrl+D` | Seleccionar múltiples ocurrencias |

### Refactorización (solo JetBrains)

| Atajo | Acción |
|-------|--------|
| `Ctrl+Shift+A` → "Rename" | Renombrar variable/método |
| `Ctrl+Alt+M` | Extraer método |
| `Ctrl+Alt+V` | Extraer variable |
| `Ctrl+Alt+P` | Extraer parámetro |

### Mini-ejercicio 2: Refactorización sin ratón
1. Abre un archivo con un método de 10+ líneas
2. Selecciona 3 líneas relacionadas (`Alt+J`)
3. Extrae a un método nuevo (`Ctrl+Alt+M`)
4. Renombra el método nuevo (`Ctrl+Shift+A` → Rename)
5. Documenta cada paso con capturas

## 6.3. Atajos Avanzados (Para destacar)

| Atajo | Rider/IntelliJ | VS Code | Para qué sirve |
|-------|----------------|---------|----------------|
| **Find in Files** | `Ctrl+Shift+F` | `Ctrl+Shift+F` | Buscar en todo el proyecto |
| **Replace in Files** | `Ctrl+Shift+R` | `Ctrl+Shift+H` | Reemplazar en todo el proyecto |
| **Bookmarks** | `F11` | `Ctrl+K Ctrl+K` | Marcar línea importante |
| **Column Selection** | `Alt+Shift+Insert` | `Ctrl+Shift+↑/↓` | Seleccionar en columna |
| **Macro** | `Edit → Macros` | `Ctrl+Shift+P` → "Record Macro" | Grabar y repetir secuencia |
| **Local History** | `Local History → Show` | — | Ver historial local |

### Mini-ejercicio 3: Búsqueda masiva
1. En tu proyecto, busca todos los `Console.Write` (o `System.out.println`)
2. Reemplázalos por `Console.WriteLine` (o `System.out.println` con formato)
3. Usa `Ctrl+Shift+R` (Replace in Files) para hacerlo en todos los archivos
4. Documenta cuántos cambios se hicieron

## 6.4. Tabla Completa de Referencia

### JetBrains Rider

| Categoría | Acción | Windows/Linux | macOS |
|-----------|--------|---------------|-------|
| **General** | Guardar todo | `Ctrl + S` | `Cmd + S` |
| | Abrir Solución | `Ctrl + Shift + O` | `Cmd + Shift + O` |
| **Búsqueda / Navegación** | Búsqueda en todas partes | `Doble Shift` | `Doble Shift` |
| | Navegar a Clase | `Ctrl + N` | `Cmd + O` |
| | Navegar a Archivo | `Ctrl + Shift + N` | `Cmd + Shift + O` |
| | Archivos recientes | `Ctrl + E` | `Cmd + E` |
| **Búsqueda / Reemplazo** | Buscar | `Ctrl + F` | `Cmd + F` |
| | Buscar en Proyecto | `Ctrl + Shift + F` | `Cmd + Shift + F` |
| | Reemplazar | `Ctrl + R` | `Cmd + R` |
| **Navegación** | Ir a declaración | `Ctrl + B` | `Cmd + B` |
| | Ir a implementación | `Ctrl + Alt + B` | `Cmd + Alt + B` |
| | Ir a línea | `Ctrl + G` | `Cmd + L` |
| **Multicursor** | Seleccionar siguiente | `F3` | `Cmd + G` |
| | Seleccionar todas | `Ctrl + Alt + Shift + J` | `Ctrl + Cmd + G` |
| **Edición** | Completado inteligente | `Ctrl + Shift + Space` | `Ctrl + Space` |
| | Generar código | `Alt + Insert` | `Cmd + N` |
| | Acciones de intención | `Alt + Enter` | `Alt + Enter` |
| | Reformatar código | `Ctrl + Alt + L` | `Cmd + Alt + L` |
| | Comentar línea | `Ctrl + /` | `Cmd + /` |
| | Duplicar línea | `Ctrl + D` | `Cmd + D` |
| **Refactorización** | Renombrar | `Shift + F6` | `Shift + F6` |
| | Extraer Método | `Ctrl + Alt + M` | `Cmd + Alt + M` |
| | Refactorizar esto | `Ctrl + Alt + Shift + T` | `Ctrl + T` |
| **Compilación / Ejecución** | Compilar | `Ctrl + F9` | `Cmd + F9` |
| | Ejecutar | `Shift + F10` | `Ctrl + R` |
| | Depurar | `Shift + F9` | `Ctrl + D` |
| **Depuración** | Step Over | `F8` | `F8` |
| | Step Into | `F7` | `F7` |
| | Continue | `F9` | `Cmd + Alt + R` |
| **VCS** | Commit | `Ctrl + K` | `Cmd + K` |
| | Update | `Ctrl + T` | `Cmd + T` |
| | Push | `Ctrl + Shift + K` | `Cmd + Shift + K` |
| **Interfaz** | Terminal | `Alt + F12` | `Alt + F12` |
| | Project sidebar | `Alt + 1` | `Cmd + 1` |

### IntelliJ IDEA

| Categoría | Acción | Windows/Linux | macOS |
|-----------|--------|---------------|-------|
| **General** | Guardar todo | `Ctrl + S` | `Cmd + S` |
| | Abrir Proyecto/Solución | `Ctrl + Shift + N` | `Cmd + Shift + O` |
| **Búsqueda / Navegación** | Búsqueda en todas partes | `Doble Shift` | `Doble Shift` |
| | Navegar a Clase | `Ctrl + N` | `Cmd + O` |
| | Navegar a Archivo | `Ctrl + Shift + N` | `Cmd + Shift + O` |
| | Navegar a Símbolo | `Ctrl + Alt + Shift + N` | `Cmd + Alt + O` |
| | Archivos recientes | `Ctrl + E` | `Cmd + E` |
| | Ubicaciones recientes | `Ctrl + Shift + E` | `Cmd + Shift + E` |
| **Búsqueda / Reemplazo** | Buscar | `Ctrl + F` | `Cmd + F` |
| | Buscar en Ruta | `Ctrl + Shift + F` | `Cmd + Shift + F` |
| | Reemplazar | `Ctrl + R` | `Cmd + R` |
| | Reemplazar en Ruta | `Ctrl + Shift + R` | `Cmd + Shift + R` |
| **Navegación** | Ir a declaración/definición | `Ctrl + B` / `Ctrl + Click` | `Cmd + B` / `Cmd + Click` |
| | Ir a implementación | `Ctrl + Alt + B` | `Cmd + Alt + B` |
| | Ir atrás/adelante | `Ctrl + Alt + ← / →` | `Cmd + Alt + ← / →` |
| | Jerarquía de clases | `Ctrl + H` | `Ctrl + H` |
| | Ir a línea | `Ctrl + G` | `Cmd + L` |
| **Multicursor** | Seleccionar siguiente | `Alt + J` | `Ctrl + G` |
| | Seleccionar todas | `Ctrl + Alt + Shift + J` | `Ctrl + Cmd + G` |
| **Edición / Código** | Completado inteligente | `Ctrl + Shift + Space` | `Ctrl + Space` |
| | Generar código | `Alt + Insert` | `Cmd + N` |
| | Acciones de intención | `Alt + Enter` | `Alt + Enter` |
| | Info de parámetros | `Ctrl + P` | `Cmd + P` |
| | Completar statement | `Ctrl + Shift + Enter` | `Cmd + Shift + Enter` |
| | Expandir selección | `Ctrl + W` | `Alt + Up` |
| | Reducir selección | `Ctrl + Shift + W` | `Alt + Down` |
| | Duplicar línea | `Ctrl + D` | `Cmd + D` |
| | Mover línea | `Alt + Shift + ↑ / ↓` | `Alt + Shift + ↑ / ↓` |
| | Borrar línea | `Ctrl + Y` | `Cmd + Backspace` |
| | Comentar línea | `Ctrl + /` | `Cmd + /` |
| | Comentar bloque | `Ctrl + Shift + /` | `Cmd + Alt + /` |
| | Reformatar código | `Ctrl + Alt + L` | `Cmd + Alt + L` |
| | Optimizar imports | `Ctrl + Alt + O` | `Ctrl + Option + O` |
| **Refactorización** | Renombrar | `Shift + F6` | `Shift + F6` |
| | Extraer Método | `Ctrl + Alt + M` | `Cmd + Alt + M` |
| | Refactorizar esto | `Ctrl + Alt + Shift + T` | `Ctrl + T` |
| **Compilación / Ejecución** | Compilar proyecto | `Ctrl + F9` | `Cmd + F9` |
| | Ejecutar | `Shift + F10` | `Ctrl + R` |
| | Depurar | `Shift + F9` | `Ctrl + D` |
| **Depuración** | Step Over | `F8` | `F8` |
| | Step Into | `F7` | `F7` |
| | Step Out | `Shift + F8` | `Shift + F8` |
| | Reanudar programa | `F9` | `Cmd + Alt + R` |
| | Toggle breakpoint | `Ctrl + F8` | `Cmd + F8` |
| | Evaluar expresión | `Alt + F8` | `Alt + F8` |
| **VCS** | Commit | `Ctrl + K` | `Cmd + K` |
| | Update | `Ctrl + T` | `Cmd + T` |
| | Push | `Ctrl + Shift + K` | `Cmd + Shift + K` |
| **Interfaz** | Terminal | `Alt + F12` | `Alt + F12` |
| | Project sidebar | `Alt + 1` | `Cmd + 1` |
| | Pantalla completa | `Ctrl + Shift + F12` | `Cmd + Shift + F12` |
| | Cerrar pestaña | `Ctrl + F4` | `Cmd + W` |

### Visual Studio Code (VS Code)

| Categoría | Acción | Windows/Linux | macOS |
|-----------|--------|---------------|-------|
| **General** | Guardar todo | `Ctrl + K S` | `Cmd + K S` |
| | Nuevo proyecto | `Ctrl + Shift + N` | `Cmd + Shift + N` |
| **Búsqueda / Navegación** | Command Palette | `Ctrl + Shift + P` | `Cmd + Shift + P` |
| | Navegar a Símbolo | `Ctrl + Shift + O` | `Cmd + Shift + O` |
| | Navegar a Archivo | `Ctrl + P` | `Cmd + P` |
| | Ir a Línea | `Ctrl + G` | `Cmd + G` |
| | Peek Definition | `Alt + F12` | `Option + F12` |
| **Búsqueda / Reemplazo** | Buscar | `Ctrl + F` | `Cmd + F` |
| | Buscar en Archivos | `Ctrl + Shift + F` | `Cmd + Shift + F` |
| | Reemplazar | `Ctrl + H` | `Cmd + Alt + F` |
| | Reemplazar en Archivos | `Ctrl + Shift + H` | `Cmd + Shift + H` |
| **Multicursor** | Seleccionar siguiente | `Ctrl + D` | `Cmd + D` |
| | Seleccionar todas | `Ctrl + Shift + L` | `Cmd + Shift + L` |
| | Cursor arriba/abajo | `Ctrl + Alt + ↑ / ↓` | `Option + Cmd + ↑ / ↓` |
| **Edición** | Trigger suggestion | `Ctrl + Space` | `Ctrl + Space` |
| | Quick Fix | `Ctrl + .` | `Cmd + .` |
| | Parameter hints | `Ctrl + Shift + Space` | `Shift + Cmd + Space` |
| | Expand selection | `Shift + Alt + →` | `Shift + Option + →` |
| | Comentar línea | `Ctrl + /` | `Cmd + /` |
| | Comentar bloque | `Shift + Alt + A` | `Shift + Option + A` |
| | Duplicar línea | `Shift + Alt + ↓` | `Shift + Option + ↓` |
| | Mover línea | `Alt + ↑ / ↓` | `Option + ↑ / ↓` |
| | Borrar línea | `Ctrl + Shift + K` | `Cmd + Shift + K` |
| | Formatear documento | `Shift + Alt + F` | `Shift + Option + F` |
| **Refactorización** | Rename Symbol | `F2` | `F2` |
| | Quick Fix / Refactor | `Ctrl + .` | `Cmd + .` |
| **Compilación / Ejecución** | Build Task | `Ctrl + Shift + B` | `Cmd + Shift + B` |
| | Run / Debug | `F5` | `F5` |
| **Depuración** | Step Over | `F10` | `F10` |
| | Step Into | `F11` | `F11` |
| | Step Out | `Shift + F11` | `Shift + F11` |
| | Continue | `F5` | `F5` |
| | Toggle Breakpoint | `F9` | `F9` |
| | Debug Console | `Ctrl + Shift + Y` | `Cmd + Shift + Y` |
| **VCS** | Source Control | `Ctrl + Shift + G` | `Cmd + Shift + G` |
| | Commit | `Ctrl + Enter` | `Cmd + Enter` |
| **Interfaz** | Terminal | `` Ctrl + ` `` | `` Cmd + ` `` |
| | Explorer | `Ctrl + Shift + E` | `Cmd + Shift + E` |
| | Extensions | `Ctrl + Shift + X` | `Cmd + Shift + X` |
| | Search | `Ctrl + Shift + F` | `Cmd + Shift + F` |
| | Modo Zen | `Ctrl + K Z` | `Cmd + K Z` |
| | Split editor | `Ctrl + \` | `Cmd + \` |
| | Cerrar pestaña | `Ctrl + W` | `Cmd + W` |

> 💡 **Atajos esenciales que debes memorizar primero:**
> | IDE | Búsqueda | Guardar | Terminal | Command Palette |
> |-----|----------|---------|----------|-----------------|
> | Rider | `Double Shift` | `Ctrl+S` | `Alt+F12` | `Ctrl+Shift+P` |
> | IntelliJ | `Double Shift` | `Ctrl+S` | `Alt+F12` | `Ctrl+Shift+P` |
> | VS Code | `Ctrl+P` | `Ctrl+S` | `` Ctrl+` `` | `Ctrl+Shift+P` |

> 📝 **Consejo de productividad:**
> 1. **Practica un atajo nuevo cada día**
> 2. **Deshazte del mouse** para navegación básica
> 3. **Personaliza** los atajos que uses frecuentemente
> 4. **Usa Key Promoter X** en IntelliJ para aprender mientras trabajas
> 5. **Instala extensiones de keymaps** si vienes de otro editor

---

**Resumen del punto:**

| IDE | Búsqueda | Guardar | Terminal | Command Palette |
|-----|----------|---------|----------|-----------------|
| **Rider** | `Double Shift` | `Ctrl+S` | `Alt+F12` | `Ctrl+Shift+A` |
| **IntelliJ** | `Double Shift` | `Ctrl+S` | `Alt+F12` | `Ctrl+Shift+A` |
| **VS Code** | `Ctrl+P` | `Ctrl+S` | `` Ctrl+` `` | `Ctrl+Shift+P` |

En el siguiente punto encontrarás un resumen completo de toda la unidad, con un mapa conceptual y un checklist de supervivencia.
