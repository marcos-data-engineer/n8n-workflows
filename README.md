# ⚡ n8n Workflows: Enterprise Data & AI Automation

<p align="center">
  <img src="https://img.shields.io/badge/n8n-Self--Hosted-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n" />
  <img src="https://img.shields.io/badge/Docker-Containers-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Fedora-44_Workstation-51A2DA?style=for-the-badge&logo=fedora&logoColor=white" alt="Fedora" />
  <img src="https://img.shields.io/badge/Ollama-Local_LLM-000000?style=for-the-badge&logo=ollama&logoColor=white" alt="Ollama" />
  <img src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" alt="License" />
</p>

Coleção de workflows reutilizáveis e pipelines de automação para o **n8n (Self-Hosted)**, focados em Engenharia de Dados, automação de processos corporativos e soluções de **IA Privada (Private AI)** com conformidade à LGPD.

---

## 🛠️ Stack Técnica & Ambiente Host

* **Orquestração de Workflows:** n8n Self-Hosted
* **Ambiente de Execução:** Fedora Workstation 44
* **Conteinerização:** Docker & Docker Compose
* **Infraestrutura de IA:** Ollama local (`qwen2.5`, `llama3.2`)
* **Linguagens & Formatos:** JSON, Python, Bash, SQL

---

## 📁 Estrutura do Repositório

```text
n8n-workflows/
├── workflows/
│   └── ia-local/
│       └── workflow-geracao-codigo-qwen2.5.json  # Geração e análise de código local via Ollama
├── .gitignore
└── README.md
🚀 Workflows Disponíveis
🧠 IA Local & Automação Privada (/workflows/ia-local)
Geração de Código com Qwen 2.5: Fluxo automatizado no n8n conectado à API do Ollama local executando o modelo qwen2.5. Permite processar requisições de código e análise técnica sem tráfego de dados para APIs proprietárias na nuvem.

⚙️ Como Importar e Executar
1. Pré-requisitos
Certifique-se de ter o Docker e o Ollama rodando no seu ambiente local:

Bash
# Baixar o modelo Qwen 2.5 no Ollama
ollama pull qwen2.5
2. Subir o n8n via Docker
Bash
docker run -d \
  --name n8n \
  -p 5678:5678 \
  -v n8n_data:/home/node/.n8n \
  docker.n8n.io/n8nio/n8n
3. Importar o Workflow
Acesse o painel do n8n em http://localhost:5678.

Clique em Workflows > Import from File.

Selecione o arquivo .json desejado dentro do diretório workflows/ia-local/.

Ajuste os nós de credenciais/HTTP Request para apontar para a URL do seu Ollama local (http://host.docker.internal:11434 ou IP da sua interface Docker).

🔒 Privacidade & Compliance (LGPD)
Todos os fluxos contidos nesta pasta foram desenvolvidos sob a premissa de Private AI (IA On-Premise). Os dados processados pelos nós do n8n e modelos do Ollama permanecem restritos à máquina/servidor local, garantindo zero vazamento de informações sensíveis.

👨‍💻 Autor
Marcos Vasconcellos de Andrade

Senior Linux Infrastructure, Automation & Data Architecture Specialist

Blog: Data Architecture & AI Insights

LinkedIn: linkedin.com/in/marcos-vasconcellos-de-andrade-098b07297

GitHub: @marcos-data-engineer

⭐ Se este repositório for útil para seus projetos de automação, considere deixar uma estrela!


<FollowUp>
Gostaria que eu gerasse também um arquivo `docker-compose.yml` pré-configurado com n8n e Ollama no mesmo barramento para você adicionar na raiz deste repositório?
</FollowUp>

<ElicitationsGroup>
</ElicitationsGroup>
