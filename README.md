# Readme


## Licença de Distribuição

## Características do problema
Nos foi apresentada a plataforma de ensino online, a Alura, com o objetivo de, após investigarmos a fundo o comportamento de seus usuários, sugerirmos soluções para, de forma orgânica, aumentar o engajamento/estudo dos inscritos com o site.
## Solução desenvolvida
Após análise e confecção de um modelo (que utilizava a quantidade de exercícios feitos, minutos de aula assistidos, quantidade de cursos inscritos e interações nos fóruns online), concluímos que, para aumentar o engajamento dos alunos, a Alura poderia criar mecanismos para sugerir descansos ao detectar "maratonas" de estudo, além de motivar os usuários a completarem os cursos nos quais estão inscritos, de modo a incentivar uma rotina de estudos mais constante, esta que, pelo que constatamos em nosso modelo, é a que apresenta maior rendimento de aprendizado na plataforma.
## Descrição dos dados
- Foram recebidas 7 arquivos no formato .csv com dados anonimizados de usuários e cursos da alura, esses arquivos são: _anonimized_courses.csv_, _anonimized_logs.csv_, _anonimized_registrations.csv_, _anonimized_section_harnessing_task.csv_, _anonimized_sections.csv_, _anonimized_tasks.csv_ e _anonimized_users.csv_ e estão detalhados no notebook inicial "EAD Alura.ipyb" e nos notebooks que os utilizaram.
- Pacotes python utilizados: pandas, matplotlib, seaborn
- Notebook "score_and_time_analysis.ipynb":
Contém a criação e implementação do modelo utilizado (batizado de score), assim como uma análise exploratória dos alunos com mais tempo de vídeo assistido na Alura, olhando como este grupo interage com os cursos em que se matriculam, completando-os ou não, em sua maioria.
- Notebook "completion_by_level":
Contém uma análise quantitativa da taxa de conclusão dos cursos comparados por nível de dificuldade
- Notebook "user_log_distribution.ipynb":
Neste notebook os dados são organizados de maneira a tornar visualizável a distribuição de atividades dos alunos ao longo dos dias.
- Notebook "user_log_clustering":
Neste notebook detalha-se a obtenção dos clusters dos usuários utilizando o algoritmo de K-means DTW. Utiliza-se aqui a biblioteca tslearn.
-

## Coisas que foram tentadas mas não deram certo
## Coisas que deram certo + resultados
- Modelo:
O modelo criado, que leva em conta a quantidade de exercícios feitos, interações nos fóruns e cursos, além da quantidade de tempo de videoaula assistido (com todos os valores normalizados), foi essencial para nos fornecer as devidas vizualisações necessárias. Os resultados mais importantes foram os plots abaixo:

![](images/graph1.png)

O desvio padrão, indicado no eixo das abcissas, tem valores maiores para ritmos de estudo mais esporádicos, com grandes picos de atividade e grandes períodos de inatividade, e valores menores para rotinas de estudo mais próximas de constancia. Conforme é possível enxergar, as maiores pontuações (Scores) estão associadas a rotinas de estudo constantes, com pouco desvio padrão.

![](images/graph2.png)

Com ambos os eixos em escala logarítmica, pode-se notar com clareza que, conforme a quantidade de cursos (eixo X) aumenta, o engajamento (Score) diminui, com uma clara correlação entre as variáveis, indicada pela linha vermelha de regressão.

- Clusterização com Dynamic Time Warping - K means:
Utilizando o método de Clusterização com Dynamic Time Warping, chegamos nos seguintes Clusters para os usuários:

![](images/clusters.png)


Exemplos de alunos classificados como Cluster 5:

![](images/cluster5.png)

Exemplos de alunos classificados como cluster 3:

![](images/cluster3.png)







## Licença 

Licença sobre a [Licença MIT](LICENSE)








