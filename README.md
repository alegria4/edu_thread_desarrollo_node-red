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
