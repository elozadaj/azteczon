# 3. Deployment model

Date: 2025-04-23

## Status

Accepted


## Context

The deployment model must support a microservices architecture (for more information see "Architecture Style" ADR),
which requires a Continuous Delivery / Continuous Deployment environment, including capabilities for test automation,
packages building; and with a robust observability layer that monitors the health of the system and alerts about
possible issues.

## Decision

We will use a Serverless deployment model, as defined in the article: https://aws.amazon.com/serverless, where a cloud
provider:
- Takes on the infrastructure responsibilities, providing enough computing, storage, network and other
requirements** for guarantying a successful software execution.
- Provides observability tools for a successful monitoring, alerting, and fixing of errors. 

** For a complete list of cloud computing requirements, see C4 Diagrams.
## Consequences

- A cloud provider must be chosen (see "Cloud Provider" ADR)
- A fast time-to-market, thanks to the benefits of relying on third-party resources' management.
  - Configuration still relies on our end, so we are in control of quotas / limits.