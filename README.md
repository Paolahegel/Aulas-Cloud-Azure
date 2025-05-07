# ☁️ Microsoft Azure: Resumos, Anotações e Dicas
Este repositório tem como objetivo centralizar resumos e boas práticas sobre o uso da plataforma de nuvem **Microsoft Azure**, com foco no entendimento de conceitos fundamentais, configuração de serviços e dicas úteis estudados durante o Bootcamp Java Cloud na DIO.

## 🔍 O que é Computação em Nuvem?
Computação em nuvem é a entrega de recursos de TI sob demanda pela internet, com pagamento conforme o uso.
Esses recursos incluem servidores, armazenamento, banco de dados, rede, software, análise e muito mais — tudo isso hospedado em datacenters de grandes provedores como o Amazon Web Service, Microsoft Azure, Google Cloud Platform, entre outros.

## 🌐 Tipos de Nuvem
### Nuvem Pública

Recursos (servidores, armazenamento, etc.) são disponibilizados por um provedor (como Azure) pela internet.

Ex: Hospedar um site ou app no Azure.

### Nuvem Privada

Infraestrutura dedicada a uma única organização, hospedada localmente ou por terceiros.

Oferece mais controle e segurança.

### Nuvem Híbrida

Combina a nuvem pública e privada.

Permite mover dados e aplicações entre ambientes conforme necessário.

---

## 🎯 Principais Vantagens da Computação em Nuvem
Alta disponibilidade: acesso a dados e serviços de praticamente qualquer lugar.

Elasticidade: escalar recursos automaticamente de acordo com a demanda.

Agilidade: provisionamento rápido de recursos.

Modelo de pagamento conforme o uso: paga-se apenas pelo que consome.

Redução de custos com infraestrutura: sem necessidade de comprar servidores físicos.

## 💸 CapEx vs OpEx
CapEx (Capital Expenditure)

Gastos com ativos fixos, como servidores físicos.

É investimento inicial (compra, manutenção, espaço físico etc.).

OpEx (Operational Expenditure)

Gastos operacionais do dia a dia, como assinaturas e serviços de nuvem.

É o modelo da nuvem: você usa e paga pelo serviço, sem precisar investir em hardware.

---

# 🌐 Introdução à Criação de Máquinas Virtuais no Microsoft Azure

Criar máquinas virtuais (VMs) no Microsoft Azure é uma das formas mais comuns de utilizar a computação em nuvem para simular servidores e ambientes operacionais de forma escalável e segura.

## 🚀 O que é uma Máquina Virtual no Azure?

Uma **máquina virtual (VM)** no Azure é um recurso de computação que simula um computador físico, permitindo que você execute sistemas operacionais e aplicativos em um ambiente virtualizado na nuvem.

## 📌 Etapas básicas para criar uma VM no Azure

### 1. Acesse o Portal do Azure  
Vá para [https://portal.azure.com](https://portal.azure.com) e faça login com sua conta Microsoft.

### 2. Crie um novo recurso de Máquina Virtual  
No menu lateral, clique em **"Máquinas Virtuais"** e depois em **"Criar" > "Máquina Virtual"**.

### 3. Configure as opções básicas  
- Selecione a **assinatura** e o **grupo de recursos**.  
- Dê um **nome** à VM.  
- Escolha a **região** de hospedagem (ex: "Brazil South").  
- Selecione a **imagem do sistema operacional** (ex: Ubuntu, Windows Server).  
- Defina o **tamanho da VM** de acordo com os recursos (CPU, RAM).  
- Crie ou selecione **credenciais de acesso** (usuário e senha ou chave SSH).

### 4. Configure o disco e rede  
- Escolha o tipo de disco (geralmente SSD padrão).  
- Configure a **rede virtual** e o **grupo de segurança de rede (NSG)** para definir portas de acesso, como:  
  - Porta 22 (SSH) para Linux  
  - Porta 3389 (RDP) para Windows

### 5. Revise e crie  
- Revise todas as configurações.  
- Clique em **"Criar"** para iniciar a implantação da VM.

### 6. Acesse sua VM  
Após a criação, você pode acessar a VM via:
- **SSH** (Linux):  
  ```bash
  ssh usuario@ip_publico
  
- RDP (Windows):
  ```bash
  Use o cliente de Área de Trabalho Remota com o IP fornecido.

---

## 📚 Tipos de Serviços em Nuvem

### 🔹 IaaS — Infraestrutura como Serviço
- Proporciona recursos básicos de computação, como **máquinas virtuais, armazenamento e redes**.
- Você gerencia o sistema operacional e o software.
- **Exemplo:** Máquinas Virtuais (Azure VM), Discos gerenciados.

### 🔹 PaaS — Plataforma como Serviço
- Fornece uma plataforma completa para desenvolvimento e implantação de aplicativos.
- A Microsoft gerencia a infraestrutura, e você se concentra no código.
- **Exemplo:** Azure App Service, Azure SQL Database.

### 🔹 SaaS — Software como Serviço
- Aplicações prontas para uso, acessadas pela internet.
- O provedor gerencia tudo: infraestrutura, aplicativo e dados.
- **Exemplo:** Microsoft 365, Outlook Web, Dynamics 365.

---

## 🔐 Modelo de Responsabilidade Compartilhada

O modelo de responsabilidade compartilhada define **quais partes da segurança e da gestão são de responsabilidade do cliente e quais são da Microsoft**, dependendo do tipo de serviço utilizado.

| Camada                        | IaaS (VMs) | PaaS (App Service, DB) | SaaS (Microsoft 365) |
|------------------------------|------------|-------------------------|-----------------------|
| Dados                        | Cliente    | Cliente                 | Cliente               |
| Controles de acesso          | Cliente    | Cliente                 | Cliente               |
| Aplicações                   | Cliente    | Cliente                 | Microsoft             |
| Sistema operacional          | Cliente    | Microsoft               | Microsoft             |
| Rede e infraestrutura        | Microsoft  | Microsoft               | Microsoft             |
| Físico (datacenter)          | Microsoft  | Microsoft               | Microsoft             |

---

## 🛠️ Configurando uma Instância de Banco de Dados no Azure

### 📌 Exemplo: Azure SQL Database (PaaS)

1. **Acesse o portal Azure:**  
   [https://portal.azure.com](https://portal.azure.com)

2. **Crie um recurso:**  
   Vá em **"Criar um recurso" > "Banco de Dados" > "SQL Database"**

3. **Preencha os dados:**
   - **Nome do banco de dados**
   - **Grupo de recursos** (crie um novo ou reutilize um existente)
   - **Servidor SQL** (crie um novo: nome, login e senha)
   - **Camada de preço** (Escolha com base em DTUs ou vCores)

4. **Configurações adicionais:**
   - Configure backups automáticos e redundância geográfica se necessário
   - Habilite regras de firewall para acesso externo (incluir IP local)

5. **Revisar e Criar:**
   - Clique em **"Revisar + criar"**
   - Após a validação, clique em **"Criar"**

6. **Acesso ao Banco de Dados:**
   - Use ferramentas como **Azure Data Studio** ou **SQL Server Management Studio (SSMS)** para se conectar
   - Use a string de conexão disponível no portal do Azure
---

## 💡 Dicas Rápidas

- Utilize **tags** nos recursos para facilitar a organização e rastreamento de custos.
- Configure **alertas de custo** para evitar gastos inesperados.
- Use a **Calculadora de Preços do Azure** para planejar antes de criar recursos.
- Sempre revise as configurações de **firewall e acesso à rede** ao expor serviços na nuvem.

---

📎 **Documentação oficial:**  
- [Microsoft Learn – Azure](https://learn.microsoft.com/azure/)
- [Calculadora de Preço do Azure](https://azure.microsoft.com/pricing/calculator/)

# 🌐 Componentes de Arquitetura do Azure

## 📍 Regiões e Zonas de Disponibilidade
- O Azure é distribuído globalmente em **regiões**, compostas por **data centers físicos**.
- **Zonas de disponibilidade** garantem **resiliência** e **baixa latência** para os clientes.
- A **Microsoft** é responsável pela gestão dos hosts (infraestrutura física), mas o cliente deve considerar a **disponibilidade** e a **manutenção** ao planejar soluções.
- Em relação à **LGPD**, a escolha da região impacta diretamente a **residência dos dados** e a **conformidade legal**.

## 🔁 Pares de Regiões
- Cada região possui uma **região par** que atua como **backup automático** para alguns serviços.
- Essa replicação aumenta a **disponibilidade** e a **recuperação de desastres**, embora **não tenha SLA definido**.

## 🛠️ Conjuntos de Disponibilidade
- São compostos por:
  - **Domínios de atualização**: minimizam a indisponibilidade durante atualizações.
  - **Domínios de falha**: distribuem recursos para resistir a falhas físicas.

## 🏛️ Regiões Soberanas
- **Azure Governamental (EUA)**: atende as necessidades de segurança e conformidade de agências federais.
- **Azure China**: instância física separada, operada pela empresa **21Vianet**.

---

## 📦 Recursos e Grupos de Recursos
- Um **grupo de recursos** é um **contêiner lógico** para agrupar e gerenciar recursos relacionados (ex: VMs, bancos de dados, armazenamento, etc).
- Estratégias de organização:
  - Todos os recursos em um único grupo (mais simples, menos escalável).
  - Separação por tipo ou função (mais organizado e escalável).
- Características importantes:
  - Um recurso pertence a **apenas um grupo de recursos**.
  - Pode estar em **diferentes regiões**.
  - Pode ser **movido entre grupos**.
  - **Aplicações** podem utilizar recursos de **vários grupos diferentes**.
  - Organização é essencial para escalabilidade e controle de acesso.

---

## 💼 Assinaturas e Grupos de Gerenciamento

### 🔹 Assinaturas
- Uma conta Azure pode ter **múltiplas assinaturas**, como:
  - Desenvolvimento
  - Testes
  - Produção
- Cada assinatura possui:
  - **Fatura individual**
  - **Limites de cobrança**
  - **Controles de acesso específicos**

### 🔸 Grupos de Gerenciamento
Estrutura para organização em larga escala:
```bash
Grupos de Gerenciamento
    └── Assinaturas
          └── Grupos de Recursos
                └── Recursos

