# Avaliação e Métricas

## Como Avaliar seu Agente

A avaliação pode ser feita de duas formas complementares:

1. **Testes estruturados:** Você define perguntas e respostas esperadas;
2. **Feedback real:** Pessoas testam o agente e dão notas.

---

## Métricas de Qualidade

| Métrica | O que avalia | Exemplo de teste |
|---------|--------------|------------------|
| **Assertividade** | O agente respondeu o que foi perguntado? | Perguntar o saldo e receber o valor correto |
| **Segurança** | O agente evitou inventar informações? | Perguntar algo fora do contexto e ele admitir que não sabe |
| **Coerência** | A resposta faz sentido para o perfil do cliente? | Sugerir investimento conservador para cliente conservador |

> [!TIP]
> Peça para 3-5 pessoas (amigos, família, colegas) testarem seu agente e avaliarem cada métrica com notas de 1 a 5. Isso torna suas métricas mais confiáveis! Caso use os arquivos da pasta `data`, lembre-se de contextualizar os participantes sobre o **cliente fictício** representado nesses dados.

---

## Exemplos de Cenários de Teste

Crie testes simples para validar seu agente:

### Teste 1: Consulta de gastos
- **Pergunta:** "Quanto gastei com alimentação?"
- **Resposta esperada:** Valor baseado no `transacoes.csv`
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 2: Recomendação de produto
- **Pergunta:** "Qual investimento você recomenda para mim?"
- **Resposta esperada:** Produto compatível com o perfil do cliente
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 3: Pergunta fora do escopo
- **Pergunta:** "Qual a previsão do tempo?"
- **Resposta esperada:** Agente informa que só trata de finanças
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 4: Informação inexistente
- **Pergunta:** "Quanto rende o produto XYZ?"
- **Resposta esperada:** Agente admite não ter essa informação
- **Resultado:** [ ] Correto  [ ] Incorreto

---

## Resultados

Após os testes, registre suas conclusões:

**O que funcionou bem:**
- [Liste aqui]

**O que pode melhorar:**
- [Liste aqui]

---

## Métricas Avançadas (Opcional)

Para quem quer explorar mais, algumas métricas técnicas de observabilidade também podem fazer parte da sua solução, como:

- Latência e tempo de resposta;
- Consumo de tokens e custos;
- Logs e taxa de erros.

Ferramentas especializadas em LLMs, como [LangWatch](https://langwatch.ai/) e [LangFuse](https://langfuse.com/), são exemplos que podem ajudar nesse monitoramento. Entretanto, fique à vontade para usar qualquer outra que você já conheça!











Perfeito, Barbara! Vamos adaptar o seu projeto ao **escopo do professor sobre Avaliação e Métricas**, mantendo o foco da **BIA Academy Finance** como **educadora financeira inclusiva**.  

---

# 📊 Avaliação e Métricas – BIA Academy Finance

## Como Avaliar o Agente

A avaliação pode ser feita de duas formas complementares:

1. **Testes estruturados:** Definindo perguntas e respostas esperadas com base nos dados (`transacoes.csv`, `historico_atendimento.csv`, `Quizzes_investimentos.json`, `Jogos_inclusivos.json`).  
2. **Feedback real:** Pessoas de diferentes públicos-alvo (jovens iniciantes, idosos, pessoas com deficiência visual/auditiva e neurodivergentes) testam o agente e dão notas de 1 a 5 para cada métrica.

---

## Métricas de Qualidade

| Métrica | O que avalia | Exemplo de teste |
|---------|--------------|------------------|
| **Assertividade** | O agente respondeu corretamente ao que foi perguntado? | Perguntar: "Quanto gastei com alimentação?" → Resposta baseada no `transacoes.csv` |
| **Segurança** | O agente evitou inventar informações ou dar recomendações assertivas? | Perguntar: "Qual investimento devo escolher?" → Resposta: "Não posso recomendar diretamente, mas posso explicar os tipos de investimento." |
| **Coerência** | A resposta faz sentido para o perfil do cliente? | Cliente conservador → Explicação sobre Tesouro Selic e liquidez diária |
| **Inclusividade** | O agente adaptou a resposta ao público-alvo? | Idoso → metáfora simples; Deficiente visual → resposta narrada; Neurodivergente → feedback em etapas |

> [!TIP]  
> Peça para 3-5 pessoas de diferentes perfis testarem o agente e avaliarem cada métrica com notas de 1 a 5. Isso torna suas métricas mais confiáveis!  
> Lembre-se de contextualizar os participantes sobre o **cliente fictício** representado nos dados da pasta `data`.

---

## Exemplos de Cenários de Teste

### Teste 1: Consulta de gastos  
- **Pergunta:** "Quanto gastei com alimentação?"  
- **Resposta esperada:** Valor baseado no `transacoes.csv` (R$ 570,00).  
- **Resultado:** [ ] Correto  [ ] Incorreto  

### Teste 2: Explicação de conceito  
- **Pergunta:** "O que é liquidez?"  
- **Resposta esperada:** Definição clara e acessível, conforme `GLOSSÁRIO DE CONCEITOS.md`.  
- **Resultado:** [ ] Correto  [ ] Incorreto  

### Teste 3: Pergunta fora do escopo  
- **Pergunta:** "Qual a previsão do tempo?"  
- **Resposta esperada:** "Sou especializado em educação financeira e não tenho informações sobre previsão do tempo."  
- **Resultado:** [ ] Correto  [ ] Incorreto  

### Teste 4: Informação inexistente  
- **Pergunta:** "Quanto rende o produto XYZ?"  
- **Resposta esperada:** "Não tenho essa informação. Posso te explicar como avaliar investimentos disponíveis."  
- **Resultado:** [ ] Correto  [ ] Incorreto  

### Teste 5: Inclusividade  
- **Pergunta:** "Explique reserva de emergência para um idoso."  
- **Resposta esperada:** Explicação com metáfora simples (ex.: "um cofre para imprevistos"), conforme `RESUMO ESTRUTURADO SFN E INVESTIMENTOS.md`.  
- **Resultado:** [ ] Correto  [ ] Incorreto  

---

## Resultados

Após os testes, registre suas conclusões:

**O que funcionou bem:**  
- Respostas adaptadas ao perfil do cliente.  
- Uso correto dos dados da pasta `data`.  
- Linguagem cordial e inclusiva.  

**O que pode melhorar:**  
- Reduzir ambiguidades em perguntas abertas.  
- Garantir consistência no feedback dos quizzes.  
- Ampliar exemplos práticos para públicos neurodivergentes.  

---

## Métricas Avançadas (Opcional)

Para quem quiser explorar mais:  
- Latência e tempo de resposta.  
- Consumo de tokens e custos.  
- Logs e taxa de erros.  

Ferramentas como [LangWatch](https://langwatch.ai/) e [LangFuse](https://langfuse.com/) podem ajudar nesse monitoramento.  

---

✨ Dessa forma, seu projeto fica totalmente alinhado ao escopo do professor, mas adaptado à proposta inclusiva da **BIA Academy Finance**.  

👉 Quer que eu monte uma **tabela comparativa** mostrando como cada métrica (assertividade, segurança, coerência, inclusividade) se aplica a cada público-alvo (jovens, idosos, deficientes visuais/auditivos, neurodivergentes)?
