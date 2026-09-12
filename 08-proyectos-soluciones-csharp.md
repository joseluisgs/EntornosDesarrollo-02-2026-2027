- [8. Creación de Proyectos y Soluciones en C#](#8-creación-de-proyectos-y-soluciones-en-c)
  - [8.1. Estructura de una Solución .NET](#81-estructura-de-una-solución-net)
    - [8.1.1. Formato .slnx (estándar .NET 10)](#811-formato-slnx-estándar-net-10)
    - [8.1.2. Diferencia entre .sln y .slnx](#812-diferencia-entre-sln-y-slnx)
  - [8.2. Estructura de un Proyecto .NET](#82-estructura-de-un-proyecto-net)
    - [8.2.1. Archivo .csproj](#821-archivo-csproj)
    - [8.2.2. Convenciones de carpetas](#822-convenciones-de-carpetas)
  - [8.3. Crear una Solución con dotnet CLI](#83-crear-una-solución-con-dotnet-cli)
    - [Paso a paso: Solución completa](#paso-a-paso-solución-completa)
  - [8.4. Gestión de paquetes NuGet](#84-gestión-de-paquetes-nuget)
    - [8.4.1. Configuración de NuGet](#841-configuración-de-nuget)
    - [8.4.2. Instalar y gestionar paquetes](#842-instalar-y-gestionar-paquetes)
    - [8.4.3. Paquetes habituales del curso](#843-paquetes-habituales-del-curso)
  - [8.5. Compilar y Ejecutar](#85-compilar-y-ejecutar)
  - [8.6. Resumen](#86-resumen)


# 8. Creación de Proyectos y Soluciones en C#

> 💡 **Punto de partida:** Sabes qué es un IDE y lo tienes instalado. Pero antes de escribir código necesitas crear la "casa" donde vivirá tu proyecto. En .NET, esa casa tiene una estructura específica: solución → proyecto → código.

> 💡 **¿Por qué me importa?**
> Crear bien la estructura desde el principio te ahorra problemas graves después. Un .csproj mal configurado puede causar errores de compilación, dependencias rotas y headaches infinitos. Este punto es la base de todo lo que hagas en C#.
> 
> 🔗 **Conexión con otros puntos:** El Punto 02 instalaste .NET SDK. Este punto lo usas para crear proyectos. El Punto 05 compilarás y depurarás desde el IDE.

**Objetivos de aprendizaje:**

- Entender la estructura de soluciones y proyectos en .NET
- Crear soluciones y proyectos con dotnet CLI
- Configurar NuGet correctamente
- Compilar y ejecutar desde la línea de comandos

## 8.1. Estructura de una Solución .NET

Una **solución** (*solution*) es un contenedor que agrupa uno o más proyectos relacionados. Es como una "carpeta maestra" que organiza todo tu trabajo.

> 💡 **Analogía:** Una solución es como un libro. Los proyectos son los capítulos. Cada capítulo tiene sus propios archivos, pero todos forman parte del mismo libro.

### 8.1.1. Formato .slnx (estándar .NET 10)

En .NET 10, el formato por defecto es `.slnx` (basado en XML), no el antiguo `.sln`. Es más legible y fácil de editar manualmente.

```xml
<Solution>
  <Project Path="MiProyecto/MiProyecto.csproj" />
</Solution>
```

### 8.1.2. Diferencia entre .sln y .slnx

| Característica | .sln (antiguo) | .slnx (nuevo, .NET 10) |
|----------------|----------------|------------------------|
| **Formato** | Texto propietario | XML legible |
| **Extensión** | `.sln` | `.slnx` |
| **Creación** | `dotnet new sln` | `dotnet new sln` |
| **Edición manual** | Difícil | Fácil (XML) |
| **Recomendado** | Proyectos legacy | **Nuevo estándar** |

> 📝 **Nota:** Si tienes un proyecto `.sln` existente, puedes migrarlo con `dotnet sln migrate`.

## 8.2. Estructura de un Proyecto .NET

Un **proyecto** (*project*) contiene el código fuente, las dependencias y la configuración de compilación. Se define en un archivo `.csproj`.

### 8.2.1. Archivo .csproj

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>net10.0</TargetFramework>
    <ImplicitUsings>enable</ImplicitUsings>
    <Nullable>enable</Nullable>
    <TreatWarningsAsErrors>true</TreatWarningsAsErrors>
    <LangVersion>14</LangVersion>
  </PropertyGroup>
</Project>
```

**Propiedades clave:**

| Propiedad | Descripción | Valor |
|-----------|-------------|-------|
| `OutputType` | Tipo de salida | `Exe` (ejecutable) o `Library` (biblioteca) |
| `TargetFramework` | Framework objetivo | `net10.0` |
| `ImplicitUsings` | Usings implícitos | `enable` (incluye System, System.Linq, etc.) |
| `Nullable` | Gestión estricta de nulos | `enable` (obligatorio en DAW) |
| `TreatWarningsAsErrors` | Tratar warnings como errores | `true` |
| `LangVersion` | Versión de C# | `14` para .NET 10 |

### 8.2.2. Convenciones de carpetas

```
MiSolucion/
├── MiSolucion.slnx              # Solución
└── MiSolucion/                  # Proyecto principal
    ├── MiSolucion.csproj        # Configuración del proyecto
    ├── Program.cs               # Punto de entrada (Top Level Statements)
    ├── Models/                  # Modelos de dominio
    ├── Services/                # Lógica de negocio
    ├── Repositories/            # Acceso a datos
    └── data/                    # Datos estáticos
```

## 8.3. Crear una Solución con dotnet CLI

### Paso a paso: Solución completa

```bash
# 1. Crear carpeta raíz
mkdir MiSolucion
cd MiSolucion

# 2. Crear la solución (.slnx)
dotnet new sln

# 3. Crear el proyecto de consola
dotnet new console -n MiProyecto

# 4. Añadir el proyecto a la solución
dotnet sln add MiProyecto/MiProyecto.csproj

# 5. Verificar que el proyecto está en la solución
dotnet sln list

# 6. Compilar toda la solución
dotnet build

# 7. Ejecutar el proyecto
dotnet run --project MiProyecto
```

> 💡 **Consejo:** El comando `dotnet new sln` crea un archivo `.slnx` en .NET 10. Si necesitas un `.sln` antiguo, usa `dotnet new sln --format sln`.

**Estructura creada:**

```
MiSolucion/
├── MiSolucion.slnx
└── MiProyecto/
    ├── MiProyecto.csproj
    └── Program.cs
```

**Verificar el contenido de Program.cs:**

```csharp
// Top Level Statements - C# 14
Console.WriteLine("¡Hola Mundo desde MiProyecto!");
```

**Ejecutar:**

```bash
dotnet run --project MiProyecto
# Salida: ¡Hola Mundo desde MiProyecto!
```

> 📝 **Nota:** En .NET 10, `dotnet new console` genera código con Top Level Statements por defecto. No necesitas `class Program` ni `static void Main()`.

## 8.4. Gestión de paquetes NuGet

**NuGet** es el gestor de paquetes de .NET. Contiene más de 350.000 bibliotecas gratuitas.

### 8.4.1. Configuración de NuGet

El archivo de configuración está en:

```
Windows:  C:\Users\TU_USUARIO\AppData\Roaming\NuGet\NuGet.Config
Linux:    ~/.nuget/NuGet/NuGet.Config
macOS:    ~/.nuget/NuGet/NuGet.Config
```

**Contenido típico:**

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <add key="nuget.org" value="https://api.nuget.org/v3/index.json" protocolVersion="3" />
  </packageSources>
</configuration>
```

> 📝 **Nota:** `nuget.org` es el repositorio oficial. Es como npm para JavaScript o pip para Python.

### 8.4.2. Instalar y gestionar paquetes

```bash
# Instalar un paquete
dotnet add package Newtonsoft.Json

# Versión específica
dotnet add package Newtonsoft.Json --version 13.0.3

# Eliminar un paquete
dotnet remove package Newtonsoft.Json

# Buscar paquetes
dotnet package search "json"

# Ver paquetes instalados
dotnet list package
```

### 8.4.3. Paquetes habituales del curso

| Paquete | Uso | Comando |
|---------|-----|---------|
| **Newtonsoft.Json** | Serialización JSON | `dotnet add package Newtonsoft.Json` |
| **Microsoft.EntityFrameworkCore** | ORM para bases de datos | `dotnet add package Microsoft.EntityFrameworkCore.Sqlite` |
| **Serilog** | Logging estructurado | `dotnet add package Serilog.Sinks.Console` |
| **NUnit** | Framework de tests | `dotnet add package NUnit` |
| **FluentAssertions** | Aserciones fluidas | `dotnet add package FluentAssertions` |

> ⚠️ **Advertencia:** No instales paquetes que no necesites. Cada paquete añade dependencias y puede aumentar el tamaño de tu aplicación.

## 8.5. Compilar y Ejecutar

```bash
# Compilar (genera archivos en bin/Debug/net10.0/)
dotnet build

# Ejecutar
dotnet run

# Ejecutar un proyecto específico de la solución
dotnet run --project MiProyecto

# Compilar en modo Release (optimizado)
dotnet build -c Release

# Limpiar archivos de compilación
dotnet clean

# Restaurar paquetes NuGet
dotnet restore

# Publicar (genera ejecutable autocontenido)
dotnet publish -c Release -o ./publish
```

> 💡 **Consejo:** Usa `dotnet build` para compilar y `dotnet run` para compilar + ejecutar. `dotnet run` es más cómodo durante el desarrollo.

**Archivos generados:**

```
MiProyecto/
├── bin/                    # Compilación
│   └── Debug/
│       └── net10.0/
│           ├── MiProyecto.dll      # Ensamblado .NET
│           ├── MiProyecto.exe      # Ejecutable (Windows)
│           └── MiProyecto.pdb      # Información de depuración
├── obj/                    # Archivos temporales
└── Program.cs              # Tu código fuente
```

## 8.6. Resumen

| Concepto | Descripción |
|----------|-------------|
| **Solución (.slnx)** | Contenedor de proyectos (formato XML en .NET 10) |
| **Proyecto (.csproj)** | Configuración del proyecto (framework, propiedades) |
| **dotnet new sln** | Crear solución |
| **dotnet new console** | Crear proyecto de consola |
| **dotnet sln add** | Añadir proyecto a la solución |
| **dotnet build** | Compilar |
| **dotnet run** | Ejecutar |
| **NuGet** | Gestor de paquetes (350.000+ bibliotecas) |
| **Top Level Statements** | Sin `class Program` ni `Main()` en C# 14 |

---

> 🔗 **Siguiente:** Con la estructura creada, en el Punto 05 aprenderás a usar el IDE para programar, depurar y gestionar el código de estos proyectos.
