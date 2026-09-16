# Windows Enterprise Security Research

An independent cybersecurity research project focused on Windows enterprise
security, adversary simulation, detection engineering, and system hardening.

## Overview

This project investigates how Windows enterprise security controls prevent,
detect, and contain documented adversary techniques.

Research is conducted in controlled lab environments using systems owned by
the researcher or systems for which explicit authorization has been granted.

The project emphasizes repeatable testing: establishing a baseline,
reproducing documented security behaviors, collecting endpoint and network
telemetry, developing detections, applying defensive controls, and retesting
to measure their effectiveness.

## Research Objectives

Research areas include:

- Windows endpoint security and hardening
- Active Directory security
- MITRE ATT&CK-mapped adversary behavior
- Windows Event Log and Sysmon telemetry
- Detection engineering
- Sigma and YARA rules
- PowerShell security
- Credential and identity protection
- Privilege management
- Network segmentation
- Security control validation

## Research Methodology

Experiments follow a repeatable process:

1. Establish and document the system configuration.
2. Collect baseline security telemetry.
3. Reproduce a documented adversary technique within the controlled lab.
4. Analyze resulting endpoint and network behavior.
5. Identify relevant telemetry and detection opportunities.
6. Develop or evaluate defensive controls.
7. Repeat the experiment against the hardened environment.
8. Document results, limitations, and findings.

See [Research Methodology](docs/research-methodology.md).

## Lab Environment

The planned environment includes:

- Windows Server with Active Directory Domain Services
- Domain-joined Windows 11 endpoints
- Windows security auditing
- Sysmon endpoint telemetry
- Microsoft Defender security controls
- Enhanced PowerShell logging
- Centralized security logging
- Isolated security-testing systems

See [Lab Architecture](docs/lab-architecture.md).

## Research Experiments

### RE-001 — Windows PowerShell Logging & Detection

**Status: Planned**

The first experiment will evaluate the visibility of PowerShell activity under
different Windows logging and endpoint-monitoring configurations.

Baseline Windows telemetry will be compared with enhanced PowerShell logging
and Sysmon telemetry to identify useful behavioral detection opportunities.

Future experiments will expand into Windows credential protection,
persistence, privilege escalation, lateral movement, Active Directory security,
endpoint hardening, and security-control validation.

## Repository Structure

    docs/          Research methodology, architecture, and scope
    research/      Individual research experiments and findings
    detections/    Sigma, YARA, and Windows detection content
    hardening/     Defensive configurations and hardening guidance
    tools/         Research and telemetry utilities
    reports/       Published research summaries and findings

## Authorization and Ethics

All adversary simulation and security testing documented by this project is
limited to controlled lab environments, systems owned by the researcher, or
systems for which explicit authorization has been provided.

This repository is intended for cybersecurity research, education, detection
engineering, and defensive security.

See [Authorization and Scope](docs/authorization-and-scope.md).

## Project Status

**Current Phase: Lab Construction & Baseline Development**

The project infrastructure is currently being developed. Research findings,
detections, and hardening configurations will be published as experiments are
completed.