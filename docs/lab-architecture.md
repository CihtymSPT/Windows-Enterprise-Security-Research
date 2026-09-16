# Lab Architecture

## Status

**Phase: Initial Design**

This document describes the planned architecture for the Windows Enterprise
Security Research lab. Configuration details will be updated as infrastructure
is deployed.

## Design Objectives

The laboratory is designed to provide:

- A representative Windows domain environment
- Windows enterprise endpoints
- Centralized security telemetry
- Endpoint security controls
- A controlled adversary-simulation environment
- Network isolation from production systems
- Repeatable system states for security experiments

## Initial Systems

| Host | Role | Operating System | Status |
|---|---|---|---|
| DC01 | Domain Controller / DNS | Windows Server | Planned |
| CLIENT01 | Domain Workstation | Windows 11 | Planned |
| SEC01 | Security / Logging Server | TBD | Planned |
| ATTACK01 | Security Testing Workstation | Linux | Planned |

Additional endpoints may be introduced as research requirements expand.

## Active Directory

Planned domain:

    LAB.INTERNAL

Initial account roles will include:

    Administrative User
    Standard User
    Test User

Specific accounts and organizational-unit design will be documented during
domain deployment.

## Network Architecture

The initial architecture will separate enterprise systems from the research
testing environment where practical.

Planned logical structure:

    ┌───────────────────────────────────────┐
    │        Enterprise Lab Network         │
    │                                       │
    │   DC01             CLIENT01           │
    │    │                   │              │
    │    └─────────┬─────────┘              │
    │              │                        │
    │            SEC01                      │
    │      Centralized Telemetry            │
    └──────────────┬────────────────────────┘
                   │
             Controlled Access
                   │
             ┌─────┴─────┐
             │ ATTACK01  │
             │ Research  │
             └───────────┘

The final virtual networking configuration will be documented after the
hypervisor and network topology are selected.

## Planned Telemetry

Endpoint telemetry is expected to include:

- Windows Security Event Log
- Windows System Event Log
- PowerShell Operational logging
- PowerShell Script Block Logging
- Microsoft Defender events
- Sysmon
- Authentication events
- Relevant network telemetry

Centralized collection will be introduced after the initial domain and
endpoint environment is operational.

## System State Management

Virtual-machine snapshots will be used to establish repeatable states.

Important research stages may include:

    CLEAN INSTALL
          ↓
    DOMAIN JOINED
          ↓
    BASELINE CONFIGURATION
          ↓
    TELEMETRY ENABLED
          ↓
    HARDENED CONFIGURATION

This allows experiments to compare baseline and hardened environments while
reducing configuration drift.

## Security Boundaries

The lab is intended to remain logically separated from production and
personal systems.

Adversary-simulation activity will be limited to authorized laboratory
systems as defined in [Authorization and Scope](authorization-and-scope.md).

## Future Architecture

Potential future additions include:

- Additional Windows workstations
- Dedicated administrative workstation
- Additional domain controllers
- SIEM platform
- Network monitoring
- Vulnerable application servers
- Certificate Services
- Additional Active Directory services

These components will only be documented as deployed once they become part of
the actual research environment.