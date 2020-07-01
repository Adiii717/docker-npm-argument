# docker-npm-argument
Pass argument to the node process using docker run command or docker-compose

### build the docker image

```
git clone https://github.com/Adiii717/docker-npm-argument.git
cd docker-npm-argument;
docker-compose build
docker-compose up
```

#### output 
```
Starting docker-npm-argument_docker-npm-param_1 ... done
Attaching to docker-npm-argument_docker-npm-param_1
docker-npm-param_1  | No argument passed to docker run command
docker-npm-param_1  | starting application
docker-npm-param_1  | 
docker-npm-param_1  | > app@0.0.0 start /app
docker-npm-param_1  | > node app.js
docker-npm-param_1  | 
docker-npm-param_1  | Node process arguments [ '/usr/local/bin/node', '/app/app.js' ]
docker-npm-argument_docker-npm-param_1 exited with code 0
```

### Pass param to npm using docker-compose

```
docker-compose run docker-npm-param  argument1 argument2
```

#### output
```
Args passed to docker run command are [ argument1 argument2 ]
starting application

> app@0.0.0 start /app
> node app.js "argument1" "argument2"

Node process arguments [ '/usr/local/bin/node', '/app/app.js', 'argument1', 'argument2' ]
```
