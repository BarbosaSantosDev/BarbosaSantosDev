<h1 align="center">João Vitor Barbosa</h1>
<h3 align="center">Desenvolvedor Backend · Python | FastAPI | Microsserviços</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/barbosasantosdev/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:joaovitorbarbosa513@gmail.com">
    <img src="https://img.shields.io/badge/E--mail-EA4335?style=flat&logo=gmail&logoColor=white" alt="E-mail" />
  </a>
</p>

---

Backend com 4 anos de experiência em Python, atuando no desenvolvimento e evolução de APIs, microsserviços e sistemas corporativos.

- ⚙️ Trabalho com **FastAPI, PostgreSQL, mensageria (RabbitMQ/PGMQ), Docker e Kubernetes**
- 🏗️ Aplico **DDD, Clean Architecture e CQRS**, com testes em **BDD (Behave)** e **TDD (Pytest)**
- 📊 Experiência com **observabilidade** (Datadog), resolução de incidentes e análise de custos
- 🤖 Integração de **LLMs** em produto real com LangChain, RAG e modelos locais via Ollama
- 📍 Santos/SP — disponível para atuação **remota ou híbrida em São Paulo**

---

### Stack

**Backend e APIs**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat&logo=sqlalchemy&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white)

**Dados e mensageria**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat&logo=redis&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat&logo=rabbitmq&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat&logo=celery&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-6BA81E?style=flat)

**Cloud, DevOps e Observabilidade**
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![Datadog](https://img.shields.io/badge/Datadog-632CA6?style=flat&logo=datadog&logoColor=white)

**Testes e IA aplicada**
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)
![Behave](https://img.shields.io/badge/Behave%20(BDD)-2C3E50?style=flat)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)

**Frontend complementar**
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)

---

### Projetos

**[jobhound](https://github.com/BarbosaSantosDev/jobhound)** — Agente de busca e ranqueamento de vagas com LLM<br>
Coleta vagas de múltiplas fontes, extrai fatos estruturados com LLM local (Ollama) e ranqueia o match com **scoring determinístico no domínio** — o modelo extrai, o domínio decide. Clean Architecture + DDD + CQRS, testes BDD com Behave, CLI em Typer e notificações via Telegram.<br>
`Python` `FastAPI` `PostgreSQL` `LangChain` `Ollama` `Docker`

**[Cofre de Documentos](https://github.com/BarbosaSantosDev/cofre-docs-backend)** — API de documentos criptografados<br>
API RESTful para upload e recuperação de PDFs com **envelope encryption** (Fernet) e autenticação JWT. Arquitetura em camadas, migrations com Alembic e suíte BDD rodando com repositórios in-memory.<br>
`Python` `FastAPI` `PostgreSQL` `Cryptography` `JWT` `Behave`

**[Barber Flow](https://agenda.barbosasystem.tech)** — SaaS de gestão para barbearias *(em produção)*<br>
Aplicação de agendamento e gestão com fluxo de reserva para clientes e painel administrativo. **Multi-tenancy** com roteamento por slug e repositórios isolados por tenant. Deploy próprio em VPS Linux com Caddy como reverse proxy e HTTPS automático.<br>
`FastAPI` `PostgreSQL` `React 19` `Vite` `Caddy` `VPS`

**[LabelFlow](https://github.com/BarbosaSantosDev/backend-industrial-labels)** — Sistema industrial de etiquetas<br>
SaaS desenvolvido do zero e comercializado para peixarias e distribuidoras que reetiquetam produtos após reprocessamento. Geração de etiquetas **ZPL** com templates Jinja2 e calibração para impressoras Zebra ZD220.<br>
`Python` `MongoDB` `Jinja2` `Docker Compose`
