# Código da Aplicação

Esta pasta contém o código do seu agente financeiro.

## Estrutura Sugerida

```
src/
src/
├── app.py              # Interface principal (Streamlit/Gradio) que consome a API
├── api.py              # API local (FastAPI/Flask) expondo endpoints
├── agente.py           # Lógica do agente (consultas, quizzes, jogos inclusivos)
├── config.py           # Configurações (variáveis de ambiente, chaves locais)
└── requirements.txt    # Dependências
data/
├── RESUMO ESTRUTURADO SFN E INVESTIMENTOS.md
├── GLOSSÁRIO DE CONCEITOS.md
├── Quizzes_investimentos.json
├── Jogos_inclusivos.json
├── historico_atendimento.csv
└── transacoes.csv

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

## Como Rodar

```bash
# Instalar dependências
pip install -r requirements.txt

# Rodar API local
uvicorn src.api:app --reload

# Em outro terminal, rodar a interface
streamlit run src/app.py

```
