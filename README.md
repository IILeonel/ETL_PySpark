# ETL utilizando PySpark

![Estrutura](https://user-images.githubusercontent.com/61874620/195886175-2f0455b1-b81e-4044-9725-0c8aa87eddc6.png)

**Parte 1**
- Instalamos e importarmos as bibliotecas do spark e pyspark
- Criamos uma conexão com o banco de dados
- Lemos todas as tabelas com o pandas, transformamos em um dataframe do spark e gravamos como parquet.

**Parte 2**
- Criamos um dataframe juntando as tabelas.
- Criamos um dataframe juntando alguns dados.

**Aplicamos algumas regras:**
  - O início e o fim do nome do produto não pode ter espaços e tem que ter todas as letras maiúsculas.
  - Concatenar um hífen e o nome da cor no final do nome do produto
  - Se o tamanho vier como “M” deverá ser 49, se vier “P” deverá ser 32, se vier “L” deverá ser 52, se vier XL deverá ser 70 e ser for null deverá ser 0 
  Nos outros casos, mantenha o valor do tamanho.
  - Criamos uma coluna chamada Codigo_Produto. Essa coluna contem os dois primeiros dígitos do número do produto.
  - Substituimos o hífen no nome do modelo do produto por um espaço.
  - Gravamos esse dataframe como parquet com o nome de “TRANSFORMACAO/PRODUTOS”, particionado por categoria_produto
  - Criamos  um dataframe trazendo as seguintes colunas das tabelas (PRODUTO,  DETALHE_PEDIDO)

# Libs utilizadas
* Python 3.8: Download em https://www.python.org/downloads
* Spark: sudo pip install spark
* PySpark: sudo pip install pyspark
* Pandas: pip install pandas
* Pyodbc: sudo pip install pyodbc
* Sqlalcjemy: sudo pip install sqlalchemy
* Boto3: pip install boto3

