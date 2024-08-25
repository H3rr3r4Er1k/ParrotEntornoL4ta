
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

Aquí tienes los comandos agrupados de manera lógica según su función:

**Shortcuts**

### **Gestión de Ventanas**
| Acción | Shortcut |
| -------- | -------- |
| Intercambiar el nodo actual con la ventana más grande | <kbd>Super</kbd> + <kbd>g</kbd> |
| Establecer el estado de la ventana | <kbd>Super</kbd> + <kbd>{t,Shift + t,s,f}</kbd> |
| Expandir una ventana moviendo uno de sus lados hacia afuera | <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>{h,j,k,l}</kbd> |
| Contraer una ventana moviendo uno de sus lados hacia adentro | <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>Shift</kbd> + <kbd>{h,j,k,l}</kbd> |
| Mover una ventana flotante | <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>{Left,Down,Up,Right}</kbd> |
| Redimensionar ventana personalizada | <kbd>Alt</kbd> + <kbd>Super</kbd> + <kbd>{Left,Down,Up,Right}</kbd> |

### **Enfoque de Ventanas y Escritorios**
| Acción | Shortcut |
| -------- | -------- |
| Enfocar la ventana siguiente/anterior en el escritorio actual | <kbd>Super</kbd> + <kbd>{,Shift + }c</kbd> |
| Enfocar el nodo en la dirección dada | <kbd>Super</kbd> + <kbd>{,Shift + }{Left,Down,Up,Right}</kbd> |
| Enfocar el nodo para el salto de ruta dado | <kbd>Super</kbd> + <kbd>{p,b,comma,period}</kbd> |
| Enfocar el escritorio siguiente/anterior en el monitor actual | <kbd>Super</kbd> + <kbd>Bracket{left,right}</kbd> |
| Enfocar el último nodo/escritorio | <kbd>Super</kbd> + <kbd>{grave,Tab}</kbd> |
| Enfocar el nodo más antiguo o más reciente en el historial de enfoque | <kbd>Super</kbd> + <kbd>{o,i}</kbd> |
| Enfocar o enviar al escritorio dado | <kbd>Super</kbd> + <kbd>{,Shift + }{1-9,0}</kbd> |

### **Preselección y Gestión de Nodos**
| Acción | Shortcut |
| -------- | -------- |
| Preseleccionar la dirección | <kbd>Super</kbd> + <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>{Left,Down,Up,Right}</kbd> |
| Preseleccionar la proporción | <kbd>Super</kbd> + <kbd>Ctrl</kbd> + <kbd>{1-9}</kbd> |
| Cancelar la preselección para el nodo enfocado | <kbd>Super</kbd> + <kbd>Ctrl</kbd> + <kbd>Space</kbd> |
| Cancelar la preselección para el escritorio enfocado | <kbd>Super</kbd> + <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Space</kbd> |
| Enviar el nodo marcado más reciente al nodo preseleccionado más reciente | <kbd>Super</kbd> + <kbd>y</kbd> |
| Establecer las banderas del nodo | <kbd>Super</kbd> + <kbd>Ctrl</kbd> + <kbd>{m,x,y,z}</kbd> |

### **Control del Sistema y Aplicaciones**
| Acción | Shortcut |
| -------- | -------- |
| Abrir el terminal | <kbd>Super</kbd> + <kbd>Return</kbd> |
| Lanzar el programa | <kbd>Super</kbd> + <kbd>d</kbd> |
| Recargar configuración de sxhkd | <kbd>Super</kbd> + <kbd>Escape</kbd> |
| Salir/reiniciar bspwm | <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>{q,r}</kbd> |
| Cerrar y matar nodo | <kbd>Super</kbd> + <kbd>{,Shift + }q</kbd> |
| Alternar entre el diseño en mosaico y monocle | <kbd>Super</kbd> + <kbd>m</kbd> |
| Abrir Firefox | <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>f</kbd> |
| Abrir Flameshot | <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>s</kbd> |
| Cambiar de teclado | <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>t</kbd> |
| Bloquear pantalla con i3lock-fancy | <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>x</kbd> |
