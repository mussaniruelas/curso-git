## Instalación y Configuración Inicial de Git

Antes de comenzar a usar Git, necesitas instalarlo en tu sistema y realizar una configuración inicial básica. Vamos a cubrir cómo hacerlo en los sistemas operativos más comunes.

### Instalación de Git

#### En macOS

1. **Instalar Git con Homebrew (recomendado):**
   - Si no tienes Homebrew instalado, primero instálalo ejecutando el siguiente comando en la terminal:

     ```bash
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
     ```

   - Luego, instala Git ejecutando:

     ```bash
     brew install git
     ```

2. **Instalar Git desde Xcode Command Line Tools:**
   - Otra forma de instalar Git en macOS es a través de las herramientas de línea de comandos de Xcode. Abre la terminal y ejecuta:

     ```bash
     xcode-select --install
     ```

#### En Linux

1. **Instalar Git en distribuciones basadas en Debian/Ubuntu:**

   ```bash
   sudo apt update
   sudo apt install git
   ```

2. **Instalar Git en distribuciones basadas en Red Hat/Fedora:**

   ```bash
   sudo dnf install git
   ```

3. **Instalar Git en distribuciones basadas en Arch Linux:**

   ```bash
   sudo pacman -S git
   ```

#### En Windows

1. **Descargar Git:**
   - Visita la página oficial de Git: [git-scm.com](https://git-scm.com).
   - Descarga el instalador para Windows.

   ![DownLoad Git](./git/11Download.png)

2. **Instalar Git:**
   - Ejecuta el instalador descargado.
   - Durante la instalación, puedes elegir las configuraciones predeterminadas o personalizarlas según tus preferencias. Por ejemplo, puedes elegir el editor de texto por defecto (como Vim, Nano, VS Code, etc.) y las opciones para la integración de la línea de comandos.

### Configuración Inicial de Git

Una vez instalado, debes configurar Git con tu nombre y dirección de correo electrónico. Esto es importante porque Git incluye esta información en cada commit que haces.

1. **Configurar el nombre de usuario:**

   ```bash
   git config --global user.name "Tu Nombre"
   ```

2. **Configurar el correo electrónico:**

   ```bash
   git config --global user.email "tuemail@example.com"
   ```

El uso de la opción `--global` asegura que esta configuración se aplique a todas las repositorios en tu máquina. Si deseas configurar diferentes nombres o correos electrónicos para repositorios específicos, puedes omitir `--global` y ejecutar estos comandos dentro del directorio del repositorio.

### Verificar la Configuración

Puedes verificar tu configuración con los siguientes comandos:

```bash
git config --global --list
```

Esto mostrará una lista de todas las configuraciones de Git aplicadas globalmente en tu sistema.

### Configuración Adicional

1. **Configurar el editor de texto por defecto para Git:**
   - Puedes especificar qué editor usar para escribir mensajes de commit. Por ejemplo, para usar VS Code:

   ```bash
   git config --global core.editor "code --wait"
   ```
   Establece **Visual Studio Code** como el editor predeterminado para las operaciones de Git que requieren una interfaz de edición, como escribir mensajes de commit, resolver conflictos de merge o editar listas de rebase interactivo. La opción --wait le indica a Visual Studio Code que espere hasta que cierres el archivo antes de devolver el control a Git.

2. **Configurar el manejo de fin de línea:**
   - Dependiendo del sistema operativo y de las necesidades del proyecto, podrías necesitar configurar cómo Git maneja los caracteres de fin de línea:
   - Para Windows:

   ```bash
   git config --global core.autocrlf true
   ```

   - Para macOS y Linux:

   ```bash
   git config --global core.autocrlf input
   ```