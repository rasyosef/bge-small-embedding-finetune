# Fine-tune bge-small Embedding model for Retrieval Augmented Generation (RAG).ipynb

This notebook contains code for fine-tuning the `33M` parameter [BAAI/bge-small-en-v1.5](https://huggingface.co/BAAI/bge-small-en-v1.5) text embedding model on a synthetic dataset from the 2023_10 NVIDIA SEC Filing ([philschmid/finanical-rag-embedding-dataset](https://huggingface.co/datasets/philschmid/finanical-rag-embedding-dataset)) using the Sentence Transformers library.

### Results
The metric used to evaluate the embedding models is normalized discounted cumulative gains (ndcg@10) 

|Dimension|Baseline|Fine-tuned|Improvement|
|:--------|:-------|:---------|:----------|
|384|0.7314|0.8202|12.14%|
|256|0.7206|0.8187|13.61%|
|128|0.6852|0.8067|17.73%|
|64|0.6216|0.7863|26.50%|

### References
https://www.philschmid.de/fine-tune-embedding-model-for-rag