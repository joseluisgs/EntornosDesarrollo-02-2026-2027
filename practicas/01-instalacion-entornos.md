# Práctica 1: Instalación de Entornos de Desarrollo

## Tabla de contenidos

- [1. Introducción](#1-introducción)
  - [1.1. Objetivos](#11-objetivos)
  - [1.2. Requisitos previos](#12-requisitos-previos)
- [2. Ejercicio 1: Instalación de IDEs](#2-ejercicio-1-instalación-de-ides)
  - [2.1. Instalación de JetBrains Rider](#21-instalación-de-jetbrains-rider)
  - [2.2. Instalación de Visual Studio Code](#22-instalación-de-visual-studio-code)
  - [2.3. Tabla comparativa de la experiencia](#23-tabla-comparativa-de-la-experiencia)
- [3. Ejercicio 2: Entorno en la nube](#3-ejercicio-2-entorno-en-la-nube)
  - [3.1. Acceso a GitHub Codespaces](#31-acceso-a-github-codespaces)
  - [3.2. Comparación local vs nube](#32-comparación-local-vs-nube)
- [4. Tiempo estimado](#4-tiempo-estimado)

---

## 1. Introducción

> 💡 **Punto de partida:** Antes de escribir una sola línea de código, necesitas una "herramienta" donde escribirlo. Así como un albañil necesita sus herramientas, un desarrollador necesita su IDE. En esta práctica vas a instalar y configurar dos de los entornos más utilizados en la industria.

### 1.1. Objetivos

- Instalar JetBrains Rider en tu equipo.
- Instalar Visual Studio Code en tu equipo.
- Documentar el proceso de instalación de cada uno.
- Comparar ambas experiencias de instalación.
- Explorar un entorno de desarrollo en la nube.

### 1.2. Requisitos previos

- Conexión a internet estable.
- Al menos 5 GB de espacio libre en disco.
- Permisos de administrador en tu equipo.
- Cuenta de GitHub (para el ejercicio de la nube).

---

## 2. Ejercicio 1: Instalación de IDEs

### 2.1. Instalación de JetBrains Rider

📌 **Dato:** JetBrains Rider es un IDE multiplataforma para C#/.NET. Se puede descargar desde https://www.jetbrains.com/rider/ con licencia de evaluación de 30 días, o usar la versión Community si está disponible.

**Pasos a seguir:**

1. Accede a la página oficial: https://www.jetbrains.com/idea/download/
2. Selecciona tu sistema operativo (Windows, macOS o Linux).
3. Descarga la versión **Community** (gratuita).
4. Ejecutado el instalador, sigue el asistente:
   - Selecciona la ruta de instalación (recomendado: la predeterminada).
   - Marca las casillas de crear acceso directo en el escritorio y asociar archivos `.java`.
   - Instala también **JetBrains Launcher** si se ofrece.

> 📝 **Nota:** JetBrains Rider requiere .NET SDK instalado. Verifica que tienes .NET 10 SDK ejecutando `dotnet --version` en la terminal.

**Documenta en tu informe:**

| Dato | Tu valor |
|------|----------|
| Sistema operativo | |
| Versión de IntelliJ instalada | |
| Tamaño en disco ocupado | |
| Tiempo de instalación | |
| JDK incluido | Sí / No |

📸 **Capturas requeridas:**
- Pantalla de descarga seleccionando Community.
- Asistente de instalación (ruta y opciones).
- Pantalla de bienvenida de IntelliJ abierto por primera vez.

### 2.2. Instalación de Visual Studio Code

📌 **Dato:** VS Code es un editor de código abierto desarrollado por Microsoft. No es propiamente un IDE, pero con extensiones se convierte en uno potente y ligero.

**Pasos a seguir:**

1. Accede a la página oficial: https://code.visualstudio.com/download
2. Descarga la versión para tu sistema operativo.
3. Ejecuta el instalador:
   - Añade VS Code al PATH (importante).
   - Marca "Add Open with Code action to Windows Explorer".
   - Marca "Register Code as an editor for supported file types".
   - Marca "Add to PATH" (requiere reiniciar la terminal).

> ⚠️ **Advertencia:** Si olvidas marcar "Add to PATH", no podrás abrir VS Code desde la terminal con el comando `code`. Puedes solucionarlo reinstallando o añadiéndolo manualmente.

**Documenta en tu informe:**

| Dato | Tu valor |
|------|----------|
| Sistema operativo | |
| Versión de VS Code instalada | |
| Tamaño en disco ocupado | |
| Tiempo de instalación | |
| Extensiones preinstaladas | |

📸 **Capturas requeridas:**
- Pantalla de descarga.
- Asistente de instalación (casillas seleccionadas).
- Pantalla de bienvenida de VS Code abierto.

### 2.3. Tabla comparativa de la experiencia

Completa la siguiente tabla comparativa:

| Criterio | JetBrains Rider | VS Code |
|----------|------------------------|---------|
| **Tamaño del instalador** | | |
| **Tamaño en disco** | | |
| **Tiempo de instalación** | | |
| **Requisitos del sistema** | | |
| **Facilidad de instalación (1-5)** | | |
| **Aspecto visual inicial** | | |
| **¿Necesita configuración extra?** | | |
| **Lenguajes listos para usar** | | |

> 💡 **Consejo:** No te limites a rellenar la tabla. Añade comentarios sobre tu experiencia: ¿qué te ha sorprendido? ¿Alguna dificultad? ¿Algo que te haya gustado especialmente?

---

## 3. Ejercicio 2: Entorno en la nube

### 3.1. Acceso a GitHub Codespaces

📌 **Dato:** Los entornos en la nube te permiten programar desde cualquier navegador sin instalar nada. GitHub Codespaces es uno de los más populares, aunque tiene un límite de horas gratuitas al mes.

**Pasos a seguir:**

1. Inicia sesión en tu cuenta de GitHub.
2. Crea un nuevo repositorio (puede ser público o privado).
3. En el repositorio, haz clic en el botón verde "Code" → pestaña "Codespaces" → "Create codespace on main".
4. Espera a que se configure el entorno (puede tardar 1-2 minutos la primera vez).
5. Una vez dentro, crea un archivo `hola.cs` con este contenido:

```csharp
Console.WriteLine("¡Hola desde la nube!");
```

6. Ejecútalo desde la terminal integrada.

> 📝 **Nota:** GitHub Codespaces ofrece 60 horas gratuitas al mes para cuentas personales. Se apaga automáticamente tras 30 minutos de inactividad.

### 3.2. Comparación local vs nube

Completa esta tabla:

| Criterio | Entorno local (VS Code/IntelliJ) | GitHub Codespaces |
|----------|----------------------------------|-------------------|
| **Velocidad de arranque** | | |
| **Disponibilidad** | | |
| **Rendimiento** | | |
| **Extensiones disponibles** | | |
| **Configuración persistente** | | |
| **Coste** | | |
| **Conexión a internet requerida** | | |
| **Ideal para...** | | |

**Reflexión final** (mínimo 100 palabras):
Escribe un párrafo comparando ambas experiencias. ¿Cuándo usarías uno u otro? ¿Crees que el entorno en la nube podría sustituir al local?

---

## 4. Tiempo estimado

**Total: 2 horas**

| Actividad | Tiempo estimado |
|-----------|----------------|
| Instalación de JetBrains Rider | 20 minutos |
| Instalación de VS Code | 15 minutos |
| Documentación y capturas | 30 minutos |
| Ejercicio de Codespaces | 30 minutos |
| Redacción de reflexión y comparativa | 25 minutos |
