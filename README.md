# 🤖 Assistente Virtual Multimodal no WhatsApp com n8n, Supabase, Google Sheets, Mega API, OpenAI e Gemini

Este projeto é um fluxo automatizado desenvolvido no **n8n**, que transforma o WhatsApp em um **assistente virtual inteligente, criativo e multimodal**, capaz de entender e responder mensagens de texto, voz e imagem com IA generativa. Utiliza integração com **Supabase, Google Sheets, Mega API, OpenAI e Gemini AI**, proporcionando uma experiência automatizada, personalizada e interativa via WhatsApp.

---
![image](https://github.com/user-attachments/assets/358ffa9d-3757-4688-be04-22e73130edf0)


## 🚀 Funcionalidades

- 📥 Recebimento de mensagens via Webhook (MegaAPI)
- 🧹 Filtro inicial para ignorar grupos, automações e mensagens do próprio bot
- 📋 Extração de dados do usuário: nome, telefone, tipo e conteúdo da mensagem
- 🧠 Identificação do tipo da mensagem: texto, imagem, áudio ou vídeo
- 📊 Consulta e registro de clientes via **Supabase**
- 📝 Atualização ou criação de cadastro automaticamente
- 🤖 Resposta inteligente com **Google Gemini** e **OpenAI (GPT-3.5 e GPT-4o)**
- 🖼️ Análise de imagem via OpenAI Vision (GPT-4o)
- 🔊 Transcrição de áudio com **Whisper (OpenAI)**
- 🎙️ Conversão de texto para áudio com IA (TTS) + envio em ptt
- 📤 Respostas multimodais (texto ou áudio) via **MegaAPI WhatsApp**
- 🧠 Contexto conversacional com memória por número de telefone

---

## 🧠 Como Funciona – Etapas do Fluxo

1. **[Webhook]**  
   Recebe mensagens do WhatsApp via MegaAPI.

2. **[Validação de Mensagem]**  
   Filtra mensagens de grupos, automações e o próprio bot.

3. **[Extração de Dados]**  
   Nome do usuário, telefone, conteúdo e tipo da mensagem.

4. **[Consulta Supabase]**  
   Verifica se o número está cadastrado. Se não estiver, cria automaticamente.

5. **[Classificação da Mensagem]**  
   Identifica se é texto, imagem, áudio ou vídeo e direciona o tratamento.

6. **[Processamento da Entrada]**  
   - **Texto:** enviado diretamente para IA  
   - **Imagem:** convertida, analisada e interpretada com IA  
   - **Áudio:** descriptografado, convertido, transcrito com IA

7. **[Geração de Resposta]**  
   IA responde com humor, persuasão ou criatividade, com base em prompt pré-definido.

8. **[Resposta Final]**  
   Envio por texto ou por áudio (ptt gerado com TTS e formatado em base64)

---

## 🛠️ Tecnologias Utilizadas

- **n8n** – automação visual low-code  
- **Supabase** – banco de dados de usuários  
- **Google Sheets** – alternativa leve de consulta e histórico  
- **MegaAPI WhatsApp** – recepção e envio de mensagens  
- **Google Gemini** – IA generativa para texto e imagem  
- **OpenAI (GPT + Whisper)** – transcrição, texto e imagem  
- **OpenAI Vision (GPT-4o)** – análise de imagem multimodal  
- **LangChain Memory** – para manter contexto de conversas  

---

## 🧩 Fluxo Visão Geral

```
[Webhook WhatsApp] ➝ [Validação] ➝ [Consulta Supabase]  
     ↳ [Novo usuário?] ➝ [Criação automática]  
     ↳ [Mensagem Texto] ➝ [Gemini IA → Texto]  
     ↳ [Mensagem Imagem] ➝ [Download → Análise com GPT-4o]  
     ↳ [Mensagem Áudio] ➝ [Download → Transcrição (Whisper)]  
     ➝ [Resposta IA → Texto ou Áudio] ➝ [Envio via MegaAPI]
```
