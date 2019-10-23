# Programming Challenge

Starting with a text document...

  * parse the text document in `spaCy`
  * iterate through each sentence...
  * filter for `token.pos_ in ["ADJ", "NOUN", "PROPN", "VERB"]`
  * print the results

Next, construct a graph...

  * create a graph in `networkx` 
  * use `key = (token.lemma_, token.pos_)`
  * create graph nodes using the key
  * link nodes in each sentence which are within 3 hops
  * visualize the graph

Next, rank tokens based on their "connectedness" within the graph...

  * run `pagerank()` on the graph (eigenvalue centrality)
  * print the ranks (sort descending) and their lemma values

Next, apply the ranks to the noun chunks within the text...

  * iterate through each noun chunk in the text document
  * sum the ranks for each token (lemma) within the noun chunk
  * print the noun chunks (sort descending)

Extras:

  * use `spacy-wordnet` to add links among hypernyms and hyponyms
  * restrict the WordNet domains to specific areas of interest
  * how could you use noun chunks and entities within the graph?