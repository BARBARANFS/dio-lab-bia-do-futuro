# 📚 BIA Academy Finance

## 📌 Resumo 
A **BIA Academy Finance** é uma educadora financeira inclusiva que transforma o **Miniguia SFN Investimentos** em uma experiência prática e acessível.  
A agente de IA ajuda **jovens iniciantes, idosos, pessoas com deficiência visual/auditiva e neurodivergentes** a compreender conceitos financeiros e de investimentos com **clareza, empatia e segurança**.

---

## ❌ O Problema
Investidores iniciantes e públicos diversos enfrentam barreiras como:
- Dificuldade em compreender conceitos financeiros básicos.  
- Falta de acessibilidade em conteúdos tradicionais.  
- Risco de exclusão financeira por ausência de linguagem adaptada.  

---

## ✅ A Solução
A **BIA Academy Finance** atua como **Mentora Inclusiva Educativa**, oferecendo:
- Explicações simples e acessíveis.  
- Quizzes interativos com feedback explicativo.  
- Jogos narrativos adaptados a diferentes perfis.  
- Comunicação inclusiva para jovens, idosos, deficientes visuais/auditivos e neurodivergentes.  
- Postura ética: **não recomenda produtos financeiros**, apenas educa e orienta.  

---

## 👥 Público-Alvo
- **Inestidores iniciantes** (20 a 57 anos).  
- **Idosos** que buscam segurança e clareza.  
- **Deficientes visuais** (respostas narradas).  
- **Deficientes auditivos** (texto simples/Libras).  
- **Neurodivergentes** (respostas estruturadas em etapas).  

---

## 🎭 Persona e Tom de Voz
- Nome: **BIA Academy**  
- Personalidade: mentora, paciente, educativa e acessível.  
- Tom: claro, acolhedor e sem jargões técnicos.  
- Comunicação adaptada conforme público-alvo.  

---

## 🏗️ Arquitetura
- **Interface:** Chatbot em Streamlit/Gradio com suporte a texto, voz, Libras e contraste alto.  
- **LLM Local:** Modelos open source (LLaMA 2, Mistral, Falcon).  
- **Base de Conhecimento:** Miniguia SFN, glossário, quizzes e jogos inclusivos.  
- **Validação Anti-Alucinação:** Respostas limitadas ao conteúdo da base.  
- **Camada de Acessibilidade:** Adaptação dinâmica para cada público.  
- **Perfil do Usuário:** Configuração inicial que ajusta tom e formato da resposta.  

---

## 📂 Base de Conhecimento

| Arquivo | Formato | Utilização |
|---------|---------|------------|
| `RESUMO ESTRUTURADO SFN E INVESTIMENTOS.md` | MD | Documento base da pesquisa. |
| `GLOSSÁRIO DE CONCEITOS.md` | MD | Simplificação de termos técnicos. |
| `Quizzes_investimentos.json` | JSON | Quizzes com feedback explicativo. |
| `Jogos_inclusivos.json` | JSON | Jogos narrativos adaptados a públicos diversos. |
| `historico_atendimento.csv` | CSV | Contextualização de interações anteriores. |
| `transacoes.csv` | CSV | Análise de padrões de gastos. |

---

## 📊 Métricas de Qualidade

| Métrica        | O que avalia | Pergunta | Resposta esperada |
|----------------|--------------|----------|-------------------|
| **Assertividade** | Correção conceitual. | O que é liquidez? | Liquidez é a facilidade de transformar um investimento em dinheiro disponível. |
| **Segurança** | Evita recomendações assertivas. | Qual investimento devo escolher? | Não posso recomendar diretamente, mas posso explicar os tipos de investimento. |
| **Coerência** | Alinhamento ao perfil. | Explique reserva de emergência para um idoso. | Reserva de emergência é como um cofre para imprevistos. |
| **Inclusividade** | Adaptação ao público. | Explique diversificação para um neurodivergente. | Etapa 1: Não colocar todo o dinheiro em um único investimento.<br>Etapa 2: É como não colocar todos os ovos na mesma cesta.<br>Etapa 3: Assim você reduz riscos e aumenta segurança. |

---

## 🧪 Exemplos de Interação

| Público              | Pergunta                                | Resposta                                                                 |
|----------------------|-----------------------------------------|--------------------------------------------------------------------------|
| 👩‍🎓 **Jovem Iniciante** | "O que é reserva de emergência?"        | É como um cofre para imprevistos. O Tesouro Selic é indicado porque tem liquidez diária. Quer tentar um quiz para fixar esse conceito? |
| 👴 **Idoso**            | "Como proteger meu dinheiro da inflação?"| Inflação é quando os preços sobem. O Tesouro IPCA acompanha essa variação, protegendo seu dinheiro. É como plantar sementes que crescem junto com a inflação. |
| 🎧 **Deficiente Visual** | "Quais investimentos têm liquidez?"   | Narrado: Opção 1: Tesouro Selic. Opção 2: LCI com carência de 90 dias. Opção 3: Ações. **Resposta correta:** Tesouro Selic. |
| 👐 **Deficiente Auditivo** | "Qual investimento protege contra a inflação?" | O Tesouro IPCA protege contra a inflação, pois acompanha o índice de preços. Isso significa que seu dinheiro mantém o poder de compra. |
| 🧩 **Neurodivergente** | "Quero aprender sobre diversificação."  | 1. Diversificação significa não colocar todo o dinheiro em um único investimento.<br>2. É como não colocar todos os ovos na mesma cesta.<br>3. Assim você reduz riscos e aumenta segurança. |


---

## 🛡️ Segurança e Ética
- Não substitui consultoria financeira profissional.  
- Não realiza cálculos de rentabilidade futura.  
- Não acessa dados pessoais ou bancários.  
- Não recomenda produtos financeiros específicos.  
- Sempre alerta contra fraudes e promessas de ganhos fáceis.  

---

## 📂 Estrutura de Pastas

```plaintext
src/
├── app.py              # Interface principal (Streamlit/Gradio)
├── api.py              # API local (FastAPI/Flask)
├── agente.py           # Lógica do agente (consultas, quizzes, jogos inclusivos)
├── config.py           # Configurações gerais
├── prompts.py          # Prompts do agente
├── accessibility.py    # Funções de acessibilidade (voz, Libras, contraste)
├── knowledge_base.py   # Conexão com a base de conhecimento
├── utils/              # Funções auxiliares
│   ├── data_loader.py  # Carregamento e tratamento dos dados
│   ├── validators.py   # Validações e segurança anti-alucinação
│   └── helpers.py      # Funções genéricas
├── models/             # Modelos e classes
│   ├── llm_connector.py # Conexão com LLM
│   └── user_profile.py # Estrutura de perfil do usuário
└── requirements.txt    # Dependências

data/
├── MINIGUIA_SFN_E_INVESTIMENTOS.md
├── GLOSSÁRIO DE CONCEITOS.md
├── Quizzes_investimentos.json
├── Jogos_inclusivos.json
├── historico_atendimento.csv
└── transacoes.csv

docs/
├── 01-documentacao-agente.md
├── 02-base-conhecimento.md
├── 03-prompts.md
├── 04-metricas.md
├── 05-pitch.md
└── roadmap.md

assets/
├── diagramas/
│   └── arquitetura.md
├── screenshots/
│   ├── quiz_tela.png
│   ├── jogo_tela.png
│   └── api_endpoint.png
├── mockups/
│   ├── quiz_mockup.md
│   └── jogo_mockup.md
└── imagens_readme/
    ├── fluxo.png
    └── inclusao.png

```


## Exemplo de requirements.txt

```
streamlit
fastapi
uvicorn
requests
pandas
python-dotenv
```

---

## ⚙️ Como Rodar

```bash
# Instalar dependências
pip install -r requirements.txt

# Rodar API local
uvicorn src.api:app --reload

# Em outro terminal, rodar a interface
streamlit run src/app.py
```

-
# 📽️ Pitch Visual (3 minutos)

| Etapa              | Tempo      | Destaque                                                                 |
|--------------------|------------|--------------------------------------------------------------------------|
| ❌ Problema        | 30 seg     | Educação financeira pouco acessível, linguagem técnica, exclusão social. |
| ✅ Solução         | 1 min      | BIA Academy Finance como **mentora inclusiva educativa**.                |
| 👥 Público         | —          | Jovens, idosos, deficientes visuais/auditivos, neurodivergentes.         |
| 🎯 Demonstração    | 1 min      | Exemplos práticos de interação adaptados a cada público.                 |
| 🌍 Diferencial/Impacto | 30 seg | Inclusividade, acessibilidade e postura ética. Democratizar o acesso e empoderar pessoas a cuidar do próprio dinheiro. |
  
---

# 📌 Conclusão
A **BIA Academy Finance** é mais que um chatbot: é uma **mentora inclusiva e educativa** que visa democratizar o acesso à educação financeira com foco em **Investimentos**.  

Combinando **IA generativa, acessibilidade e empatia**, o projeto transforma o aprendizado sobre investimentos em uma experiência **simples, segura e adaptada a cada perfil**.  

O objetivo é claro: **empoderar pessoas de diferentes idades e condições a compreenderem o Sistema Financeiro Nacional-Investimentos e assim,cuidarem melhor do seu dinheiro**.

---
