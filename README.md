
# 🚀 Testes de API com Postman – Typicode Demo  
### **Portfolio QA – Felipe Lucena**

Este repositório contém uma coleção completa de testes automatizados no **Postman**, utilizando a API pública **Typicode Demo**.  
Aqui você encontrará cenários **positivos**, **negativos**, **testes de contrato**, **validações funcionais**, **performance simples** e **workflow automatizado** utilizando variáveis de ambiente.

Este projeto foi estruturado para demonstrar habilidades práticas como **QA Pleno/Sênior**.

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
└── README.md
```

---

## 🔧 **Tecnologias Utilizadas**

- **Postman**
- **JavaScript (Postman Tests)**
- **JSON Schema Validation**
- **Postman Variables / Environment**
- **APIs REST**
- **Workflow de chamadas**

---

## 🌐 **API Utilizada**

**Typicode Demo API**  
Base URL:

```
https://my-json-server.typicode.com/typicode/demo
```

---

## 🧩 **Como Importar o Projeto**

### 1️⃣ Importar a Collection
No Postman:
1. Clique em **Import**
2. Selecione o arquivo:
```
collections/demo-api-typicode.postman_collection.json
```

### 2️⃣ Importar o Environment
1. Clique em **Import**
2. Selecione:
```
environments/demo-api-typicode.postman_environment.json
```
3. Selecione o environment no topo do Postman.

### 3️⃣ Executar os Testes
- Clique em **Send**  
- Ou use o **Collection Runner**

---

# 🧪 **Cenários Testados**

## ✅ **Cenários Positivos**
- GET `/posts` – valida contrato, status, tempo e estrutura
- GET `/posts/1` – valida item existente
- GET `/comments` – valida lista e campos
- GET `/comments?postId=1` – filtro funcional
- GET `/profile` – valida objeto

## ❌ **Cenários Negativos**
- ID inexistente
- ID inválido
- Filtro sem retorno
- Query param inválido
- Rota inexistente

## 🔄 **Workflow (encadeamento)**
- Salva `postId` da lista de posts
- Usa `postId` salvo para buscar comentários relacionados

---

# 👨‍💻 **Autor**

**Felipe Lucena**  
Analista de Testes (QA) – Manual & Automação  
LinkedIn: https://br.linkedin.com/in/felipeeLucena
