# 🌪️ ClimaResponde — Global Solution FIAP 2025

## 🎯 Objetivo do Projeto

Este projeto tem como objetivo desenvolver uma solução completa utilizando práticas de DevOps e conteinerização com Docker, simulando um sistema de controle de estoque de itens emergenciais para situações de catástrofes climáticas.

---

**ClimaResponde** é uma API RESTful em Java com Spring Boot que apoia ações em resposta a eventos climáticos extremos. Com um banco de dados PostgreSQL persistente em container separado, a aplicação permite o gerenciamento de recursos críticos (como água, alimentos e primeiros socorros), sendo **totalmente conteinerizada** com Docker, **orquestrada via Docker Compose** e preparada para deploy em VM Linux na nuvem.

---

## 🚀 Como executar a aplicação

### ✅ Pré-requisitos
- Docker instalado
- Docker Compose instalado
- Terminal (CMD/PowerShell no Windows ou Bash no Linux)
- Acesso à pasta do projeto

---

## 🪟 Instruções para Windows (CMD ou PowerShell)

1. Navegue até a pasta raiz do projeto:

```sh
cd caminho\para\DevOps_Java_API_Project
```

2. Execute os containers em segundo plano com build:

```sh
docker-compose up -d --build
```

---

## 🐧 Instruções para Linux (Bash)

1. Navegue até a pasta raiz do projeto:

```sh
cd ~/caminho/para/DevOps_Java_API_Project
```

2. Execute os containers em segundo plano com build:

```bash
docker-compose up -d --build
```

---

## 🔎 Verificação e Logs dos Containers

Após iniciar, valide a execução com:

```bash
docker ps
docker-compose logs
```

A aplicação estará disponível em:

- Localmente: [http://localhost:8080/api/items](http://localhost:8080/api/items)
- VM (se aplicável): [http://<ip-da-vm>:8080/api/items](http://<ip-da-vm>:8080/api/items)

---

## ✅ Testes de uso da API

### Criar item (POST)

**Windows:**
```sh
curl -X POST http://localhost:8080/api/items -H "Content-Type: application/json" -d "{\"nome\": \"Emergencial\", \"quantidade\": 5}"
```

**Linux:**
```bash
curl -X POST http://localhost:8080/api/items -H "Content-Type: application/json" -d '{"nome":"Água potável","descricao":"Distribuição emergencial"}'
```

---

### Listar todos os itens (GET)
```sh
curl http://localhost:8080/api/items
```

---

### Consultar item por ID (GET)
```sh
curl http://localhost:8080/api/items/1
```

---

### Atualizar item (PUT)

**Windows:**
```sh
curl -X PUT http://localhost:8080/api/items/1 -H "Content-Type: application/json" -d "{\"nome\": \"Atualizado\", \"quantidade\": 10}"
```

**Linux:**
```bash
curl -X PUT http://localhost:8080/api/items/1 -H "Content-Type: application/json" -d '{"nome":"Água mineral","descricao":"Atualizado"}'
```

---

### Remover item (DELETE)
```sh
curl -X DELETE http://localhost:8080/api/items/1
```

---

## 🐳 Containers

- **App:** imagem construída localmente via `Dockerfile` (Java 17 + Spring Boot)
- **DB:** imagem PostgreSQL com `Dockerfile` personalizado (`USER`, `WORKDIR`, `ENV`)
- **Volume:** persistência dos dados configurada
- **Portas expostas:** 8080 (app), 5432 (db)

---

## 🧪 Execução via Terminal (Evidência)

Todos os containers são executados em segundo plano:

```sh
docker-compose up -d
```

Logs e verificação:

```sh
docker ps
docker-compose logs
```

---

## 🎓 Projeto acadêmico

**Curso:** Análise e Desenvolvimento de Sistemas  
**Disciplina:** DevOps Tools & Cloud Computing  
**Instituição:** FIAP  
**Semestre:** 2025/1  
**Desafio:** Global Solution

---

## 👤 Autor

**Eduardo Ferreira Silva de Jesus**  
**RM:** 98410  
