# wordEZ
Word finding query engine based micro-services with Spring-Cloud-Gateway and Spring-WebFlux

## service-registry
service-registry for all the microservices in the project.

-- [Spring Boot 3, Eureka server]


## api-gateway
This microservice is responsible for application level routing and filter requests for authentication and authorization from identity-service (uses declarative client).

-- [Spring Boot 3, Spring-Cloud-Gateway, Spring Webflux]


## identity-service
Microservice build to handle security for the whole application at one place.
It uses JWT tokens with refresh tokens.
> refresh_token can have multiple jwt_token and has cascade on delete

-- [Spring Boot 3, Spring Security, JWT, PostgreSQL]<br/>


## wordez
Makes use of [datamuse-api](https://www.datamuse.com/api/?word=hello) and expose non-blocking endpoints.
> The Datamuse API is a word-finding query engine for developers. You can use it in your apps to find words that match a given set of constraints and that are likely in a given context. You can specify a wide variety of constraints on meaning, spelling, sound, and vocabulary in your queries, in any combination.

-- [Spring Boot 3, Spring Webflux, PostgreSQL]
