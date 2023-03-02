# Hello App Runner

![](/static/banner_sample.png)

## Features

The service exposes a basic splash page with links to relevant App Runner content.
It has two unique features which benefit from running it in App Runner.

Upon first request it generates a unique avatar for each service which is saved in `./static/social.png`.
This image is used for social preview images when shared online and will be the same across different all of your container instances.
It is an example of using a local disk for small assets in an application.

The service also provides a `/metrics` endpoint so you can see some of the long running metrics of requests coming into the service.
This is an example of global state stored on a per container basis.
It can be used for state management, in memory cache, or other application needs.

There also might be an easter egg or two if you read the code. ;)

## Development

To run this application locally you can use `pipenv`

```
pipenv install
pipenv run python app.py
```

To run the application locally in a container you can use `docker`

```
docker build -t hello-app-runner .
docker run -it -p 8000:8000 hello-app-runner
```
