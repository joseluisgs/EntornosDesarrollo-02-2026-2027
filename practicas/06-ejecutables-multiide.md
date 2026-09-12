# Práctica 6: Mismo Código en Varios IDEs

## Tabla de contenidos

- [1. Introducción](#1-introducción)
  - [1.1. Objetivos](#11-objetivos)
  - [1.2. Requisitos previos](#12-requisitos-previos)
- [2. Ejercicio 1: C# en Rider y VS Code](#2-ejercicio-1-c-en-rider-y-vs-code)
  - [2.1. Crear el proyecto con dotnet CLI](#21-crear-el-proyecto-con-dotnet-cli)
  - [2.2. Abrir en Rider](#22-abrir-en-rider)
  - [2.3. Abrir en VS Code](#23-abrir-en-vs-code)
  - [2.4. Comparar experiencias](#24-comparar-experiencias)
- [3. Ejercicio 2: Java en IntelliJ y VS Code](#3-ejercicio-2-java-en-intellij-y-vs-code)
  - [3.1. Crear el proyecto](#31-crear-el-proyecto)
  - [3.2. Abrir en IntelliJ](#32-abrir-en-intellij)
  - [3.3. Abrir en VS Code](#33-abrir-en-vs-code)
  - [3.4. Comparar experiencias](#34-comparar-experiencias)
- [4. Tabla comparativa general](#4-tabla-comparativa-general)
- [5. Tiempo estimado](#5-tiempo-estimado)

---

## 1. Introducción

> 💡 **Punto de partida:** El mismo código fuente se puede abrir en diferentes IDEs. Pero, ¿funciona igual? ¿Compila igual? ¿La experiencia es la misma? En esta práctica vas a comparar cómo se comporta el mismo proyecto en distintos entornos de desarrollo.

### 1.1. Objetivos

- Crear un proyecto C# con la línea de comandos de .NET.
- Abrirlo y compilarlo en Rider y en VS Code.
- Crear un proyecto Java y abrirlo en IntelliJ y VS Code.
- Comparar tiempos, experiencia y errores entre IDEs.

### 1.2. Requisitos previos

- .NET SDK 8.0+ instalado (para C#).
- JetBrains Rider instalado.
- VS Code con extensión **C# Dev Kit** instalada.
- JDK 17+ instalado (para Java).
- IntelliJ IDEA Community instalado.
- VS Code con extensión **Extension Pack for Java** instalada.

---

## 2. Ejercicio 1: C# en Rider y VS Code

### 2.1. Crear el proyecto con dotnet CLI

1. Abre una terminal (PowerShell o CMD).
2. Navega a la carpeta donde quieras crear el proyecto.
3. Ejecuta:

```bash
dotnet new console -n HolaMundo
cd HolaMundo
```

4. Abre el archivo `Program.cs` y reemplaza su contenido por:

```csharp
Console.WriteLine("¡Hola Mundo desde C#!");
Console.WriteLine($"Fecha: {DateTime.Now}");
Console.WriteLine($"Sistema: {Environment.OSVersion}");
```

5. Verifica que compila desde la terminal:

```bash
dotnet build
dotnet run
```

📸 **Capturas requeridas:**
- Terminal con los comandos ejecutados.
- Salida del programa.

### 2.2. Abrir en Rider

1. Abre JetBrains Rider.
2. **File → Open** y selecciona la carpeta `HolaMundo`.
3. Espera a que Rider indexe el proyecto.
4. Abre `Program.cs`.
5. Haz clic en ▶️ para ejecutar.
6. Observa:
   - Tiempo desde que abres el proyecto hasta que puedes ejecutar.
   - ¿Rider detecta el proyecto automáticamente?
   - ¿Hay errores de IntelliSense?

**Documenta:**

| Criterio | Rider |
|----------|-------|
| Tiempo de apertura del proyecto | |
| Tiempo hasta primera ejecución | |
| ¿Detecta el proyecto? | Sí / No |
| ¿Autocompletado funciona? | Sí / No |
| ¿Errores显示? | Sí / No |
| Errores encontrados (si any) | |

📸 **Capturas requeridas:**
- Rider abriendo el proyecto.
- Panel de errores (si los hay).
- Salida de la ejecución.

### 2.3. Abrir en VS Code

1. Abre VS Code.
2. **File → Open Folder** y selecciona `HolaMundo`.
3. Si VS Code detecta un proyecto C#, te ofrecerá instalar la extensión **C# Dev Kit**. Instálala si no la tienes.
4. Abre `Program.cs`.
5. Para ejecutar desde VS Code:
   - Abre la terminal integrada (`Ctrl+`` `).
   - Ejecuta `dotnet run`.
6. Alternativamente, usa el botón ▶️ si la extensión C# Dev Kit lo ofrece.

**Documenta:**

| Criterio | VS Code |
|----------|---------|
| Tiempo de apertura del proyecto | |
| Tiempo hasta primera ejecución | |
| ¿Detecta el proyecto? | Sí / No |
| ¿Autocompletado funciona? | Sí / No |
| ¿Errores显示? | Sí / No |
| Errores encontrados (si any) | |
| ¿Necesita extensiones extra? | |

📸 **Capturas requeridas:**
- VS Code abriendo el proyecto.
- Oferta de instalar C# Dev Kit (si aparece).
- Terminal con `dotnet run`.
- Salida de la ejecución.

### 2.4. Comparar experiencias

**Tabla comparativa C#:**

| Criterio | Rider | VS Code |
|----------|-------|---------|
| **Velocidad de apertura** | | |
| **Detección automática del proyecto** | | |
| **Calidad del autocompletado** | | |
| **Depuración gráfica** | | |
| **Integración con terminal** | | |
| **Consumo de RAM** | | |
| **Facilidad de uso (1-5)** | | |
| **¿Recomendarías para C#?** | | |

> 📝 **Nota:** VS Code es más ligero pero menos integrado para C#. Rider es más pesado pero ofrece una experiencia completa sin configurar.

---

## 3. Ejercicio 2: Java en IntelliJ y VS Code

### 3.1. Crear el proyecto

1. Crea una carpeta `HolaMundoJava`.
2. Crea un archivo `Main.java` con este contenido:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("¡Hola Mundo desde Java!");
        System.out.println("Java: " + System.getProperty("java.version"));
        System.out.println("SO: " + System.getProperty("os.name"));
    }
}
```

3. Compila y ejecuta desde la terminal:

```bash
javac Main.java
java Main
```

📸 **Capturas requeridas:**
- Terminal con compilación y ejecución.

### 3.2. Abrir en IntelliJ

1. Abre IntelliJ IDEA.
2. **File → Open** y selecciona la carpeta `HolaMundoJava`.
3. IntelliJ puede ofrecer crear un proyecto. Acepta las opciones por defecto.
4. Abre `Main.java`.
5. Ejecuta con ▶️.

**Documenta:**

| Criterio | IntelliJ |
|----------|----------|
| Tiempo de apertura del proyecto | |
| Tiempo hasta primera ejecución | |
| ¿Detecta el proyecto? | Sí / No |
| ¿Autocompletado funciona? | Sí / No |
| ¿Errores显示? | Sí / No |

### 3.3. Abrir en VS Code

1. Abre VS Code.
2. **File → Open Folder** y selecciona `HolaMundoJava`.
3. Si no tienes la extensión **Extension Pack for Java**, instálala.
4. Abre `Main.java`.
5. Haz clic en ▶️ o usa la terminal: `javac Main.java && java Main`.

**Documenta:**

| Criterio | VS Code |
|----------|---------|
| Tiempo de apertura del proyecto | |
| Tiempo hasta primera ejecución | |
| ¿Detecta el proyecto? | Sí / No |
| ¿Autocompletado funciona? | Sí / No |
| ¿Errores显示? | Sí / No |
| ¿Necesita extensiones extra? | |

### 3.4. Comparar experiencias

**Tabla comparativa Java:**

| Criterio | IntelliJ | VS Code |
|----------|----------|---------|
| **Velocidad de apertura** | | |
| **Detección automática del proyecto** | | |
| **Calidad del autocompletado** | | |
| **Depuración gráfica** | | |
| **Integración con terminal** | | |
| **Consumo de RAM** | | |
| **Facilidad de uso (1-5)** | | |
| **¿Recomendarías para Java?** | | |

---

## 4. Tabla comparativa general

| Criterio | Rider (C#) | VS Code (C#) | IntelliJ (Java) | VS Code (Java) |
|----------|------------|--------------|-----------------|----------------|
| **IDE principal recomendado** | | | | |
| **Experiencia de primera ejecución** | | | | |
| **Calidad del autocompletado** | | | | |
| **Depuración integrada** | | | | |
| **Facilidad para principiantes** | | | | |
| **Ideal para proyecto grande** | | | | |

> 💡 **Consejo:** No hay un IDE "mejor" en general. El mejor depende del lenguaje, del tipo de proyecto y de tu experiencia. La clave es probar varios y quedarte con el que mejor se adapte a tu workflow.

---

## 5. Tiempo estimado

**Total: 2,5 horas**

| Actividad | Tiempo estimado |
|-----------|----------------|
| Crear proyecto C# con dotnet CLI | 10 minutos |
| Abrir y compilar en Rider | 20 minutos |
| Abrir y compilar en VS Code | 20 minutos |
| Comparar experiencias C# | 15 minutos |
| Crear proyecto Java | 10 minutos |
| Abrir y compilar en IntelliJ | 20 minutos |
| Abrir y compilar en VS Code | 20 minutos |
| Comparar experiencias Java | 15 minutos |
| Tabla comparativa general | 10 minutos |
