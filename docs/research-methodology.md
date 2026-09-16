# Research Methodology

## Purpose

This project uses a repeatable experimental methodology to evaluate Windows
enterprise security controls against documented adversary behaviors.

The objective is to understand the relationship between:

**Adversary Behavior → Telemetry → Detection → Mitigation → Validation**

Each experiment should produce enough documentation to understand what was
tested, what was observed, and whether defensive controls changed the outcome.

## Experiment Identification

Each research experiment receives a unique identifier.

Examples:

- RE-001 — Windows PowerShell Logging & Detection
- RE-002 — Windows Credential Protection
- RE-003 — Persistence Detection
- RE-004 — Privilege Escalation Detection
- RE-005 — Lateral Movement Detection

Experiment numbers identify research projects rather than individual commands
or tools.

## Experimental Process

### 1. Research Question

Define the security question being investigated.

Example:

> How does enhanced PowerShell logging affect the visibility of PowerShell
> activity compared with a default Windows configuration?

### 2. Environment

Document the systems involved in the experiment, including:

- Operating system
- Host role
- Relevant security configuration
- Logging configuration
- Security software
- Network placement

### 3. Technique Mapping

Where appropriate, map the behavior under investigation to a recognized
framework such as MITRE ATT&CK.

### 4. Baseline

Document the system's security and logging configuration before additional
hardening controls are introduced.

### 5. Controlled Simulation

Reproduce the behavior being investigated within the authorized laboratory.

The purpose of the simulation is to generate realistic system behavior and
telemetry for defensive analysis.

### 6. Telemetry Collection

Collect relevant evidence such as:

- Windows Event Logs
- Sysmon events
- Microsoft Defender events
- PowerShell logs
- Authentication events
- Process execution information
- Registry activity
- File activity
- Network telemetry

### 7. Analysis

Determine:

- What activity was visible?
- Which telemetry sources captured it?
- Which important behaviors were not visible?
- What indicators or behavioral patterns could support detection?

### 8. Detection Development

Where appropriate, develop detection logic using formats such as:

- Sigma
- SIEM queries
- Windows Event Log queries
- YARA
- Behavioral detection logic

Detection logic should be tested against collected telemetry when practical.

### 9. Hardening

Apply relevant defensive controls.

Examples may include:

- Windows security policy
- Microsoft Defender controls
- Attack Surface Reduction rules
- PowerShell security controls
- Credential protections
- Windows Firewall policy
- Active Directory security controls
- Enhanced auditing

### 10. Retest

Repeat the controlled experiment after defensive controls are introduced.

Compare the hardened results with the baseline.

### 11. Findings

Document:

- Baseline behavior
- Hardened behavior
- Telemetry differences
- Detection results
- Security-control effectiveness
- Limitations
- Additional research opportunities

## Reproducibility

Experiments should document enough environmental information for the test to
be repeated in a comparable laboratory.

Software versions, configuration changes, relevant commands, detection rules,
and assumptions should be recorded where appropriate.

## Limitations

Laboratory results do not necessarily represent every production environment.

Differences in Windows versions, enterprise configurations, security products,
network architecture, identity systems, and organizational policies may
produce different results.

Findings should therefore describe the tested environment rather than claim
universal effectiveness.