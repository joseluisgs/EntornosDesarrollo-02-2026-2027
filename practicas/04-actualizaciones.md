# Práctica 4: Gestión de Actualizaciones

## Tabla de contenidos

- [1. Introducción](#1-introducción)
  - [1.1. Objetivos](#11-objetivos)
  - [1.2. Requisitos previos](#12-requisitos-previos)
- [2. Ejercicio: Gestión de actualizaciones](#2-ejercicio-gestión-de-actualizaciones)
  - [2.1. Verificar versiones actuales](#21-verificar-versiones-actuales)
  - [2.2. Configurar canal de actualización](#22-configurar-canal-de-actualización)
  - [2.3. Buscar actualizaciones pendientes](#23-buscar-actualizaciones-pendientes)
  - [2.4. Documentar proceso de actualización de un plugin](#24-documentar-proceso-de-actualización-de-un-plugin)
  - [2.5. Investigar: Rollback en JetBrains](#25-investigar-rollback-en-jetbrains)
- [3. Tabla resumen de versiones](#3-tabla-resumen-de-versiones)
- [4. Tiempo estimado](#4-tiempo-estimado)

---

## 1. Introducción

> 💡 **Punto de partida:** Los IDEs se actualizan constantemente para corregir errores, añadir funciones y mejorar la seguridad. Pero, ¿qué pasa cuando una actualización rompe algo? ¿Cómo vuelves atrás? En esta práctica aprenderás a gestionar actualizaciones y a hacer rollback si algo sale mal.

### 1.1. Objetivos

- Verificar la versión actual de tus IDEs.
- Configurar el canal de actualización adecuado.
- Buscar y aplicar actualizaciones pendientes.
- Documentar el proceso de actualización de plugins.
- Investigar cómo hacer rollback en JetBrains.

### 1.2. Requisitos previos

- IntelliJ IDEA Community instalado.
- VS Code instalado.
- Conexión a internet.

---

## 2. Ejercicio: Gestión de actualizaciones

### 2.1. Verificar versiones actuales

**En IntelliJ IDEA:**

1. Ve a **Help → About**.
2. Anota:
   - Build
   - JBR (Java Runtime)
   - Versión de Kotlin

**En Rider:**

1. Ve a **Help → About**.
2. Anota la misma información.

**En VS Code:**

1. Abre la paleta de comandos (`Ctrl+Shift+P`).
2. Escribe "About".
3. Anota la versión.

**Completa esta tabla:**

| IDE | Versión | Build | JBR/Kotlin | Fecha de lanzamiento |
|-----|---------|-------|------------|---------------------|
| IntelliJ IDEA Community | | | | |
| Rider | | | | |
| VS Code | | | | |

> 📝 **Nota:** La fecha de lanzamiento la puedes encontrar en las release notes oficiales de cada herramienta.

### 2.2. Configurar canal de actualización

**En IntelliJ/Rider:**

1. Ve a **File → Settings → Appearance & Behavior → System Settings → Updates**.
2. Configura:
   - **Check for updates automatically**: Marcada.
   - **Channel**: Stable releases (recomendado).
3. Opciones de canal:

| Canal | Descripción | ¿Cuándo usarlo? |
|-------|-------------|------------------|
| Stable | Versión estable, probada | Siempre (recomendado) |
| Beta | Versión beta, funcionalidades nuevas | Si quieres probar lo último |
| EAP | Early Access Program, versión experimental | Solo para testing avanzado |

**En VS Code:**

1. Ve a **File → Preferences → Settings**.
2. Busca "Update".
3. Configura:
   - **Update mode**: `default` (usa el del sistema operativo).

> ⚠️ **Advertencia:** No recomiendo usar canales Beta o EAP en tu equipo de producción o estudio. Las versiones experimentales pueden tener bugs que afecten a tu trabajo diario.

### 2.3. Buscar actualizaciones pendientes

**En IntelliJ/Rider:**

1. Ve a **Help → Check for Updates**.
2. Si hay una actualización disponible, se mostrará un diálogo con los cambios.
3. Puedes decidir:
   - **Update and restart**: Actualizar ahora.
   - **Remind me later**: Recordármelo más tarde.
   - **Ignore this version**: Ignorar esta versión.

**En VS Code:**

1. Ve a **Help → Check for Updates**.
2. O usa la paleta de comandos: "Code: Check for Updates".

**Documenta:**
- ¿Había actualizaciones disponibles?
- ¿Cuál era la versión disponible?
- ¿Qué cambios incluía? (mira las release notes)

### 2.4. Documentar proceso de actualización de un plugin

Elige un plugin/extension que tengas instalado y documenta su proceso de actualización:

**En IntelliJ:**

1. Ve a **File → Settings → Plugins → Updates**.
2. Verás la lista de plugins con actualizaciones disponibles.
3. Selecciona uno y haz clic en **Update**.
4. Documenta: nombre, versión anterior, versión nueva, cambios.

**En VS Code:**

1. Abre el panel de extensiones (`Ctrl+Shift+X`).
2. Si hay actualizaciones, aparecerá un número junto a "Installed".
3. Haz clic en **Update** junto a la extensión.
4. Documenta el proceso.

**Tabla de documentación:**

| Plugin/Extensión | IDE | Versión anterior | Versión nueva | Cambios principales | ¿Requiere reinicio? |
|------------------|-----|------------------|---------------|--------------------|--------------------|
| | | | | | |
| | | | | | |

### 2.5. Investigar: Rollback en JetBrains

📌 **Dato:** "Rollback" significa volver a una versión anterior. Es útil cuando una actualización causa problemas.

**Investiga y documenta:**

1. **¿Cómo hacer rollback de IntelliJ IDEA?**
   - Descargar versiones anteriores desde: https://www.jetbrains.com/idea/download/other.html
   - Usar JetBrains Toolbox para gestionar múltiples versiones.
   - La Toolbox permite instalar varias versiones simultáneamente.

2. **¿Cómo hacer rollback de un plugin?**
   - En IntelliJ: **File → Settings → Plugins → Installed** → seleccionar el plugin → engranaje → **Roll Back to Previous Version** (si está disponible).
   - Alternativa: descargar la versión anterior del plugin desde el marketplace.

3. **¿Cómo hacer rollback de VS Code?**
   - Descargar versiones anteriores desde: https://code.visualstudio.com/updates
   - VS Code no tiene opción nativa de rollback, pero puedes desinstalar y reinstalar una versión específica.

> 💡 **Consejo:** JetBrains Toolbox App es muy recomendable si necesitas trabajar con varias versiones de IntelliJ o Rider. Permite instalar, actualizar y cambiar entre versiones fácilmente.

**Tabla de rollback:**

| Herramienta | ¿Tiene rollback nativo? | ¿Cómo se hace? | Dificultad (1-5) |
|-------------|------------------------|-----------------|------------------|
| IntelliJ IDEA | | | |
| Rider | | | |
| VS Code | | | |
| Plugins IntelliJ | | | |
| Extensiones VS Code | | | |

---

## 3. Tabla resumen de versiones

Completa con la información recopilada:

| Herramienta | Versión instalada | Última versión disponible | ¿Actualizada? | Última actualización |
|-------------|-------------------|--------------------------|----------------|---------------------|
| IntelliJ IDEA | | | | |
| Rider | | | | |
| VS Code | | | | |
| Plugins IntelliJ | | | | |
| Extensiones VS Code | | | | |

---

## 4. Tiempo estimado

**Total: 1,5 horas**

| Actividad | Tiempo estimado |
|-----------|----------------|
| Verificar versiones actuales | 15 minutos |
| Configurar canal de actualización | 10 minutos |
| Buscar actualizaciones pendientes | 15 minutos |
| Documentar actualización de plugin | 20 minutos |
| Investigar rollback | 20 minutos |
| Redacción del informe | 10 minutos |
