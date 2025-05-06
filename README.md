# Introdução a Cloud Compunting (Azure Fundamentals) ☁️

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

