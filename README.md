# [ENG]
# Human Resources System

## Microservices Monorepo

Mono repo containing seven projects structured as microservices, built with Spring Cloud and a set of tools that provide resilience, scalability, and secure communication across services:

- Feign → API request for communication between microsservices
- Ribbon → Client-side load balancer to distribute requests
- Eureka Server → Server to register microservices
- Zuul API Gateway → Routes requests and handles authorizations
- Hystrix → Circuit breaker to provide latency tolerance and avoid cascading failures
- OAuth2 + JWT → Authentication and authorization across microservices
- Docker → Containerization of services for local and cloud deployment

## Conceptual Model

This UML (Unified Modeling Language) diagram includes a few core entities and a Many-to-Many relationship between Users and Roles. It provides the foundation for demonstrating the implementation of Spring Cloud solutions and the design of a microservices architecture.

<img width="1992" height="1322" alt="image" src="https://github.com/user-attachments/assets/cc08c5fa-1dbc-42a1-886b-3a2201399e22" />

## Microservices architecture

The microservices architecture below was designed with system scalability in mind. Each green box represents a microservice (MS), all registered in Eureka (Discovery Server) and retrieving configuration from a private GitHub repository.

The Zuul Gateway centralizes most of the project, acting as a single entry point between the system and clients. The User and Worker microservices each have their own PostgreSQL database to ensure data isolation.

Finally, three Worker instances are shown to illustrate the system’s ability to scale dynamically, taking advantage of load balancing while maintaining ephemeral instances.

<img width="1862" height="1380" alt="image" src="https://github.com/user-attachments/assets/02dc1a4a-6840-4894-b6bf-f9e92df66dbb" />


# [PT-BR]

# Sistema de Recursos Humanos

## Mono repositório de Microsserviços

Monorepo contendo sete projetos estruturados como microsserviços, desenvolvidos com Spring Cloud e um conjunto de ferramentas que oferecem resiliência, escalabilidade e comunicação segura entre os serviços:

- Feign → Comunicação entre microsserviços
- Ribbon → Balanceador de carga no lado do cliente para distribuir requisições
- Eureka Server → Servidor para registrar os microsserviços
- Zuul API Gateway → Roteamento de requisições e gerenciamento de autorizações
- Hystrix → Circuit breaker para tolerância a latência e prevenção de falhas em cascata
- OAuth2 + JWT → Autenticação e autorização entre microsserviços
- Docker → Containerização dos serviços para execução local e em nuvem

## Modelo Conceitual

Este diagrama UML apresenta algumas entidades centrais e um relacionamento Many-to-Many entre Users e Roles. Ele serve como base para demonstrar a implementação das soluções do Spring Cloud e o design de uma arquitetura de microsserviços.

<img width="1992" height="1322" alt="image" src="https://github.com/user-attachments/assets/cc08c5fa-1dbc-42a1-886b-3a2201399e22" />

## Arquitetura dos Microsserviços

A arquitetura de microsserviços abaixo foi projetada com foco na escalabilidade do sistema. Cada caixa verde representa um microsserviço (MS), todos registrados no Eureka (Servidor de Registro) e obtendo configuração de um repositório privado no GitHub.

O Zuul Gateway centraliza grande parte do projeto, funcionando como um ponto único de entrada entre o sistema e o client. Os microsserviços User e Worker possuem seu próprio banco de dados PostgreSQL para garantir o isolamento de dados.

Por fim, três instâncias do Worker são mostradas para ilustrar a capacidade do sistema de escalar dinamicamente, aproveitando o balanceamento de carga e mantendo instâncias efêmeras, ou seja, podem ser criadas e destruídas dinamicamente conforme a necessidade do sistema.

<img width="1862" height="1380" alt="image" src="https://github.com/user-attachments/assets/02dc1a4a-6840-4894-b6bf-f9e92df66dbb" />





