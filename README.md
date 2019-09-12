<p align="center">
  <img src="https://github.com/austinmajor/amiGO/blob/master/amigo.png" alt="amiGO" width="225"/>
<p/>

# amiGO (a·mi·go)

A generalized unit tested Golang RESTful API micro-service template - built for re-purposing

## General Usage

This repository runs a simple list daemon (`listd`) that implements a API for lists and items in relation to lists. 
The daemon uses a PostgreSQL database to persist data.

## API

For information regarding the `listd` API, visit https://amigoapi.docs.apiary.io/ to view documentation. 

## Dependencies

The only dependencies required to run the services in this repository are:

- `docker`
- `docker-compose`

## Make Rules

### Testing

To test the go code in this repository execute the following command:

```shell
make test
```

This will build the containers in docker-compose.test.yml and run
`GO111MODULE=on go test ./...` against all testable go code in the
repository.

### Running

To run the services execute the following command:

```shell
make run
```

This will stop any containers defined by the compose file if already running
and then rebuild the containers using the compose file. The list daemon (`listd`)
will be available at `localhost:3000` and the postgres instance will be available
at `localhost:5432`.

### Stopping

To stop the services and save data execute the following command:

```shell
make stop
```

## Special Thanks

George Shaw, Jim Rice, Jacob Walker
