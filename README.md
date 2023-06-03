## Conceitos de NLP

### Expressões Regulares (Regex)
As expressões regulares, também conhecidas como regex, são padrões de busca utilizados para identificar e manipular sequências de caracteres em texto. Elas fornecem uma maneira flexível e poderosa de realizar tarefas como busca, substituição, extração e validação de padrões de texto. No NLP, as regex são comumente usadas para realizar tarefas como filtragem de palavras, identificação de entidades, extração de informações, entre outras.

### Tokenização
A tokenização é o processo de dividir um texto em unidades menores chamadas tokens. Um token pode ser uma palavra, uma frase, um caractere, ou qualquer outra unidade de interesse. A tokenização é uma etapa fundamental no pré-processamento de texto em NLP, uma vez que muitas tarefas de processamento de linguagem natural requerem que o texto seja dividido em unidades significativas antes de ser analisado ou modelado.

### One-Hot Encoding
One-Hot Encoding é uma técnica de representação de dados categóricos em formato numérico. No contexto de NLP, é comum representar palavras ou tokens como vetores one-hot. Nesse formato, cada token é representado por um vetor binário de tamanho igual ao vocabulário total, onde todas as posições são preenchidas com zero, exceto a posição correspondente ao token em questão, que é preenchida com um. Essa representação é útil para alimentar os dados para modelos de aprendizado de máquina que requerem entrada numérica.

### Byte-Pair Encoding (BPE)
Byte-Pair Encoding (BPE) é uma técnica de compressão de dados que também pode ser usada para representar palavras em NLP. No BPE, as palavras são divididas em subpalavras (subword units) usando um algoritmo iterativo. A ideia é dividir palavras frequentes em subpalavras menores e representá-las como uma sequência de unidades subword. Isso permite que o modelo lide melhor com palavras desconhecidas e aumenta a flexibilidade da representação textual.
