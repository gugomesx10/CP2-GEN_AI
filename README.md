# CP2 — Assistente de IA Generativa para Suporte Técnico de IoT

**FIAP | Análise e Desenvolvimento de Sistemas**

**Disciplina:** Disruptive Architectures: IoT, IoB & Generative AI

## Integrantes

| Nome | RM |
|---|---|
| Gustavo Gomes Martins | 555999 |
| Matheus de Mattos Vecchi | 561716 |
| Nicholas Albuquerque Buzo | 561082 |
| Nicholas Camillo Canadas de Paula | 561262 |

## Sobre o projeto

O **IoT Tech Support** é um assistente de inteligência artificial especializado em suporte técnico para dispositivos IoT, incluindo ESP32, Arduino, sensores e conexões Wi-Fi.

O projeto utiliza o Google Gemini 3.5 Flash-Lite para responder dúvidas técnicas, identificar possíveis falhas e orientar usuários de maneira clara e objetiva.

A implementação foi desenvolvida no Google Colab, utilizando Python, Google Gemini API, Gradio e FastAPI.

## Tecnologias utilizadas

- Python
- Google Gemini 3.5 Flash-Lite
- Google Colab
- Gradio
- FastAPI e Uvicorn
- API REST

## System Prompt

O assistente foi configurado para atuar exclusivamente em suporte técnico de IoT, respondendo em português, utilizando até cinco frases e evitando orientações tecnicamente inseguras.

Perguntas fora do tema devem ser recusadas educadamente.

## Etapas desenvolvidas

| Etapa | Descrição | Status |
|---|---|---|
| 1 | Guardrails e restrições de tema | Concluída |
| 2 | Comparação de temperaturas 0.0 e 1.0 | Concluída |
| 3 | Chat com memória e limpeza de histórico | Concluída |
| 4 | Interface web Gradio com slider | Concluída |
| 5 | API REST com sessões independentes | Concluída (bônus) |

## Resultados

**Guardrails:** O Gemini respeitou as restrições de tema e formato, recusando perguntas fora de IoT.

**Temperatura:** As temperaturas 0.0 e 1.0 produziram respostas tecnicamente semelhantes, com pequenas variações de linguagem e detalhamento.

**Memória:** O assistente recuperou informações anteriores e deixou de utilizá-las após a limpeza do histórico.

**Interface Gradio:** A interface permitiu enviar perguntas e ajustar a temperatura do Gemini.

**API REST:** As sessões foram isoladas com `session_id`. A sessão A recuperou corretamente o nome Gustavo e o dispositivo ESP32, enquanto a sessão B não possuía essas informações.

## Interface Gradio

A interface foi testada com diferentes temperaturas, permitindo comparar as respostas geradas pelo Gemini.

![Interface Gradio - Print 1](Screenshot%202026-10-07%20215942.png)

![Interface Gradio - Print 2](Screenshot%202026-10-07%20215946.png)

## Notebook

[Visualizar notebook do Checkpoint 2](CP2_ia_generativa.ipynb)

## Execução

1. Abrir o notebook no Google Colab.
2. Configurar `GEMINI_API_KEY` nos Secrets do Colab.
3. Executar as células em ordem.
4. Testar os guardrails, as temperaturas, o histórico e a interface Gradio.
5. Executar os testes de sessões independentes da API REST.

As credenciais de acesso não devem ser publicadas no repositório.
