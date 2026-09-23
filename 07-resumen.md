- [7.1. Mapa Conceptual de la Unidad](#71-mapa-conceptual-de-la-unidad)
- [7.2. Conceptos Clave](#72-conceptos-clave)
  - [Entorno de Desarrollo Integrado (IDE)](#entorno-de-desarrollo-integrado-ide)
  - [Herramientas Fundamentales](#herramientas-fundamentales)
  - [Anatomía del IDE](#anatomía-del-ide)
  - [Configuración y Personalización](#configuración-y-personalización)
  - [Operativa Básica](#operativa-básica)
- [7.3. Herramientas y Perfiles](#73-herramientas-y-perfiles)
  - [Kits de Desarrollo](#kits-de-desarrollo)
  - [IDEs del Curso](#ides-del-curso)
  - [Herramientas de Apoyo](#herramientas-de-apoyo)
- [7.4. Checklist de Supervivencia](#74-checklist-de-supervivencia)
- [7.5. Errores Comunes a Evitar](#75-errores-comunes-a-evitar)
- [7.6. Glosario de Términos](#76-glosario-de-términos)
- [7.7. Ejercicios de Repaso](#77-ejercicios-de-repaso)
- [7.8. ¿Qué viene después?](#78-qué-viene-después)
- [7.9. Mapa de Conexiones entre Temas](#79-mapa-de-conexiones-entre-temas)


# 7. Resumen y Conclusiones

> 💡 **Punto de partida:** Hemos recorrido todo el camino desde qué es un IDE hasta cómo usarlo como un profesional. Este resumen consolida todo lo aprendido.

Hemos visto la teoría completa de Entornos de Desarrollo. Este punto consolida todos los conceptos en una sola mirada.

**Objetivos de aprendizaje:**

- Repasar los conceptos fundamentales de la unidad
- Consolidar el vocabulario técnico
- Tener una referencia rápida para el examen

## 7.1. Mapa Conceptual de la Unidad

```mermaid
graph TD
    UD02[UD02: Entornos de Desarrollo] --> IDE[Concepto de IDE]
    UD02 --> HERR[Instalación de Herramientas]
    UD02 --> ANAT[Anatomía del IDE]
    UD02 --> CONF[Configuración]
    UD02 --> OPER[Operativa Básica]
    UD02 --> ATAJ[Atajos de Teclado]

    IDE --> IDE1[Editor de código]
    IDE --> IDE2[Compilador]
    IDE --> IDE3[Depurador]
    IDE --> IDE4[Control de versiones]
    IDE --> IDE5[Gestión de proyectos]
    IDE --> IDE6[Terminal integrada]
    IDE --> IDE7[Refactorización]
    IDE --> IDE8[IntelliSense/Autocompletado]

    HERR --> HERR1[JDK 25 — Java]
    HERR --> HERR2[.NET 10 SDK — C#]
    HERR --> HERR3[JetBrains Rider — IDE principal]
    HERR --> HERR4[IntelliJ IDEA — IDE secundario]
    HERR --> HERR5[VS Code — Editor extensible]
    HERR --> HERR6[Git — Control de versiones]
    HERR --> HERR7[GitKraken — Cliente visual]
    HERR --> HERR8[Oh My Posh — Terminal]

    ANAT --> ANAT1[JetBrains: Tool Windows, Gutter, Status Bar]
    ANAT --> ANAT2[VS Code: Activity Bar, Editor, Panel]
    ANAT --> ANAT3[Filosofía de uniformidad]

    CONF --> CONF1[Plugins y extensiones]
    CONF --> CONF2[Temas y fuentes]
    CONF --> CONF3[Atajos personalizados]
    CONF --> CONF4[Dotfiles y sincronización]
    CONF --> CONF5[Sistema de actualizaciones]

    OPER --> OPER1[Edición asistida]
    OPER --> OPER2[Build vs Rebuild vs Clean]
    OPER --> OPER3[Debugging: breakpoints, Step]
    OPER --> OPER4[Refactorización]
    OPER --> OPER5[Git integrado]

    ATAJ --> ATAJ1[Rider / IntelliJ — Ctrl+Shift+A]
    ATAJ --> ATAJ2[VS Code — Ctrl+Shift+P]
    ATAJ --> ATAJ3[Progresión: básico → intermedio → avanzado]

    style UD02 fill:#2196F3,color:#fff
    style IDE fill:#4CAF50,color:#fff
    style HERR fill:#FF9800,color:#fff
    style ANAT fill:#9C27B0,color:#fff
    style CONF fill:#f44336,color:#fff
    style OPER fill:#607D8B,color:#fff
    style ATAJ fill:#4CAF50,color:#fff
```

## 7.2. Conceptos Clave

### Entorno de Desarrollo Integrado (IDE)
- **Definición:** Aplicación que agrupa editor, compilador, depurador y herramientas de gestión
- **Componentes esenciales:** Editor, compilador/intérprete, depurador, control de versiones
- **IDEs del curso:** JetBrains Rider, IntelliJ IDEA, VS Code

### Herramientas Fundamentales
| Herramienta | Función | Comando clave |
|-------------|---------|---------------|
| **JDK 25** | Desarrollo Java | `javac`, `java` |
| **.NET 10** | Desarrollo C# | `dotnet` |
| **Git** | Control de versiones | `git commit`, `git push` |
| **GitKraken** | Cliente Git visual | UI gráfica |

### Anatomía del IDE

**JetBrains (Rider/IntelliJ):**
- Tool Windows (`Alt+1` a `Alt+12`)
- Gutter (números, breakpoints, acciones)
- Status Bar (línea, encoding, branch)
- Widgets en toolbar (Project, VCS, Run)

**VS Code:**
- Activity Bar (vistas laterales)
- Command Palette (`Ctrl+Shift+P`)
- Terminal integrada (`` Ctrl+` ``)
- Multi-cursor y fuzzy search

### Configuración y Personalización
- **Plugins/Extensiones:** Modularidad y funcionalidades adicionales
- **Temas:** Light/Dark/Darcula
- **Fuentes:** JetBrains Mono, Fira Code con ligaduras
- **Atajos:** Personalizables en Settings
- **Dotfiles:** Sincronización de configuración entre máquinas
- **Actualizaciones:** Canal Stable, actualizaciones automáticas

### Operativa Básica
- **Edición asistida:** IntelliSense, autocompletado, Code Actions
- **Build:** Compilación incremental vs clean rebuild
- **Debugging:** Breakpoints, Step Over/Into/Out, variables
- **Git:** Commit, push, pull, branch, merge

## 7.3. Herramientas y Perfiles

### Kits de Desarrollo
- **JDK 25:** Java Development Kit — necesita `JAVA_HOME` y `PATH` configurados
- **.NET 10 SDK:** Incluye compilador, runtime y CLI (`dotnet`)

### IDEs del Curso
- **JetBrains Rider:** IDE principal, multiplataforma, profesional (.NET, Java)
- **IntelliJ IDEA:** IDE secundario, Java/Kotlin (Community gratuito)
- **VS Code:** Editor extensible, gratuito, multiplataforma

### Herramientas de Apoyo
- **Git:** Control de versiones distribuido (imprescindible)
- **GitKraken:** Cliente visual de Git (alternativa a la línea de comandos)
- **Oh My Posh:** Temas para terminal (personalización visual)

## 7.4. Checklist de Supervivencia

Antes de dar por cerrado el tema, asegúrate de poder responder **SÍ** a estas preguntas:

- [ ] ¿Conozco los componentes esenciales de un IDE?
- [ ] ¿Sé instalar JDK 25 y configurar el PATH?
- [ ] ¿Puedo instalar y configurar JetBrains Rider, IntelliJ IDEA y VS Code?
- [ ] ¿Sé qué son los plugins y cómo instalarlos?
- [ ] ¿Puedo personalizar temas, fuentes y atajos?
- [ ] ¿Sé usar el editor con autocompletado e IntelliSense?
- [ ] ¿Puedo compilar y ejecutar un proyecto desde el IDE?
- [ ] ¿Sé usar breakpoints y ejecutar paso a paso en debug?
- [ ] ¿Puedo usar Git integrado para commit y push?
- [ ] ¿He memorizado al menos 10 atajos de teclado esenciales?
- [ ] ¿Entiendo la diferencia entre Build y Rebuild?
- [ ] ¿Sé crear un nuevo proyecto, configurar su estructura y crear un ejecutable?
- [ ] ¿Puedo comparar IDEs y elegir el más adecuado según el lenguaje y proyecto?
- [ ] ¿Puedo crear un proyecto, compilarlo, depurarlo desde la consola con su CLI y desde el IDE?

## 7.5. Errores Comunes a Evitar

| Error | Por qué está mal | Cómo evitarlo |
|-------|------------------|---------------|
| No instalar el SDK (JDK/.NET) | El IDE no puede compilar sin el SDK | Siempre instalar el SDK ANTES del IDE |
| Confundir Build y Rebuild | Build es incremental, Rebuild limpia todo | Usar Build normalmente, Rebuild solo si hay problemas de dependencias |
| No usar breakpoints | Depurar con `Console.WriteLine` es lento y sucio | Aprender a usar breakpoints y Step Over/Into |
| Instalar demasiados plugins | Ralentizan el IDE significativamente | Instalar solo los que uses diariamente |
| No sincronizar configuración | Pierdes tu entorno al cambiar de máquina | Usar Settings Sync (VS Code) o Settings Repository (JetBrains) |
| Ignorar las actualizaciones | Te pierdes correcciones de bugs y seguridad | Configurar actualizaciones automáticas en canal Stable |
| No usar control de versiones | Pierdes código y no puedes colaborar | Git integrado en el IDE, hacer commit frecuente |
| Olvidar `.editorconfig` | Formato inconsistente en equipo | Crear `.editorconfig` en la raíz del proyecto |
| No conocer atajos básicos | Evas tiempo usando el ratón para todo | Memorizar los 10 atajos esenciales primero |
| Confundir Rider con IntelliJ | Rider es para .NET, IntelliJ para Java | Usar el IDE según el lenguaje del proyecto |

## 7.6. Glosario de Términos

| Término | Definición |
|---------|------------|
| **IDE** | Entorno de Desarrollo Integrado: aplicación que agrupa editor, compilador y depurador |
| **Rider** | IDE de JetBrains para C#/.NET, multiplataforma |
| **IntelliJ IDEA** | IDE de JetBrains para Java/Kotlin |
| **VS Code** | Editor extensible de Microsoft, gratuito y open source |
| **Plugin/Extensión** | Módulo que añade funcionalidades al IDE |
| **Build** | Compilación incremental (solo archivos modificados) |
| **Rebuild** | Reconstrucción completa desde cero |
| **Clean** | Eliminación de archivos compilados sin recompilar |
| **Breakpoint** | Punto de ruptura para detener la ejecución en depuración |
| **Step Over** | Ejecutar línea sin entrar en métodos |
| **Step Into** | Ejecutar línea entrando en el método |
| **Step Out** | Salir del método actual |
| **Refactorización** | Mejorar código sin cambiar su comportamiento |
| **IntelliSense** | Sistema de autocompletado inteligente |
| **Dotfiles** | Archivos de configuración que empiezan por punto |
| **JDK** | Java Development Kit: plataforma para desarrollar en Java |
| **.NET SDK** | Kit de desarrollo para C#/.NET |
| **NuGet** | Gestor de paquetes de .NET |
| **Gradle** | Sistema de construcción para Java/Kotlin |
| **Top Level Statements** | Sintaxis C# sin clase Main explícita |
| **Main simplificado** | Sintaxis Java 25: `void main()` sin `public static` |

## 7.7. Ejercicios de Repaso

1. **Conceptos:** Explica con tus palabras qué es un IDE y por qué no basta con un editor de texto.
2. **Instalación:** Instala Rider, IntelliJ y VS Code. Configura el mismo tema en los tres.
3. **Anatomía:** Abre Rider y localiza: Gutter, Status Bar, Tool Windows, Terminal.
4. **Configuración:** Crea un snippet personalizado en VS Code y sincroniza tu configuración con Settings Sync.
5. **Compilación:** Crea un proyecto C# en Rider, compílalo con Build y luego con Rebuild. Explica la diferencia.
6. **Depuración:** Crea un proyecto con error lógico, usa breakpoints para encontrarlo.
7. **Atajos:** Sin usar el ratón, abre un archivo, compila, depura y formatea el código.
8. **Comparativa:** Evalúa Rider, IntelliJ y VS Code para un proyecto de Java. Justifica tu elección.

## 7.8. ¿Qué viene después?

En la siguiente unidad (**UD03: Sistema de Control de Versiones**) veremos en profundidad **Git**: ramas, merges, conflictos, flujos de trabajo y colaboración en equipo. Todo lo que aprendiste aquí sobre Git integrado en el IDE será la base para dominar el control de versiones.

> 📌 **Ejemplo real:** Netflix usa IDEs configurados con extensiones específicas para cada microservicio. Los desarrolladores tienen entornos personalizados con atajos de teclado estandarizados, lo que les permite cambiar de proyecto sin fricción. Herramientas como IntelliJ y VS Code son la base de su productividad.

> 💡 **Buenas Prácticas:** 1) Invierte tiempo en configurar bien tu IDE al inicio del curso, 2) Aprende los atajos esenciales antes de instalar extensiones, 3) Usa la misma configuración en todos tus ordenadores con sincronización en la nube, 4) Documenta tus atajos y configuraciones favoritas.

## 7.9. Mapa de Conexiones entre Temas

```mermaid
graph LR
    UD01[UD01: Desarrollo] --> UD02[UD02: Entornos]
    UD02 --> UD03[UD03: Control de Versiones]
    UD03 --> UD04[UD04: Diagrama de Clases]
    UD04 --> UD05[UD05: Diagramas Comportamiento]
    UD05 --> UD06[UD06: Optimización]
    UD06 --> UD07[UD07: Pruebas]

    UD02 -.->|IDEs| UD03
    UD02 -.->|Compilación| UD01
    UD02 -.->|Refactorización| UD06

    style UD02 fill:#2196F3,color:#fff
    style UD01 fill:#4CAF50,color:#fff
    style UD03 fill:#FF9800,color:#fff
    style UD04 fill:#9C27B0,color:#fff
    style UD05 fill:#f44336,color:#fff
    style UD06 fill:#607D8B,color:#fff
    style UD07 fill:#4CAF50,color:#fff
```
