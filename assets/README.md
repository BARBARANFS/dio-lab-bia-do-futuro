# Assets


├── diagramas/
│   └── arquitetura.md       # Diagrama em ASCII/Markdown + versão em imagem
├── screenshots/
│   ├── quiz_tela.png        # Screenshot da tela de quiz rodando no Streamlit
│   ├── jogo_tela.png        # Screenshot da tela do jogo inclusivo
│   └── api_endpoint.png     # Screenshot da API local rodando
├── mockups/
│   ├── quiz_mockup.md       # Mockup em ASCII/Markdown da tela de quiz
│   └── jogo_mockup.md       # Mockup em ASCII/Markdown da tela do jogo
└── imagens_readme/
    ├── fluxo.png            # Imagem do fluxo de integração
    └── inclusao.png         # Imagem ilustrando públicos-alvo inclusivos

----------------------------------------


1- Diagrama de Arquitetura
+---------+    +---------+    +---------+    +-----------+    +---------+    +-----------+
| Usuário | -> | app.py  | -> | api.py  | -> | agente.py | -> |  data/  | -> |  assets/  |
+---------+    | UI      |    | API     |    | Lógica    |    | Arquivos|    | Diagramas |
               |Streamlit|    | FastAPI |    | Quiz/Jogo |    | Base    |    | Screens   |
               +---------+    +---------+    +-----------+    +---------+    | Mockups   |
                                                                             | Imagens   |
                                                                             +-----------+
----------------------------------------


2- Diagrama de Fluxo (Quiz vs Jogo Inclusivo)
+---------+    +-------------------+    +-------------------+    +-------------------+
| Usuário | -> | Identificação     | -> | Perfil/Público    | -> | Decisão do Agente |
+---------+    | (app.py + api.py) |    | alvo detectado    |    | Quiz ou Jogo      |
               +-------------------+    +-------------------+    +-------------------+
                                                                  |
                                                                  v
+-------------------+    +-------------------+    +-------------------+    +-------------------+
| Jovem Iniciante   | -> | Quiz Interativo   |    | Idoso             | -> | Jogo Interativo   |
+-------------------+    +-------------------+    +-------------------+    +-------------------+
                                                                  |
                                                                  v
+-------------------+    +-------------------+    +-------------------+    +-------------------+
| Def. Visual       | -> | Quiz narrado      |    | Def. Auditivo     | -> | Quiz em Libras    |
+-------------------+    +-------------------+    +-------------------+    +-------------------+
                                                                  |
                                                                  v
+-------------------+    +-------------------+
| Neurodivergente   | -> | Jogo em etapas    |
+-------------------+    +-------------------+

----------------------------------------

3- Mockup em ASCII (quiz_mockup.md)
----------------------------------------
|   BIA Academy Finance Inclusiva       |
----------------------------------------
Pergunta: Qual investimento tem maior liquidez?
[ ] Tesouro Selic
[ ] LCI com carência de 90 dias
[ ] Ações

Botão: Confirmar resposta
Feedback: "O Tesouro Selic pode ser resgatado a qualquer momento."
Pontuação: +10
----------------------------------------

4- Mockup em ASCII (jogo_mockup.md)
----------------------------------------
| História Interativa: Maria investindo |
----------------------------------------
Cenário: Maria quer montar uma reserva de emergência.
Pergunta: Qual metáfora representa melhor esse conceito?
[ ] Cofre
[ ] Sementes
[ ] Fruta

Botão: Escolher
Feedback: "O cofre simboliza segurança e liquidez, como o Tesouro Selic."
Pontuação: +10
----------------------------------------
