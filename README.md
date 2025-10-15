# Network-Design-Proposal

[![Group: 6](https://img.shields.io/badge/Group-6-blue)](https://github.com/Group6/INFO6033-NDP)  
[![Course: INFO6033](https://img.shields.io/badge/Course-INFO--6033-green)](Network Design Proposal.pdf)  
[![Submitted: Fall 2024](https://img.shields.io/badge/Submitted-Fall%202024-yellow)](Network Design Proposal.pdf)

This repository contains the Network Design Proposal for North American Widget Inc. (NAWI), developed by Group 6 for INFO6033 in Fall 2024. The PDF outlines the integration of GCWC (Canada) and GAWC (US) networks post-merger, featuring SD-WAN/SDN solutions, Zero Trust security, cloud strategies, failover designs, VPN setups, and future expansion plans. Created for educational purposes with fictional merger details.

**Key Themes**: Post-merger network integration, OpenDaylight SD-WAN, spine-leaf architecture, Zero Trust, public/private clouds, BGP failover, SNMP management, and scalability. Highlights 30% revenue growth and NIST alignment.

## Abstract

This proposal integrates GCWC and GAWC networks into NAWI, dividing operations into five regions. It details current tiered/modular setups, proposes SDN datacenter designs with automation benefits, cloud connectivity, Zero Trust security, failover mechanisms, SNMP ROI, VPN for remote access, and expansion potential. Aimed at boosting efficiency and preparing for European growth.

## Table of Contents

- [Executive Summary](#executive-summary)
- [GCWC Environment](#gcwc-environment)
- [GAWC Environment](#gawc-environment)
- [Current Environment](#current-environment)
  - [Modularized Branch, Regional and Datacenters](#modularized-branch-regional-and-datacenters)
  - [Tiered Hierarchical Design in Canada](#tiered-hierarchical-design-in-canada)
  - [Purpose and ROI for the Network Management module (SNMP)](#purpose-and-roi-for-the-network-management-module-snmp)
- [Proposed Solution](#proposed-solution)
  - [Network Changes in Both Countries](#network-changes-in-both-countries)
  - [How Networks will be Integrated](#how-networks-will-be-integrated)
  - [SDN Datacenter design and its Benefits to NAWI](#sdn-datacenter-design-and-its-benefits-to-nawi)
  - [Public and Private Clouds for Canada and the US](#public-and-private-clouds-for-canada-and-the-us)
  - [How the connectivity will function, between countries, sites, and SD-WAN](#how-the-connectivity-will-function-between-countries-sites-and-sd-wan)
  - [How Zero trust provide additional Security](#how-zero-trust-provide-additional-security)
  - [Fail-over Design](#fail-over-design)
  - [Network Management Implementation](#network-management-implementation)
  - [VPN Design for Offices and Remote Personnel](#vpn-design-for-offices-and-remote-personnel)
  - [Ability for Future Expansion](#ability-for-future-expansion)
- [Conclusion](#conclusion)
- [References](#references)
- [Key Concepts and Tools](#key-concepts-and-tools)
- [Best Practices Learned](#best-practices-learned)
- [Ethics and Challenges](#ethics-and-challenges)
- [Authors](#authors)
- [License](#license)
- [How to View/Download](#how-to-viewdownload)

## Document Overview

### Cover Page
**Objective and Explanation**: Introduces the project for INFO6033 Fall 2024, listing Group 6 members, roles (PM, Visio, research, presentation, change requests), and approvals.  
**Key Details**: Fictional merger context for educational simulation.  
**Broader Insight**: Highlights team collaboration in network design.

### Table of Contents
**Objective and Explanation**: Outlines sections from Executive Summary to References with page references for navigation.  
**Key Details**: Structured for comprehensive review.  
**Broader Insight**: Aids in accessing key proposal elements.

### Executive Summary
**Objective and Explanation**: Overviews merger benefits (30% revenue increase), regional divisions, SD-WAN/Zero Trust cost savings, IT integration priorities, and Europe expansion potential.  
**Key Details**: Canadian operations retained; SDN for agility; 2-year app consolidation.  
**Broader Insight**: Sets strategic direction for unified network.

## GCWC Environment
**Objective and Explanation**: Describes GCWC’s tiered structure with Toronto HQ/data center, Markham backup, and regional offices (Southwestern, Central, Western, Atlantic) using SD-WAN and VLANs.  
**Key Details**: Centralized connectivity in Canada.  
**Broader Insight**: Leverages existing infrastructure.

## GAWC Environment
**Objective and Explanation**: Details GAWC’s US networks with Dallas HQ, Boston Eastern, Chicago Central, San Francisco Western, transitioning from Frame Relay to SD-WAN.  
**Key Details**: Prepares for alignment with GCWC.  
**Broader Insight**: Addresses legacy system upgrades.

## Current Environment
### Modularized Branch, Regional and Datacenters
**Objective and Explanation**: Segregates GCWC/GAWC networks into manageable modules for policy application and scalability.  
**Key Details**: Enhances monitoring and growth capacity.  
**Broader Insight**: Supports efficient management.

### Tiered Hierarchical Design in Canada
**Objective and Explanation**: Uses core, distribution, and access layers for efficiency and security in Toronto/Markham.  
**Key Details**: Structured for troubleshooting.  
**Broader Insight**: Optimizes layered operations.

### Purpose and ROI for the Network Management module (SNMP)
**Objective and Explanation**: Implements SNMP for real-time monitoring via OpenDaylight, reducing downtime and costs.  
**Key Details**: Automates alerts and resource optimization.  
**Broader Insight**: Improves IT reliability.

## Proposed Solution
### Network Changes in Both Countries
**Objective and Explanation**: Migrates from Frame Relay to OpenDaylight SD-WAN, deploying SDN, spine-leaf topology, and Cisco hardware with cross-DC mirroring.  
**Key Details**: Toronto renamed Northern Region; Markham as Dallas backup.  
**Broader Insight**: Enhances scalability and efficiency.

### How Networks will be Integrated
**Objective and Explanation**: Uses OpenDaylight SDN with Azure ExpressRoute and IPSec VPN for seamless Canada-US connectivity.  
**Key Details**: Centralized management approach.  
**Broader Insight**: Ensures unified operations.

### SDN Datacenter design and its Benefits to NAWI
**Objective and Explanation**: Implements spine-leaf architecture with OpenDaylight for automation, scalability, and security.  
**Key Details**: Vendor-neutral with community support.  
**Broader Insight**: Future-proofs infrastructure.

### Public and Private Clouds for Canada and the US
**Objective and Explanation**: Utilizes Dallas private cloud, Toronto unchanged, and Azure public for scalability with data residency compliance.  
**Key Details**: Regional data management.  
**Broader Insight**: Balances control and regulation.

### How the connectivity will function, between countries, sites, and SD-WAN
**Objective and Explanation**: Employs NETCONF, BGP, and mesh networks for low-latency global traffic.  
**Key Details**: Azure ExpressRoute with QoS policies.  
**Broader Insight**: Ensures redundant connectivity.

### How Zero trust provide additional Security
**Objective and Explanation**: Applies "Never Trust, Always Verify" with IAM (MFA, RBAC) and microsegmentation via Palo Alto NGFW.  
**Key Details**: AES/TLS encryption and monitoring.  
**Broader Insight**: Limits breach risks.

### Fail-over Design
**Objective and Explanation**: Uses clustered OpenDaylight and BGP auto-rerouting for redundancy between Markham and Dallas.  
**Key Details**: Full-mesh spine-leaf setup.  
**Broader Insight**: Minimizes downtime.

### Network Management Implementation
**Objective and Explanation**: Centralizes via OpenDaylight with NETCONF, SNMP, and Grafana for monitoring.  
**Key Details**: Cisco integration included.  
**Broader Insight**: Streamlines operations.

### VPN Design for Offices and Remote Personnel
**Objective and Explanation**: Deploys Palo Alto Global Protect for remote and site-to-site VPNs with Panorama management.  
**Key Details**: IPSec encryption ensured.  
**Broader Insight**: Secures distributed access.

### Ability for Future Expansion
**Objective and Explanation**: Plans WAN edge routers for Europe with NETCONF auto-config.  
**Key Details**: Supports plug-and-play growth.  
**Broader Insight**: Enables dynamic scalability.

## Conclusion
**Objective and Explanation**: Highlights SDN/Zero Trust benefits, addressing challenges with phased pilots and training.  
**Key Details**: Enhances security and flexibility.  
**Broader Insight**: Positions NAWI for digital growth.

## References
**Objective and Explanation**: Cites Cisco, Microsoft, and SDN research papers.  
**Key Details**: Ensures credible support.  
**Broader Insight**: Aligns with industry standards.

## Key Concepts and Tools
- **Architectures**: SD-WAN, SDN (OpenDaylight), spine-leaf, tiered hierarchical.
- **Protocols/Tools**: NETCONF, SNMP, BGP, IPSec, Azure ExpressRoute, Palo Alto NGFW.
- **Security**: Zero Trust, microsegmentation, AES/TLS.
- **Clouds**: Azure public/private.
- **Hardware**: Cisco 8000 Routers/Catalyst Switches.

## Best Practices Learned
- **Integration**: Phased migrations, centralized control.
- **Security**: Least privilege, continuous monitoring.
- **Failover**: Active redundancy, auto-rerouting.
- **Management**: Automation, metrics visualization.
- **Expansion**: Plug-and-play configs.

## Ethics and Challenges
- **Challenges**: Integration complexity, hardware compatibility.
- **Ethics**: Fictional scenarios only; focus on education.
- **Overcoming**: Phased approach, stakeholder alignment.

## Authors
- **Group 6**: Sunshine Cotejo (1140357), Aashish KC (1164325), Saiganesh Jeyapandi (1154547), Ahmad Malkawi (1171774)
- Semester: Fall 2024
- Contact: Update with emails if sharing.

## License
Academic work under MIT License - see [LICENSE](LICENSE) for details. Free to view/fork for learning; no commercial redistribution.

## How to View/Download
- **PDF**: Use Adobe Reader or online viewers.
- **File**: [Download PDF](Network Design Proposal.pdf). Folder: root/. Last updated: 15 October 2025.

--- 

Let me know if you need further adjustments!
