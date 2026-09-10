# Comandos de Limpieza y Mantenimiento del Sistema en Windows

Guía rápida de comandos útiles en la consola para realizar tareas básicas de mantenimiento, verificación de archivos y escaneo de virus en Windows.

---

### Método 1: Mostrar Archivos Ocultos y Recuperar Visibilidad
Útil para hacer visibles archivos que han sido ocultados por algún script o software en una unidad específica (como una memoria USB).

1. Abre el **Símbolo del sistema (CMD)**.
2. Navega hasta la unidad deseada (por ejemplo, `D:`).
3. Ejecuta el siguiente comando:

```cmd
attrib -s -h -r /s /d *.*

```

* **`-s`**: Quita el atributo de sistema.
* **`-h`**: Quita el atributo de oculto.
* **`-r`**: Quita el atributo de solo lectura.
* **`/s`**: Aplica el proceso a los subdirectorios.
* **`/d`**: Incluye las carpetas en el proceso.

---

### Método 2: Reparación de Archivos del Sistema (`sfc`)

Examina la integridad de todos los archivos protegidos del sistema y reemplaza las versiones dañadas o alteradas.

1. Abre el **Símbolo del sistema (CMD)** como **Administrador**.
2. Ejecuta el comando:

```cmd
sfc /scannow

```

---

### Método 3: Escaneo de Antivirus con Windows Defender vía PowerShell

Permite iniciar un análisis del sistema utilizando el motor integrado de Windows Defender desde la línea de comandos.

1. Abre **PowerShell** como **Administrador**.
2. Para un **análisis rápido**, ejecuta:

```powershell
Start-MpScan -ScanType QuickScan

```

3. Para un **análisis completo**, ejecuta:

```powershell
Start-MpScan -ScanType FullScan

```

---

### Método 4: Herramienta de Eliminación de Software Malintencionado (`MRT`)

Abre la interfaz gráfica de la herramienta nativa de Windows para detectar y eliminar amenazas específicas.

1. Presiona la combinación de teclas **Windows + R** para abrir la ventana *Ejecutar*.
2. Escribe el siguiente comando y presiona **Enter**:

```text
mrt

```
