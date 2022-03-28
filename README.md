
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

## Installation
```
$ docker-compose up 
```
### Access
`http://localhost`

### Basic auth
Id and password are written in docker/web/nginx.Dockerfile.

## Usage
### API
- GET /programing_languages
