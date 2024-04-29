# A Simple Hello World Python Demo

## Run the application

You can simply use `python3 app.py` command.

This code defines a handler that responds to GET requests with the specified text and starts an HTTP server listening on port 8080. When you run the script, you can access the server at http://localhost:8080 and see the same message as the Python program.

Those commands will start a http server listening on port `8080`
and if your request `http://localhost:8080` you'll see the following output:

```shell
❯ curl http://localhost:8080

          ##         .
    ## ## ##        ==
 ## ## ## ## ##    ===
/"""""""""""""""""\___/ ===
{                       /  ===-
\______ O           __/
 \    \         __/
  \____\_______/


Hello from Docker!

```

## Using Docker init

### Run the following command:

```bash
 docker init
```

This utility will walk you through creating the following files with sensible defaults for your project:

- .dockerignore
- Dockerfile

## Modify the Dockerfile

```
FROM python:3.8-alpine
RUN mkdir /app
ADD . /app
WORKDIR /app
CMD ["python3", "app.py"]
```

## Running the container service

```
 docker build . python-app:latest
 docker run -p 8080:8080 python-app:latest
```

## Accessing the Python app

```
curl localhost:8080

         ##         .
   ## ## ##        ==
## ## ## ## ##    ===
/"""""""""""""""""\___/ ===
{                       /  ===-
\______ O           __/
\    \         __/
 \____\_______/


Hello from Docker!
```
