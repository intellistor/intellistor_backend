# 🧠 Intellistor Backend

Este repositório contém o backend da **Intellistor**, uma plataforma inteligente para gestão de ambientes de armazenamento e backup corporativo. A solução foi desenvolvida com foco em automação, integração multivendor e inteligência operacional.

---

## 🚀 Visão Geral

O backend da Intellistor é responsável por:
- Gerenciar e orquestrar operações de storage e backup
- Integrar com múltiplos fornecedores e protocolos
- Oferecer APIs RESTful para consumo por sistemas externos
- Monitorar e gerar insights sobre ambientes críticos

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.11+**
- **FastAPI** como framework principal
- **MySQL** como banco de dados relacional
- **SQLAlchemy** ou **Tortoise ORM** *(dependendo do ORM que você usa)*
- **Docker** para empacotamento e deploy
- **JWT** para autenticação segura
- **Swagger/OpenAPI** para documentação automática das APIs

---

## 📦 Instalação

### 1. Clone o repositório
````bash
git clone https://github.com/seu-usuario/intellistor-backend.git
cd intellistor-backend
````

### 2. Crie e ative o ambiente virtual
````bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
````

### 3. Instale as dependências
````bash
pip install -r requirements.txt
````

### 4. Configure as variáveis de ambiente
````bash
DB_HOST=localhost
DB_PORT=3306
DB_USER=seu_usuario
DB_PASSWORD=sua_senha
DB_NAME=intellistor
JWT_SECRET=sua_chave_secreta
````

### 5. Configurar o MySQL localmente
Se você ainda não tem o MySQL instalado, pode usar Docker para subir um container:
````bash
docker run --name intellistor-mysql \
  -e MYSQL_ROOT_PASSWORD=rootpass \
  -e MYSQL_DATABASE=intellistor \
  -e MYSQL_USER=intellistor_user \
  -e MYSQL_PASSWORD=intellistor_pass \
  -p 3306:3306 \
  -d mysql:8.0
````
Obs.: Isso criará um banco chamado intellistor com o usuário e senha definidos acima.

### 6. Execute a aplicação
````bash
uvicorn main:app --reload
````

### 7. (Alternativa) Executar com Docker Compose

Se preferir rodar tudo com Docker, crie um arquivo docker-compose.yml com o seguinte conteúdo:
````bash
version: '3.8'

services:
  backend:
    build: .
    ports:
      - "8000:8000"
    env_file:
      - .env
    depends_on:
      - db

  db:
    image: mysql:8.0
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: rootpass
      MYSQL_DATABASE: intellistor
      MYSQL_USER: intellistor_user
      MYSQL_PASSWORD: intellistor_pass
    ports:
      - "3306:3306"
````

## 📡 Endpoints Principais

A documentação interativa da API está disponível em:
http://localhost:8000/docs

---

## 🧪 Testes

Execute os testes com: **pytest**

---

## 📄 Licença

Este projeto está licenciado sob a MIT License – veja o [licença](#)

---

## 📬 Contato

Para dúvidas, sugestões ou parcerias, entre em contato:
- Renato de Carvalho Machado – renatodicmachado@gmail.com
- [Linkedin](https://www.linkedin.com/in/renatodicmachado/)
