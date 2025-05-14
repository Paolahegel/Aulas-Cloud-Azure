# ☁️ Microsoft Azure: Resumos, Anotações e Dicas
Repositório com foco em **resumos essenciais** com foco para a certificação AZ-900, abordando os **conceitos fundamentais de computação em nuvem**, os **principais serviços do Microsoft Azure**, e **dicas práticas** com base em experiências nas aulas e laboratórios.

---

## 🔍 O que é Computação em Nuvem?

Computação em nuvem é a entrega sob demanda de recursos de TI via internet com modelo de pagamento por uso. Exemplos:

* Servidores
* Armazenamento
* Redes
* Banco de Dados
* Software e análise de dados

**Provedores populares:** Microsoft Azure, AWS, Google Cloud.

---

## 🌐 Tipos de Nuvem

* **Pública**: recursos compartilhados, acessíveis pela internet.
* **Privada**: infraestrutura dedicada a uma organização.
* **Híbrida**: combina névoa pública e privada para maior flexibilidade.

---

## 🎯 Benefícios da Nuvem

* Alta disponibilidade
* Elasticidade e escalabilidade
* Agilidade no provisionamento
* Redução de custos com infraestrutura
* Pagamento conforme o uso (OpEx)

## 💸 CapEx vs OpEx

* **CapEx**: investimento inicial (servidores físicos, manutenção)
* **OpEx**: despesas operacionais recorrentes (modelo da nuvem)

---

## ⚙️ Tipos de Serviços em Nuvem

* **IaaS (Infraestrutura como Serviço)**: VMs, redes, discos
* **PaaS (Plataforma como Serviço)**: Azure App Service, bancos de dados
* **SaaS (Software como Serviço)**: Microsoft 365, Outlook, Dynamics

---

## 🔐 Modelo de Responsabilidade Compartilhada

A responsabilidade pela segurança depende do modelo:

| Camada                      | IaaS      | PaaS      | SaaS      |
| --------------------------- | --------- | --------- | --------- |
| Dados                       | Cliente   | Cliente   | Cliente   |
| Sistema operacional         | Cliente   | Microsoft | Microsoft |
| Infraestrutura / datacenter | Microsoft | Microsoft | Microsoft |

---

## 💻 Criação de Máquinas Virtuais (VMs)

### Etapas:

1. Acesse o [Portal Azure](https://portal.azure.com)
2. Navegue até "Máquinas Virtuais" > "Criar"
3. Escolha subscrição, grupo de recurso, nome, SO, tamanho
4. Configure disco, rede e regras de acesso (SSH, RDP)
5. Revise e crie a VM
6. Acesse via SSH (Linux) ou RDP (Windows)

### Recursos:

* 🔁 Dimensionamento automático
* 🔒 Conjuntos de disponibilidade (falha + atualização)

---

## 🗃️ Banco de Dados no Azure
### Criando Azure SQL Database:

1. Portal Azure > Criar recurso > SQL Database
2. Nome, grupo de recurso, servidor SQL
3. Preço e performance (DTUs ou vCores)
4. Regras de firewall para acesso externo
5. Acesse via Azure Data Studio ou SSMS

---

## 🧱 Componentes de Arquitetura do Azure

### 📍 Regiões e Zonas

* Datacenters distribuídos globalmente
* Zonas aumentam resiliência
* Região afeta conformidade legal (LGPD)

### 🔁 Pares de Região

* Backup e recuperação de desastres

### 🧱 Conjuntos de Disponibilidade

* Domínios de falha + domínios de atualização

### 🏛️ Regiões Soberanas

* Azure Governamental (EUA)
* Azure China (21Vianet)

---

## 📦 Recursos e Grupos de Recursos

* Contêiner lógico para organizar recursos
* Um recurso pertence a um grupo
* Possível mover entre grupos

---

## 💼 Assinaturas e Grupos de Gerenciamento

* **Assinaturas**: separa fatura, limites e acesso
* **Grupos de gerenciamento** organizam em larga escala:

```bash
Grupos de Gerenciamento
   └── Assinaturas
         └── Grupos de Recursos
               └── Recursos
```

---

# ☁️ Computação e Rede no Azure

## 💻 VMs e Lift-and-Shift

* Migra aplicações legadas
* Total controle e responsabilidade

## 🖥️ Azure Virtual Desktop

* Acesso remoto via navegador ou app
* Sessões simultâneas e isoladas

## 📦 Contêineres

* PaaS leve e escalável para microserviços
* Menos sobrecarga que VMs

## ⚙️ Azure Kubernetes Service (AKS)

* Orquestração e gerenciamento de contêineres

## ⚡ Azure Functions

* Executa código sob demanda
* Baseado em eventos

## 🛠️ App Service

* PaaS para aplicativos web e APIs
* Suporte a CI/CD, SSL, escalabilidade

## 🌐 VNet e Conectividade

* Isola recursos em rede privada
* Integra com redes locais via:

  * 🔒 VPN Gateway
  * ⚡ ExpressRoute (conexão dedicada)

## 🧭 DNS no Azure

* Integra RBAC, logs, redes personalizadas e domínios privados

---

## 🔐 Identidade, Acesso e Segurança no Azure
🧑‍💼 Microsoft Entra ID (antigo Azure Active Directory)
O Microsoft Entra ID é o serviço de gerenciamento de identidades e acessos baseado em nuvem da Microsoft. Ele oferece:

- Autenticação: valida a identidade dos usuários.

- Autorização: define os níveis de acesso aos recursos após a autenticação.

- Logon único (SSO): permite que os usuários acessem múltiplos aplicativos com uma única autenticação.

- Gerenciamento de dispositivos e aplicativos: controla quais dispositivos e aplicativos podem acessar os recursos.

- Colaboração B2B: permite a colaboração segura com parceiros externos.

- Gerenciamento de senhas: inclui recursos como redefinição de senha self-service.

---

## 🛡️ Métodos de Autenticação
O Entra ID suporta diversos métodos de autenticação para melhorar a segurança:

- Autenticação multifator (MFA): exige uma segunda forma de verificação, como um código enviado ao celular.

- Autenticação sem senha: utiliza métodos como Windows Hello, chaves de segurança FIDO2 ou o aplicativo Microsoft Authenticator.

- Autenticação baseada em certificado: utiliza certificados digitais para autenticar usuários.

- Senha tradicional: ainda suportada, mas recomendada em conjunto com MFA para maior segurança.

---

⚙️ Acesso Condicional e RBAC
- Acesso Condicional: permite aplicar políticas de acesso baseadas em condições específicas, como localização, dispositivo ou risco de login.

- Controle de Acesso Baseado em Função (RBAC): atribui permissões aos usuários com base em suas funções, seguindo o princípio de menor privilégio.

---

## 🧅 Modelo de Segurança em Camadas (Defesa em Profundidade)
A segurança no Azure é estruturada em camadas para fornecer múltiplas barreiras de proteção:

- Dados

- Aplicações

- Computação

- Rede

- Perímetro

- Identidade e Acesso

- Segurança Física

- Essa abordagem garante que, mesmo que uma camada seja comprometida, as outras continuem protegendo os recursos.

---

## 🔍 Microsoft Defender for Cloud
O Microsoft Defender for Cloud é uma plataforma unificada de gerenciamento de segurança que oferece:

- Gerenciamento de postura de segurança na nuvem (CSPM): identifica e corrige configurações inseguras.

- Proteção de cargas de trabalho na nuvem (CWPP): protege servidores, contêineres, bancos de dados e mais.

- Análise de caminhos de ataque: modela o tráfego da rede para identificar riscos potenciais.

- Conformidade regulatória: ajuda a atender padrões como HIPAA, GDPR e PCI DSS.

- Integração multicloud: suporta ambientes Azure, AWS e Google Cloud.

---

## 📎 Documentação oficial:

* [Microsoft Learn – Azure](https://learn.microsoft.com/azure/)
* [Calculadora de Preço do Azure](https://azure.microsoft.com/pricing/calculator/)
* [Microsoft Entra ID - Visão Geral](https://learn.microsoft.com/entra/)
* [Microsoft Defender for Cloud - Visão Geral](https://learn.microsoft.com/azure/defender-for-cloud/)
