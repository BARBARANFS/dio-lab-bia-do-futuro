# 📚 BIA Academy Finance

## 📌 Resumo 
A **BIA Academy Finance** é uma educadora financeira inclusiva que transforma o **Miniguia SFN Investimentos** em uma experiência prática e acessível.  
Nosso agente de IA ajuda **jovens iniciantes, idosos, pessoas com deficiência visual/auditiva e neurodivergentes** a compreender conceitos financeiros e de investimentos com **clareza, empatia e segurança**.

---

## ❌ O Problema
Investidores iniciantes e públicos diversos enfrentam barreiras como:
- Dificuldade em compreender conceitos financeiros básicos.  
- Falta de acessibilidade em conteúdos tradicionais.  
- Risco de exclusão financeira por ausência de linguagem adaptada.  

---

## ✅ A Solução
A **BIA Academy Finance** atua como **mentora inclusiva**, oferecendo:
- Explicações simples e acessíveis.  
- Quizzes interativos com feedback explicativo.  
- Jogos narrativos adaptados a diferentes perfis.  
- Comunicação inclusiva para jovens, idosos, deficientes visuais/auditivos e neurodivergentes.  
- Postura ética: **não recomenda produtos financeiros**, apenas educa e orienta.  

---

## 👥 Público-Alvo
- **Jovens iniciantes** (20 a 57 anos).  
- **Idosos** que buscam segurança e clareza.  
- **Deficientes visuais** (respostas narradas).  
- **Deficientes auditivos** (texto simples/Libras).  
- **Neurodivergentes** (respostas estruturadas em etapas).  

---

## 🎭 Persona e Tom de Voz
- Nome: **BIA Academy**  
- Personalidade: consultiva, paciente, educativa e acessível.  
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

- **Jovem iniciante:**  
  Pergunta: "O que é reserva de emergência?"  
  Resposta: "É como um cofre para imprevistos. O Tesouro Selic é indicado porque tem liquidez diária. Quer tentar um quiz para fixar esse conceito?"

- **Idoso:**  
  Pergunta: "Como proteger meu dinheiro da inflação?"  
  Resposta: "Inflação é quando os preços sobem. O Tesouro IPCA acompanha essa variação, protegendo seu dinheiro. É como plantar sementes que crescem junto com a inflação."

- **Deficiente visual:**  
  Pergunta: "Quais investimentos têm liquidez?"  
  Resposta narrada: "Opção 1: Tesouro Selic. Opção 2: LCI com carência de 90 dias. Opção 3: Ações. Resposta correta: Tesouro Selic."

- **Neurodivergente:**  
  Pergunta: "Quero aprender sobre diversificação."  
  Resposta:  
  - Etapa 1: Diversificação significa não colocar todo o dinheiro em um único investimento.  
  - Etapa 2: É como não colocar todos os ovos na mesma cesta.  
  - Etapa 3: Assim você reduz riscos e aumenta segurança.  

---

## 🛡️ Segurança e Ética
- Não substitui consultoria financeira profissional.  
- Não realiza cálculos de rentabilidade futura.  
- Não acessa dados pessoais ou bancários.  
- Não recomenda produtos financeiros específicos.  
- Sempre alerta contra fraudes e promessas de ganhos fáceis.  

---

# 💻 Código da Aplicação

## Estrutura de Pastas

```
src/
├── app.py              # Interface principal (Streamlit/Gradio)
├── api.py              # API local (FastAPI/Flask)
├── agente.py           # Lógica do agente (consultas, quizzes, jogos inclusivos)
├── config.py           # Configurações
└── requirements.txt    # Dependências
data/
├── RESUMO ESTRUTURADO SFN E INVESTIMENTOS.md
├── GLOSSÁRIO DE CONCEITOS.md
├── Quizzes_investimentos.json
├── Jogos_inclusivos.json
├── historico_atendimento.csv
└── transacoes.csv
```

---

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

---

# 📽️ Pitch

### 🎤 Apresentação (3 minutos)

#### 1. O Problema (30 seg)
Investidores iniciantes e públicos diversos enfrentam barreiras como:  
- Dificuldade em compreender conceitos financeiros básicos.  
- Falta de acessibilidade em conteúdos tradicionais.  
- Risco de exclusão financeira por ausência de linguagem adaptada.  

#### 2. A Solução (1 min)
A **BIA Academy Finance** atua como **mentora inclusiva**, oferecendo:  
- Explicações simples e acessíveis.  
- Quizzes interativos com feedback explicativo.  
- Jogos narrativos adaptados a diferentes perfis.  
- Linguagem inclusiva para jovens, idosos, deficientes visuais/auditivos e neurodivergentes.  

#### 3. Demonstração (1 min)
Exemplo prático do agente em ação:  
- **Jovem iniciante** → "O que é reserva de emergência?" → metáfora simples + quiz.  
- **Idoso** → "Como proteger meu dinheiro da inflação?" → explicação clara + metáfora de sementes.  
- **Deficiente visual** → "Quais investimentos têm liquidez?" → resposta narrada com opções.  
- **Neurodivergente** → "Quero aprender sobre diversificação." → resposta em etapas curtas e estruturadas.  

#### 4. Diferencial e Impacto (30 seg)
- **Diferencial:** Inclusividade (linguagem adaptada, metáforas, jogos, quizzes).  
- **Impacto:** Democratizar a educação financeira, tornando conceitos de investimentos acessíveis e seguros para todos os públicos.  

---

# 📌 Conclusão
A **BIA Academy Finance** é mais que um chatbot: é uma **mentora inclusiva** que democratiza o acesso à educação financeira.  

Combinando **IA generativa, acessibilidade e empatia**, o projeto transforma o aprendizado sobre investimentos em uma experiência **simples, segura e adaptada a cada perfil**.  

Nosso objetivo é claro: **empoderar pessoas de diferentes idades e condições a compreenderem o Sistema Financeiro Nacional e cuidarem melhor do seu dinheiro**.
```



