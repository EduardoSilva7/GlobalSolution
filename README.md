# GlobalSolution


# 🌪️ ClimaResponde — Global Solution FIAP 2025

**ClimaResponde** é uma API RESTful em Java que apoia ações em resposta a eventos climáticos extremos. Com um banco de dados PostgreSQL persistente, a aplicação permite o gerenciamento de recursos críticos (como água, alimentos e primeiros socorros), sendo totalmente conteinerizada com Docker e orquestrada via Docker Compose.

---

## 🚀 Como executar a aplicação

### ✅ Pré-requisitos (ambos os sistemas)
- Docker + Docker Compose instalados: 
- Terminal (CMD ou PowerShell no Windows / Bash no Linux)

---

## 🪟 Instruções para Windows (CMD ou PowerShell)

1. Navegue até a pasta do projeto:

```
cd caminho\para\DevOps_Java_API_Project
```

2. Execute o projeto com:

```
docker-compose up --build
```

A aplicação estará disponível em: [http://localhost:8080/api/items](http://localhost:8080/api/items)

---

## 🐧 Instruções para Linux (Bash)

1. Navegue até a pasta do projeto:

```
cd ~/caminho/para/DevOps_Java_API_Project
```

2. Execute o projeto com:

```
docker-compose up --build
```

A aplicação estará disponível em: [http://localhost:8080/api/items](http://localhost:8080/api/items)

---

## ✅ Testes de uso da API

### Criar item (POST)

**Windows:**
```
curl -X POST "http://localhost:8080/api/items" -H "Content-Type: application/json" -d "{"nome":"Água potável","descricao":"Distribuição emergencial"}"
```

**Linux:**
```
curl -X POST http://localhost:8080/api/items -H "Content-Type: application/json" -d '{"nome":"Água potável","descricao":"Distribuição emergencial"}'
```

### Listar todos os itens (GET)

```
curl http://localhost:8080/api/items
```

### Consultar item por ID (GET)

```
curl http://localhost:8080/api/items/1
```

### Atualizar item (PUT)

**Windows:**
```
curl -X PUT "http://localhost:8080/api/items/1" -H "Content-Type: application/json" -d "{"nome":"Água mineral","descricao":"Atualizado"}"
```

**Linux:**
```
curl -X PUT http://localhost:8080/api/items/1 -H "Content-Type: application/json" -d '{"nome":"Água mineral","descricao":"Atualizado"}'
```

### Remover item (DELETE)

```
curl -X DELETE http://localhost:8080/api/items/1
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
**GitHub:** 
**Vídeo de demonstração:**
