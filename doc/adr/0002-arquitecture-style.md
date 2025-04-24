# 2. Arquitecture Style

Date: 2025-04-23

## Status

Accepted


## Context

The e-commerce system should be highly available and scalable, supporting fluctuations derived from natural free-market.

Among the available architecture style options, an event-driven arquitecture (EDA) would be a suitable option due to
its distributed-systems nature.

For modeling the business domain, a Domain-Driven Design (DDD) approach has proven to evolve along with the business
needs. 

## Decision

We will use a Microservices Architecture, as described in this article: https://aws.amazon.com/microservices/ as it
follows an EDA style, and letting DDD guide the development process.

## Consequences

- Development, observability, communication, maintainability complexity increases as the number of components and
connections increases.
- See "Deployment Model" ADR for further implications about choosing a microservices architecture.
