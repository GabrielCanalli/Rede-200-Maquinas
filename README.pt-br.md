# Rede-200-Maquinas
Projeto de infraestrutura de rede segmentada para ambiente universitário, focado em segurança de dados e isolamento de tráfego (VLANs) para mais de 400 hosts.

# 🌐 Projeto de Infraestrutura de Rede Universitária (413 Hosts)

Este projeto apresenta a implementação de uma rede de computadores para um ambiente acadêmico e administrativo, focando em **segmentação de tráfego (VLANs)** e **segurança de dados**.

## 📋 Cenário e Requisitos
A rede foi projetada para suportar uma infraestrutura robusta com os seguintes ativos:
* **Setor Administrativo:** 200 Máquinas + 3 Máquinas da Coordenação.
* **Setor Acadêmico:** 9 Laboratórios (180 Máquinas no total).
* **Infraestrutura Wi-Fi:** 20 Access Points distribuídos entre ADM e Acadêmico.
* **Servidores Dedicados:** DHCP, DNS, NTP, Backup, Câmeras, Web, FTP e E-mail.
* **Periféricos:** 5 Impressoras de rede.

## 🔒 Restrição de Segurança
Conforme os requisitos do projeto, foi implementada uma regra de isolamento:
> **Regra:** A rede Administrativa é isolada da rede Acadêmica. O tráfego originado na rede ADM não possui permissão de acesso aos hosts da rede Acadêmica, garantindo a integridade dos dados sensíveis.

## 🛠️ Detalhes Técnicos
* **Segmentação:** Utilização de VLANs para separar os domínios de broadcast.
* **Endereçamento:** Planejamento baseado em VLSM para otimização do espaço de endereçamento IP.
* **Segurança:** Implementação de ACLs (Access Control Lists) para bloqueio de tráfego inter-VLAN.

## 🧪 Como Testar o Projeto
1.  Faça o download do arquivo `.pkt` presente neste repositório.
2.  Abra o arquivo no **Cisco Packet Tracer**.
3.  Selecione um host na **VLAN Administrativa**.
4.  Abra o Desktop > Command Prompt.
5.  Tente realizar um `ping` para um IP da **VLAN Acadêmica**.
6.  **Resultado esperado:** O ping deve retornar "Destination Host Unreachable", confirmando que a restrição de segurança está ativa.

## 🔒 Restrição de Segurança
Conforme os requisitos do projeto, foi implementada uma regra de isolamento:
> *Regra:* A rede Administrativa é isolada da rede Acadêmica. O tráfego originado na rede ADM não possui permissão de acesso aos hosts da rede Acadêmica, garantindo a integridade dos dados sensíveis.

---
### 👤 Autor
**Gabriel Canalli**
*Estudante de Análise e Desenvolvimento de Sistemas (3º Período)*
