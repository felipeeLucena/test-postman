
# 🚀 Testes de API com Postman – Typicode Demo  
### **Portfolio QA – Felipe Lucena**

Este repositório contém uma coleção completa de **testes automatizados de API** utilizando **Postman + JavaScript**, aplicados sobre a API pública **Typicode Demo**.

Aqui você encontrará:

✔️ Cenários **positivos**  
✔️ Cenários **negativos**  
✔️ Validações de **contrato**  
✔️ Validações de **performance (response time)**  
✔️ Testes com **workflow encadeado**  
✔️ Uso de **variáveis de ambiente**  
✔️ Preparado para integração com **CI/CD (Newman + HTML Report)**  

Todo o projeto foi estruturado para demonstrar habilidades práticas de um **QA Pleno/Sênior**.

---

## 📁 **Estrutura do Projeto**

```
test-postman/
│
├── collections/
│   └── demo-api-typicode.postman_collection.json
│
├── environments/
│   └── demo-api-typicode.postman_environment.json
│
├── .github/
│   └── workflows/
│       └── newman.yml
│
└── README.md
```

---

## 🔧 **Tecnologias e Ferramentas Utilizadas**

- **Postman**
- **JavaScript (Test Scripts)**
- **Newman**
- **HTMLExtra Reporter**
- **Variables & Environments**
- **GitHub Actions**
- **API REST Typicode**

---

## 🌐 **API Utilizada**

> **Typicode Demo API**

Base URL:

```
https://my-json-server.typicode.com/typicode/demo
```

---

# 📥 Como Importar e Executar o Projeto

## 1️⃣ Importar a Collection  
No Postman:

1. Clique em **Import**
2. Selecione:  
```
collections/demo-api-typicode.postman_collection.json
```

## 2️⃣ Importar o Environment  
1. Clique em **Import**
2. Selecione:
```
environments/demo-api-typicode.postman_environment.json
```
3. Escolha o environment no topo do Postman.

---

# ▶️ Executando os Testes

## ✅ **Manual (pelo Postman)**
- Abra qualquer request e clique em **Send**
- Ou execute tudo com o **Collection Runner**

## ⚙️ **Via Newman (terminal)**

Instale:

```bash
npm install -g newman newman-reporter-htmlextra
```

Execute:

```bash
newman run collections/demo-api-typicode.postman_collection.json -e environments/demo-api-typicode.postman_environment.json -r htmlextra --reporter-htmlextra-export report.html
```

---

# 🤖 CI/CD – GitHub Actions

Este repositório possui um workflow pronto em:

```
.github/workflows/newman.yml
```

Ele executa automaticamente:

- Push
- Pull Request
- Execução manual (`workflow_dispatch`)

E gera um **relatório HTML** como artifact.

---

# 🧪 **Cenários Implementados**

## ✅ **Cenários Positivos**
- ✔️ GET `/posts` – status, contrato, tempo, estrutura  
- ✔️ GET `/posts/1` – item único válido  
- ✔️ GET `/comments` – lista e campos  
- ✔️ GET `/comments?postId=1` – filtro válido  
- ✔️ GET `/profile` – objeto válido  

---

## ❌ **Cenários Negativos**
- ❗ GET `/posts/999999` – ID inexistente  
- ❗ GET `/posts/abc` – ID inválido  
- ❗ GET `/comments?postId=999` – sem retorno  
- ❗ GET `/postsss` – rota inexistente (404)  
- ❗ Query inválida  
- ❗ Validação de campos ausentes  

---

## 🔄 **Workflow Encadeado**
Demonstra conhecimento avançado em testes de API:

1. GET `/posts` → salva automaticamente o `postId`  
2. GET `/comments?postId={{postId}}`  
   - Valida que todos pertencem ao post salvo  

---

# 📊 **Relatórios**

Um relatório HTML é gerado automaticamente:

- status dos testes  
- request/response  
- tempos de execução  
- logs detalhados  

Disponível na aba **Artifacts** após o pipeline rodar.

---

# 👨‍💻 **Autor**

**Felipe Lucena**  
Analista de Testes (QA) – Manual & Automação  
🔗 https://br.linkedin.com/in/felipeeLucena

