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

No obstante, como segunda prueba se ingresa la cadena "int main(){
int b;
b=1;
while (b<9){
       print(b);
       b=b+1;	
}
}" para su respectivo análisis. Como también es una cadena válida se muestra la ventana con el mensaje de "cadena aceptada!" y también la siguiente información de interfaz y consola tal y como en la corrida anterior pero con sus datos específicos de la cadena analizada.

![otra1](https://user-images.githubusercontent.com/70919055/197358288-15bcdecc-624a-475b-813d-94f044fce012.png)
![otra2](https://user-images.githubusercontent.com/70919055/197358332-2dd3bb2c-7a6a-4016-851a-b3d5575c61a6.png)
![otra3](https://user-images.githubusercontent.com/70919055/197358354-5f6bf96c-9d62-469e-95ae-d85239989cbc.png)
![otra4](https://user-images.githubusercontent.com/70919055/197358380-698a1099-c94a-4b44-9655-3b3a9ad3d080.png)
![otra5](https://user-images.githubusercontent.com/70919055/197358405-0b352084-c722-4d94-bf49-7b04d0f92a96.png)
![otra6](https://user-images.githubusercontent.com/70919055/197358422-e7113955-7a13-492c-abfd-7fe945a038e7.png)
![otra7](https://user-images.githubusercontent.com/70919055/197358450-1669c325-ec09-4577-a00b-42e715830ed0.png)
![otra8](https://user-images.githubusercontent.com/70919055/197358524-98c142e5-247c-4942-a847-441c78508902.png)
![otra9](https://user-images.githubusercontent.com/70919055/197358547-28f7c67c-7999-4205-b31f-08fd4a15ca47.png)
![otra10](https://user-images.githubusercontent.com/70919055/197358570-39e83439-0d69-45d6-bd0e-a6fe6569e054.png)
![otra11](https://user-images.githubusercontent.com/70919055/197358611-10b5c6f1-5491-4e65-827b-ef2975501609.png)
![stringC2](https://user-images.githubusercontent.com/70919055/197358656-721ba037-b812-43c8-b875-d73e88757278.png)
![stringC22](https://user-images.githubusercontent.com/70919055/197358682-e30f6d0d-ac14-482e-9d0c-b552166ac8fe.png)
![stringC23](https://user-images.githubusercontent.com/70919055/197358712-69b77ebf-fd3d-451a-8d57-610d5f9b95ef.png)
![stringC24](https://user-images.githubusercontent.com/70919055/197358741-208b77c8-2df8-4020-9c33-e3796235fde9.png)
Cabe mencionar que el programa acepta cadenas más complejas pero que por dicha cualidad cubrirían mucho más espacio por el número de imágenes que demandarían, por lo que se omitieron este tipo de cadenas como documentación en este apartado.
Entonces, es así como se comprobó el debido funcionamiento de la práctica denominada "Gramática completa del compilador".
