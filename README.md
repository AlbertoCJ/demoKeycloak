DEMO APP KEYCLOAK SPRING-BOOT
==========================

## Project tech list

Listado de tecnologías/librerias usadas en el proyecto:

* Spring-boot
* Spring-data
* Base de datos H2
* Lombok
* keycloak


## Requirements
Run as any other Spring Boot app:
For building and running the application you need:

* [JDK 11](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
* [Maven 3.8.1](https://maven.apache.org/download.cgi)

## Build

* From command line:
```script
mvn clean install
```

This will use the application local configuration and will run the app server on the url:
```script
http://localhost:8083/
```
* Keycloak admin
```script
http://localhost:8083/auth/   <-- Admin

User Name: admin
Password: admin
```
* Para obtener un token (Usando POSTMAN)
```script
POST  http://localhost:8083/auth/realms/prueba/protocol/openid-connect/token

Body  ->  x-www-form-urlencode:

- username = [Nombre del usuario]
- client_id = login-app
- client_secret = 3emZWWBJNIEyQhOPifce02XE58uymDQU
- grant_type = password
- password = [ Contraseña del usuario ] reset password al usuario "john@test.com" desde administración

```