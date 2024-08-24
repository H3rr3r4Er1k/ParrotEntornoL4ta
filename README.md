
# Entorno de S4vitar en Parrot 100% Funcional

![Entorno S4vitar](images/01.png)

Bienvenidos a la guía de personalización del entorno de S4vitar en Parrot. Aquí encontrarás todos los pasos necesarios para una instalación completa y funcional.

## Video Tutorial

Puedes seguir el video tutorial paso a paso en mi [canal de YouTube](https://youtu.be/rY6S9CS6KDc). Si el contenido es de tu agrado, considera suscribirte y seguirme en [LinkedIn](https://www.linkedin.com/in/johnosoriob/).

## Instalación

Clona el repositorio y prepara la instalación con los siguientes comandos:

```bash
git clone https://github.com/Balthael/ParrotEntorno
cd ParrotEntorno
chmod +x install.sh
sudo ./install.sh
```

Después de la instalación, asegúrate de seleccionar BSPWM e instalar `fzf` y `nvim`, ya que no están incluidos en el script inicial.

 ![bspwm](images/02.png)

### Problemas comunes

Si encuentras un error al cambiar al usuario root, sigue estos pasos para corregirlo:

![Error root](images/03.png)

Solución:

```bash
Ctrl + C
compaudit
chown root:root /usr/local/share/zsh/site-functions/_bspc
exit
```

![Solución error](images/04.png)

### Instalación de fzf

Instalación para usuarios root y no privilegiados:

**Root:**

```bash
sudo su
```

```bash
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```

**Usuario no privilegiado:**

```bash
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```
**Shortcuts**
| Acción | Shortcut |
| -------- | -------- |
| Cambiar de workspace específico | <kbd>Windows</kbd> + <kbd>[1\|2\|3\|4\|5\|6\|7\|8\|9\|0]</kbd> |
| Cambiar de workspace a el siguiente o el anterior | <kbd>Windows</kbd> + <kbd>]\|[</kbd> |
| Alternar entre los dos últimos workspaces | <kbd>Windows</kbd> + <kbd>Tab</kbd> |
| Seleccionar ventana abierta en el workspace actual | <kbd>Windows</kbd> + <kbd>⇦⇧⇩⇨</kbd> | 
| Mover la ventana seleccionada a otro workspace | <kbd>Windows</kbd> + <kbd>Shift</kbd> + <kbd>[1\|2\|3\|4\|5\|6\|7\|8\|9\|0]</kbd> |
| Abrir terminal (*Kitty*) | <kbd>Windows</kbd> + <kbd>Enter</kbd> |
| Abrir navegador (*Firefox*) | <kbd>Windows</kbd> + <kbd>Shift</kbd> + <kbd>F</kbd> |
| Abrir navegador (*Chromium*) | <kbd>Windows</kbd> + <kbd>Shift</kbd> + <kbd>G</kbd> |
| Abrir *BurpSuite* | <kbd>Windows</kbd> + <kbd>Shift</kbd> + <kbd>B</kbd> |
| Abrir menú de aplicaciones (*Rofi*) | <kbd>Windows</kbd> + <kbd>D</kbd> |
| Tomar screenshot (*Flameshot*) | <kbd>Windows</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd> |
| Bloquear pantalla (*i3lock-color*) | <kbd>Windows</kbd> + <kbd>Shift</kbd> + <kbd>X</kbd> |
| Abrir menú para apagar, suspender, etc. El sistema (*Rofi*) | <kbd>Windows</kbd> + <kbd>P</kbd>|
| Cerrar ventana seleccionada | <kbd>Windows</kbd> + <kbd>W</kbd> |
| Abrir preselección | <kbd>Windows</kbd> + <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Space</kbd> + <kbd>⇦⇧⇩⇨</kbd> |
| Resize de preselección | <kbd>Windows</kbd> + <kbd>Ctrl</kbd> + <kbd>[1\|2\|3\|4\|5\|6\|7\|8\|9\|0]</kbd> |
| Cerrar preselección | <kbd>Windows</kbd> + <kbd>Ctrl</kbd> + <kbd>Space</kbd> |
| Cambiar la ventana seleccionada a modo *Flotante* | <kbd>Windows</kbd> + <kbd>S</kbd> |
| Cambiar la ventana seleccionada a modo *Terminal* | <kbd>Windows</kbd> + <kbd>T</kbd> |
| Cambiar layout de la ventana seleccionada entre *Tiled* y *Monocle* | <kbd>Windows</kbd> + <kbd>M</kbd> |
| Resize de ventanas flotantes | <kbd>Windows</kbd> + <kbd>Alt</kbd> + <kbd>⇦⇧⇩⇨</kbd> |
| Mover ventanas flotantes | <kbd>Windows</kbd> + <kbd>Ctrl</kbd> + <kbd>⇦⇧⇩⇨</kbd> |
| Recargar configuración (*bspwm*) | <kbd>Windows</kbd> + <kbd>Alt</kbd> + <kbd>R</kbd> |
| Cerrar sesión | <kbd>Windows</kbd> + <kbd>Alt</kbd> + <kbd>Q</kbd> |
| Recargar configuración (*sxhkd*) | <kbd>Windows</kbd> + <kbd>Esc</kbd> |
| Subir volumen del sistema | <kbd>Fn</kbd> + <kbd>F3</kbd> |
| Bajar volumen del sistema | <kbd>Fn</kbd> + <kbd>F2</kbd> |
| Subir brillo del monitor | <kbd>Fn</kbd> + <kbd>F6</kbd> |
| Bajar brillo del monitor | <kbd>Fn</kbd> + <kbd>F5</kbd> |


