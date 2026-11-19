# 🤖 Agent Foundry: Engenharia e Construção de Agentes com Google ADK

Material da palestra apresentada no **DevFest João Pessoa 2026** (20 e 21/11/2026).

Este repositório foi montado para você conseguir **reproduzir os exemplos em casa**, mesmo que nunca tenha criado um agente de IA antes.

---

## 📦 O que tem neste repositório

| Arquivo | O que é |
|---|---|
| `ADK_DevFestJoão Pessoa_Ahirton.pptx` | Os slides da palestra (agentes, blocos do Google ADK, MCP, A2A, estudo de caso e guardrails) |
| `demo_devfest_joao_pessoa.ipynb` | **Notebook único da demo**: FunctionTool, Sessions, Agent-as-a-Tool, LoopAgent e "quebrar um agente" |

▶️ Abrir direto no Google Colab (não precisa instalar nada na sua máquina):

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ahirtonlopes/devfest-joao-pessoa-2026/blob/main/demo_devfest_joao_pessoa.ipynb) **Notebook da demo**

---

## 🚀 Comece por aqui (passo a passo para iniciantes)

### 1. Gere sua API key do Google AI Studio

1. Acesse https://aistudio.google.com/app/apikey com sua conta Google.
2. Clique em **"Create API key"** e copie a chave.

### 2. Abra o notebook no Colab

Use o botão **"Open in Colab"** acima. Depois salve uma cópia sua: `Arquivo → Salvar uma cópia no Drive`.

### 3. Guarde a chave no Colab

1. No menu lateral esquerdo do Colab, clique no ícone de **chave (🔑 Secrets)**.
2. Crie um secret chamado `GOOGLE_API_KEY`, cole sua chave e habilite o acesso do notebook.

### 4. Rode as células na ordem

Execute célula por célula (`Shift+Enter`), da Parte 0 até a Parte 5.

---

## 🧠 O que você vai aprender

- **Parte 1, FunctionTool:** uma função Python comum vira ferramenta do agente (o exemplo consulta o clima de João Pessoa em tempo real).
- **Parte 2, Sessions:** a diferença entre um agente que lembra da conversa e um com amnésia.
- **Parte 3, Agent-as-a-Tool:** um agente especialista dentro de outro agente.
- **Parte 4, LoopAgent:** planejar, criticar e refinar, com uma regra de negócio verificável e um teto de iterações.
- **Parte 5, Quebrar um agente:** o risco de *excessive agency*, a validação de entrada que falta e a trava no código que resolve.

O exemplo da Parte 4 é uma versão em miniatura do estudo de caso da palestra: um orquestrador multiagente que transforma uma solicitação de vendas em proposta comercial para spots publicitários.

---

## 💡 Dicas sobre modelos e limites gratuitos

- Os exemplos usam por padrão o **`gemini-3.5-flash-lite`**. Para trocar de modelo, edite a variável `MODEL_NAME`, definida em uma única célula, logo no início do notebook.
- O plano gratuito do AI Studio limita as chamadas por minuto, e os limites variam por modelo. Se aparecer o erro **`429 RESOURCE_EXHAUSTED`**, espere cerca de um minuto e rode a célula de novo. Se precisar, aumente a variável `PAUSA` na Parte 2.
- A versão do ADK está fixada em `google-adk==2.13.0` para os exemplos se comportarem igual em qualquer dia. No ADK 2.x, `SequentialAgent` e `LoopAgent` aparecem como deprecados em favor de `Workflow`: continuam funcionando, e o notebook silencia o aviso.
- Na Parte 5, o comportamento do modelo varia de uma execução para outra (às vezes ele se autolimita, às vezes não). Por isso o notebook termina com uma tabela que chama as ferramentas **direto, sem modelo**: a trava no código não depende do humor do modelo.

---

## 🙏 Créditos

- Os exemplos das Partes 1 a 4 seguem a estrutura didática do material **ADK Adventure**, criado por [Qingyue (Annie) Wang](https://www.linkedin.com/in/anniewangtech/), Developer Advocate no Google, e foram reescritos para João Pessoa e para o estudo de caso da palestra.
- A Parte 5 vem da demo de guardrails apresentada no DevFest Natal 2026.
- [Google Agent Development Kit (ADK)](https://google.github.io/adk-docs/) e [Gemini API](https://ai.google.dev/).
- [OWASP GenAI Security Project](https://genai.owasp.org/).

Os dados dos exemplos (empresa de logística, pedidos, regras comerciais) são **fictícios**.

## 👋 Fale comigo

**Ahirton Lopes, PhD** - AI/ML/GenAI

- LinkedIn: https://www.linkedin.com/in/ahirtonlopes
- GitHub: https://github.com/ahirtonlopes
- X: https://x.com/ahirtonlopes
