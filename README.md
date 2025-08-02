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

````bash
1. Clone o repositório
git clone https://github.com/seu-usuario/intellistor-backend.git
cd intellistor-backend

2. Crie e ative o ambiente virtual
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows

3. Instale as dependências
pip install -r requirements.txt

4. Configure as variáveis de ambiente
DB_HOST=localhost
DB_PORT=3306
DB_USER=seu_usuario
DB_PASSWORD=sua_senha
DB_NAME=intellistor
JWT_SECRET=sua_chave_secreta

5. Execute a aplicação
uvicorn main:app --reload

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
