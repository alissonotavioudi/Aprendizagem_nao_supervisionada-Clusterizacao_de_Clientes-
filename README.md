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
Tendo a base já no mesmo formato, o próximo passo foi identificar qual o volume de Clusters ideal (K) para a base avaliada. Para isso, utilizei aqui das variáveis Annual Income (k$) e Spending Score (1-100), variáveis estas relacionadas a Renda do Cliente e ainda qual o Gasto Médio do cliente.
O método empregado para identificar a quantidade ideal de clusters foi a Curva de Cotovelo (Elbow), que nos sinalizou que o número ideal seria de 5 clusters. Afim de garantir ainda este número, utilizei ainda outro método que é a Curva de Silhouette, que nos mostra em qual cluster tivemos o maior Coeficiente, que no caso, foi no Cluster 5 (0.55).

Vale ressaltar ainda que avaliei a necessidade de padronizar ou normalizar a base de dados, e o que conclui é que como a base desta clusterização é relativamente pequena, seria indiferente normalizar a base neste caso, uma vez que temos o mesmo coeficiente Silhouette Score = 0.5594854531227246 tanto na base normalizada quanto na base original.

Resultados
Os resultados obtidos durante a aplicação dos algoritmos de clusterização podem ser encontrados na pasta results. Isso pode incluir visualizações gráficas, tabelas de métricas e insights sobre os grupos identificados.

Conclusões e Próximos Passos
Descreva as principais conclusões derivadas da clusterização e sugira possíveis aprimoramentos ou extensões para o projeto. Isso pode incluir experimentar diferentes algoritmos, otimizar parâmetros ou explorar técnicas adicionais de pré-processamento de dados.

Contribuições
Se você deseja contribuir para este projeto, por favor, siga as orientações de contribuição no arquivo CONTRIBUTING.md.

Licença
Este projeto é distribuído sob a licença [especificar a licença utilizada].

Nota: Certifique-se de fornecer informações específicas sobre o conjunto de dados, detalhes do ambiente de execução, e personalize o README para se adequar ao contexto e aos objetivos do seu projeto de clusterização.
