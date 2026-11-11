# 🎬 Flix API

API REST desenvolvida com **Python, Django e Django REST Framework** para gerenciamento de filmes, atores, gêneros e avaliações.

O projeto permite realizar operações CRUD, autenticação de usuários utilizando JWT e consulta de estatísticas relacionadas aos filmes.

## 🚀 Funcionalidades

- Cadastro, consulta, atualização e exclusão de filmes.
- Gerenciamento de atores.
- Gerenciamento de gêneros.
- Gerenciamento de avaliações.
- Consulta de estatísticas dos filmes.
- Autenticação utilizando JWT (JSON Web Token).
- API REST organizada por recursos.
- Integração com banco de dados SQLite.

## 🛠️ Tecnologias utilizadas

- Python
- Django
- Django REST Framework
- SQLite
- JWT (JSON Web Token)
- Flake8

## ⚙️ Instalação e execução

### 1. Clone o repositório

```bash
git clone https://github.com/Luiz-Bonalda/Flix-API.git
```

### 2. Acesse a pasta do projeto

```bash
cd Flix-API
```

### 3. Crie um ambiente virtual

```bash
python -m venv venv
```

### 4. Ative o ambiente virtual

**Windows (PowerShell):**

```powershell
.\venv\Scripts\Activate.ps1
```

**Linux:**

```bash
source venv/bin/activate
```

### 5. Instale as dependências

```bash
pip install -r requirements.txt
```

Para instalar também as dependências de desenvolvimento:

```bash
pip install -r requirements_dev.txt
```

### 6. Configure as variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto, utilizando o arquivo `.env.example` como referência.

Configure as variáveis necessárias para a execução da aplicação.

### 7. Execute as migrações

```bash
python manage.py migrate
```

### 8. Inicie o servidor

```bash
python manage.py runserver
```

A aplicação estará disponível em:

```text
http://127.0.0.1:8000/
```

## 🔗 Endpoints da API

Os endpoints da API estão organizados sob o prefixo `/api/v1/`.

| Método | Endpoint | Descrição |
|---|---|---|
| GET / POST | `/movies/` | Listar e cadastrar filmes |
| GET / PUT / PATCH / DELETE | `/movies/{id}/` | Consultar, atualizar e excluir filmes |
| GET | `/movies/stats/` | Consultar estatísticas dos filmes |
| GET / POST | `/actors/` | Listar e cadastrar atores |
| GET / PUT / PATCH / DELETE | `/actors/{id}/` | Consultar, atualizar e excluir atores |
| GET / POST | `/genres/` | Listar e cadastrar gêneros |
| GET / PUT / PATCH / DELETE | `/genres/{id}/` | Consultar, atualizar e excluir gêneros |
| GET / POST | `/reviews/` | Listar e cadastrar avaliações |
| GET / PUT / PATCH / DELETE | `/reviews/{id}/` | Consultar, atualizar e excluir avaliações |

### 🔐 Autenticação JWT

A API disponibiliza endpoints para autenticação e gerenciamento de tokens JWT.

| Método | Endpoint | Descrição |
|---|---|---|
| POST | `/authentication/token/` | Obter tokens de acesso |
| POST | `/authentication/token/refresh/` | Renovar token |
| POST | `/authentication/token/verify/` | Verificar token |

## 🗄️ Banco de dados

O projeto utiliza **SQLite** como banco de dados, armazenando as informações da aplicação localmente.

O SQLite é integrado ao Django e não exige a instalação de um servidor de banco de dados separado.

## 🧪 Testes

Para executar os testes automatizados:

```bash
python manage.py test
```
