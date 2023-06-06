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
