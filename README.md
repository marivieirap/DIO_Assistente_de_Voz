# Assistente de Voz com IA (Whisper + ChatGPT + Python)

Projeto desenvolvido com base no artigo da DIO sobre criação de um assistente de voz utilizando IA, combinando **Speech-to-Text**, **Processamento de Linguagem Natural** e **Text-to-Speech**.
---

## 🚀 Sobre o Projeto

Este projeto implementa um assistente de voz capaz de:

* 🎙️ Capturar áudio do usuário
* 🧠 Transcrever fala em texto utilizando o Whisper
* 🤖 Gerar respostas inteligentes com IA
* 🔊 Converter respostas em áudio

A solução permite uma comunicação completa por voz, inclusive com suporte a múltiplos idiomas.

---

## 🧠 Arquitetura da Solução

O projeto foi estruturado em **4 etapas principais**:

### 1. 🎙️ Captura de Áudio

Gravação do áudio diretamente pelo navegador utilizando APIs web e processamento via Python.

### 2. 🧾 Speech-to-Text com Whisper

Utilização do modelo Whisper para transcrição de áudio em texto.

> O Whisper é um sistema de reconhecimento de fala treinado com centenas de milhares de horas de dados multilíngues, sendo altamente robusto a sotaques e ruídos. ([OpenAI][1])

---

### 3. 🤖 Integração com IA (ChatGPT)

Envio do texto transcrito para um modelo de linguagem que gera respostas coerentes e contextuais.

---

### 4. 🔊 Text-to-Speech com gTTS

Conversão da resposta em texto para áudio utilizando a biblioteca gTTS.

---

## 🔄 Fluxo do Sistema

```mermaid
graph LR
A[Áudio] --> B[Whisper (STT)]
B --> C[ChatGPT]
C --> D[gTTS (TTS)]
D --> E[Áudio de resposta]
```

---

## 🧰 Tecnologias Utilizadas

* Python
* Google Colab
* Whisper (OpenAI)
* OpenAI API (ChatGPT)
* gTTS (Google Text-to-Speech)

---

## ⚙️ Como Executar

1. Clone o repositório:

```id="proj02"
git clone https://github.com/marivieirap/DIO_Assistente_de_Voz.git
```

2. Abra o notebook no Google Colab

3. Instale as dependências:

```id="proj03"
pip install openai gtts whisper
```

4. Configure sua API Key (de forma segura):

```python id="proj04"
from getpass import getpass
import os

os.environ["OPENAI_API_KEY"] = getpass("Digite sua API Key: ")
```

5. Execute as células do notebook

---

## 🔐 Segurança

⚠️ Nunca exponha sua API Key no código.

* Utilize variáveis de ambiente
* Revogue chaves expostas
* Não suba credenciais para o GitHub

---

## 💡 Aplicações

Este projeto pode ser utilizado como base para:

* Assistentes virtuais
* Chatbots por voz
* Sistemas de acessibilidade
* Automação residencial
* Transcrição de áudio em tempo real

---

## 📌 Contexto do Projeto

Este projeto foi inspirado no artigo:

👉 Digital Innovation One – *Conversando por Voz com o ChatGPT utilizando Whisper e Python*

O artigo demonstra como integrar tecnologias de voz e IA para criar experiências conversacionais completas. ([DIO][2])

---


[1]: https://openai.com/pt-BR/index/whisper/?utm_source=chatgpt.com "Apresentamos o Whisper | OpenAI"
[2]: https://www.dio.me/articles/conversando-por-voz-com-o-chatgpt-utilizando-whisper-openai-e-python?utm_source=chatgpt.com "Conversando Por Voz Com o ChatGPT Utilizando Whisper (OpenAI) e Python | Venilton FalvoJr | Inteligência Artificial (IA) | Machine Learning | Python | DIO"
