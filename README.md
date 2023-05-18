# Modality Shifts
## TLDR
This repo contains supplemental materials accompanying the "Leverage Points in Modality Shifts: Comparing Language-only and Multimodal Word Representations" paper, presented at StarSEM 2023. 

## Data
The dataset consists of word pairs. To collect them, we start with 1000 most frequent words in FastText. For each of them, we take 100 closest words, by cosine distance over FastText embeddings. We filter this list of pairs in several ways. 
Each of the resulting pairs was characterized along a set of properties of interest, collected over a variety of available sources of human-annotated semantic information. 
This gives us 13k word pairs in total, each of the pairs gets characterized along 30 individual semantic parameters (\*2, for the first and the second noun in the pair) and 16 relational parameters; plus, word count for each of the words in the pair.

We use several textual and multimodal models to generate embeddings and collect the distances between the words in each pair for their embeddings from the models of interest. 
See the paper for more details.

The resulting dataset is stored in the `data/words_features.zip` file.

## Code and results

The results are available in `report.tsv` and `pivot.tsv` files.
You can reproduce them by running `modality_shifts_playbook.ipynb`.