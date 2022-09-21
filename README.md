# Flow-5
Este repositorio contiene el flujo de NodeRed para obtener la información climática por API desde openweathermap.org


## Introducción 
En este flujo podrá observarse un conjunto de gráficos en Dasboard, las cuales tienen como propósito reportar la información climática recibida manualmente por MQTT, la información recibida automáticamente por API y la información de varios usuarios compartidos por MQTT en un broker público

## Material Necesario

Para realizar el flow 1 sera necesario lo siguiente:

- [Ubuntu20.04 ](https://releases.ubuntu.com/20.04/)
- [NodeJS](https://nodejs.org/es/)
-   [NPM](https://www.npmjs.com/)
-  [NodeRed](https://nodered.org/docs/getting-started/local)
- [Nodos Dashboard](https://flows.nodered.org/node/node-red-dashboard)
- [Mosquitto](https://mosquitto.org/)


## Material de Referencia

A continuación podras puedes encontrar los enlaces a cursos de la plataforma de edu.codigoiot.com con ellos podras realizar  las configuraciones necesarias

- [Instalación de Virutal Box y Ubuntu 20.04](https://edu.codigoiot.com/course/view.php?id=812)
-  [Instalación de NodeRed](https://edu.codigoiot.com/enrol/index.php?id=817)
-  [Introducción a NodeRed](https://edu.codigoiot.com/enrol/index.php?id=278)
-  [Introducción a Mosquitto](https://edu.codigoiot.com/enrol/index.php?id=851)


## Servicios
Para que este ejercicio funcione, necesita los siguientes servicios:

[ColmenaMQ]:Es un corredor publico y no se necesita cuenta
[OpenWeatherMap](https://openweathermap.org/) :Servicio meteorológico gratuito. Se requiere crear una cuenta.
[]
[]
## Instrucciones

### Requisitos previos

Para que el flow-4 funcione de manera adecuada se debe cumplir con los siguientes requisitos:

1.- Instalación de NodeJS: Se recomienda tener instalado NodeJS en alguna versión LTS. Para la creación de este Flow se usó la versión 16.17.0LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM

2.- Instalación de NodeRed: La instalación se realiza por NPM. Al momento de la creación de este documento se usó la versión 3.0.2.

3.- Instalar los nodos node-red-dashboard. Para ello, dirigete a la opcion "Manage Palet" de NodeRed y en la pestaña Install busca node-red-dashboard. Finalmente haz clic en instalar.

4.- Instalación de Broker local Mosquitto MQTT.

5.-Cuenta en OpenWeatherMap.org. Este es el servidor del cual se obtendrán los datos del clima por API
Validación de la clave API. 

6.- Debes generar una API Key con tu cuenta de openweathermaps.org

### Instrucciones de preparación del entorno
Para ejecutar este flujo, es necesario lo siguiente:

1.-Arrancar NodeRed (usando el comando "node-red" en nuestra terminal)
2.-Importar el flujo desde el repositorio
3.-Coloca tu API Key personal en la API Call del nodo HTTP Request.
4.-Actualiza la IP del corredor público
5.-Hacer clic en el boton Deploy

### Instrucciones de operacion
- Para poder visualizar el resultado de este flujo, sólo necesitas abrir la pestaña Debug.
- Enviar por MQTT un mensaje que contenga un JSON con las variables ID, temp y hum-
## Notas

1.-Instalar MySQL
  -Abrir la terminal
  -Ejecutar los siguientea comandos:
    sudo apt actualizar
    sudo apt install servidor mysql
* Para rrancar MySQL Server se usa el siguiente comando 'sudo mysql'

2.- La sección manual de este flujo se suscribe al tema codigoIoT/fow5/mqtt en un broker local.

3.- El mensaje mqtt usado para probar este flow esmosquitto_pub -h localhost -t ccodigoIoT/fow5/mqtt -m '{"ID":"Hugo Vargas","temp":18,"hum":78}'

4.-Para que la gráfica histórica muestre información, deben enviarse al menos 2 puntos.

5.-Para actualizar la IP del broker publico, se recomienda el siguiente comando nslookup broker.hivemq.com. Puedes usar el broker publico de tu elección.

6.-Para que múltiples gráficas se muestren en la sección de Histórico Público, es necesario que múltiples usuarios se encuentren publicando a la vez.

### Resultados 
En la siguiente imagen se puede ver los nodos
![](https://github.com/Fridaa-Andrade/Flow-5/blob/main/flow5-nodos.jpeg)

En la siguiente imagen se puede ver el tablero
![](https://github.com/Fridaa-Andrade/Flow-5/blob/main/flow5-tablero.jpeg)
## Evidencias

## Créditos

