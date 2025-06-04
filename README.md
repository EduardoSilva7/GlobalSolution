# 🌪️ ClimaResponde — Global Solution FIAP 2025

## 🎯 Objetivo do Projeto

Este projeto tem como objetivo desenvolver uma solução completa utilizando práticas de DevOps e conteinerização com Docker, simulando um sistema de controle de estoque de itens emergenciais para situações de catástrofes climáticas.

---

**ClimaResponde** é uma API RESTful em Java com Spring Boot que apoia ações em resposta a eventos climáticos extremos. Utiliza banco de dados PostgreSQL para persistência e está totalmente conteinerizada, com a imagem publicada no Docker Hub, pronta para execução via `docker run` ou `docker-compose`, inclusive em ambientes de nuvem como máquinas virtuais Linux.

---

## 🚀 Como executar a aplicação

### ✅ Pré-requisitos

* Docker instalado
* Terminal (CMD/PowerShell no Windows ou Bash no Linux)
* Acesso à internet para puxar a imagem

---

## 🔧 Etapas do projeto 


### 1. Criar as imagens e subir os containers

```bash
sudo docker-compose up --build -d
```

### 2. Verificar os logs da aplicação

```bash
sudo docker logs -f <nome_do_container_da_api>
```

### 3. Acessar a aplicação

* VM: http://52.170.77.61:8080/api/items

### 4. Publicar no Docker Hub

```bash
sudo docker login

# Build da imagem 
sudo docker build -t rm98410/climaresponde-api:1.0 .

# Enviar para o Docker Hub
sudo docker push rm98410/climaresponde-api:1.0
```

---

## ✅ Testes de uso da API

### Criar item (POST)

```bash
curl -X POST http://localhost:8080/api/items -H "Content-Type: application/json" -d '{"nome":"Água potável","descricao":"Distribuição emergencial"}'
```

### Listar todos os itens (GET)

```bash
curl http://localhost:8080/api/items
```

### Consultar item por ID (GET)

```bash
curl http://localhost:8080/api/items/1
```

### Atualizar item (PUT)

```bash
curl -X PUT http://localhost:8080/api/items/1 -H "Content-Type: application/json" -d '{"nome":"Água mineral","descricao":"Atualizado"}'
```

### Remover item (DELETE)

```bash
curl -X DELETE http://localhost:8080/api/items/1
```


---

## 🔮 Evidências de Execução

* Imagem publicada no Docker Hub
* Container executado com sucesso
* Logs verificados via `docker logs`
* API acessível via browser e terminal `curl`

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
