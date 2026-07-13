## HMI 
Este repositorio contiene el desarrollo de la interfaz HMI implementada mediante Node-RED, encargada de la supervisión y control del sistema IoT. A través de esta interfaz es posible visualizar en tiempo real las variables medidas por los nodos sensores, consultar el histórico de datos, actuar sobre el nodo actuador mediante el control del relé y modificar el periodo de muestreo de los nodos sensores.

La interfaz se comunica con el sistema a través del bróker MQTT, suscribiéndose a los distintos tópicos en los que se publican las medidas procedentes de los sensores. 

Se adjunta tambien al repositorio el manual de usuario del HMI.

## Base de datos

La base de datosn del sistema fue implementada en SQLite mediante la herramienta DB Browser. Esta cuenta con una parte dedicada a el registro y al acceso al sistema de los usuarios y otra para el almacenamiento de los datos. 

El siguiente diagrama muestra las diferentes tablas planteadas en ella:

<img width="1792" height="872" alt="Captura de pantalla 2026-06-15 113104" src="https://github.com/user-attachments/assets/eb795537-1934-4aec-8ffa-6e3eac89120c" />

Las consultas e incorporaciones de datos se realizan desde el PC a medida que van llegando las medidas y se va interactuando con la Interfaz Humano-Maquina.

La base de datos utilizada en el proyecto no se incluye en el repositorio.



