# Rede-200-Maquinas
Projeto de infraestrutura de rede segmentada para ambiente universitário, focado em segurança de dados e isolamento de tráfego (VLANs) para mais de 400 hosts.

# 🌐 University Network Infrastructure (413 Hosts)

This project implements a robust network infrastructure for an academic and administrative environment, focusing on **traffic segmentation (VLANs)** and **data security**.

## 📋 Scenario and Requirements
The network was designed to support a high-scale infrastructure with the following assets:
* **Administrative Sector:** 200 Workstations + 3 Coordination Machines.
* **Academic Sector:** 9 Labs (180 Workstations total).
* **Wi-Fi Infrastructure:** 20 Access Points distributed between ADM and Academic SSIDs.
* **Dedicated Servers:** DHCP, DNS, NTP, Backup, Security Cameras, Web, FTP, and E-mail.
* **Peripherals:** 5 Network Printers.

## 🔒 Security Restriction
Following the project requirements, a strict isolation rule was implemented:
> **Rule:** The Administrative network is isolated from the Academic network. Traffic originating from the ADM network is not allowed to access Academic hosts, ensuring the integrity of sensitive data.

## 🛠️ Technical Details
* **Segmentation:** IEEE 802.1Q (VLANs) used to separate broadcast domains.
* **Addressing:** IP planning based on **VLSM (Variable Length Subnet Masking)** for optimized address space.
* **Security:** Implementation of **ACLs (Access Control Lists)** to block inter-VLAN traffic between restricted zones.

## 🧪 How to Test
1.  Download the `.pkt` file from this repository.
2.  Open the file in **Cisco Packet Tracer**.
3.  Select a host in the **Administrative VLAN**.
4.  Open Desktop > Command Prompt.
5.  Try to `ping` an IP address from the **Academic VLAN**.
6.  **Expected Result:** The ping should return "Destination Host Unreachable", confirming the security restriction is active.

---

# 🌐 Infraestrutura de Rede Universitária (413 Hosts)

Este projeto apresenta a implementação de uma rede de computadores para um ambiente acadêmico e administrativo, focando em **segmentação de tráfego (VLANs)** e **segurança de dados**.

## 📋 Cenário e Requisitos
A rede foi projetada para suportar uma infraestrutura robusta com os seguintes ativos:
* **Setor Administrativo:** 200 Máquinas + 3 Máquinas da Coordenação.
* **Setor Acadêmico:** 9 Laboratórios (180 Máquinas no total).
* **Infraestrutura Wi-Fi:** 20 Access Points distribuídos entre ADM e Acadêmico.
* **Servidores Dedicados:** DHCP, DNS, NTP, Backup, Câmeras, Web, FTP e E-mail.
* **Periféricos:** 5 Impressoras de rede.

## 🔒 Security Restriction
Following the project requirements, a strict isolation rule was implemented:
> **Rule:** The Administrative network is isolated from the Academic network. Traffic originating from the ADM network is not allowed to access Academic hosts, ensuring the integrity of sensitive data.

---
### 👤 Autor / Author
**Gabriel Canalli**
*Systems Analysis and Development Student (3rd Period)*
