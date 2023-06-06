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

## Tipos de Normalização em NLP

Existem várias técnicas de normalização utilizadas no Processamento de Linguagem Natural (NLP) para melhorar a consistência e o processamento do texto. Aqui estão alguns tipos comuns de normalização:

### 1. Case Folding

Case Folding é o processo de converter todas as letras do texto em um formato consistente, geralmente minúsculas. Isso ajuda a tratar palavras com diferentes variações de capitalização que devem ser consideradas equivalentes. Por exemplo:
- "Casa", "casa" e "CASA" seriam convertidos para "casa".

### 2. Lemmatization

A Lemmatization é uma técnica que envolve a redução das palavras à sua forma base ou lema. Em contraste com o Stemming (abordagem mais simples), a lematização considera o contexto das palavras e retorna formas base que são semanticamente válidas. Por exemplo:
- "Correndo" seria lematizado para "correr".
- "Jogando" seria lematizado para "jogar".

### 3. Stemming

Stemming é o processo de reduzir as palavras à sua raiz ou stem. Ele remove os sufixos das palavras para obter uma forma básica. O Stemming é um método mais simples em comparação com a lematização, mas não leva em consideração o contexto e pode gerar raízes que não são palavras semanticamente válidas. Por exemplo:
- "Correndo" seria reduzido para "corr".
- "Jogando" seria reduzido para "jog".

### 4. Sentence Segmentation

A Sentence Segmentation é o processo de dividir um texto em frases ou sentenças individuais. Isso é importante porque muitas tarefas de NLP, como a análise de sentimentos e a tradução automática, são aplicadas em nível de sentença. Por exemplo:
- "Olá! Como você está? Eu estou bem." seria segmentado em duas sentenças: "Olá! Como você está?" e "Eu estou bem."


## Minimum Text Edit em NLP

O Minimum Text Edit (Edição Mínima de Texto) é um conceito no Processamento de Linguagem Natural (NLP) que se refere à quantidade mínima de alterações necessárias para transformar um texto de origem em um texto de destino. Essas alterações podem incluir inserções, exclusões ou substituições de caracteres, palavras ou frases. O objetivo é encontrar a sequência mais curta de edições para transformar um texto no outro.

Essa medida é frequentemente usada em tarefas como correção automática de texto, detecção de plágio e alinhamento de texto. O algoritmo de Edição Mínima de Texto mais comum é conhecido como "Distância de Levenshtein", que calcula o número mínimo de edições necessárias para transformar uma sequência de caracteres em outra.

### Exemplo de Minimum Text Edit

Vamos considerar o exemplo de transformar a palavra "casa" na palavra "casaco". Aqui está o processo de Edição Mínima de Texto:

1. Inserção: Adicionar o caractere "o" após o último caractere da palavra "casa".
2. Resultado: "casao".

Portanto, a distância de edição mínima entre "casa" e "casaco" é 1, representando a única alteração necessária.

## Modelo de Linguagem

O Modelo de Linguagem é uma técnica fundamental no Processamento de Linguagem Natural (NLP) que visa modelar a probabilidade de ocorrência de sequências de palavras em um determinado idioma. Ele é usado para prever a próxima palavra em uma sequência ou para avaliar a fluidez de uma sentença. 

### O que é um Modelo de Linguagem

Um Modelo de Linguagem é uma representação estatística das estruturas e padrões encontrados na linguagem. Ele captura a probabilidade de uma sequência de palavras ocorrer em um idioma específico. Um bom Modelo de Linguagem é capaz de prever com precisão a próxima palavra em um contexto dado.

### Definição Formal de um Modelo de Linguagem

Um Modelo de Linguagem é uma distribuição de probabilidade sobre todas as possíveis sequências de palavras em um idioma. Formalmente, dada uma sequência de palavras W = w1, w2, ..., wn, a probabilidade de ocorrência dessa sequência pode ser representada por P(W) ou P(w1, w2, ..., wn).

### O Problema da Dimensão do Modelo de Linguagem

O Problema da Dimensão ocorre no Modelo de Linguagem devido ao grande número de possíveis sequências de palavras. O número de sequências cresce exponencialmente com o tamanho do vocabulário e o comprimento da sequência. Isso leva à escassez de dados e à necessidade de métodos de suavização para lidar com sequências de palavras não observadas durante o treinamento.

### Suposição de Markov e N-Gramas no Modelo de Linguagem

O Modelo de Linguagem faz uso da suposição de Markov, que assume que a probabilidade de uma palavra depende apenas de um contexto limitado de palavras anteriores. Os N-Gramas são uma representação comum de um Modelo de Linguagem baseado nessa suposição. Um N-Grama é uma sequência de N palavras consecutivas em um texto.

### Configuração da Implementação do Modelo de Linguagem

A implementação de um Modelo de Linguagem geralmente envolve as seguintes etapas:

1. **Leitura do Corpus**: O corpus, que é um conjunto de textos de treinamento, é lido e pré-processado.

2. **Atualização de Contagens**: As contagens de ocorrência de N-Gramas são atualizadas com base no corpus.

3. **Modelo de Probabilidade**: As probabilidades de ocorrência de N-Gramas são calculadas a partir das contagens atualizadas.

4. **Amostragem de Texto**: O modelo treinado é usado para amostrar novas sequências de texto, gerando sentenças com base nas probabilidades aprendidas.

### Implementação do Modelo de Linguagem - Função de N-Gramas

Uma função comum em um Modelo de Linguagem é a criação de N-Gramas. Por exemplo, a função `create_ngrams(text, n)` recebe um texto de entrada e um valor N, e retorna uma lista de todos os N-Gramas presentes no texto.

### Implementação do Modelo de Linguagem - Função de Atualização de Contagens

Outra função importante é a atualização de contagens de N-Gramas com base no corpus. Por exemplo, a função `update_counts(ngrams, counts, corpus)` recebe uma lista de N-Gramas, um dicionário de contagens e um corpus, e atualiza as contagens com base nas ocorrências de N-Gramas no corpus.

### Implementação do Modelo de Linguagem - Função de Modelo de Probabilidade

A função de modelo de probabilidade é responsável por calcular as probabilidades de ocorrência dos N-Gramas com base nas contagens atualizadas. Por exemplo, a função `calculate_probability(ngrams, counts)` recebe uma lista de N-Gramas e as contagens correspondentes, e retorna as probabilidades de ocorrência dos N-Gramas.

### Implementação do Modelo de Linguagem - Leitura do Corpus

É necessário ler um corpus, que é um conjunto de textos, para treinar um Modelo de Linguagem. Por exemplo, a função `read_corpus(file_path)` recebe o caminho de um arquivo de texto e retorna o conteúdo do arquivo como um corpus.

### Implementação do Modelo de Linguagem - Amostragem de Texto

Por fim, a amostragem de texto permite gerar novas sequências de texto com base no Modelo de Linguagem treinado. Por exemplo, a função `sample_text(model, seed, length)` recebe um modelo de linguagem, uma semente inicial e um comprimento desejado e gera uma sequência de texto amostrada com base nas probabilidades aprendidas.

## Topic Modelling com Representações de Palavras e Documentos

- Vetores One-Hot: Representações binárias onde cada palavra ou documento é representado por um vetor de tamanho igual ao vocabulário.
- Implementação de Vetores One-Hot: Matriz em que cada linha representa um documento e cada coluna representa uma palavra do vocabulário.
- Limitações dos Vetores One-Hot: Não capturam a semântica entre as palavras e são ineficientes para grandes vocabulários.
- Frequência do Termo (TF): Métrica que representa a importância de uma palavra em um documento, calculada pela contagem do número de ocorrências.
- Implementação da Frequência do Termo: Cálculo da contagem de ocorrências de palavras em cada documento.
- TF-IDF (Term Frequency-Inverse Document Frequency): Métrica que combina a Frequência do Termo com a Frequência Inversa de Documentos, considerando a importância do termo no documento e em relação ao conjunto de documentos.
- Implementação do TF-IDF: Leitura do corpus, cálculo da Frequência de Documentos e cálculo do TF-IDF para cada termo em cada documento.
- Topic Modeling com TF-IDF: Identificação de tópicos ocultos nos documentos usando técnicas de agrupamento ou modelagem probabilística.
- Exemplo de Topic Modeling com Gensim: Uso da biblioteca Gensim para implementar algoritmos de Topic Modeling, como o LDA (Latent Dirichlet Allocation).



