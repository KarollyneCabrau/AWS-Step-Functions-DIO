# Explorando Workflows Automatizados com AWS Step Functions

## 🎯 Objetivo do Desafio

Este repositório visa **consolidar e demonstrar** o conhecimento e a prática na criação de **Workflows Automatizados utilizando o AWS Step Functions**.

O foco é na orquestração de múltiplos serviços AWS em arquiteturas *serverless*, priorizando a gestão de estados, o tratamento de erros e a construção de fluxos de decisão complexos de maneira escalável.


## 🚀 Conceito: AWS Step Functions

O AWS Step Functions é um serviço de orquestração de fluxo de trabalho *serverless* que permite coordenar serviços AWS como parte de uma aplicação coesa. Ele é essencial para:

* **Definir Fluxos:** Utilizando a **Amazon States Language (ASL)**, que é baseada em JSON, para descrever cada passo (estado) do processo.
* **Garantir Resiliência:** Implementa lógica nativa de **`Retry`** e **`Catch`** para garantir que o fluxo de trabalho se recupere de falhas sem intervenção manual.
* **Gerenciar Estados:** Mantém o controle do progresso do fluxo, facilitando a auditoria e a depuração.

É a ferramenta ideal para processos de longa duração e pipelines de processamento de dados.


## 📦 Entregáveis

O resultado deste projeto é um **repositório organizado** que serve como material de referência técnica, contendo:

1.  **Definições de State Machine (JSON/ASL):** Os arquivos `.json` que definem a arquitetura do fluxo de trabalho.
2.  **Anotações e Insights:** Documentação dos principais conceitos e práticas adquiridas.
3.  **Exemplos de Codebase:** Código das funções AWS Lambda (ou outros serviços) utilizadas nas tarefas do fluxo.
4.  **Diagramas:** Representações visuais do fluxo de trabalho geradas pelo console do Step Functions.

---

## 🛠️ Tecnologias Envolvidas

| Serviço/Tecnologia | Função no Workflow |
| :--- | :--- |
| **AWS Step Functions** | Orquestração central e gerenciamento de transições de estado. |
| **AWS Lambda** | Execução da lógica de negócio (*Function-as-a-Service*) em cada tarefa. |
| **IAM (Identity and Access Management)** | Gerenciamento de permissões e políticas de segurança para o fluxo. |
| **Amazon States Language (ASL)** | Linguagem declarativa (JSON) utilizada para modelar a máquina de estados. |

---

## 🧠 Tópicos Explorados

A prática envolveu o domínio dos seguintes aspectos do Step Functions:

### 1. Tipos de Estados (Componentes Essenciais)
* **`Task`:** Para invocar serviços AWS e executar trabalho.
* **`Choice`:** Implementação de lógica de decisão condicional.
* **`Parallel`:** Execução simultânea de ramificações independentes do fluxo.
* **`Pass` / `Wait` / `Succeed` / `Fail`:** Controle de fluxo, manipulação de dados e definição de saídas.

### 2. Fluxo de Dados e Controle
* Entendimento do uso de **`InputPath`**, **`OutputPath`** e **`ResultPath`** para filtrar e transformar dados entre os estados.
* Utilização do objeto de **`Context` (`$$`)** para acessar metadados da execução do workflow.

### 3. Resiliência e Tratamento de Erros
* Configuração de **`Retriers`** para repetição automática de tarefas.
* Configuração de **`Catchers`** para desvio e tratamento de erros irrecuperáveis.


## 🔗 Próximos Passos e Expansão

O projeto estabelece a base para futuras implementações, que podem incluir:

* **Integração com ECS/Fargate:** Orquestração de tarefas de contêineres.
* **Padrão de Aprovação:** Utilização de *callback tokens* para pausar o fluxo e aguardar eventos externos.
* **Workflows Express:** Implementação de fluxos de alta taxa e curta duração.

* ## 📌 Referências  
- [AWS Step Functions - Documentação Oficial](https://docs.aws.amazon.com/step-functions/)  
- [GitHub Docs](https://docs.github.com/)  
  [Guia Markdown - GitHub](https://www.markdownguide.org/)  
- Este repositório contém a resolução do desafio AWS Step Functions da DIO e pode ser utilizado como base para consultas e revisões posteriores.
