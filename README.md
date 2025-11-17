### Sunshine — Plataforma de Conexão entre Psicólogos e Pacientes

O Sunshine é um sistema desenvolvido em Python com FastAPI para facilitar a comunicação entre psicólogos e pacientes.
O objetivo principal é oferecer uma plataforma simples e eficiente, permitindo o gerenciamento de consultas, perfis, análises e comunicação dentro de um ambiente seguro.

O projeto utiliza ferramentas modernas como Pydantic, SQLAlchemy, Passlib, Python-JOSE, bcrypt e ambiente virtual venv, oferecendo uma arquitetura organizada e pronta para expansão.

## Estrutura do Projeto

A estrutura completa do diretório do projeto:

###  CODIGO(SUNSHINE)/
│
├── core/
│   ├── database.py
│   └── __pycache__/
│
├── models/
│   ├── models.py
│   └── __pycache__/
│
├── routers/
│   ├── appointments.py
│   ├── auth.py
│   ├── ml_analysis.py
│   ├── patients.py
│   ├── psychologists.py
│   ├── requests.py
│   ├── reports.py
│   └── __pycache__/
│
├── schemas/
│   ├── schemas.py
│   └── __pycache__/
│
├── services/
│   ├── auth_service.py
│   ├── ml_services.py
│   ├── report_service.py
│   └── __pycache__/
│
├── venv/
│
├── seed_data.py
├── test.py
├── Utils.py
├── main.py
├── lunysse.db
├── .env
├── requirements.txt
└── README.md

### Tecnologias Utilizadas
Backend

Python 3

FastAPI — framework principal da API

SQLAlchemy — ORM e comunicação com banco de dados

Pydantic — validação e serialização de dados

Passlib — hashing seguro de senhas

bcrypt — backend de criptografia

python-jose — geração e validação de tokens JWT

Ambiente

venv — ambiente virtual isolado

### Instalação e Configuração
 Clone o repositório
git clone https://seu-repositorio.git
cd sunshine

 Crie e ative o ambiente virtual

Windows PowerShell:

python -m venv venv
.\venv\Scripts\activate


Linux/Mac:

python3 -m venv venv
source venv/bin/activate

 Instale as dependências
pip install -r requirements.txt

 Configure o arquivo .env

Exemplo de conteúdo:

SECRET_KEY=sua_chave_jwt
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=60
DATABASE_URL=sqlite:///./lunysse.db

 Gere dados de teste (opcional)
python seed_data.py

 Execute o servidor FastAPI
uvicorn main:app --reload


## A API ficará disponível em:

 http://127.0.0.1:8000

### Documentação automática:

 http://127.0.0.1:8000/docs
 (Swagger)
 http://127.0.0.1:8000/redoc
 (ReDoc)

 ### Rodando os Testes

Para rodar os testes simples incluídos no projeto:

python test.py


Se você futuramente adicionar pytest, poderá rodar:

pytest

###  Funcionalidades Principais
 Autenticação com JWT

Login

Registro

Tokens de acesso

Autorização por rotas protegidas

  Gestão de Pacientes

Cadastro

Perfil

Histórico

  Gestão de Psicólogos

Cadastro

Perfil profissional

Relatórios

 Consultas

Agendamento

Status

Cancelamento

Módulo de Relatórios

Geração automática de análises

✔️ Integração com Machine Learning

Endpoint dedicado para análises (ml_analysis)

### Dependências Principais (requirements.txt)

Exemplo típico de dependências usadas:

fastapi
uvicorn
sqlalchemy
pydantic
passlib[bcrypt]
python-jose
bcrypt
python-multipart


(Seu arquivo real pode conter mais itens)

### Créditos

Projeto desenvolvido por Gustavo Andrade Vidal como uma plataforma para conectar psicólogos e pacientes de maneira simples, rápida e segura.

