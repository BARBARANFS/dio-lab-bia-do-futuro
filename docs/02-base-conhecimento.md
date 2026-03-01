# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo | Formato | Utilização no Agente |
|---------|---------|---------------------|
| `RESUMO ESTRUTURADO SFN E INVESTIMENTOS.md` | MD |Doc. base da pesquisa, estruturando toda a lógica dos jogos inclusivos. |
| `GLOSSÁRIO DE CONCEITOS.md` | MD | Suporte didático para simplificar termos técnicos |
| `Quizzes_investimentos.json` | JSON | Quizzes com feedback explicativo adequados ao perfil |
| `Jogos_inclusivos.json` | JSON | Jogos narrativos e metáforas adaptadas a diferentes públicos (jovens, idosos, pessoas com deficiência visual/auditiva e           neurodivergentes).|
|`historico_atendimento.csv` | CSV | Contextualizar interações anteriores |
| `transacoes.csv` | CSV | Analisar padrão de gastos do cliente |

> [!TIP]
> **Quer um dataset mais robusto?** Você pode utilizar datasets públicos do [Hugging Face](https://huggingface.co/datasets) relacionados a finanças, desde que sejam adequados ao contexto do desafio.

---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

Foram introduzidos para expandir o escopo do projeto idealizado e dando continuação prática ao Miniguia_SFN_Investimentos do 1º Desafio_DIO:

RESUMO ESTRUTURADO SFN E INVESTIMENTOS.md: base da pesquisa.
GLOSSÁRIO DE CONCEITOS.md: suporte didático 
Quizzes_investimentos.json: método para inclusão e ensino didático e dinâmico focando cada perfil
Jogos_inclusivos.json: jogos narrativos e metáforas adaptadas a diferentes públicos (jovens, idosos, pessoas com deficiência visual/auditiva e neurodivergentes)

Foram mantidos sem alterações:
* historico_atendimento.csv
* transacoes.csv
---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

[Os arquivos JSON/Markdown criados e os CSV originais são carregados no início da sessão. E, o agente acessa dinamicamente os dados conforme o perfil/público-alvo do usuário].

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

[Os dados não são inseridos diretamente no system prompt.São consultados dinamicamente:

Markdowns → suporte conceitual e explicações simplificadas.
JSONs → quizzes e jogos inclusivos.
CSV → contextualização e análise de gastos.]

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Dados do Cliente:
- Nome: João Silva
- Perfil: Moderado
- Saldo disponível: R$ 5.000

Últimas transações:
- 01/11: Supermercado - R$ 450
- 03/11: Streaming - R$ 55
...
```
