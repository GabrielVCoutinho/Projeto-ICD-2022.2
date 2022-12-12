# Projeto-ICD-2022.2
Projeto de Introdução à Ciência de Dados

Alunos: Gabriel Vieira Coutinho, Gustavo Henrique de Carvalho Costa Filho

Pergutnas:
  1) Qual é o time com os jogadores com melhores estatísticas?
  2) Quais são os atacantes com melhores eficiências de chute ao gol?
  3) Qual é a relação desarme falta dos jogadores?

DataSet: https://www.kaggle.com/datasets/azminetoushikwasi/ucl-202122-uefa-champions-league?select=key_stats.csv

Relatório - Champions League
Gabriel Vieira, Gustavo Henrique de Carvalho

A UEFA Champions League é uma competição anual de clubes de futebol a nível continental, organizada pela União das Associações Europeias de Futebol (UEFA) e disputada por clubes europeus. É um dos torneios mais prestigiados do mundo e a competição de clubes mais prestigiada no futebol europeu, disputada pelas equipes mais bem classificadas nos respectivos campeonato nacionais na temporada anterior, sendo o número de vagas atribuído consoante o ranking da UEFA. A final da Liga dos Campeões da UEFA é o evento esportivo anual mais visto em todo o mundo. Por conta do alto nível tecnico decidimos que esta seria uma competição adequada para se realizar uma análise de dados com a finalidade de encontrar os melhores clubes e jogadores do mundo.
O dataset contem estatísticas dos jogadores da UEFA Champions League temporada 2021-22. O dataset está dividido em sete partes, sendo elas:
Attacking: Contém as estatísticas de ataque como assistências, dribles e impedimentos.
Attempts: Contém as estatísticas de tentativas de gol como chutes totais, chutes a gol, chutes para fora, gols, etc.
Defending: Contém as estatísticas de defesa como divididas ganhas, perdidas e recuperação de bola.
Disciplinary: Contém as estatísticas de disciplina dos jogadores como faltas cometidas e sofridas, além dos cartões que 
o jogador recebeu.
Distribution: Contém as estatísticas de passes como tentativas de passe, passes completos, precisão de passe, etc.
Goalkeeping: Contém as estatísticas dos goleiros como gols salvos, penaltis salvos e espalmos.
Goals: Contém as estatísticas de gols dos jogadores como perna esquerda e direita, cabeçadas e gols de dentro da área.
Key stats: Reune as principais estátisticas dos jogadores como o número de partidas e minutos jogados.

Decidimos juntar as tabelas em uma só para analisar correlações entre os dados, que estavam distribuídos entre as sete tabelas preexistentes. Além disso, retiramos colunas que continham dados que não seriam úteis para nossa análise como as colunas referentes as estatísticas de goleiros.
1. Qual é o time com os jogadores com melhores estatísticas?

Aqui buscamos os times que tivessem as melhores estatísticas coletivas usando as médias os dados de tentativas de chute a gol, divididas de bola, gols, assistências, bolas recuperadas, faltas cometidas e bolas afastadas do gol.

Observando as tabelas percebemos que o Real Madrid foi o time que mais apareceu nas tabelas com a média das estatísticas dos jogadores de seus respectivos times, levando a conclusão que foi um dos melhores times do campeonato.

2. Quais são os atacantes com melhores eficiências de chute ao gol?

Usando os dados de tentativas totais e gols podemos traçar a eficiência percentual de chute a gol dos jogadores, no qual o Haller, atacante do Ajax, se destacou por possuir 24 tentativas de gol e uma taxa de conversão de 45.8%. Nós tambem criamos um score(gols²/tentativas de gol) já que jogadores com poucas tentativas de gol geravam taxas de eficiência muito altas, que muitas vezes não refletiam a qualidade do jogador e ofuscavam jogadores como Lewandowski que tinha 31 tentativas de gol e uma taxa de conversão de 41.9%.

3. Qual é a relação desarme falta dos jogadores?

Inicialmente não foi possível estabelecer uma relação entre faltas e divididas pois muitos jogadores tinham poucas divididas e muitas faltas. Porém, usando KMeans e regressão linear, um método de clusterização, foi possível indentificar que quanto menos divididas de bolas menor é a tendência do jogador cometer uma falta.

Conclusão:
Utilizando da análise de dados e das ferramentas aprendidas na disciplina de Introdução a Ciência de Dados foi possível indentificar padrões e comportamentos dos jogadores e correlações entre as estatísticas apresentadas pelo dataset. Como visto, no caso dos clubes, o Real Madrid se destacou em todas as estatísticas coletivas e consequentemente ganhou o campeonato em questão. Além disso, diferente do coletivo as estatísticas não apontam nenhum jogador em específico do Real Madrid acima da média, mostrando que o mérito do Real Madrid foi o jogo coletivo e o trabalho em equipe.
