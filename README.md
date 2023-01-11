# JmeterMidChallenge
Steps to follow are:

* Enter RickAndMortyAPI and perform the following steps:
* Create a setUp thread group in which the status of the base url will be checked:  https://rickandmortyapi.com/api/
  * If the status code is 200, continue with the execution.
* Create a thread group called csvTest, the following will be done:
  * Get the list of all characters and save the char_id from this endpoint: /api/characters . They have to be saved in csv file.
  * Read the csv file and get the id of the characters and query the endpoint /api/characters/[char_id]
* Create a thread group named variableTestOne
  * Get the id of a random character in /api/characters
  * Save the id in a variable
* Create a thead group called variableTestTwo
  * Pass variable from variableTestOne to variableTestTwo
  * Use the variable on the /api/characters/[char_id] endpoint
* Create a tearDown thread group in which the content of the csv containing the ids will be deleted.

## Jmeter installation
You can download the free version at: https://jmeter.apache.org/download_jmeter.cgi

## Project setup
* Create a folder for our project.
* to open jmeter in mac:
  * we open a terminal
  * We navigate to the jmeter folder
  * Inside the jmeter folder, navigate to the bin folder
  * Type sh jmeter.sh in terminal
* Add a theard group so you could save the project
