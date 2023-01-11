# JmeterMidChallenge
Lo que se cubre en esta prueba es:

* Ingresar a RickAndMortyAPI y realizar los siguientes pasos:

* Crear un setUp thread group en el cual se verificará el estado de la url base:  https://rickandmortyapi.com/api/
  * Si el status code es 200, continuar con la ejecución.
* Crear un thread group llamado csvTest, se hará lo siguiente:
  * Obtener la lista de todos los personajes y guardar el char_id desde este endpoint: /api/characters . Tienen que ser guardados en archivo csv.
  * Leer el archivo csv y obtener el id de los personajes y consultar el endpoint  /api/characters/[char_id]
* Crear un thread group llamado variableTestOne
  * Obtener el id de un personaje random en /api/characters
  * Guardar este id en una variable
* Crear un thead group llamado variableTestTwo
  * Pasar la variable de variableTestOne a variableTestTwo
  * Usar la variable en el endpoint de /api/characters/[char_id]
* Crear un tearDown thread group en el cual se borrara el contenido del csv que contiene los ids.

## Jmeter instalacion
Puedes descargar la version gratuita en: https://jmeter.apache.org/download_jmeter.cgi

## Creacion del proyecto
* Creamos una carpeta para nuestro proyecto.
* Para abrir jmeter en Mac
* Abrimos una terminal
* Navegamos a la carpeta de jmeter
* Dentro de la carpeta de jmeter navegamos a la carpeta de bin
* Usamos sh jmeter.sh
* Agregamos un thread group y guardamos el proyecto
