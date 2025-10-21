# 🚀 Projeto de Integração Contínua (CI) com Go e Docker 

Este projeto demonstra a implementação de um pipeline de **Integração Contínua (CI)** usando **GitHub Actions**, com um ambiente configurado em **Docker Compose** para testes automatizados em uma aplicação **Go (Golang)** conectada ao **PostgreSQL**.

---

## 🧱 Estrutura do Projeto

```
projeto-ci/
│
├── .github/
│   └── workflows/
│       ├── go.yml          # Pipeline principal de CI
│       └── docker.yml      # Workflow reutilizável para build e push de imagem Docker
│
├── database/
│   └── db.go               # Conexão com o banco de dados PostgreSQL
│
├── docker-compose.yml       # Configuração do ambiente de containers
├── main.go                  # Código principal da aplicação Go
├── main_test.go             # Testes automatizados
└── README.md                # Documentação do projeto
```

---

## ⚙️ Tecnologias Utilizadas

- **Go (Golang)** — linguagem principal da aplicação  
- **Docker e Docker Compose** — para orquestração do ambiente de testes  
- **PostgreSQL** — banco de dados relacional  
- **GitHub Actions** — automação do pipeline de CI/CD  

---

## 🔁 Pipeline de CI

O pipeline é definido no arquivo `.github/workflows/go.yml` e executa as seguintes etapas:

1. **Checkout do código**
2. **Configuração do Go**
3. **Instalação do Docker Compose**
4. **Criação do ambiente de testes**
5. **Execução dos testes automatizados**
6. **Build da aplicação**
7. **Build e Push da Imagem Docker**

---


## 🧪 Testes Automatizados

Os testes estão definidos em `main_test.go` e validam o comportamento da aplicação Go, incluindo:
- Conexão com o banco de dados
- Rotas e Handlers
- Funções principais da aplicação

Execução local:
```bash
go test -v
```

---

## ☁️ Deploy com Docker Hub

O arquivo `.github/workflows/docker.yml` é um workflow reutilizável responsável por:
- Fazer login no Docker Hub usando `secrets.SENHA_DOCKER_HUB`
- Buildar a imagem com o `docker/build-push-action`
- Enviar para o repositório remoto

---


## 🧩 Objetivo do Projeto

O propósito deste projeto é demonstrar o uso de **Integração Contínua (CI)** para:
- Automatizar builds e testes de aplicações Go  
- Garantir que cada commit seja testado e validado  
- Facilitar a entrega contínua com imagens Docker publicadas automaticamente

<img width="1024" height="1024" alt="ChatGPT Image 20 de out  de 2025, 16_32_09" src="https://github.com/user-attachments/assets/07bd8c3e-1149-4060-a347-8d3917975fcc" />

---

## 👨‍💻 Autor

**Fernando Tobace**  
📧 fertobace@gmail.com
![Imagem do WhatsApp de 2025-10-20 à(s) 23 33 58_18e84178](https://github.com/user-attachments/assets/51e0c4d1-3a23-40b8-bc17-5f7cdb6a3e36)


---
