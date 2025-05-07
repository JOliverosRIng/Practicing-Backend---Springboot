# Practicing-Backend---Springboot
Práctica de desarrollo backend con Spring Boot. El repositorio compara dos versiones de una API REST simple: una sin estructura y otra bien organizada. Ambas exponen un endpoint /users, usan H2 como base de datos en memoria y devuelven datos en JSON. Incluye configuración, datos de ejemplo y capturas de prueba.

# Comparación de estructuras en Spring Boot

## Autor: J. Oliveros
**Práctica de backend con Spring Boot**

---

## Descripción

Este repositorio contiene dos implementaciones de una API REST simple desarrollada en Spring Boot. El objetivo es comparar una estructura desorganizada frente a una bien organizada siguiendo buenas prácticas de arquitectura en capas.

Ambas versiones:
- Usan una base de datos en memoria (H2).
- Exponen un endpoint REST en `/users`.
- Devuelven una respuesta JSON con usuarios predefinidos.

---

## Estructura del repositorio

```
springboot-rest-comparison/
├── proyecto-1-mal/
│   ├── User.java
│   ├── UserRepository.java
│   ├── UserController.java
│   ├── application.properties
│   └── data.sql
└── proyecto-2-bien/
    ├── model/User.java
    ├── repository/UserRepository.java
    ├── service/UserService.java
    ├── controller/UserController.java
    ├── application.properties
    └── data.sql
```

---

## Cómo ejecutar

### Requisitos

- Java 17+
- Maven

### Ejecutar el proyecto

Para ambos proyectos:

```bash
./mvnw spring-boot:run
```

Accede al endpoint:

```
GET http://localhost:8080/users
```

---

## Resultado

### JSON de respuesta esperado

```json
[
  {
    "id": 1,
    "name": "Alice"
  },
  {
    "id": 2,
    "name": "Bob"
  }
]
```

---

## Git

No se usaron ramas, por ahora :D

---

## Licencia

Este proyecto es parte de una práctica educativa y no está destinado para uso en producción.
