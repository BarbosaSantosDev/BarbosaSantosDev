<h1 align="center">João Vitor Barbosa</h1>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com/?lines=Backend+Python+com+FastAPI;Agentes+de+IA+com+LangGraph;Observabilidade+de+LLM+com+Langfuse;Clean+Architecture+%C2%B7+DDD+%C2%B7+BDD&font=Fira+Code&center=true&vCenter=true&width=520&height=40&size=20&pause=1200&color=C6F135">
    <img alt="Backend Python, agentes de IA, observabilidade de LLM" src="https://readme-typing-svg.demolab.com/?lines=Backend+Python+com+FastAPI;Agentes+de+IA+com+LangGraph;Observabilidade+de+LLM+com+Langfuse;Clean+Architecture+%C2%B7+DDD+%C2%B7+BDD&font=Fira+Code&center=true&vCenter=true&width=520&height=40&size=20&pause=1200&color=3F6212">
  </picture>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/joao-vitor-barbosa-a9238a194/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"></a>
  <a href="mailto:joaovitorbarbosa513@gmail.com"><img alt="E-mail" src="https://img.shields.io/badge/E--mail-0E0F10?style=flat-square&logo=gmail&logoColor=white"></a>
  <a href="https://leetcode.com/u/joao-vitor/"><img alt="LeetCode" src="https://img.shields.io/badge/LeetCode-0E0F10?style=flat-square&logo=leetcode&logoColor=FFA116"></a>
  <img alt="Visitas ao perfil" src="https://komarev.com/ghpvc/?username=BarbosaSantosDev&label=visitas&color=0E0F10&style=flat-square">
</p>

---

## Sobre mim

Sou desenvolvedor backend Python há cerca de quatro anos. Comecei na área de operações de uma empresa, aprendi a programar sozinho e migrei para o time de desenvolvimento por dentro. Trabalho principalmente com FastAPI, PostgreSQL e mensageria, organizando o código com Clean Architecture e DDD e escrevendo as regras de negócio como cenários BDD antes do código.

Hoje a maior parte do meu tempo vai para **agentes de IA em produção**: atendimento por WhatsApp construído com LangChain e LangGraph, monitorado com Langfuse e, aos poucos, coberto por avaliações automáticas com DeepEval. Também mantenho um ERP com emissão de NFC-e e um SaaS de etiquetas industriais, os dois com clientes pagantes.

```python
from pydantic import BaseModel, ConfigDict


class Dev(BaseModel):
    model_config = ConfigDict(frozen=True)

    role: str
    location: str
    current_focus: list[str]
    learning: list[str]
    ask_me_about: list[str]


joao = Dev(
    role="Backend Python · agentes de IA",
    location="Baixada Santista, SP · remoto ou híbrido",
    current_focus=[
        "agentes com estado em LangGraph",
        "tracing, custo e prompts no Langfuse",
        "evals de regressão com DeepEval",
    ],
    learning=["avaliação de LLM", "Go para agentes locais"],
    ask_me_about=[
        "migrar sistema legado sem parar a operação",
        "um banco PostgreSQL por cliente em SaaS",
        "observar agente de IA em produção",
        "NFC-e e impressão térmica/ZPL",
    ],
)
```

---

## IA aplicada

O que faço hoje com LLMs, em produção, e não só em projeto de estudo:

| | |
|---|---|
| 🤖 **Construção** | Agentes de atendimento e automação comercial com **LangChain** e **LangGraph**, integrados ao WhatsApp e ao CRM do cliente, usando Gemini como modelo. Estou refatorando agentes legados para grafos do LangGraph, com estado e ferramentas separados por responsabilidade. |
| 🔭 **Observabilidade** | Implantei o **Langfuse** self-hosted (Docker Compose em VPS dedicada) para todos os agentes da empresa, com um projeto por cliente. Isso deu tracing de cada conversa, custo de tokens por cliente e versionamento de prompts pelo Prompt Management, e deixou visível a queda de custo depois das otimizações. |
| 🧪 **Avaliação** | Montando suítes com **DeepEval** para medir relevância, fidelidade ao contexto e uso correto de ferramentas antes de cada refatoração, para mudar o agente sem quebrar o que já funciona. |
| ⚙️ **Operação** | Tirei os agentes de containers sem versionamento e levei cada um para um repositório com deploy por **GitHub Actions**. Centralizei as chaves de API em um cofre de segredos (Infisical). |
| 🏠 **LLM local** | No [jobhound](https://github.com/BarbosaSantosDev/jobhound), extraio dados de vagas com um modelo rodando no **Ollama** e saída estruturada pelo LangChain; a nota de compatibilidade fica numa regra determinística no domínio, fora do LLM. |

---

## Projetos principais

Os projetos que estão em produção têm código fechado. Para eles publiquei repositórios só com a arquitetura, as decisões técnicas e o que cada sistema faz.

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/BarbosaSantosDev/abaku-erp-architecture"><b>Abaku</b></a><br/>
      ERP/PDV para bares, restaurantes e mercados pequenos, migrando um sistema em Visual FoxPro para Python. Emite NFC-e em produção, roda como SaaS com um banco PostgreSQL por cliente e tem PDV desktop em JavaFX que continua vendendo sem internet.<br/><br/>
      <sub>Python · FastAPI · PostgreSQL · Java · JavaFX · React · código privado</sub>
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/BarbosaSantosDev/labelflow-architecture"><b>LabelFlow</b></a><br/>
      SaaS de etiquetas ZPL com códigos de barras GS1 para peixarias que reprocessam caixas de salmão. A impressão sai do navegador para a impressora Zebra por um agente local escrito em Go. Em produção com cliente pagante.<br/><br/>
      <sub>Python · FastAPI · MongoDB · PostgreSQL · Go · React · código privado</sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/BarbosaSantosDev/jobhound"><b>jobhound</b></a><br/>
      Agente que coleta vagas da Gupy, Nerdin e RemoteOK, extrai os dados de cada vaga com um LLM local e calcula o match com uma pontuação determinística no domínio. Avisa pelo Telegram.<br/><br/>
      <sub>Python · FastAPI · LangChain · Ollama · PostgreSQL · React · código aberto</sub>
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/BarbosaSantosDev/cofre-docs-backend"><b>cofre-docs</b></a><br/>
      API para guardar documentos PDF criptografados com envelope encryption e autenticação JWT.<br/><br/>
      <sub>Python · FastAPI · PostgreSQL · cryptography · código aberto</sub>
    </td>
  </tr>
</table>

---

## Stack

<details open>
  <summary><b>🧠 IA e LLMs</b></summary>
  <p>
    <img alt="LangChain" src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white">
    <img alt="LangGraph" src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square">
    <img alt="Langfuse" src="https://img.shields.io/badge/Langfuse-0E0F10?style=flat-square">
    <img alt="DeepEval" src="https://img.shields.io/badge/DeepEval-0E0F10?style=flat-square">
    <img alt="Gemini" src="https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white">
    <img alt="Ollama" src="https://img.shields.io/badge/Ollama-0E0F10?style=flat-square&logo=ollama&logoColor=white">
  </p>
</details>

<details open>
  <summary><b>⚙️ Backend e mensageria</b></summary>
  <p>
    <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
    <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white">
    <img alt="Go" src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white">
    <img alt="Java" src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white">
    <img alt="RabbitMQ" src="https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white">
    <img alt="PGMQ" src="https://img.shields.io/badge/PGMQ-4169E1?style=flat-square">
    <img alt="Behave" src="https://img.shields.io/badge/BDD-Behave%20%2F%20Gherkin-23D96C?style=flat-square&logo=cucumber&logoColor=white">
  </p>
</details>

<details open>
  <summary><b>🗄️ Dados</b></summary>
  <p>
    <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white">
    <img alt="MongoDB" src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white">
  </p>
</details>

<details open>
  <summary><b>🚀 Infra e observabilidade</b></summary>
  <p>
    <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
    <img alt="Kubernetes" src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white">
    <img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white">
    <img alt="Datadog" src="https://img.shields.io/badge/Datadog-632CA6?style=flat-square&logo=datadog&logoColor=white">
    <img alt="Linux" src="https://img.shields.io/badge/Linux-0E0F10?style=flat-square&logo=linux&logoColor=white">
  </p>
</details>

<details open>
  <summary><b>🖥️ Front-end</b></summary>
  <p>
    <img alt="React" src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB">
    <img alt="JavaFX" src="https://img.shields.io/badge/JavaFX-ED8B00?style=flat-square&logo=openjdk&logoColor=white">
  </p>
</details>

**Como organizo o código:** Clean Architecture · DDD · CQRS · BDD com cenários escritos antes da implementação.

---

<details>
  <summary><b>📊 Atividade no GitHub</b></summary>
  <br/>
  <p align="center">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/BarbosaSantosDev/BarbosaSantosDev/output/github-contribution-grid-snake-dark.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/BarbosaSantosDev/BarbosaSantosDev/output/github-contribution-grid-snake.svg">
      <img alt="animação do grid de contribuições" src="https://raw.githubusercontent.com/BarbosaSantosDev/BarbosaSantosDev/output/github-contribution-grid-snake.svg" width="700">
    </picture>
  </p>
  <p align="center">
    <img alt="Estatísticas do GitHub" height="165" src="https://github-readme-stats.vercel.app/api?username=BarbosaSantosDev&show_icons=true&count_private=true&include_all_commits=true&hide_border=true&bg_color=0E0F10&title_color=C6F135&icon_color=C6F135&text_color=F4F5F2">
    <img alt="Sequência de contribuições" height="165" src="https://streak-stats.demolab.com/?user=BarbosaSantosDev&hide_border=true&background=0E0F10&ring=C6F135&fire=C6F135&currStreakLabel=C6F135&sideLabels=F4F5F2&currStreakNum=F4F5F2&sideNums=F4F5F2&dates=8A8D88&locale=pt_BR">
  </p>
  <p align="center"><sub>Os números refletem só o código público. Os sistemas principais estão em repositórios privados.</sub></p>
</details>

<p align="center">
  <sub>Aberto a conversas sobre backend Python, agentes de IA e projetos PJ · <a href="mailto:joaovitorbarbosa513@gmail.com">joaovitorbarbosa513@gmail.com</a></sub>
</p>
