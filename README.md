# Gramática completa del compilador 
Este proyecto fue realizado en el lenguage de programación Python, utilizando la versión 3.10 y empleando el entorno de Visual Studio Code para su desarrollo. No obstante, se trabajó a modo de consola e interfaz (utilizando la librería de Pyside2 del entorno QT), realizando esta compactación hibrida para un mejor manejo de la información procesada.

## Instalación
### 1ra forma.
Dar clic en Code, luego en Donwload ZIP y después de que termine la descarga, descomprimirlo.

### 2da forma.
Crear una carpeta, ingresar a git bash y ejecutar el siguiente comando:  git clone https://github.com/OTG-16/Gramatica_Compilador.git

### Nota
Es importante resaltar que en este proyecto se utilizan herramientas que deben ser instaladas previamente para el correcto funcionamiento de este analizador. Entre ellas están las siguientes:

- IDE QT Creator
- Librería Pyside2 (Se podría consultar el siguiente video para su instalación https://www.youtube.com/watch?v=INSimE1tW34&list=PLNN_J-C1-lZvgVgnoYXeZo49Boz6CDGTf&index=4 y este otro como introducción para su manejo https://www.youtube.com/watch?v=T0qJdF1fMqo&list=PLNN_J-C1-lZvgVgnoYXeZo49Boz6CDGTf&index=5&t=1533s)
- Librería Colorama (Utlizar en el cmd el comando: pip install colorama)
- Librería Matplotlib (Utlizar en el cmd el comando: pip install matplotlib)
- Librería Networkx (Utlizar en el cmd el comando: pip install networkx)

## Probando el programa
En un principio, al momento de correr el programa este muestra lo siguiente:
![c1](https://user-images.githubusercontent.com/70919055/191636160-03a7d676-64d0-44b7-be3e-5f74b06b9f8a.PNG)

Puede apreciarse una interfaz. Al lado izquierdo se cuenta con un cuadro de texto (ignorar el de la derecha) para ingresar la información a analizar. En la parte de a medias se tiene un botón, este se usa para comenzar con el análisis tanto léxico como sintáctico. Ahora bien, se ingresa en el cuadro correspondiente, el texto "int main(){
int a;
a=1;
}" y se da click en el botón de analizar. Al ser una cadena válida el programa muestra una ventana con el mensaje de "cadena aceptada!" y despliega la siguiente información:
![entero1](https://user-images.githubusercontent.com/70919055/197355779-e7b3235a-1565-439a-8b59-1d82e59a2dd8.png)
![entero2](https://user-images.githubusercontent.com/70919055/197355981-df526f60-970e-4bea-8a82-c0f1a7c02043.png)
![entero3](https://user-images.githubusercontent.com/70919055/197356031-6082d233-a08a-46ee-8b4b-f01ae2f901cc.png)
![entero4](https://user-images.githubusercontent.com/70919055/197356086-80fc926a-a1df-4579-b249-842fdf5fae0f.png)
![stringC1](https://user-images.githubusercontent.com/70919055/197356206-62f1b969-1e3b-43ba-b397-1770c41e531f.png)

Ahí se puede ver en la parte de la interfaz tanto el texto ingresado como el resultado del análisis léxico y en la de la consola se despliega su respectivo análisis sintáctico. Cabe mencionar que inicialmente en la consola solo se muestra el análisis sintáctico de la pila de enteros, entonces, si se quiere obtener el de la pila de strings en lugar del de la pila de enteros se tiene que hacer lo siguiente: en el archivo mainwindow.py se tienen que comentar las líneas 476, 477, 478 y 501, además de descomentar las líneas 481, 482, 483 y 505. 

