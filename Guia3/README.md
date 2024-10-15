# Guía 3

La Guía 3 consiste en la creacio de un gestor de profesores, el cual hace interaccion con una base de datos de MySQL. La aplicacion se divide en 2 fases, un backend y un frontend, el backend esta en un servidor de express, mientras que el frontend es una aplicacion de React.

## Clonación desde DockerHub

La imagen ha sido subida a DockerHub con el fin de que se pueda clonar. Esta se encuentra en el siguiente repositorio:

[Guía 3 - Backend](https://hub.docker.com/r/dsvillacorta/backend)

_El frontend se encuentra en este repositorio de GitHub._ 

## Comando para hacer _pull_

```bash
docker pull dsvillacorta/backend
```

## Base de Datos

Para hacer uso de la base de datos se tiene que seguir el siguiente proceso:

1. Abrir MySQL en el puerto 3306 (puedes usar XAMPP, WAMP, etc).
2. Crear la base de datos: _profesores_db_.

```bash
create database profesores_db;
```

## En dado caso, se quiera correr localmente (En un ambiente de desarrollo).

### Instalar las dependencias

```bash
npm install
```

### Correr el proyecto
```bash
npm start
```
