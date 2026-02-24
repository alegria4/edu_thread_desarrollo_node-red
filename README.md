## Descripcion del sistema
El sistema implementado consta de una red IoT con diferentes nodos sensores encargados 
de realizar medidas periódicamente y toda una arquitectura capaz de hacer que esas 
medidas lleguen al ordenador para ser almacenadas en una base de datos y se muestren 
en pantalla mediante un HMI. 

El esquema que representa el sistema implementado es el siguiente:
<img width="886" height="493" alt="image" src="https://github.com/user-attachments/assets/4790078a-971e-42f2-8b1a-259b75558129" />

## Integracion en el BR

<img width="1134" height="374" alt="image" src="https://github.com/user-attachments/assets/d277489a-f403-4a70-9814-4fc6d5abbcf9" />

La imagen muestra lo que se realiza en node-red dentro del border router. El BR funciona como servidor COAP y espera los post de los clientes para luego pasarselos al
broker para que lo envie al ordenador.

## Integracion en el ordenador

<img width="962" height="673" alt="image" src="https://github.com/user-attachments/assets/00fe4c9f-8ddd-4708-bd69-bcb49e2c58c2" />

En el ordenador, recibimos los mensajes del broker y los enviamos tanto al HMI para que se vean en tiempo real como a la base de datos para almacenarlos.

## HMI (GUIA DE USO)

La interfaz humano-maquina diseñada permite supervisar y controlar el sistema en tiempo real. Esta incluye una interfaz de usuario destinada a la gestión de personas que entran al sistema, así como diferentes ventanas que permiten ver los datos obtenidos.

La primera pantalla que se ve nada mas entras es la siguiente:

<img width="886" height="412" alt="image" src="https://github.com/user-attachments/assets/18259dab-58f9-474d-80df-9235fb7e4165" />
 
Se trata de la interfaz de usuario, la cual dispone de un apartado de inicio de sesión que permite el acceso a la visualización de los datos, así como de un apartado de registro que debe completarse previamente al inicio de sesión.

Una vez inicias sesión entras a la siguiente ventana:

<img width="886" height="405" alt="image" src="https://github.com/user-attachments/assets/3828313d-0f6c-45bc-8556-915a93a83437" />

En este caso se muestran las medidas de los diferentes sensores en tiempo real, así como gráficos que se van construyendo a medida que llegan los datos. A la derecha se encuentran dos botones: el rojo nos permite cerrar sesión y volver a la interfaz de usuario, mientras que el azul nos llevara a unas ventanas para ver el histórico de datos.

Cuando pulsamos el azul nos lleva a la siguiente zona:

<img width="886" height="409" alt="image" src="https://github.com/user-attachments/assets/749907b3-ef0a-46d6-a8ad-6ff81cd4f115" />
 
Se trata de una zona empleada para que se seleccione el sensor del que se quiere ver el histórico de datos.

Para terminar, en esta última ventana se encuentran las diferentes graficas de los últimos cien datos leídos por el sensor de cada medida. Estas graficas se realizan mediante consultas a la base de datos.

<img width="886" height="404" alt="image" src="https://github.com/user-attachments/assets/2656418c-c112-4ed9-9732-5b2b8b5286c1" />

 


