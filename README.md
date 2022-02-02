# Kotlin + Hexagonal Architecture

## Overview

**Kotlin**

A modern programming language that makes developers happier.

https://kotlinlang.org/


**Hexagonal Architecture**

![alt text](assets/images/arch.png)

The hexagonal architecture, or ports and adapters architecture, is an architectural pattern used in software design. It aims at creating loosely coupled application components that can be easily connected to their software environment by means of ports and adapters. This makes components exchangeable at any level and facilitates test automation.

https://medium.com/ssense-tech/hexagonal-architecture-there-are-always-two-sides-to-every-story-bc0780ed7d9c


## Requirements
- docker: https://www.docker.com/
- docker-compose: https://docs.docker.com/compose/

## Setup

1. build application

`$ (cd app && rm -f -r -- build && ./gradlew build)`

2. Start application

`$ docker-compose up -d`


## Testing

1. Create transaction

`$ curl -d '{"user":"john", "amount":99.99, "description": "Transfer"}' -H "Content-Type: application/json" -X POST http://localhost:8080/transactions`

2. Get transactions

`$ curl http://localhost:8080/transactions?user=john -H "Accept: application/json"`
