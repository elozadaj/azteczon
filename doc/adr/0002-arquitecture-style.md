# 2. Arquitecture Style

Date: 2025-04-23

## Status

Accepted


## Context

The e-commerce system should be highly available and scalable, supporting fluctuations derived from natural free markets.

Among the available architecture style options:
- EDA (event-driven architecture) is a suitable option due to its distributed-systems nature, allowing for independent
scalability of components and flexible infrastructure choices, e.g., compute, storage, and messaging. 
- A multi-layered approach would help in a quick time-to-market, but maintainability and software "evolvability" becomes a
major issue as the system grows.
  - Time-to-market is irrelevant for the e-commerce system as other products have already been successfully shipped.
  - See "Deployment model" ADR for other options to reduce time-to-market.

### Business domain
Domain-Driven Design (DDD) helps to incrementally create a model that represents the business. Such a model should be
understandable by all interested parties (stakeholders, software architects, software engineers), facilitating the
addition of new features, bug fixes, maintainability and software "evolvability" overall. 

## Decision

We will use a Microservices Architecture, as described in this article: https://aws.amazon.com/microservices/ as it
implements an EDA style, letting DDD guide the design and development of the system.

## Consequences

- A Microservices architecture is more complex to develop and maintain, compared to a monolithic approach, imposing
additional challenges in non-functional requirements (ilities), like security, observability and maintainability.
- See "Deployment Model" ADR for further implications about choosing a microservices architecture.
