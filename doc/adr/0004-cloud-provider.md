# 4. Cloud Provider

Date: 2025-04-23

## Status

Accepted


## Context

Record the cloud provider decisions made on this project.

Derived from the system architecture style (microservices) and deployment model (serverless) chosen for this system, the
cloud provider must:
- Have a mature serverless development ecosystem
  - including support for Java
- Offer a serverless option for the cloud-components that integrates into the architecture of the system, e.g.,
messaging, storage, networking, computing.
- Provide documentation, examples, and a transparent price plan. 

## Decision

The cloud provider chosen is Amazon Web Services, as defined in https://aws.amazon.com/serverless/

## Consequences
- High cohesion between cloud provider platform and our system.
  - See "Package Structure" ADR for ways to mitigate high cohesion. 
- Another pop star in quick trip to space.