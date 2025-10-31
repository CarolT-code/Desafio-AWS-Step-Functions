# Desafio-AWS-Step-Functions

Este repositório reúne minhas anotações, insights e exemplos sobre o AWS Step Functions, realizados durante o Bootcamp Santander Code Girls 2025.  
O objetivo é servir como material de apoio e consulta para futuras implementações e estudos relacionados à orquestração de fluxos de trabalho na nuvem AWS.

---

## O que é o AWS Step Functions

O AWS Step Functions é um serviço de orquestração visual** que permite criar e coordenar fluxos de trabalho compostos por múltiplos serviços da AWS — como Lambda, S3, DynamoDB, ECS, entre outros.

Ele permite definir visualmente a sequência e as condições de execução das etapas (estados) de um processo, sem precisar escrever toda a lógica de controle no código.  
A orquestração é feita através de diagramas visuais e arquivos de definição no formato JSON, usando a Amazon States Language (ASL).

---

## Características Principais

- Interface visual intuitiva, permite arrastar e conectar etapas (caixinhas) para formar o fluxo de trabalho.  
- Permite criar, validar e executar rotinas que envolvem diferentes serviços AWS.  
- Possibilita definir condições (choices), tempos de espera, validações e exceções.  
- É possível adicionar novos recursos gradualmente, implantando conforme a necessidade.  
- Facilita a colaboração: é possível adicionar comentários e documentar cada validação.  
- Contém modelos prontos (exemplos básicos) para aplicações como Machine Learning, ETL e processamento de dados.

---

##  Benefícios

| Benefício | Descrição |
|------------|------------|
| **Automação Visual** | Permite criar fluxos complexos sem precisar escrever código de orquestração. |
| **Integração Nativa** | Conecta-se facilmente com Lambda, S3, DynamoDB, SNS, SQS, ECS, entre outros. |
| **Alta Observabilidade** | Acompanhe execuções em tempo real, visualize falhas e tempos de execução. |
| **Tolerância a Falhas** | Retenta automaticamente etapas que falham e gera logs detalhados. |
| **Escalabilidade** | Suporta desde poucos até milhares de fluxos simultâneos. |
| **Controle e Segurança** | Permite definir timeouts, validações e controle de acesso via IAM. |

---

##  Fluxos de Trabalho e Estados

Cada workflow no Step Functions é composto por estados, que representam etapas do processo.  
Os tipos mais comuns são:

| Tipo de Estado | Função |
|-----------------|--------|
| **Task** | Executa uma tarefa, como chamar uma função Lambda. |
| **Choice** | Define decisões condicionais (if/else). |
| **Wait** | Adiciona um tempo de espera antes de seguir o fluxo. |
| **Parallel** | Executa várias tarefas em paralelo. |
| **Fail / Succeed** | Define o fim da execução, com sucesso ou falha. |

Os estados e suas transições são definidos em JSON, seguindo a Amazon States Language.

---


