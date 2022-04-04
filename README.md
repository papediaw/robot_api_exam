## Requirements
- Develop a ruby client application to fetch list of programming_languages from this server
  - Command line specification:
    - `$ ruby robot_api_client.rb [OUTPUT_FORMAT(csv or json)] [BASIC_AUTH_ID] [BASIC_AUT_PASSWORD]`
- Write tests for your ruby client application using `RSpec Mock`
- Optional
  - Implement error handlings

### Expected output example
- json
```
$ ruby robot_api_client.rb json someId somePassword
[
  {
    "code": "ruby",
    "displayName": "Ruby"
  },
  {
    "code": "python",
    "displayName": "Python"
  },
  {
    "code": "java",
    "displayName": "Java"
  }
]
```

- csv
```
$ ruby robot_api_client.rb csv someId somePassword
code,displayName
ruby,Ruby
python,Python
java,Java
```
## How to develop
- Clone this repository and build a local enviroment.
- Create another repository to develop a ruby client application which can interect with the server.

<br>
This application is also dockerized. 
if you use docker

```
$ docker-compose up 
```
then you can access to `http://localhost`

#### Basic auth
Id and password are written in docker/web/nginx.Dockerfile.

#### API
- GET /programing_languages


## How to submit
Bonsoir M. DIOP, Pour le développement d'une application cliente Ruby, les contrôleurs d'action sont au cœur d'une requête Web dans Rails. Ils sont constitués d'une ou plusieurs actions qui sont exécutées à la demande qui permettrons de basculé directement vers la page web dédié. seul l' application rails hérite de ActionController:Base. Tous les autres contrôleurs héritent d'ApplicationController. Cela donne une classe pour configurer des éléments tels que la l'ID, le Mot de passe, la protection contre la falsification des demandes et le filtrage des paramètres de demande sensibles. Mettre en place un csv rapide pour le traitement des données au niveau du json et la modification du localhoste:6379/1 pour la communication avec le server interne pour ne pas avoir une erreur url.
