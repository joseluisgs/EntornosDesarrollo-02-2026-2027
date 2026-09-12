# Práctica 5: Generación de Ejecutables en Múltiples Lenguajes

## Tabla de contenidos

- [1. Introducción](#1-introducción)
  - [1.1. Objetivos](#11-objetivos)
  - [1.2. Requisitos previos](#12-requisitos-previos)
- [2. Ejercicio 1: Proyecto Java en IntelliJ](#2-ejercicio-1-proyecto-java-en-intellij)
  - [2.1. Crear el proyecto](#21-crear-el-proyecto)
  - [2.2. Compilar y ejecutar](#22-compilar-y-ejecutar)
  - [2.3. Documentar archivos generados](#23-documentar-archivos-generados)
- [3. Ejercicio 2: Proyecto Kotlin en IntelliJ](#3-ejercicio-2-proyecto-kotlin-en-intellij)
  - [3.1. Crear el proyecto](#31-crear-el-proyecto)
  - [3.2. Compilar y ejecutar](#32-compilar-y-ejecutar)
  - [3.3. Documentar archivos generados](#33-documentar-archivos-generados)
- [4. Ejercicio 3: Proyecto C# en Rider](#4-ejercicio-3-proyecto-c-en-rider)
  - [4.1. Crear el proyecto](#41-crear-el-proyecto)
  - [4.2. Compilar y ejecutar](#42-compilar-y-ejecutar)
  - [4.3. Documentar archivos generados](#43-documentar-archivos-generados)
- [5. Tabla comparativa](#5-tabla-comparativa)
- [6. Tiempo estimado](#6-tiempo-estimado)

---

## 1. Introducción

> 💡 **Punto de partida:** Un IDE no solo sirve para escribir código: también compila, ejecuta y genera ejecutables. En esta práctica vas a crear proyectos en tres lenguajes diferentes (Java, Kotlin y C#) y comparar cómo cada IDE genera los archivos ejecutables.

### 1.1. Objetivos

- Crear un proyecto Java en IntelliJ IDEA.
- Crear un proyecto Kotlin en IntelliJ IDEA.
- Crear un proyecto C# en JetBrains Rider.
- Compilar y ejecutar cada proyecto.
- Documentar los archivos generados y comparar resultados.

### 1.2. Requisitos previos

- IntelliJ IDEA Community instalado con plugin de Kotlin.
- JetBrains Rider instalado.
- .NET SDK instalado (para C#).
- JDK 17+ instalado (para Java/Kotlin).

---

## 2. Ejercicio 1: Proyecto Java en IntelliJ

### 2.1. Crear el proyecto

1. Abre IntelliJ IDEA.
2. **File → New → Project**.
3. Selecciona **Java**.
4. Configura:
   - **Name**: HolaMundoJava
   - **Location**: ruta de tu elección
   - **Language**: Java
   - **Build system**: IntelliJ (o Maven/Gradle si prefieres)
   - **JDK**: 17 o superior
5. Haz clic en **Create**.
6. Crea un archivo `Main.java` en `src`:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("¡Hola Mundo desde Java!");
        System.out.println("Java version: " + System.getProperty("java.version"));
    }
}
```

### 2.2. Compilar y ejecutar

1. Haz clic derecho en `Main.java` → **Run 'Main.main()'**.
2. Observa la salida en la consola.
3. Para compilar sin ejecutar: **Build → Build Project**.

### 2.3. Documentar archivos generados

**Archivos en el proyecto:**

| Archivo/Carpeta | Descripción |
|-----------------|-------------|
| `src/Main.java` | Código fuente |
| `out/production/HolaMundoJava/` | Directorio de compilación |
| `out/production/HolaMundoJava/Main.class` | Bytecode compilado |
| `.idea/` | Configuración del proyecto |
| `HolaMundoJava.iml` | Descriptor del módulo |

> 📝 **Nota:** El bytecode Java (`.class`) no es un ejecutable nativo del sistema operativo. Necesita la JVM (Java Virtual Machine) para ejecutarse.

📸 **Capturas requeridas:**
- Estructura del proyecto en el panel lateral.
- Salida de la consola al ejecutar.
- Contenido de la carpeta `out/` tras compilar.

---

## 3. Ejercicio 2: Proyecto Kotlin en IntelliJ

### 3.1. Crear el proyecto

1. Abre IntelliJ IDEA.
2. **File → New → Project**.
3. Selecciona **Kotlin**.
4. Configura:
   - **Name**: HolaMundoKotlin
   - **Language**: Kotlin/JVM
   - **Build system**: IntelliJ (o Gradle)
   - **JDK**: 17 o superior
5. Crea un archivo `Main.kt`:

```kotlin
fun main() {
    println("¡Hola Mundo desde Kotlin!")
    println("Kotlin version: ${KotlinVersion.CURRENT}")
}
```

### 3.2. Compilar y ejecutar

1. Haz clic derecho en `Main.kt` → **Run 'MainKt'**.
2. Observa la salida.
3. **Build → Build Project** para compilar sin ejecutar.

### 3.3. Documentar archivos generados

**Archivos en el proyecto:**

| Archivo/Carpeta | Descripción |
|-----------------|-------------|
| `src/Main.kt` | Código fuente Kotlin |
| `out/production/HolaMundoKotlin/` | Directorio de compilación |
| `out/production/HolaMundoKotlin/MainKt.class` | Bytecode compilado |
| `.idea/` | Configuración del proyecto |

> 💡 **Consejo:** Kotlin se compila a bytecode de JVM, por lo que los archivos generados son `.class` igual que en Java. La diferencia está en la sintaxis del código fuente.

📸 **Capturas requeridas:**
- Estructura del proyecto.
- Salida de la consola.
- Comparación visual con el proyecto Java.

---

## 4. Ejercicio 3: Proyecto C# en Rider

### 4.1. Crear el proyecto

1. Abre JetBrains Rider.
2. **New Solution**.
3. Selecciona **Console App (.NET)**.
4. Configura:
   - **Solution name**: HolaMundoCSharp
   - **Solution location**: ruta de tu elección
   - **Framework**: .NET 8.0 o superior
5. Haz clic en **Create**.
6. Edita `Program.cs`:

```csharp
Console.WriteLine("¡Hola Mundo desde C#!");
Console.WriteLine($".NET version: {Environment.Version}");
```

> 📝 **Nota:** En .NET 6+ se usa Top Level Statements, por lo que no necesitas `class Main` ni `namespace`. El código se escribe directamente.

### 4.2. Compilar y ejecutar

1. Haz clic en el botón ▶️ (Run) o pulsa `Shift+F10`.
2. Observa la salida en la consola.
3. Para compilar sin ejecutar: **Build → Build Solution** (`Ctrl+Shift+B`).

### 4.3. Documentar archivos generados

**Archivos en el proyecto:**

| Archivo/Carpeta | Descripción |
|-----------------|-------------|
| `Program.cs` | Código fuente C# |
| `HolaMundoCSharp.csproj` | Archivo de proyecto |
| `bin/Debug/net8.0/` | Directorio de compilación |
| `bin/Debug/net8.0/HolaMundoCSharp.dll` | Ensamblado .NET |
| `bin/Debug/net8.0/HolaMundoCSharp.exe` | Ejecutable nativo (Windows) |
| `bin/Debug/net8.0/HolaMundoCSharp.pdb` | Símbolos de depuración |
| `obj/` | Archivos temporales de compilación |
| `HolaMundoCSharp.sln` | Archivo de solución |

> 📝 **Nota:** .NET genera tanto un `.dll` (ensamblado) como un `.exe` (ejecutable nativo en Windows). Puedes ejecutar cualquiera de los dos.

📸 **Capturas requeridas:**
- Estructura del proyecto en Rider.
- Salida de la consola.
- Contenido de la carpeta `bin/Debug/`.

---

## 5. Tabla comparativa

Completa con la información recopilada:

| Criterio | Java (IntelliJ) | Kotlin (IntelliJ) | C# (Rider) |
|----------|-----------------|-------------------|------------|
| **Lenguaje** | Java | Kotlin | C# |
| **IDE utilizado** | IntelliJ IDEA | IntelliJ IDEA | Rider |
| **Framework/Runtime** | JVM | JVM | .NET |
| **Comando de compilación** | Build Project | Build Project | Build Solution |
| **Archivo fuente** | `.java` | `.kt` | `.cs` |
| **Archivo compilado** | `.class` | `.class` | `.dll` / `.exe` |
| **Tamaño del ejecutable** | | | |
| **¿Necesita runtime?** | JVM | JVM | .NET Runtime |
| **Tiempo de compilación** | | | |
| **¿Genera ejecutable nativo?** | No | No | Sí (también .dll) |

> 💡 **Consejo:** Para generar un ejecutable nativo en Java puedes usar `jlink` o herramientas como GraalVM. En Kotlin, lo mismo. En C#, `dotnet publish -r win-x64 --self-contained` genera un ejecutable sin necesitar .NET instalado.

---

## 6. Tiempo estimado

**Total: 2 horas**

| Actividad | Tiempo estimado |
|-----------|----------------|
| Crear y ejecutar proyecto Java | 25 minutos |
| Crear y ejecutar proyecto Kotlin | 25 minutos |
| Crear y ejecutar proyecto C# | 25 minutos |
| Documentación y capturas | 25 minutos |
| Tabla comparativa | 20 minutos |
