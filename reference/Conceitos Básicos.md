# Conceitos de NLP

### Expressões Regulares (Regex)
As expressões regulares, também conhecidas como regex, são padrões de busca utilizados para identificar e manipular sequências de caracteres em texto. Elas fornecem uma maneira flexível e poderosa de realizar tarefas como busca, substituição, extração e validação de padrões de texto. No NLP, as regex são comumente usadas para realizar tarefas como filtragem de palavras, identificação de entidades, extração de informações, entre outras.

Exemplo: Identificação de endereços de e-mail em um texto usando o seguinte padrão regex: `[\w\.-]+@[\w\.-]+\.\w+`

### Tokenização
A tokenização é o processo de dividir um texto em unidades menores chamadas tokens. Um token pode ser uma palavra, uma frase, um caractere, ou qualquer outra unidade de interesse. A tokenização é uma etapa fundamental no pré-processamento de texto em NLP, uma vez que muitas tarefas de processamento de linguagem natural requerem que o texto seja dividido em unidades significativas antes de ser analisado ou modelado.

Exemplo: Tokenização de uma frase em palavras individuais: "A tokenização é importante para NLP" se torna `["A", "tokenização", "é", "importante", "para", "NLP"]`

## Vocabulário em NLP

No Processamento de Linguagem Natural (NLP), o vocabulário refere-se ao conjunto único de palavras ou tokens presentes em um determinado corpus de texto. O vocabulário desempenha um papel crucial em várias tarefas de NLP, como classificação de texto, modelagem de linguagem e tradução automática.

### Construção do Vocabulário

A construção do vocabulário geralmente envolve as seguintes etapas:

1. **Tokenização**: O texto é dividido em unidades menores chamadas tokens. Isso pode ser feito por palavras, caracteres, subpalavras ou até mesmo por unidades mais granulares, dependendo da tarefa e do modelo.

2. **Remoção de Pontuação e Stop Words**: Pontuação e palavras comuns que não agregam significado ao texto, como artigos e preposições, são geralmente removidas do vocabulário.

3. **Remoção de Duplicatas**: Tokens duplicados são removidos para garantir que o vocabulário seja composto apenas por palavras únicas.

### Tamanho do Vocabulário

O tamanho do vocabulário pode variar dependendo do tamanho do corpus de texto e das decisões tomadas durante a construção do vocabulário. Um vocabulário maior captura uma variedade maior de palavras, o que pode ser útil para tarefas de NLP mais abrangentes. No entanto, um vocabulário muito grande também pode aumentar a complexidade computacional e o consumo de memória durante o treinamento e a inferência.

### Vocabulário OOV (Out-of-Vocabulary)

Durante a tokenização e a construção do vocabulário, é possível encontrar palavras que não estão presentes no vocabulário pré-existente. Essas palavras são conhecidas como palavras Out-of-Vocabulary (OOV). O tratamento adequado das palavras OOV é importante para garantir que o modelo de NLP seja capaz de lidar com dados desconhecidos ou novas palavras encontradas durante a inferência.

### Gerenciamento do Vocabulário

O gerenciamento do vocabulário em NLP envolve decisões sobre o tamanho máximo do vocabulário, a inclusão ou exclusão de certas palavras, técnicas de redução de vocabulário (como truncagem ou substituição de palavras raras) e estratégias para lidar com palavras OOV.

Um vocabulário bem construído e gerenciado desempenha um papel crítico no desempenho e na generalização de modelos de NLP. Ele fornece a base para representar o texto de forma significativa e permite que o modelo aprenda padrões e relações entre as palavras durante o treinamento.

### One-Hot Encoding
One-Hot Encoding é uma técnica de representação de dados categóricos em formato numérico. No contexto de NLP, é comum representar palavras ou tokens como vetores one-hot. Nesse formato, cada token é representado por um vetor binário de tamanho igual ao vocabulário total, onde todas as posições são preenchidas com zero, exceto a posição correspondente ao token em questão, que é preenchida com um. Essa representação é útil para alimentar os dados para modelos de aprendizado de máquina que requerem entrada numérica.

Exemplo: Representação one-hot encoding de três palavras: "gato", "cachorro" e "peixe" com um vocabulário total de 5 palavras: 
- "gato" -> [1, 0, 0, 0, 0]
- "cachorro" -> [0, 1, 0, 0, 0]
- "peixe" -> [0, 0, 1, 0, 0]

### Byte-Pair Encoding (BPE)
Byte-Pair Encoding (BPE) é uma técnica de compressão de dados que também pode ser usada para representar palavras em NLP. No BPE, as palavras são divididas em subpalavras (subword units) usando um algoritmo iterativo. A ideia é dividir palavras frequentes em subpalavras menores e representá-las como uma sequência de unidades subword. Isso permite que o modelo lide melhor com palavras desconhecidas e aumenta a flexibilidade da representação textual.

Exemplo: Divisão da palavra "desconhecido" em subpalavras usando o algoritmo BPE: "des", "co", "nhe", "ci", "do"

