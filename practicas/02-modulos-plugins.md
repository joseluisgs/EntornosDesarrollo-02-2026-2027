# Práctica 2: Gestión de Módulos y Plugins

## Tabla de contenidos

- [1. Introducción](#1-introducción)
  - [1.1. Objetivos](#11-objetivos)
  - [1.2. Requisitos previos](#12-requisitos-previos)
- [2. Ejercicio 1: Plugins en IntelliJ IDEA](#2-ejercicio-1-plugins-en-intellij-idea)
  - [2.1. Instalación de Key Promoter X](#21-instalación-de-key-promoter-x)
  - [2.2. Verificación de funcionamiento](#22-verificación-de-funcionamiento)
  - [2.3. Desinstalación del plugin](#23-desinstalación-del-plugin)
- [3. Ejercicio 2: Extensiones en VS Code](#3-ejercicio-2-extensiones-en-vs-code)
  - [3.1. Instalación de la extensión Python](#31-instalación-de-la-extensión-python)
  - [3.2. Configuración del interpreter](#32-configuración-del-interpreter)
  - [3.3. Desactivación de la extensión](#33-desactivación-de-la-extensión)
- [4. Tabla resumen de plugins/extensiones](#4-tabla-resumen-de-pluginsextensiones)
- [5. Tiempo estimado](#5-tiempo-estimado)

---

## 1. Introducción

> 💡 **Punto de partida:** Un IDE sin plugins es como un móvil sin aplicaciones: funciona, pero le faltan funcionalidades que te harían la vida más fácil. En esta práctica vas a aprender a instalar, verificar y gestionar plugins en IntelliJ y extensiones en VS Code.

### 1.1. Objetivos

- Instalar y gestionar plugins en IntelliJ IDEA.
- Instalar y gestionar extensiones en VS Code.
- Verificar que cada plugin/extensión funciona correctamente.
- Documentar el proceso paso a paso.

### 1.2. Requisitos previos

- IntelliJ IDEA Community instalado (Práctica 1).
- VS Code instalado (Práctica 1).
- Conexión a internet.

---

## 2. Ejercicio 1: Plugins en IntelliJ IDEA

### 2.1. Instalación de Key Promoter X

📌 **Dato:** Key Promoter X es un plugin que te enseña a usar atajos de teclado. Cada vez que haces clic en un botón del menú, te muestra el atajo de teclado correspondiente. Es como un profesor particular que te va enseñando.

**Pasos a seguir:**

1. Abre IntelliJ IDEA.
2. Ve a **File → Settings → Plugins** (en macOS: **IntelliJ IDEA → Preferences → Plugins**).
3. En la pestaña **Marketplace**, busca "Key Promoter X".
4. Haz clic en **Install** y espera a que se descargue e instale.
5. Reinicia IntelliJ cuando te lo pida.

> 📝 **Nota:** Los plugins se descargan desde los servidores de JetBrains. Si la descarga es lenta, verifica tu conexión a internet.

### 2.2. Verificación de funcionamiento

Una vez reiniciado IntelliJ:

1. Abre cualquier proyecto existente o crea uno nuevo.
2. Haz clic en algún botón de la barra de herramientas (por ejemplo, el botón de "Run").
3. Debería aparecer una notificación emergente mostrando el atajo de teclado para esa acción.
4. Repite con otras acciones: buscar archivo, abrir terminal, etc.

**Documenta:**

| Acción | Atajo mostrado por Key Promoter X |
|--------|-----------------------------------|
| Run | |
| Search Everywhere | |
| Open File | |
| Terminal | |

📸 **Capturas requeridas:**
- Notificación de Key Promoter X tras hacer clic en un botón.
- Panel de notificaciones del plugin.

### 2.3. Desinstalación del plugin

1. Ve a **File → Settings → Plugins → Installed**.
2. Busca "Key Promoter X".
3. Haz clic en el botón deengranaje (⚙️) y selecciona **Uninstall**.
4. Reinicia IntelliJ.
5. Verifica que la notificación ya no aparece.

> ⚠️ **Advertencia:** Al desinstalar un plugin, IntelliJ guarda su configuración por si lo vuelves a instalar. Sin embargo, es buena práctica documentar qué configuraciones tenías antes de desinstalar.

---

## 3. Ejercicio 2: Extensiones en VS Code

### 3.1. Instalación de la extensión Python

📌 **Dato:** La extensión de Python de Microsoft es una de las más descargadas de VS Code. Aporta resaltado de sintaxis, depuración, autocompletado y mucho más para Python.

**Pasos a seguir:**

1. Abre VS Code.
2. Haz clic en el icono de extensiones en la barra lateral izquierda (o pulsa `Ctrl+Shift+X`).
3. En el buscador, escribe "Python".
4. Selecciona la extensión de **Microsoft** (la oficial).
5. Haz clic en **Install**.

### 3.2. Configuración del interpreter

1. Abre la paleta de comandos (`Ctrl+Shift+P`).
2. Escribe "Python: Select Interpreter".
3. Selecciona el interpreter de Python que tengas instalado.
4. Si no tienes Python instalado, descárgalo de https://www.python.org/ y vuelve a este paso.

**Verificación:**

1. Crea un archivo `prueba.py`.
2. Escribe: `print("¡Hola desde VS Code con Python!")`.
3. Ejecútalo con el botón ▶️ o desde la terminal.

> 📝 **Nota:** Si VS Code no encuentra Python, asegúrate de que está en el PATH del sistema.

### 3.3. Desactivación de la extensión

1. Ve al panel de extensiones (`Ctrl+Shift+X`).
2. Busca "Python" en la lista de extensiones instaladas.
3. Haz clic en **Disable** (no en Uninstall).
4. Verifica que VS Code ya no resalta sintaxis de Python.

> 💡 **Consejo:** Desactivar una extensión es útil cuando no la usas temporalmente pero no quieres perder su configuración. Es diferente a desinstalarla.

---

## 4. Tabla resumen de plugins/extensiones

Completa esta tabla con todos los plugins/extensiones que hayas gestionado:

| Plugin/Extensión | IDE | Funcionalidad | ¿Cómo verificas que funciona? | Estado actual |
|------------------|-----|---------------|-------------------------------|---------------|
| Key Promoter X | IntelliJ | | | |
| Python | VS Code | | | |
| | | | | |
| | | | | |

> 💡 **Consejo:** Añade al menos una extensión más de tu elección en las filas vacías. Puedes buscar extensiones populares en el marketplace de cada IDE.

---

## 5. Tiempo estimado

**Total: 1,5 horas**

| Actividad | Tiempo estimado |
|-----------|----------------|
| Instalación y verificación de Key Promoter X | 20 minutos |
| Desinstalación de Key Promoter X | 10 minutos |
| Instalación y configuración de Python en VS Code | 20 minutos |
| Desactivación de la extensión | 10 minutos |
| Redacción del informe y tablas | 30 minutos |
