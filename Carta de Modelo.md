Carta de Modelo – Predição de Renda Anual

Detalhes do Modelo

1.	Modelo desenvolvido por Nicholas Kluge, pesquisador da Pontifícia Universidade Católica do Rio Grande do Sul (PUCRS), em outubro de 2021. 
2.	Trata-se de uma rede neural profunda direta (densa), treinada para resolver uma tarefa de classificação binária, versão 0.1. Este modelo foi treinado para classificar indivíduos entre “Renda anual > $50,000 USD” ou “Renda anual < $50,000 USD”. 
3.	Este modelo foi treinado apenas por motivações acadêmicas, e ele não segue nenhum tipo de restrição de equidade/justiça. Ele não foi criado para ser implementado em aplicações reais.
4.	O conjunto de dados utilizado é o Adult Census Income Data Set, disponibilizado pela UCI Machine Learning Repository. Disponível em: http://archive.ics.uci.edu/ml/datasets/Census+Income.  
5.	O código para este modelo pode ser encontrado em: https://github.com/Nkluge-correa/AI-Ethics-Exercice-2.  
6.	Licença: MIT License;  
7.	Contato: nicholas.correa@acad.pucrs.br. 

Uso Pretendido

1.	O uso pretendido deste modelo, e o código compartilhado, é apresentar ao desenvolvedor algumas ferramentas para se explorar um conjunto de dados, e avaliar possíveis implicações éticas e falhas de segurança de um modelo treinado por aprendizagem de máquina. Este modelo, e código, não foram criados para serem utilizados em aplicações reais. Contudo, as ferramentas utilizadas podem sim ser utilizadas para avaliações éticas de modelos treinados por aprendizagem de máquina.
2.	Este modelo foi desenvolvido para o público acadêmico, desenvolvedores e praticantes de aprendizagem de máquina interessados em aprender como desenvolver modelos “justos”.
3.	Como um experimento acadêmico, a única utilização para este modelo é a predição de Renda Anual de amostras retiradas do Adult Census Income Data Set. Este modelo não deve ser usado para, e.g., predição de renda vitalícia, ou qualquer outro tipo de tarefa diferente do seu uso primário pretendido.

Fatores

1.	As características utilizadas para o treinamento do modelo são: “Classe Trabalhadora”, “Raça”, “Educação”, “Estado Civil”, “Idade”, “Parentesco”, “Nacionalidade”, “Ocupação”. Atributos como “Gênero” foram velados, enquanto que “Raça” e “Estado Civil” foram considerados como atributos sensíveis. 
2.	Os dados utilizados para treinamento não possuem uma distribuição uniforme entre os subgrupos de cada característica. Existe um forte enviesamento, para certos tipos de subgrupos, como gêneros e raças específicas.

Métricas

1.	As métricas de performance utilizadas foram acurácia (83%), precisão (70%), recall (55%) e AUC (88%).
2.	O modelo possui uma boa precisão ao classificar pessoas que possuem renda anual > $50,000 USD (70%). Contudo, a maior parte das classificações erradas feitas por este modelo são Falsos Negativos (indivíduos com renda anual > $50,000 USD, que são classificados como possuindo renda anual < $50,000 USD. 
3.	Aviso: a performance do modelo varia consideravelmente entre subgrupos de atributos sensíveis (e.g., gênero, raça, estado civil). 
4.	Dados de treinamento e testagem foram adquiridos diretamente do conjunto de dados fornecidos pela UCI Machine Learning Repository (i.e., Adult Census Income Data Set);
5.	Este conjunto de dados foi escolhido por sua disponibilidade pública;
6.	5.	Amostras com valores ausentes (i.e., “”?” ou “NaN”) foram excluídas do conjunto de dados.

Considerações Éticas

1.	Dada a distribuição enviesada dos dados de treinamento, o modelo pode se comportar de forma ineficiente quando lidando com amostras pouco vistas. Sua performance varia consideravelmente entre subgrupos, não alcançado padrões mínimos de poder preditivo para certos subgrupos (e.g., Casado-cônjuge-militar);
2.	Recomenda-se que para aplicações reais, o conjunto de dados seja reconstruído/alterado, de forma que aja uma melhor distribuição de amostras por subgrupos de características;
3.	De acordo com os resultados de performance e matrizes de confusão entre subgrupos, atributos sensíveis podem interferir na predição deste modelo;

Detalhes e Recomendações

1.	O modelo treinado resulta em uma performance que varia entre subgrupos pertencentes a características/atributos sensíveis. Se utilizado para aplicações que podem causar impacto na vida das pessoas (e.g., determinando que deve pagar impostos mais elevados), o modelo pode vir a prejudicar populações sub representadas no Adult Census Income Data Set;
2.	Os dados utilizados para este exemplo não refletem o contexto social e histórico de um lugar como, por exemplo, Brasil. Eles refletem o contexto social e histórico Norte-Americano. Assim, não se recomenda utilizá-lo para desenvolvimento de aplicações fora deste domínio específico. 

Análise Quantitativa

<p align="center">
<img alt="pattern demo" src="https://gdurl.com/F8A6U">
</p>


 

