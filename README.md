# 🖥️ Windows Server Administration Homelab

A hands-on Windows Server homelab built using Oracle VirtualBox to practice administration in a simulated enterprise environment.

The lab uses DC01 as the domain controller for `InfiniteVoid.local` and PC01 as a Windows 11 client. The project is archived at its current scope: the completed work and its evidence are documented in Phases 1–4. No further phases are planned.

**Start here:** [Prerequisites](Documentation/Prerequisites.md) → [Phase 1](Documentation/phase1.md) → [Phase 2](Documentation/phase2.md) → [Phase 3](Documentation/phase3.md) → [Phase 4](Documentation/phase4.md)

## Contents

* [Lab environment](#lab-environment)
* [Completed work](#completed-work)
* [Repository structure](#repository-structure)
* [Skills practiced](#skills-practiced)
* [Scope and limitations](#scope-and-limitations)

## Lab Environment

| Component | Technology / configuration |
| --- | --- |
| Virtualization | Oracle VirtualBox |
| Server OS | Windows Server 2025 Evaluation |
| Client OS | Windows 11 Enterprise Evaluation |
| Domain | `InfiniteVoid.local` |
| Domain controller | `DC01` |
| Client | `PC01` |
| Network | NAT Network |
| DC01 IP / preferred DNS | `10.0.3.10` |
| Subnet mask | `255.255.255.0` |
| Default gateway | `10.0.3.1` |

The Server 2025 download is confirmed by the saved Phase 1 screenshot and matches the prerequisites and Phase 2 notes.

## Completed Work

Phases 1–4 are recorded as complete for their documented scopes. Phase 3 includes evidence of effective domain policy, password reset acceptance/rejection, and actual test-account lockout. Group Policy work spans the original phase plan, so the phases describe documented work rather than a strict build sequence.

| Phase | Scope | Status / documentation |
| --- | --- | --- |
| 1 | VM installation, networking, and connectivity | [Complete](Documentation/phase1.md) |
| 2 | AD DS, domain controller promotion, and DNS installation | [Complete](Documentation/phase2.md) |
| 3 | OUs, users, groups, and initial Group Policy validation | [Complete](Documentation/phase3.md) |
| 4 | Client setup walkthrough, network/domain checks, and domain-session evidence | [Complete](Documentation/phase4.md) |

Client installation is covered in Phase 1. Phase 3 includes domain-user testing and PC01 organization. Phase 4 documents the rename and domain-join procedure for reproducing the setup and verifies the existing client configuration. These phases overlap in scope and are presented as a record of the work completed.

Download resources are listed in [Prerequisites](Documentation/Prerequisites.md). Screenshots are stored by phase in [Screenshots](Screenshots/).

View the Windows client evidence in [Phase 4 screenshots](Screenshots/phase4/).

## Repository Structure

```text
WindowsAdminProjects/
├── Documentation/
│   ├── Prerequisites.md
│   ├── phase1.md
│   ├── phase2.md
│   ├── phase3.md
│   └── phase4.md
├── Screenshots/
│   ├── phase1/
│   ├── phase2/
│   ├── phase3/
│   └── phase4/
└── README.md
```

Windows installation ISOs are not included in this repository.

## Skills Practiced

* Virtual machine setup and Windows networking
* Windows Server installation and administration
* Active Directory Domain Services deployment with DNS
* Active Directory Users and Computers (ADUC)
* Organizational unit, user, and security group administration
* Initial Group Policy configuration
* PowerShell commands for Active Directory verification
* Technical documentation and troubleshooting

The repository does not include shared-folder administration, NTFS permission testing, or reusable PowerShell automation. Verification commands used in the lab are documented in Phase 3.

## Scope and Limitations

* Phase 1 does not record VM hardware allocations, the NAT Network name, or its DHCP range.
* Phase 4 includes a reproduction guide; historical screenshots of the original client rename/join wizard are unavailable.
* Phase 4 records successful forward DNS resolution, an initial timeout of unconfirmed cause, and an unavailable reverse lookup. It does not claim these DNS observations were repaired.

This repository is an educational record of the completed lab work. Its status does not imply that unlisted Windows Server features or future improvements have been implemented.
