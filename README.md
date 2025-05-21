# ☁️ Microsoft Azure: Resumos do Bootcamp
Repositório com foco em **resumos essenciais** com foco para a certificação AZ-900, abordando os **conceitos fundamentais de computação em nuvem**, os **principais serviços do Microsoft Azure**, e **dicas práticas** com base em experiências nas aulas e laboratórios.

---

🔍 O que é Computação em Nuvem?

Computação em nuvem é a entrega sob demanda de recursos de TI via internet com modelo de pagamento por uso. Exemplos:

* Servidores
* Armazenamento
* Redes
* Banco de Dados
* Software e análise de dados

**Provedores populares:** Microsoft Azure, AWS, Google Cloud.


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

# 🧠 Conceitos Fundamentais de IA no Azure

A Inteligência Artificial é a capacidade de sistemas computacionais de simular comportamentos humanos, como:

- **Prever resultados** com base em dados históricos.
- **Reconhecer padrões** e eventos anormais.
- **Tomar decisões autônomas** baseadas em dados.
- **Interpretar informações visuais**, textos e fala de forma automatizada.

---

## ⚙️ Cargas de Trabalho com IA no Azure

### 🔍 Machine Learning
- Foca na **criação de modelos preditivos** a partir de dados históricos.
- Utiliza estatísticas e algoritmos para prever comportamentos futuros.
- Requer dados passados para treinar modelos que ajudem na tomada de decisão.

### 👁️ Visão Computacional
- Capacidade da IA de **interpretar imagens, vídeos e transmissões ao vivo**.
- Utilizada para identificar objetos, pessoas, gerar legendas e insights visuais.
- Exemplo: reconhecimento facial, leitura de placas, análise de raio-X.

### 🗣️ Processamento de Linguagem Natural (NLP)
- Permite que o computador **entenda e interprete linguagem humana**, falada ou escrita.
- Aplicações incluem **análise de sentimentos, resposta a perguntas, tradução e transcrição**.
- Utiliza recursos como o **Azure Speech Studio** e **Language Studio**.

### 📄 Inteligência de Documentos
- IA aplicada ao **gerenciamento e extração de informações de documentos**.
- Valida, interpreta e organiza os dados contidos em documentos digitalizados.
- Exemplo: automação de formulários, leitura de contratos.

### ⛏️ Mineração do Conhecimento
- Processo em três etapas:
  1. **Ingestão** de conteúdo e dados.
  2. **Enriquecimento** com padrões, modelos e insights.
  3. **Exploração** para uso prático das informações.
- Foco em organização, acessibilidade e aplicabilidade do conhecimento.

### 🤖 IA Generativa
- Capaz de **criar imagens, textos, códigos, vídeos e mais**, imitando comportamento humano.
- Usa **grandes massas de dados** para gerar conteúdos de forma criativa e natural.
- Exemplos: ChatGPT, DALL·E, Copilot, Azure OpenAI Service.

---

## 🛡️ Princípios da IA Responsável

### ⚖️ Imparcialidade
- Evitar **viés e discriminação** com base em raça, gênero ou outros grupos.

### 🔐 Confiabilidade e Segurança
- As soluções de IA devem ser **previsíveis, controláveis e seguras**, respeitando normas técnicas.

### 🛡️ Privacidade e Segurança de Dados
- Garantir que os dados pessoais estejam **seguros, protegidos e acessíveis apenas a quem for autorizado**.
- Práticas incluem auditorias, políticas de coleta e controle de acesso.

### 🌍 Inclusão e Transparência
- A IA deve **funcionar para todos**, e os usuários precisam **confiar nos processos automáticos**.

### 👤 Responsabilidade
- Deve haver **clareza sobre quem responde por decisões automatizadas** tomadas por soluções de IA.

---

## 📊 Tipos de Modelos Preditivos

### 📉 Regressão
- Modelo supervisionado onde o **rótulo previsto é um valor numérico contínuo**.
- Exemplo: previsão de vendas, temperatura, lucro.

### ✅ Classificação Binária
- Define se uma observação pertence ou não a uma determinada classe.
- Exemplo: detectar se um e-mail é **spam ou não spam**.

---

## 🧬 Recursos e Ferramentas de NLP no Azure

### 🧠 NLP (Natural Language Processing)
- Ferramentas para **entender, analisar e gerar linguagem natural**.

### 📊 Análise de Sentimentos e Perguntas/Respostas
- Identifica **emoções em textos** ou fornece **respostas automáticas a perguntas** com base no conteúdo analisado.

### 🎤 Texto para Fala / Fala para Texto / Tradução
- Utiliza o **Azure Speech Studio** para converter áudio em texto, texto em fala ou traduzir conteúdo automaticamente.

### 🤖 Azure Bot Service
- Criação de **bots inteligentes** que respondem a dúvidas e interações com o usuário.
- Identifica **intenção, entidade e contexto** para responder com assertividade.

### 🧠 Compreensão de Linguagem Coloquial
- Identifica e interpreta **declarações informais ou contextuais**.
- Baseia-se na tríade:
  - **Declaração**: o que o usuário quer.
  - **Entidade**: sobre o que se refere.
  - **Intenção**: o que o usuário espera como resultado.

---

## 🧭 Ferramentas Azure para IA

- **Azure Machine Learning**
- **Azure Cognitive Services**
- **Azure OpenAI**
- **Azure Bot Service**
- **Azure Language Studio**
- **Azure Speech Studio**

---

# Azure Cognitive Search com AI Search

O **Azure Cognitive Search** é um serviço de pesquisa na nuvem da Microsoft que permite criar experiências de busca enriquecidas em seus aplicativos, utilizando inteligência artificial para **indexar**, **analisar** e **consultar dados estruturados e não estruturados**. Utiliza **técnicas de IA para transformar dados em informações pesquisáveis**.

---

## 🔍 Conceitos-Chave

### ✅ Indexação de Dados

- **Índice**: estrutura que armazena e organiza dados pesquisáveis.
- **Indexador**: componente que extrai dados de uma fonte (ex: Azure SQL Database, Blob Storage).
- **Pipeline de Enriquecimento Cognitivo**:
  - Usa **Cognitive Skills** (como OCR, análise de sentimentos e extração de entidades).
  - Permite transformar dados brutos em informações pesquisáveis com IA.

### ✅ Consulta de Dados

- Os dados indexados podem ser consultados usando **queries** baseadas em texto.
- Suporte a filtros, ordenações, ranking de relevância e análise linguística.
- Integração com APIs RESTful ou SDKs (ex: .NET, Python, Java).

---

## 🧩 AI Search com Cognitive Skills

As **Cognitive Skills** são modelos de IA que enriquecem o conteúdo durante o processo de indexação, como:

- **Reconhecimento de Imagem (OCR)** para extrair texto de imagens.
- **Detecção de Sentimentos** em textos.
- **Extração de Frases-Chave e Entidades Nomeadas**.

Essas habilidades podem ser combinadas em um **pipeline de enriquecimento**, permitindo que dados não estruturados se tornem pesquisáveis.

---

## 🧠 Casos de Uso Comuns

- Busca em documentos PDF, imagens digitalizadas ou arquivos de áudio transcritos.
- Construção de sistemas de FAQ inteligentes.
- Indexação de grandes volumes de conteúdo de suporte ao cliente.

---

# 🧠 IA Generativa no Azure

A **Inteligência Artificial Generativa** simula o comportamento humano com base em aprendizado de máquina, permitindo que a IA interaja com o ambiente e execute tarefas **sem instruções explícitas**.

### Características:
- Interação natural com máquinas
- Curva de aprendizado rápida e prática
- Modelos baseados em linguagem natural

---

## 🤝 Copilotos: Assistência Inteligente em Ações Comuns

**Copilotos** são funcionalidades baseadas em IA integradas a aplicativos como Word, Excel, GitHub, etc., que ajudam usuários a realizar tarefas com maior eficiência.

### O que eles fazem:
- Fornecem suporte inteligente baseado em contexto
- Ajudam com tarefas como escrita, programação e análise
- Enviam prompts para LLMs e retornam conteúdo útil

### Exemplo de uso:
- No GitHub Copilot, completar código automaticamente com base no contexto já escrito.
- No Word, gerar um relatório com base em tópicos ou anotações brutas.

---

## ✍️ Engenharia de Prompts

**Engenharia de prompts** é a prática de estruturar comandos (prompts) para obter as melhores respostas da IA.

### Boas práticas:
- Use **linguagem direta**: seja claro e objetivo
- Forneça **contexto** e **exemplos**
- Utilize **mensagens de sistema** para moldar o comportamento da IA (ex: chatbot)
- Alimente a IA com **dados de fundamentação**

---

## 🧠 Modelos de Linguagem de Grande Escala (LLMs)

Os **LLMs** são a base da IA Generativa e permitem tarefas de **Processamento de Linguagem Natural (PLN)**.

### Aplicações:
- Análise de sentimentos
- Classificação e resumo de textos
- Comparação semântica entre textos
- Geração de linguagem natural

---

## ⚙️ Como funcionam os LLMs?

### 1. **Tokenização**
- Quebra do texto em blocos (tokens)
- Cada palavra ou parte dela é associada a um valor

### 2. **Inserções**
- As relações entre tokens são representadas como vetores
- A IA "encaixa" tokens para gerar algo com sentido

### 3. **Atenção**
- A técnica de atenção avalia o grau de importância entre tokens
- Usa probabilidades para prever o que deve vir a seguir

---

## 🔄 Modelos Transformadores

### Transformador 1:
- **Codificador**: cria representações semânticas do vocabulário
- **Decodificador**: gera novas sequências de linguagem

### Transformador 2:
- Usa tokenização baseada em probabilidade
- Quanto mais a IA é treinada, mais precisa ela se torna

---

## ☁️ Serviço OpenAI no Azure

Plataforma da Microsoft para usar IA generativa com recursos robustos de segurança e escalabilidade.

### Funcionalidades:
- **Implantação e personalização** de LLMs
- **Hospedagem na nuvem**
- **Suporte a modelos**: GPT-3.5, GPT-4, Embeddings, DALL-E
- **Integração via API**
- **Controle de Acesso (RBAC)**

### Recursos:
- Geração e edição de imagens com DALL-E
- Geração de código e explicações com GPT
- Respostas em linguagem natural com PLN

---

## 🛡️ IA Generativa Responsável

A Microsoft propõe quatro fases para garantir um uso ético e seguro da IA:

1. **Identificar**:
   - Quais danos podem ocorrer com a solução planejada?

2. **Medir**:
   - Esses danos estão presentes nas respostas da IA?

3. **Mitigar**:
   - O que pode ser feito para reduzir esses danos?

4. **Operar**:
   - Como garantir que a IA seja usada com responsabilidade e controle?

---


## 📎 Documentação oficial:

* [Microsoft Learn – Azure](https://learn.microsoft.com/azure/)
* [Calculadora de Preço do Azure](https://azure.microsoft.com/pricing/calculator/)
* [Microsoft Entra ID - Visão Geral](https://learn.microsoft.com/entra/)
* [Microsoft Defender for Cloud - Visão Geral](https://learn.microsoft.com/azure/defender-for-cloud/)
* [Documentação Azure Cognitive Search](https://learn.microsoft.com/azure/search/)
* [Microsoft Learn – AI-900](https://learn.microsoft.com/training/paths/get-started-ai-fundamentals/)
