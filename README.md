# ConstrucaoDeInterpretadores
--------------------------------------------------------------------------------------------------------
# Máquina de estados finitos
Para  obter  os  pontos  relativos  a  este  trabalho,  você  deverá  criar  um  programa,  utilizando  a 
linguagem  Python, C, ou C++.  Este  programa,  quando  executado,  irá  determinar  se  uma  string de 
entrada  faz  parte  da  linguagem  𝐿    definida  por  𝐿 = {𝑥 | 𝑥 ∈
 {𝑎,𝑏}∗ 𝑒 𝑐𝑎𝑑𝑎 𝑎 𝑒𝑚 𝑥 é 𝑠𝑒𝑔𝑢𝑖𝑑𝑜 𝑝𝑜𝑟 𝑝𝑒𝑙𝑜 𝑚𝑒𝑛𝑜𝑠 𝑑𝑜𝑖𝑠 𝑏} segundo o alfabeto  Σ={𝑎,𝑏,𝑐}.  
O  programa  que  você  desenvolverá  irá  receber  como  entrada um arquivo de texto  (.txt) 
contendo várias strings. A primeira linha do arquivo indica quantas strings estão no arquivo de texto de 
entrada. As linhas subsequentes contém uma string por linha.  A seguir está um exemplo das linhas que 
podem existir em um arquivo de testes para o programa que você irá desenvolver: 

3 

abbaba 

abababb 

bbabbaaab 

Neste  exemplo  temos  3  strings  de  entrada.  O  número  de  strings em  cada  arquivo  será 
representado  por  um  número  inteiro  positivo.  A  resposta  do  seu  programa  deverá  conter  uma, e 
somente uma linha de saída para cada string. Estas linhas conterão a string de entrada e o resultado 
da validação conforme o formato indicado a seguir: 

abbaba: não pertence

A saída poderá ser enviada para um arquivo de textos, ou para o terminal padrão e será 
composta de uma linha de saída por string de entrada. No caso do exemplo, teremos 3 linhas de saída. 
Para que seu programa possa ser testado você deve criar, no mínimo, três arquivos de entrada 
contendo um número diferente de strings diferentes. 

--------------------------------------------------------------------------------------------------------

# Parser lógica proporcional
Para  obter  os  pontos  relativos  a  este  trabalho,  você  deverá  fazer  um  programa,  usando  a 
linguagem de programação que desejar, que seja capaz de validar expressões de lógica propisicional 
escritas em latex e definir se são expressões gramaticalmente corretas. Você validará apenas a forma 
da expressão (sintaxe).  
A entrada será fornecida por um arquivo de textos que será carregado em linha de comando, 
com a seguinte formatação:  

1. Na primeira linha deste arquivo existe um número inteiro que informa quantas expressões 
lógicas estão no arquivo.  
2. Cada uma das linhas seguintes contém uma expressão lógica que deve ser validada. 

A saída do seu programa será no terminal padrão do sistema e constituirá de uma linha de saída 
para cada expressão lógica de entrada contendo ou a palavra valida ou a palavra inválida e nada mais. 
Gramática:  

Formula=Constante|Proposicao|FormulaUnaria|FormulaBinaria.  
Constante="T"|"F". 
Proposicao=[a−z0−9]+ 
FormulaUnaria=AbreParen OperadorUnario Formula FechaParen 
FormulaBinaria=AbreParen OperatorBinario Formula Formula FechaParen 
AbreParen="(" 
FechaParen=")" 
OperatorUnario="¬" 
OperatorBinario="∨"|"∧"|"→"|"↔" 
 
Cada  expressão  lógica  avaliada  pode  ter  qualquer  combinação  das  operações  de  negação, 
conjunção, disjunção, implicação e bi-implicação sem limites na combiação de preposições e operações. 
Os valores lógicos True e False estão representados na gramática e, como tal, podem ser usados em 
qualquer expressão de entrada. 
Para  validar  seu  trabalho,  você  deve  incluir  no  repl.it,  no  mínimo  três  arquivos  contendo 
números  diferentes  de  expressões  proposicionais.  O  professor  irá  incluir  um  arquivo  de  testes  extra 
para validar seu trabalho. Para isso, caberá ao professor incluir o arquivo no seu repl.it e rodar o seu 
programa carregando o arquivo de testes.

--------------------------------------------------------------------------------------------------------

# Construção do Corpus

Sua  tarefa  será  transformar  um  conjunto  de  5  sites,  sobre  o  tema  de  processamento  de 
linguagem natural em um conjunto de cinco listas distintas de sentenças. Ou seja, você fará uma função 
que, usando a biblioteca Beautifull Soap, faça a requisição de uma url, e extrai todas as sentenças desta 
url. Duas condições são importantes: 

a) A página web (url) deve apontar para uma página web em inglês contendo, não menos que 
1000 palavras.  
b) O texto desta página deverá ser transformado em um array de senteças.  
 
Para separar as sentenças você pode usar os sinais de pontuação ou as funções da biblibioteca 
Spacy. 

--------------------------------------------------------------------------------------------------------

# Bag of Words

Sua tarefa será  gerar a matriz termo documento, dos documentos recuperados da internet e 
imprimir esta matriz na tela. Para tanto: 

a) Considere que todas as listas de sentenças devem ser transformadas em listas de vetores, 
onde cada item será uma das palavras da sentença. 

b) Todos  os  vetores  devem  ser  unidos  em  um  corpus  único  formando  uma  lista  de  vetores, 
onde cada item será um lexema. 

c) Este único corpus será usado para gerar o vocabulário. 

d) O  resultado  esperado  será  uma  matriz  termo  documento  criada  a  partir  da  aplicação  da 
técnica bag of Words em todo o corpus. 

--------------------------------------------------------------------------------------------------------

# TFIDF e Cosseno

1. Sua tarefa será gerar a matriz termo-documento usando TF-IDF por meio da aplicação das 
fórmulas  TF-IDF  na  matriz  termo-documento  criada  com  a  utilização  do  algoritmo  Bag of 
Words. Sobre o Corpus que recuperamos anteriormente. O entregável desta tarefa é uma 
matriz termo-documento onde a primeira linha são os termos e as linhas subsequentes são 
os vetores calculados com o TF-IDF. 

2. Sua tarefa será gerar uma matriz de distância, computando o cosseno do ângulo entre todos 
os vetores que encontramos usando o tf-idf. Para isso use a seguinte fórmula para o cálculo 
do  cosseno  use  a  fórmula  apresentada  em  Word2Vector  (frankalcantara.com) 
(https://frankalcantara.com/Aulas/Nlp/out/Aula4.html#/0/4/2). O resultado deste trabalho será uma matriz que relaciona cada 
um dos vetores já calculados com todos os outros vetores disponíveis na matriz termo-documento mostrando a distância 
entre cada um destes vetores. 

