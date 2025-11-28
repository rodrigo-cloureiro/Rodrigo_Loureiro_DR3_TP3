# 📘 TP3 – GitHub Actions: Workflows, Runners, Deploy e Monitoramento

Este repositório contém todas as atividades realizadas para o Teste de Performance 3 (TP3), envolvendo criação e
execução de workflows utilizando GitHub Actions, incluindo testes, variáveis de ambiente, secrets, deploys, matrix
strategy e monitoramento.

# ✅ Resumo das Atividades do TP3

## 🔹 Parte 1 – Workflows Básicos

### ✔ hello.yml

- Disparado em push.
- Exibe "Hello CI/CD" no log.

### ✔ tests.yml

- Disparado em pull_request.
- Usa actions/checkout.
- Executa echo "Rodando testes".

### ✔ gradle-ci.yml

- Disparado em push na branch main.
- Usa runs-on: ubuntu-latest.
- Executa o build com maven.

## 🔹 Parte 2 – Runners, Variáveis e Segurança

### ✔ env-demo.yml

- Usa variável de ambiente DEPLOY_ENV=staging.
- Exibe valor no log.

### ✔ secret-demo.yml

- Utiliza secret API_KEY.
- Exibe a mensagem “API_KEY configurado” sem mostrar o valor real.

### ✔ Explicação adicionada no PDF:

- Diferenças entre runners GitHub-hosted e self-hosted, com vantagens e desvantagens.

## 🔹 Parte 3 – Deploys e Estratégias

### ✔ release-deploy.yml

- Disparado em release published.
- Mostra "Deploy realizado com sucesso".

### ✔ Workflow com Matrix Strategy

- Roda em Java 11 e 17.
- Exibe versão ativa da JVM no log.

### ✔ Explicações incluídas no PDF:

- Estratégias Blue-Green e Rolling Update com cenários adequados para cada uma.

## 🔹 Parte 4 – Monitoramento e Logs

### ✔ Badge de status

Badges de status foram adicionadas ao README para acompanhar o status dos workflows:

[![Build](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/maven.yml/badge.svg)](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/maven.yml)

[![Environment demo](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/env-demo.yml/badge.svg)](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/env-demo.yml)

[![Hello CI/CD](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/hello.yml/badge.svg)](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/hello.yml)

[![Matrix strategy](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/matrix-strategy.yml/badge.svg)](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/matrix-strategy.yml)

[![Release deploy](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/release-deploy.yml/badge.svg)](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/release-deploy.yml)

[![Secret demo](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/secret-demo.yml/badge.svg)](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/secret-demo.yml)

[![Tests](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/tests.yml/badge.svg)](https://github.com/rodrigo-cloureiro/Rodrigo_Loureiro_DR3_TP3/actions/workflows/tests.yml)

### ✔ Debug logs

- Foi ativado modo debug (ACTIONS_RUNNER_DEBUG / ACTIONS_STEP_DEBUG).

### ✔ Explicação no PDF:

- Como mascarar dados sensíveis usando nos logs do GitHub Actions

## 🔹 Parte 5 – Questão Integrada (Final)

## ✔ deploy.yml

- Disparado somente em push na branch main.
- Usa variáveis para diferenciar dev, staging, prod.
- Usa secrets para credenciais.
- Log exibe mensagens diferentes por ambiente:
    - "Deploy em dev concluído"
    - "Deploy em staging concluído"
    - "Deploy em prod concluído"

# ▶ Como Reexecutar os Workflows

1. **hello.yml**\
   Fazer qualquer alteração no repositório e enviar um push.

2. **tests.yml**\
   Abrir um pull request.

3. **maven.yml**\
   Enviar push na branch main.

4. **env-demo.yml**\
   Dispatch manual.

5. **secret-demo.yml**\
   Dispatch manual.

6. **release-deploy.yml**\
   Criar uma release no GitHub.

7. **Matrix Strategy**\
   Dispatch manual.

8. **deploy.yml**\
   Push na branch main.
