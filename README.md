## 📘 gran-forum-n8n

**Projeto acadêmico** desenvolvido por **Jorgyvan Braga Lima** como parte da graduação em Sistemas de Informação.  
Este projeto consiste em um fórum inteligente com automações via **n8n**, notificações por **e-mail** e **WhatsApp**, além de integração com APIs de **vagas de emprego**.

---

## 📁 Estrutura do Repositório

```
gran-forum-n8n/
├── backend/              # API Express + Prisma
│   └── src/server.js     # Lógica principal do backend
├── frontend/
│   └── gran-forum-web/   # Interface web (Vite)
├── logs/                 # Logs e registros do sistema
├── n8n-flows/            # Workflows n8n (WhatsApp, e-mail, importação de vagas)
└── README.md             # Documentação do projeto
```

---

## 🚀 Funcionalidades

- 📬 Notificações por **e-mail** usando Nodemailer
- 📱 Notificações por **WhatsApp** via webhook do n8n
- 🧠 Integração com **IA Gemini** para respostas automáticas (via n8n)
- 🧵 Criação de **usuários**, **grupos**, **tópicos** e **respostas**
- 🔔 Assinatura de grupos para receber alertas
- 📦 Importação de **vagas de emprego** via API (Adzuna, Jooble etc.)
- 🌐 Frontend integrado via build do Vite
- 🧩 Backend em Node.js + Express + Prisma

---

## 🔧 Tecnologias Utilizadas

- **Node.js**
- **Express**
- **Prisma ORM**
- **Zod** (validação de dados)
- **Nodemailer**
- **n8n** (automação)
- **Vite** (frontend)
- **MySQL** (banco de dados)

---

## 📡 Endpoints principais

- `GET /api/groups` – Listar grupos
- `POST /api/users` – Criar usuário
- `POST /api/groups` – Criar grupo
- `POST /api/groups/:groupId/subscribe` – Assinar grupo
- `POST /api/groups/:groupId/threads` – Criar tópico (com notificação)
- `POST /api/threads/:threadId/replies` – Responder tópico
- `POST /api/webhooks/whatsapp` – Receber mensagens do WhatsApp via n8n
- `POST /api/jobs/import` – Importar vagas
- `GET /api/jobs` – Listar vagas

---

## 📌 Como rodar localmente

```bash
# Instalar dependências
npm install

# Configurar variáveis no .env
PORT=3001
SMTP_HOST=127.0.0.1
SMTP_PORT=1025
SMTP_SECURE=false
SMTP_USER=usuario
SMTP_PASS=senha
FROM_EMAIL=no-reply@forum.local
N8N_WHATSAPP_WEBHOOK=https://seu-webhook.com

# Rodar servidor
node src/server.js
```

---

## 🎓 Objetivo acadêmico

Este projeto visa demonstrar a aplicação de automações inteligentes em sistemas web, com foco em **comunicação multicanal**, **integração de APIs externas** e **uso de IA** para suporte a usuários em fóruns online.
 
