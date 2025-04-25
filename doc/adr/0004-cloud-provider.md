# 4. Cloud Provider

Date: 2025-04-23

## Status

Accepted


## Context

Derived from the system architecture style (microservices) and deployment model (serverless) chosen for this system, cloud
providers must:
- Have a mature serverless development ecosystem, including support for Java, as this is the programming language chosen
for this project.
- Offer a serverless option for the corresponding cloud components included in the system architecture:
  - messaging, storage, networking, computing, etc.
- Provide complete and detailed code documentation and examples
- Provide a transparent price plan. 

## Decision

The cloud provider chosen is Amazon Web Services, as defined in https://aws.amazon.com/serverless/

## Consequences
- Another pop star in a televised quick trip to "space".
