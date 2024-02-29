**1. Título do projeto**

Clusterização de Clientes de Supermercados

**2. Objetivo do projeto**

Este projeto teve como objetivo identificar padrões nas variáveis estudadas que permitissem o agrupamento dos Clientes em Clusters, afim de permitir a empresa estudada direcionar estratégias distintas para os diferentes clusters.

**3. Base de Dados**

O conjunto de dados utilizado neste Projeto está disponível em .CSV no caminho https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python.
O dataset possui 200 linhas e 5 features (4 númericas e 1 categórica). Afim de manter todas as variáveis em formáto númerico, foi necessário realizar o pré-processamento da variável "Gender".
Ainda, cale ressaltar que o dataset não possui dados nulos, não sendo assim necessário realizar a etapa de remoção ou preechimento dos valores ausentes.
 
**4. Algoritmo utilizado**

Para este trabalho, optei por usar o algoritmo K-Means, um dos mais utilizados para clusterizar bases. Este algoritmo trabalha atribuindo a cada ponto(dados) o cluster cujo centro (média) é mais próximo.

Cabe ressaltar que existem ainda outros algoritmos para clusterização, entre eles:

- Hierarchical Clustering: Método que constrói uma hierarquia de clusters, começando com cada ponto como um cluster separado e combinando clusters sucessivos.
* DBSCAN (Density-Based Spatial Clustering of Applications with Noise): Um algoritmo que agrupa pontos em regiões de alta densidade, separadas por regiões de baixa densidade.

**5. Estrutura do Projeto**

Inicialmente, após realizar a importação dos dados, realizei uma análise exploratória afim de entender melhor os dados trabalhados. Aqui pode-se destacar a análise multivariada realizada utilizando a variável Gender x demais variáveis do dataset. O objetivo aqui foi avaliar se já teria algum grupo definido avaliando o sexo do cliente x demais features, o que conforme foi visto, não existe.

![download](https://github.com/alissonotavioudi/Aprendizagem_nao_supervisionada-Clusterizacao_de_Clientes-/assets/153277228/612d3a8c-b763-4414-943b-b48d4fed77ad)

Passado a etapa de exploração dos dados, foi realizado um pré-processamento da variável Gender, onde a transformei de variável categórica para númerica.
Tendo a base já no mesmo formato, o próximo passo foi identificar qual o volume de Clusters ideal (K) para a base avaliada. Para isso, utilizei aqui das variáveis Annual Income (k$) e Spending Score (1-100), variáveis estas relacionadas a Renda do Cliente e qual o Gasto Médio do cliente.
O método empregado para identificar a quantidade ideal de clusters foi a Curva de Cotovelo (Elbow), que nos sinalizou que o número ideal seria de 5 clusters. Afim de garantir ainda este número, utilizei ainda outro método que é a Curva de Silhouette, que nos mostra em qual cluster tivemos o maior Coeficiente, que no caso, foi no Cluster 5 (0.55).

Vale ressaltar ainda que avaliei a necessidade de padronizar ou normalizar a base de dados, e o que conclui é que como a base desta clusterização é relativamente pequena, seria indiferente normalizar a base neste caso, uma vez que temos o mesmo coeficiente Silhouette Score = 0.5594854531227246 tanto na base normalizada quanto na base original.

**6. Conclusões e Próximos Passos**

![Clusters formados](https://github.com/alissonotavioudi/Aprendizagem_nao_supervisionada-Clusterizacao_de_Clientes-/assets/153277228/41cb9d34-2220-467a-ba26-0ac625b37675)

Com base nos Clusters formados, é possível o Supermercado adotar estratégias distintas para a sua base ativa, desde pensar em ações de Fidelização até tomar ações visando o cuidado com potenciais perdas (Provisão Devedores Duvidosos - PDD).

Inicialmente, a minha recomendação seria o Supermercado focar em **Ativação**, utilizando para isso dos clientes do Cluster 2 (Alta renda e Gasto médio baixo). O objetivo aqui seria fomentar que estes clientes passassem a comprar mais no supermercado, de modo que no curto prazo estes clientes pudessem "migrar" para o Cluster 4 (Alta renda e Gasto médio alto). 

Uma outra estratégia passível de ser feita pelo Supermercado, pensando que o supermercado possa ter um "cartão próprio", e que assim, exista um risco de PDD inerente a sua operação, seria ser estabelecido uma política que liberasse para os clientes do Cluster 3 compras apenas pagas a vista ou em cartão que não o vinculado ao supermercado (Private Label). 

Ressalto que esta são apenas duas estratégias, mas certamente existem novas abordagens possíveis a partir desta clusterização.

Como oportunidades de desenvolvimento para este projeto, é válido pensar em criar os clusters utilizando os demais algoritmos existentes.



Contribuições
Se você deseja contribuir para este projeto, fique a vontade para criar uma cópia e realizar as melhorias !



