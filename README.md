# 📝 WordPress Auto Post com OpenAI via n8n

Projeto de automação que cria e publica automaticamente artigos otimizados para SEO no WordPress usando **n8n**, **OpenAI**, **Google Sheets** e **LangChain**.

---

## 🚀 Funcionalidades

- 🔍 Lê palavras-chave e produtos de uma Google Sheet
- 🤖 Usa OpenAI GPT-4o para gerar:
  - Título
  - Introdução HTML
  - Texto "como escolher"
  - Agrupamento de produtos em 3 a 5 categorias com HTML otimizado
  - Links internos
  - FAQ com perguntas reais buscadas no Google
  - Meta description
- 🛠️ Monta todo o conteúdo final com HTML estruturado
- ✅ Publica automaticamente como **rascunho** no WordPress via API

---

## 🧰 Tecnologias Utilizadas

- [n8n.io](https://n8n.io) – Plataforma de automação
- [OpenAI API](https://platform.openai.com/) – Geração de conteúdo (GPT-4o)
- [Google Sheets API](https://developers.google.com/sheets/api) – Fonte de dados
- [WordPress REST API](https://developer.wordpress.org/rest-api/) – Publicação de posts
- Redis (opcional) – Armazenamento temporário de contexto
- LangChain Agent Node – Para prompt modular e gerenciável

---

## 📂 Estrutura do Fluxo

1. 🔄 Trigger manual (`Manual Trigger`)
2. 📄 Lê dados da planilha: `Keyword`, `Produtos`, `Links`
3. 🧠 Passa por nós OpenAI para:
   - Criar título
   - Criar introdução
   - Explicar como escolher
   - Agrupar produtos em categorias
   - Gerar links internos
   - Gerar FAQ
   - Criar meta description
4. 🧱 Todos os blocos são processados em JSON → HTML
5. 📤 Publicação via WordPress API (`status: draft`)

---

## 📌 Requisitos

- Conta OpenAI com GPT-4o ativado  
- Conta Google com permissão para a planilha  
- API do WordPress ativada  
- n8n self-hosted ou com acesso à conta

---

## 🎯 Objetivo

Ajudar produtores de conteúdo e afiliados a criarem artigos otimizados e estruturados com rapidez, reduzindo o trabalho manual e aumentando o alcance orgânico.

---

## 👨‍💻 Autor

**Pedro Lucas Tomazeti Fernandes**  
📧 pltf8001@gmail.com  
📍 Maranhão – Brasil  
🔗 [LinkedIn](www.linkedin.com/in/pedro-lucas-tomazeti-fernandes-5a35b6320)
---

## 📜 Licença

MIT
