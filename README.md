Este repositorio contiene el desarrollo de la interfaz HMI implementada mediante Node-RED, encargada de la supervisión y control del sistema IoT. A través de esta interfaz es posible visualizar en tiempo real las variables medidas por los nodos sensores, consultar el estado del sistema y actuar sobre el nodo actuador mediante el control del relé.

La interfaz se comunica con el sistema a través del bróker MQTT, suscribiéndose a los distintos tópicos donde se publican las medidas procedentes de los sensores. Del mismo modo, permite modificar el periodo de muestreo y el estado del relé, publicando los valores correspondientes para que sean procesados por el servidor CoAP y enviados a los nodos de la red Thread. Además, la interfaz integra la visualización de los datos almacenados en la base de datos, proporcionando una supervisión centralizada del sistema.

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

## Base de datos

La base de datos fue implementada en SQLite mediante la herramienta DB Browser. Esta cuenta con una parte dedicada a el registro y al acceso al sistema de los usuarios y otra para el almacenamiento de los datos. 

El siguiente diagrama muestra las diferentes tablas planteadas en ella:

<img width="886" height="463" alt="image" src="https://github.com/user-attachments/assets/9e0d396b-df72-42fa-8ade-74e3ea7b74a3" />

Las consultas e incorporaciones de datos se realizan desde el PC a medida que van llegando las medidas y se va interactuando con la Interfaz Humano-Maquina.



