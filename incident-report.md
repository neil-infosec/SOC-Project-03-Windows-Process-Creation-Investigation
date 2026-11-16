# SOC Project 03 – Windows Process Creation Investigation

## Overview

This project demonstrates how to monitor and investigate Windows process creation activity using Security Event ID **4688**.

The investigation was performed on Windows 11 using Event Viewer and PowerShell. A Notepad process was launched through PowerShell, and its process creation event was analysed.

## Objectives

- Enable Windows Process Creation auditing.
- Identify Event ID 4688 in Windows Security logs.
- Analyse process information and parent-child relationships.
- Enable and verify command-line logging.
- Document the investigation and findings.

## Tools Used

- Windows 11
- Windows Event Viewer
- PowerShell
- Windows Registry

## Key Findings

| Attribute | Result |
|---|---|
| Event ID | 4688 |
| Test Process | Notepad.exe |
| Parent Process | powershell.exe |
| Process ID | 0x4d48 |
| Parent Process ID | 0x13f8 |
| Integrity Level | High |
| Command-Line Logging | Enabled |

## Investigation Result

Windows successfully recorded the creation of Notepad.exe and identified PowerShell as its creator process.

The event included process identifiers, token elevation information, integrity level, and command-line information.

The activity was consistent with the controlled lab test. No malicious activity was established from this event alone.

## Skills Demonstrated

- Windows Security Event Log Analysis
- Process Creation Monitoring
- Event ID 4688 Investigation
- PowerShell
- Registry Configuration
- Parent-Child Process Analysis
- SOC Investigation Documentation

## Evidence

See the screenshots included in this repository for the event details and audit configuration.

## Detailed Report

Read [`incident-report.md`](incident-report.md) for the complete investigation report.

---

**Project:** SOC Analyst L1 Home Lab  
**Project Number:** 03  
**Status:** Completed
