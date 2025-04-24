# 3. Deployment model

Date: 2025-04-23

## Status

Accepted


## Context

Record the deployment model selected for this project.

The deployment model must support a microservices architecture (for more information see
"Architecture Style" ADR), wich requires Continuous Delivery / Continuous Deployment for automated testing and package
of potentially shippable software. 

## Decision

We will use a Serverless deployment model, as defined in the article: https://aws.amazon.com/serverless. A cloud
provider takes on the infrastructure responsibilities, providing enough computing, storage, network and other
requirements** for guarantying a successful software execution.

** For more information, see C4 Diagrams.
## Consequences

- A cloud provider must be chosen (see "Cloud Provider" ADR)
- A fast initial deployment phase, thanks to the benefits of relying on third-party resources' management.
  - Configuration still relies on our end, so we are in control of quotas / limits.