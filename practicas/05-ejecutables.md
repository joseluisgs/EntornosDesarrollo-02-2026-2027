## Práctica 5: Creación y Ejecución de Proyectos en Múltiples Entornos

**Objetivo:** Crear, compilar y ejecutar proyectos en C#, Java y Kotlin utilizando diferentes IDEs y herramientas, demostrando la generación de ejecutables a partir de código fuente.

**Requisito de Documentación:** Capturas de pantalla de cada paso: creación, compilación, ejecución y archivos generados.

---

### PARTE I: C# con JetBrains Rider

#### 1. Proyecto de consola en Rider

1. Abra Rider → **New Solution** → **Console Application**
2. Nombre: `HolaMundoRider`
3. Lenguaje: **C#**, Framework: **.NET 10.0**
4. Escriba en `Program.cs`:
   ```csharp
   Console.WriteLine("¡Hola desde Rider!");
   Console.WriteLine($"Hora actual: {DateTime.Now}");
   Console.WriteLine($"Entorno: {Environment.OSVersion}");
   ```
5. Ejecute con **Shift+F10** o el botón ▶
6. **[CAPTURAR]** Salida en la consola

#### 2. Generar ejecutable

1. **Build → Build Solution** (`Ctrl+Shift+B`)
2. Busque el ejecutable en `bin/Debug/net10.0/HolaMundoRider.exe`
3. Ejecute desde la terminal:
   ```bash
   cd bin/Debug/net10.0
   ./HolaMundoRider.exe
   ```
4. **[CAPTURAR]** El ejecutable funcionando desde terminal

---

### PARTE II: C# con Visual Studio Code

#### 3. Proyecto de consola en VS Code

1. Abra la terminal integrada (`` Ctrl+` ``)
2. Cree el proyecto:
   ```bash
   dotnet new console -n HolaMundoVSCode
   cd HolaMundoVSCode
   ```
3. Abra la carpeta en VS Code: **File → Open Folder**
4. Escriba en `Program.cs`:
   ```csharp
   Console.WriteLine("¡Hola desde VS Code!");
   Console.WriteLine($"Compilado con dotnet CLI");
   ```
5. Ejecute:
   ```bash
   dotnet run
   ```
6. **[CAPTURAR]** Salida en la terminal

#### 4. Generar ejecutable

```bash
dotnet publish -c Release -o ./publish
cd publish
./HolaMundoVSCode.exe
```

**[CAPTURAR]** El ejecutable generado y funcionando

---

### PARTE III: C# con dotnet CLI (sin IDE)

#### 5. Proyecto completo desde línea de comandos

Abra una terminal **fuera de cualquier IDE** y ejecute:

```bash
# Crear carpeta y proyecto
mkdir HolaMundoCLI
cd HolaMundoCLI
dotnet new sln
dotnet new console -n MiApp
dotnet sln add MiApp/MiApp.csproj

# Escribir código directamente
echo 'Console.WriteLine("¡Hola desde la CLI!");' > MiApp/Program.cs

# Compilar y ejecutar
dotnet build
dotnet run --project MiApp

# Generar ejecutable
dotnet publish MiApp -c Release -o ./publish
```

**[CAPTURAR]** Cada paso: creación de solución, proyecto, compilación y ejecución

---

### PARTE IV: Java con IntelliJ IDEA (Gradle)

#### 6. Proyecto Java con Gradle en IntelliJ

1. Abra IntelliJ → **New Project** → **Gradle** → **Java**
2. Nombre: `HolaMundoJava`
3. Build system: **Gradle**, Language: **Java**
4. JDK: **25** (el que instalaste)
5. En `build.gradle` (o `build.gradle.kts`), asegúrese de tener:
   ```groovy
   plugins {
       id 'java'
       id 'application'
   }

   application {
       mainClass = 'com.example.App'
   }
   ```
6. Cree `src/main/java/com/example/App.java`:
   ```java
   package com.example;

   public class App {
       public static void main(String[] args) {
           System.out.println("¡Hola desde IntelliJ + Gradle!");
           System.out.println("Java version: " + System.getProperty("java.version"));
       }
   }
   ```
7. Ejecute con el botón ▶ junto al método `main`
8. **[CAPTURAR]** Salida en la consola

#### 7. Generar ejecutable JAR

En la terminal del proyecto:
```bash
./gradlew build
java -jar build/libs/HolaMundoJava.jar
```

**[CAPTURAR]** El JAR generado y ejecutándose

---

### PARTE V: Kotlin con IntelliJ IDEA (Gradle)

#### 8. Proyecto Kotlin con Gradle en IntelliJ

1. Abra IntelliJ → **New Project** → **Gradle** → **Kotlin/JVM**
2. Nombre: `HolaMundoKotlin`
3. Build system: **Gradle**, Language: **Kotlin**
4. En `build.gradle.kts`:
   ```kotlin
   plugins {
       kotlin("jvm") version "2.1.0"
       application
   }

   application {
       mainClass.set("com.example.MainKt")
   }
   ```
5. Cree `src/main/kotlin/com/example/Main.kt`:
   ```kotlin
   package com.example

   fun main() {
       println("¡Hola desde IntelliJ + Kotlin + Gradle!")
       val version = KotlinVersion.CURRENT
       println("Kotlin version: $version")
   }
   ```
6. Ejecute con el botón ▶
7. **[CAPTURAR]** Salida en la consola

#### 9. Generar ejecutable

```bash
./gradlew build
java -jar build/libs/HolaMundoKotlin.jar
```

**[CAPTURAR]** El JAR generado y ejecutándose

---

### TABLA RESUMEN

| # | Lenguaje | IDE/Herramienta | Comando compilación | Archivo generado | Ejecución |
|---|----------|-----------------|---------------------|------------------|-----------|
| 1 | C# | Rider | `dotnet build` | `HolaMundoRider.exe` | `./HolaMundoRider.exe` |
| 2 | C# | VS Code | `dotnet publish` | `HolaMundoVSCode.exe` | `./HolaMundoVSCode.exe` |
| 3 | C# | dotnet CLI | `dotnet build` | `MiApp.dll` / `.exe` | `dotnet run` |
| 4 | Java | IntelliJ + Gradle | `./gradlew build` | `.jar` | `java -jar app.jar` |
| 5 | Kotlin | IntelliJ + Gradle | `./gradlew build` | `.jar` | `java -jar app.jar` |

---

### Criterios de Evaluación

| Criterio | Puntos |
|----------|--------|
| Proyecto C# creado y ejecutado en Rider | 1 |
| Proyecto C# creado y ejecutado en VS Code | 1 |
| Proyecto C# creado con dotnet CLI (sin IDE) | 1 |
| Proyecto Java con Gradle creado y ejecutado | 1 |
| Proyecto Kotlin con Gradle creado y ejecutado | 1 |
| Generación de ejecutables (todos los casos) | 2 |
| Capturas completas de cada paso | 1 |
| Tabla resumen rellenada | 1 |
| **Total** | **9** |
