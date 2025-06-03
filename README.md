# 🌪️ ClimaResponde — Global Solution FIAP 2025

## 🎯 Objetivo do Projeto

Este projeto tem como objetivo desenvolver uma solução completa utilizando práticas de DevOps e conteinerização com Docker, simulando um sistema de controle de estoque de itens emergenciais para situações de catástrofes climáticas.

---

**ClimaResponde** é uma API RESTful em Java com Spring Boot que apoia ações em resposta a eventos climáticos extremos. Utiliza banco de dados PostgreSQL para persistência e está totalmente conteinerizada, com a imagem publicada no Docker Hub, pronta para execução via `docker run`, inclusive em ambientes de nuvem como máquinas virtuais Linux.

---

## 🚀 Como executar a aplicação

### ✅ Pré-requisitos
- Docker instalado
- Terminal (CMD/PowerShell no Windows ou Bash no Linux)
- Acesso à internet para puxar a imagem

---

## 🔧 Execução da aplicação

1. Execute o container da API diretamente via Docker Hub:

```bash
docker run -d -p 8080:8080 rm98410/climaresponde-api
```

2. Acesse a aplicação:

- Em VM: http://52.170.77.61:8080/api/items

---

## ✅ Testes de uso da API

### Criar item (POST)

**Windows:**

**Linux:**
```bash
curl -X POST http://localhost:8080/api/items -H "Content-Type: application/json" -d '{"nome":"Água potável","descricao":"Distribuição emergencial"}'
```

---

### Listar todos os itens (GET)
```bash
curl http://localhost:8080/api/items
```

---

### Consultar item por ID (GET)
```bash
curl http://localhost:8080/api/items/1
```

---

### Atualizar item (PUT)

**Windows:**
```bash
curl -X PUT http://localhost:8080/api/items/1 -H "Content-Type: application/json" -d "{\"nome\": \"Atualizado\", \"quantidade\": 10}"
```

**Linux:**
```bash
curl -X PUT http://localhost:8080/api/items/1 -H "Content-Type: application/json" -d '{"nome":"Água mineral","descricao":"Atualizado"}'
```

---

### Remover item (DELETE)
```bash
curl -X DELETE http://localhost:8080/api/items/1
```

---

## 🐳 Container da aplicação

- **Imagem:** [`rm98410/climaresponde-api`](https://hub.docker.com/r/rm98410/climaresponde-api)
- **Base:** Java 17 + Spring Boot
- **Porta exposta:** 8080
- **Deploy:** Executável em qualquer host com Docker, inclusive em VMs Linux na nuvem

---

## 🧪 Evidências de Execução

- Imagem publicada no Docker Hub
- Container executado com:

```bash
docker run -d -p 8080:8080 rm98410/climaresponde-api
```

- Testes validados via `curl`
- API acessível externamente pela porta 8080

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
