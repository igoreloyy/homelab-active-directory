# 🏠 Homelab Active Directory com pfSense

## 📌 Visão Geral

Este projeto consiste na implementação de um ambiente corporativo simulado utilizando virtualização com Hyper-V. O objetivo foi reproduzir cenários reais de infraestrutura de TI, incluindo gerenciamento de usuários, políticas de segurança, controle de acesso e segmentação de rede.

O ambiente foi projetado para simular boas práticas utilizadas em empresas, com foco em Active Directory, GPO, firewall e servidor de arquivos.

---

## 🏗️ Arquitetura do Ambiente

### 🔧 Máquinas Virtuais

* **pfSense 2.8.1** – Firewall e roteador da rede
* **Windows Server 2025 (DC)** – Active Directory Domain Services + DNS
* **Windows Server 2025 (FS)** – Servidor de Arquivos
* **2x Windows 11** – Máquinas clientes

### 🌐 Redes Virtuais (Hyper-V)

* **LAN** – Rede dos clientes
* **SERVIDORES** – Rede dos servidores

---

## 🌐 Topologia da Rede

<img width="321" height="571" alt="topologia-rede" src="https://github.com/user-attachments/assets/ea0377ec-8e76-4729-bbf7-f2bc9c3460b2" />

---

## 🔐 Serviços Implementados

### 🧩 Active Directory

* Criação do domínio: homelab.local
* Gerenciamento centralizado de usuários e grupos
* Organização lógica via Active Directory

### 📜 Group Policy (GPO)

* Aplicação de wallpaper corporativo
* Mapeamento automático de unidades de rede por grupo
* Política de senha configurada na GPO padrão do domínio:

  * Requisitos de complexidade
  * Tamanho mínimo de senha
  * Expiração de senha

### 📁 Servidor de Arquivos

* Compartilhamento de pastas na rede
* Controle de acesso baseado em grupos do AD
* Permissões NTFS configuradas

### 🔥 Firewall / Rede (pfSense)

* Segmentação de rede entre clientes e servidores
* Controle de tráfego entre redes
* Gerenciamento central de conectividade
* Utilização de serviço DHCP via endereço MAC

---

## 👥 Controle de Acesso

Os usuários foram organizados em grupos dentro do Active Directory, permitindo:

* Controle de acesso a pastas compartilhadas
* Aplicação de políticas específicas via GPO
* Mapeamento automático de drives conforme grupo do usuário

---

## ⚙️ Tecnologias Utilizadas

* Hyper-V
* Windows Server 2025
* Windows 11
* pfSense 2.8.1

---

## 📸 Evidências do Projeto

* Usuários e grupos no Active Directory
* GPOs configuradas
* Wallpaper aplicado nos clientes
* Unidade de rede mapeada automaticamente
* Permissões NTFS no servidor de arquivos
* Dashboard do pfSense
* Testes de conectividade (ping entre redes)

---

## 🚀 Objetivos do Projeto

* Consolidar conhecimentos em infraestrutura de TI
* Praticar administração de Active Directory
* Implementar políticas de segurança corporativas
* Simular ambiente real de rede empresarial

---

## 🧠 Aprendizados

Durante este projeto, foram desenvolvidas habilidades em:

* Administração de usuários e grupos no AD
* Criação e aplicação de GPOs
* Gerenciamento de permissões NTFS
* Segmentação de rede e firewall
* Troubleshooting de autenticação e rede

---

## 🔗 Possíveis Melhorias Futuras

* Backup automatizado
* Monitoramento de rede
* Criação de mais OUs (RH, TI, Financeiro)
* Hardening de segurança

---

## 📎 Autor

Projeto desenvolvido por Igor Eloy Kloch Correa

---

## ⭐ Observação

Este homelab foi desenvolvido com fins educacionais e para aprimoramento profissional na área de suporte e infraestrutura de TI.

