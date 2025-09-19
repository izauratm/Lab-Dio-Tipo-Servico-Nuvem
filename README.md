# ☁️ Resumo do Lab: Configurando uma instância de Banco de Dados com Microsoft Azure AZ-900
Este repositório reúne os principais aprendizados adquiridos durante o laboratório de **Configurando uma instância de Banco de Dados na Azure** da plataforma [DIO.me](https://web.dio.me), Módulo 1, do qual estou atualmente participando.
O foco está nos benefícios e aplicações práticas da plataforma Microsoft Azure, explorando seus recursos e funcionalidades.
O Bootcamp oferece uma base sólida em tecnologias de nuvem, abordando desde os conceitos fundamentais até os componentes essenciais da arquitetura Azure. Entre os temas estudados estão: criação e gerenciamento de máquinas virtuais, configuração de bancos de dados e soluções de armazenamento, além de tópicos avançados como arquitetura em nuvem, governança, monitoramento e segurança de ambientes cloud. 

---

## 📘 Tópicos Abordados

### 🌐 Introdução à Nuvem e à Azure

A computação em nuvem é a entrega de serviços de computação, incluindo servidores, armazenamento, bancos de dados, redes, software, análise e inteligência, pela internet (a "nuvem"). O Microsoft Azure é uma plataforma de nuvem robusta, oferecendo uma vasta gama de serviços para atender a diversas necessidades.

### 🌦️ Tipos de Serviços de Nuvem

Compreender os modelos de serviço é fundamental para escolher a solução correta para seu projeto.

* **IaaS (Infrastructure as a Service):**
    * **O que é:** Azure fornece a infraestrutura (VMs, rede, armazenamento).
    * **Sua responsabilidade:** Gerenciar o SO, aplicações, segurança, patches.
    * **Exemplo:** Criar uma Máquina Virtual (VM) e instalar o SQL Server nela.

* **PaaS (Platform as a Service):**
    * **O que é:** Azure fornece uma plataforma completa (SO, middleware, ferramentas).
    * **Sua responsabilidade:** Focar no código da aplicação e nos dados.
    * **Exemplo:** Usar o **Azure SQL Database**, que é a nossa principal abordagem neste guia. A Azure gerencia o servidor, você gerencia o banco de dados.

* **SaaS (Software as a Service):**
    * **O que é:** Software pronto para uso, gerenciado e hospedado pela Azure.
    * **Sua responsabilidade:** Apenas usar o serviço.
    * **Exemplo:** Microsoft 365, Dynamics 365, OneDrive.

### 🔐 Modelo de Responsabilidade Compartilhada

No Azure, a segurança é uma parceria.

* **Responsabilidade da Azure (Segurança "da" Nuvem):**
    * Segurança física dos data centers.
    * Segurança da infraestrutura de rede e hardware.
    * Garantia de que os serviços básicos estão operacionais.

* **Responsabilidade do Usuário (Segurança "na" Nuvem):**
    * Gerenciamento de identidades e acessos (IAM).
    * Segurança dos dados e da sua criptografia.
    * Configuração do firewall e das regras de rede.
    * Segurança das aplicações.
 
📄 Exemplo: ao usar Azure SQL Database (PaaS), a Microsoft gerencia o sistema operacional e o banco, mas você é que deve configurar as regras de firewall, autenticação e criptografia.

**Anotação:** Em um serviço PaaS como o **Azure SQL Database**, a responsabilidade do usuário se concentra principalmente na segurança dos dados e no controle de acesso.

### 📌 Guia de Configuração: Azure SQL Database

Este guia detalha os passos para criar uma instância de banco de dados PaaS no Azure.

#### **Passo 1: Criar uma Instância do Azure SQL Database**

1.  Acesse o **Portal do Azure**.
2.  Clique em "Criar um recurso" e procure por **"Azure SQL Database"**.
3.  Selecione "Criar".
4.  Preencha os detalhes:
    * **Grupo de Recursos:** Crie um novo ou use um existente para organizar seus recursos.
    * **Nome do Banco de Dados:** Escolha um nome exclusivo.
    * **Servidor:** Crie um novo servidor para hospedar o seu banco de dados. Defina o nome do servidor, o login de administrador e a senha. **Guarde essas credenciais!**

#### **Passo 2: Configurar o Firewall do Servidor**

1.  Após a criação, navegue para o recurso do servidor SQL que acabou de criar.
2.  No menu lateral, vá para **"Rede"**.
3.  Em "Regras de Firewall", adicione seu endereço IP atual. Isso permite que você se conecte ao banco de dados a partir do seu computador.
4.  Clique em "Salvar".

#### **Passo 3: Conectar ao Banco de Dados**

1.  Use uma ferramenta de gerenciamento como o **SQL Server Management Studio (SSMS)** ou o **Azure Data Studio**.
2.  No SSMS, clique em "Conectar" -> "Database Engine".
3.  **Nome do Servidor:** Copie o nome do servidor do Azure (ex: `seunomeservidor.database.windows.net`).
4.  **Autenticação:** Selecione "SQL Server Authentication".
5.  **Login:** Use o nome de login de administrador que você definiu.
6.  **Senha:** Use a senha que você definiu.
7.  Clique em "Conectar".

#### **Passo 4: Gerenciar e Implementar**

Pronto! Agora ja pode criar tabelas, importar dados e gerenciar seu banco de dados diretamente da ferramenta de gerenciamento.
#### **Previsão de Custo** 
* Há uma previsão dos custos ao criar um banco de dados no Azure na tela de "Computação + Armazenamento" ou "Configurar Banco de Dados" durante o processo de criação.
1. Inicie a Criação do Recurso: No portal do Azure, clique em "Criar um recurso" e selecione a opção de banco de dados que deseja, como "Azure SQL Database".
2. Acesse a Seção de "Computação + Armazenamento": Após preencher os detalhes básicos (como nome do banco de dados e servidor), será direcionado para uma tela que geralmente se chama "Computação + Armazenamento" ou "Configurar Banco de Dados".
3. Explorando as opções de preços: as seguintes configurações impactam diretamente no custo = modelo da compra, nível do serviço e configuração do hardware.
---
## ✅ Conclusão

Este repositório consolidou os principais conceitos e práticas relacionados à criação e configuração das instâncias de banco de dados na plataforma Microsoft Azure: os modelos de serviço em nuvem (IaaS, PaaS e SaaS), destacando as principais diferenças e  suas aplicações práticas; 
o modelo de responsabilidade compartilhada, essencial para compreender os limites e deveres de segurança entre o usuário e o provedor bem como criar uma instância de banco de dados SQL.
Este material serve como apoio para quem está iniciando na jornada de computação em nuvem com Azure, oferecendo uma base sólida para futuras aplicações, certificações ou projetos profissionais.
> Este conteúdo faz parte do projeto **Configurando uma instância de Banco de Dados na Azure - Laboratório** da plataforma DIO.me.

---
 
### 📚 Recursos Complementares
- [Início Rápido: criar Instância Gerenciada de SQL do Azure](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)
- [Tutorial oficial para criar e gerenciar VMs Windows](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/tutorial-manage-vm)
- [Guia rápido para criar instância gerenciada de SQL](https://learn.microsoft.com/pt-br/azure/azure-sql/managed-instance/instance-create-quickstart?view=azuresql&tabs=cli)
- [SQL do Azure para Iniciantes](https://learn.microsoft.com/pt-br/shows/azure-sql-for-beginners/)
- [O que é o Banco de Dados SQL do Azure?](https://learn.microsoft.com/pt-br/azure/azure-sql/database/sql-database-paas-overview?view=azuresql)

📎 Link do curso: [Microsoft Azure AZ-900 - DIO.me](https://web.dio.me/track/microsoft-azure-az-900)
