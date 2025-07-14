# Azure Speech Studio e Language Studio: O que são, Problemas que Resolvem e Como Usar

## ✅ O que é o Azure Speech Studio?

O Azure Speech Studio é uma plataforma da Microsoft baseada em IA para criar aplicações com **reconhecimento de fala**, **síntese de voz** e **tradução de fala em tempo real**.

### 💡 Problemas que Resolve:
- Transcrição automática de reuniões, entrevistas e áudios.
- Criação de bots com entrada de voz.
- Leitura automática de textos com voz natural (TTS).
- Tradução multilíngue para atendimento global.

---

## ✅ O que é o Azure Language Studio?

O Azure Language Studio oferece recursos de **processamento de linguagem natural (NLP)** para analisar textos, classificar sentimentos, extrair entidades, traduzir e responder perguntas.

### 💡 Problemas que Resolve:
- Classificação de sentimentos (positivo/negativo).
- Análise de opiniões de clientes.
- Extração de dados relevantes em textos longos.
- Respostas automáticas com IA (tipo ChatGPT).
- Identificação de tópicos em grandes volumes de texto.

---

## 🔧 Exemplos Práticos

### 🔹 Exemplo 1 – Speech Studio
**Problema:** Gravar uma reunião e obter a transcrição automática.  
**Solução:** Usar o Speech-to-Text para converter o áudio em texto em tempo real.  
**Resultado esperado:** Arquivo `.txt` com a fala de cada participante separada por tempo.

### 🔹 Exemplo 2 – Speech Studio com TTS
**Problema:** Criar um assistente virtual com voz natural.  
**Solução:** Usar Text-to-Speech (TTS) com vozes neurais em português.  
**Resultado esperado:** Arquivo `.mp3` ou resposta de API com fala sintetizada.

### 🔹 Exemplo 3 – Language Studio
**Problema:** Detectar emoções em comentários de clientes.  
**Solução:** Usar análise de sentimentos em lote.  
**Resultado esperado:** Lista com polaridade de cada comentário (positivo, neutro, negativo).

### 🔹 Exemplo 4 – Language Studio QnA
**Problema:** Criar um chatbot com perguntas e respostas sobre um produto.  
**Solução:** Usar o recurso "Question Answering" com seus próprios documentos.  
**Resultado esperado:** Chatbot capaz de responder perguntas com base no seu conteúdo.

---

## 🚀 Como Usar: Passo a Passo

### 1. Criar Conta no Azure
- Acesse [https://portal.azure.com](https://portal.azure.com)
- Faça login ou crie uma conta gratuita (ganha R$ 1.000 de crédito por 30 dias)

---

### 2. Criar um Recurso de **Speech** ou **Language**
- Vá em **Criar um recurso > IA + Machine Learning > Speech** ou **Language**
- Preencha:
  - Nome do recurso
  - Região (ex: Brazil South)
  - Plano de preço (pode ser gratuito)
- Clique em **Revisar + Criar > Criar**

---

### 3. Acessar o **Speech Studio** ou **Language Studio**
- Speech Studio: [https://speech.microsoft.com](https://speech.microsoft.com)
- Language Studio: [https://language.azure.com](https://language.azure.com)

---

## 🔧 Configurações Básicas

### Speech Studio
- Após criar o recurso, acesse **Speech Studio**
- Escolha uma ferramenta (Speech-to-Text, TTS, Translation)
- Faça upload de um áudio ou escreva um texto
- Defina o idioma e tipo de voz

### Language Studio
- Escolha entre:
  - Análise de Sentimentos
  - Extração de Entidades
  - Tradução
  - Perguntas e Respostas
- Faça upload de documentos ou digite textos
- Analise os resultados diretamente na interface

---

## 🔑 Onde Encontro as Chaves e Endpoints?
- Vá no **Portal do Azure**
- Acesse o recurso criado (Speech ou Language)
- Clique em **Chaves e Endpoint**
- Copie a **Chave 1** e o **Endpoint** para uso com API

---

📚 Links Úteis

Speech Studio: https://speech.microsoft.com

Language Studio: https://language.azure.com

Documentação oficial: https://learn.microsoft.com/pt-br/azure/cognitive-services/

Preços: https://azure.microsoft.com/pt-br/pricing/



## 🧪 Testar com API (Opcional)
Você pode usar ferramentas como Postman ou código com Python/JavaScript.

### Exemplo de chamada Speech-to-Text com curl:
```bash
curl -X POST "https://<seu-endpoint>/speechtotext/v3.0/transcriptions" \
-H "Ocp-Apim-Subscription-Key: <sua-chave>" \
-H "Content-Type: application/json" \
-d '{
  "contentUrls": ["https://seuarquivo.blob.core.windows.net/audio.mp3"],
  "locale": "pt-BR",
  "displayName": "Teste de Transcrição"
}'

