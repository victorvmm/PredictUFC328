# PredictUFC328
Predictions of Khamzat Chimaev vs Sean Strickland for UFC 328

# Files:

Fighters CSV attributes:
- Name 
- Age 
- Height (cm)
- Reach (cm)
- Wins
- Losses
- Significant strikes landed per minute
- Significant striking accuracy 
- Significant strike defense
- Significant strikes absorbed per minute
- Average takedown landed per 15 minutes
- Takedown accuracy
- Takedown defense
- Average submissions attempted per 15 minutes

Fighters record CSVs - ChimaevFights (for Khamzat Chimaev) and StricklandFights (for Sean Strickland):
- Fight (Opponent) 
- Belt (1 = Title fight, 0 = regular fight)
- Won (1 = won, 0 = lost)
- KO/TKO/Submission (1 = Yes, 0 = Decision)
- Fight time (min)
- Significant strikes landed 
- Opponent's significant strikes 
- Significant strikes landed % 
- Takedowns
- Takedown accuracy
- Control time (min)
- Opponent's takedowns
- Opponent's takedowns accuracy 
- Opponent's control time (min)

DataCleaning Jupyter Notebook:

Models Jupyter Notebook:

# A Fazer: 

Organizar o projeto, documentar tentativas e erros etc.


Adicionar o próprio lutador no data/target ou não? No que isso afetaria?
Pegar os resultados dos dois dataset e fazer uma média entre eles? Ver quais as diferenças?

Alternativa 1:

Alternativa 2:

Alternativa 3:
Chimaev como dataset principal, deu errado (pegar porcentagens para exibir erro) por só ter vitórias

# "Bibliografia"

Data source:
http://www.ufcstats.com/statistics/events/completed

Os dados foram obtidos de fontes públicas disponíveis para uso não comercial, apenas educacional.