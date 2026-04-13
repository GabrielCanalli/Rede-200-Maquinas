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
* <details>
  <summary>📡 Ver imagem dos requisistos </summary>

  ![Requirements-Requisitos](./IMAGENS/Requirements-Requisitos.png)

</details>






<details>
  <summary><strong>📡 VER IMAGEM DOS REQUISITOS</strong></summary>

  <br>

  <p align="center">
    <img src="./images/Requirements-Requisitos.png" width="500">
  </p>

</details>












## 🔒 Restrição de Segurança
Conforme os requisitos do projeto, foi implementada uma regra de isolamento:
> **Regra:** A rede Administrativa é isolada da rede Acadêmica. O tráfego originado na rede ADM não possui permissão de acesso aos hosts da rede Acadêmica, garantindo a integridade dos dados sensíveis.

## 🛠️ Detalhes Técnicos
* **Segmentação:** Utilização de VLANs para separar os domínios de broadcast.
* **Endereçamento:** Planejamento baseado em VLSM para otimização do espaço de endereçamento IP.
* **Segurança:** Implementação de ACLs (Access Control Lists) para bloqueio de tráfego inter-VLAN.

## 🧪 Guia de Testes e Demonstração
Para validar a implementação, siga os passos abaixo no **Cisco Packet Tracer**:

### 1. Validação de Serviços (Servidores)
* **DHCP:** Em qualquer PC, acesse *Desktop > IP Configuration* e selecione **DHCP**. O host deve receber um IP, Gateway e o DNS `[192.168.30.10]` automaticamente.
* **Web (HTTP):** No navegador de qualquer host, digite `www.rede.com` (ou seu domínio configurado). A página deve carregar com sucesso.
* **E-mail:** Utilize o Mail Browser para enviar mensagens entre usuários de diferentes setores.
* **FTP:** No prompt de comando, utilize `ftp [192.168.30.10]` e realize o login para validar o acesso aos arquivos.

### 2. Infraestrutura Wi-Fi e Periféricos
* **Wi-Fi:** Conecte um dispositivo sem fio aos SSIDs de cada setor. Verifique se a autenticação e a navegação estão operacionais.
* **Impressão:** Realize um teste de conectividade (ping) entre as máquinas da coordenação e as impressoras de rede `[192.168.20.205]` (Para um impressora da rede academica) `[192.168.10.201]` (Para um impressora da rede admnistrativa).

### 3. Teste de Restrição de Segurança (ACL)
Este passo valida a regra principal de isolamento do projeto:
1.  Selecione um host na **VLAN Administrativa**.
2.  Abra o **Desktop > Command Prompt**.
3.  Tente realizar um `ping` para um IP da **VLAN Acadêmica**.
4.  **Resultado esperado:** O ping deve retornar **"Destination Host Unreachable"**, confirmando que a ACL está bloqueando o tráfego conforme o requisito.
5.  Tente um `ping` para um host da **mesma VLAN** ou para o **Servidor Web**.
6.  **Resultado esperado:** Sucesso (confirmando que apenas o tráfego proibido está bloqueado).


---
### 👤 Autor
**Gabriel Canalli**
*Estudante de Análise e Desenvolvimento de Sistemas (3º Período)*
