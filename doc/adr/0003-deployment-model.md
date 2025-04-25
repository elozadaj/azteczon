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

As the system grows in usage and complexity, we can consider migrating to another deployment model, like:
- Serverless compute for containers: https://aws.amazon.com/fargate/
- Containers with self-managed cloud-infrastructure.

It is important to follow the Architecture Style principles to facilitate such migrations, with a strong
Package Structure alignment that enforces divisions across the different system components. 

** For a complete list of cloud computing requirements, see C4 Diagrams.

## Consequences

- A cloud provider must be chosen (see "Cloud Provider" ADR)
- A faster time-to-market, b of superseding infrastructure management to third-party cloud providers.
  - Configuration still relies on our end, so we are in control of quotas / limits.
- A serverless architecture inherently increases the coupling between the selected cloud provider and our system.
  - See "Package Structure" ADR, where we explore ways to mitigate high coupling. 
