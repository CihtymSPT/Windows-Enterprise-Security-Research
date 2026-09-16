# Authorization and Scope

## Purpose

This document defines the authorization boundaries and testing scope for the
Windows Enterprise Security Research project.

The project is intended to study adversary behavior, security telemetry,
detection engineering, and defensive controls within controlled environments.

## Authorized Environments

Security testing documented by this repository is limited to:

- Virtual machines and infrastructure owned and controlled by the researcher.
- Isolated cybersecurity laboratory environments.
- Intentionally vulnerable systems intended for security research.
- Capture-the-flag and other environments that explicitly authorize security
  testing.
- Systems for which explicit authorization to perform the documented testing
  has been granted.

## Out of Scope

The following activities are outside the scope of this project:

- Testing third-party systems without authorization.
- Deploying research tooling against production environments without
  authorization.
- Accessing accounts, credentials, or data belonging to other individuals.
- Distributing malware for deployment against real-world targets.
- Attempting to evade security controls on systems outside the authorized
  research environment.

## Research Isolation

Adversary-simulation experiments will be conducted within isolated laboratory
networks whenever practical.

Lab systems may intentionally contain insecure configurations for research
purposes. These configurations should not be interpreted as recommended
production configurations.

Snapshots and recovery mechanisms will be used where appropriate to restore
systems to known states between experiments.

## Responsible Publication

Published findings will focus on:

- Technical behavior
- Security telemetry
- Detection opportunities
- Defensive controls
- Hardening recommendations
- Reproducible research methodology

Sensitive information, real credentials, private organizational information,
and information obtained from unauthorized systems will not be published.

## Scope Changes

The project scope may expand as additional laboratory systems and research
areas are introduced.

Any new research environment must remain within the authorization principles
defined by this document.