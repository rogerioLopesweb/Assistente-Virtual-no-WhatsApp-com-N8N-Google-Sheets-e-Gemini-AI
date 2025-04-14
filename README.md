# 🤖 Assistente Virtual no WhatsApp com N8N, Google Sheets e Gemini AI

Este projeto é um fluxo desenvolvido no [N8N](https://n8n.io/) que transforma o WhatsApp em um assistente virtual inteligente, criativo e carismático. Utilizando integração com **Google Sheets**, **Mega API** e **Google Gemini AI**, ele oferece uma experiência automatizada e humanizada de interação com usuários via mensagens no WhatsApp.

---

## 🚀 Funcionalidades

- 📥 **Recebimento de mensagens via Webhook**
- 🔎 **Validação de mensagens (exclui grupos, automatizadas e mensagens do próprio bot)**
- 📋 **Extração e registro de informações do usuário (nome, número, horário, mensagem)**
- 📊 **Integração com Google Sheets para busca e atualização de cadastro**
- 🤖 **Resposta personalizada com IA usando Google Gemini**
- 📤 **Envio de mensagens via Mega API diretamente no WhatsApp**

---

## 📌 Como Funciona

1. **Webhook**
   - Captura mensagens recebidas via API do WhatsApp.

2. **Validação de Condições**
   - Verifica se a mensagem não é de grupo, broadcast ou enviada pelo próprio bot.

3. **Extração de Informações**
   - Nome, número de celular, horário e texto da mensagem são processados.

4. **Consulta e Atualização no Google Sheets**
   - O número é usado como identificador para buscar e atualizar registros na planilha.

5. **IA com Gemini**
   - O texto do usuário é processado e respondido com criatividade e bom humor.

6. **Envio de Mensagem**
   - A resposta gerada é enviada de volta via Mega API no WhatsApp.

---

## 🛠️ Tecnologias Utilizadas

- [N8N](https://n8n.io/) (Automação no-code)
- [Google Sheets](https://www.google.com/sheets/about/)
- [Mega API WhatsApp](https://megaapi.com.br/)
- [Google Gemini (IA generativa)](https://deepmind.google/technologies/gemini/)

---

## 🧠 Fluxo Resumido

```plaintext
[Webhook] ➝ [Validação de mensagem] ➝ [Extração de dados]
        ➝ [Consulta no Google Sheets]
          ↳ (Novo usuário) ➝ [Cria registro]
          ↳ (Existente) ➝ [Atualiza registro]
        ➝ [Envia dados para IA Gemini]
        ➝ [Recebe resposta] ➝ [Envia via Mega API]
