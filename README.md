# Basic Employee Onboarding (AD)(RBAC)

## Problem Statement
* Northstar Medical Group's IT environment had been managed for years by an outside MSP with little oversight, resulting in a network that ran on inconsistent, undocumented configurations rather than any defined structure. There was no organizational hierarchy in place; users, departments, and permissions were never separated in any meaningful way, leaving Finance, HR, IT, and Operations staff with overlapping and often inappropriate access to systems and data. Onboarding, offboarding, and access changes were handled manually and inconsistently, with no standardized naming conventions or group-based permissioning, making it nearly impossible to track who had access to what. Given that Northstar handles sensitive patient and employee data, this lack of structure created significant HIPAA compliance risk, as access to protected health information was neither controlled nor auditable. The organization needed a properly structured, documented Active Directory environment built from the ground up to replace the ad hoc setup left behind by the previous MSP.

## Solution Overview
* A new Active Directory domain (NMG.com) was built from scratch on a dedicated domain controller, replacing the previous MSP's undocumented environment with a clean, centrally managed foundation. The domain was structured around four Organizational Units: Finance, HR, IT, and Operations — mirroring the actual business departments, with a corresponding security group in each OU (Finance-Users, HR-Users, IT-Users, Operations-Users) to establish a flat, department-based RBAC model. Rather than managing permissions per individual, access is granted at the group level, reducing administrative overhead and eliminating inconsistent, unaudited permissions. All 15 users were provisioned using a strict, consistent naming convention and placed into the correct OU and security group at creation, removing the manual guesswork that previously left access unmanaged. This same structure made resolving access issues fast and reliable, since a user's OU and group membership clearly show what access they should have. Overall, the design gives Northstar a documented, auditable access model that directly addresses the HIPAA-related risks created by the prior lack of structure.

## Video Walkthrough
https://www.loom.com/share/6502d61cf9d841cfaea6f388adc1afa9

## Tools Used
* Windows Server
* Active Directory Domain Services
* VirtualBox
* UTM
* RBAC
* GitHub

## Project Timeline
* Day 1: Domain creation and domain controller promotion
* Day 2: Organizational unit and security group design
* Day 3: User provisioning and RBAC implementation
* Day 4: Incident response and resolution (NMG-0047)
* Day 5: Documentation and case study packaging

## Key Accomplishments
* Built NMG.com domain from scratch
* Designed and deployed a full Active Directory Domain Services environment (NMG.com) from scratch, including domain controller promotion, DNS configuration, and static IP assignment on a virtualized Windows Server instance.
* Architected a department-based OU and security group structure (Finance, HR, IT, Operations), implementing a flat RBAC model, then provisioned and correctly assigned 15 user accounts following a consistent naming convention.
* Diagnosed and resolved a real-world access control ticket by identifying OU misplacement and incorrect group membership as the root cause, then documented the fix following standard IT resolution/ticketing practices.




