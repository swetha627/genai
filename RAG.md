RAG - Retrieval Augmented Generation:

Embedding ---> Indexing ---> Augmentation ---> Generation

**Embedding** - generate vectors from text using an embedding model
**Indexing** - Vectors are indexed for fast retrieval, **ANN(Approximate nearest neighbours)** algo is used to index. indexed vectors are stored in Vector Db's for similarity search.
**Retrieval** - User Query is converted into dense vector using same embedding model. This embeded query is then searched against the Vector Database and retrieve relevant chunks.
                these retrieved relevent chunks are then passed to the LLM as context along with the user query. A **Reranker Model** is used to get the best out of all the retrievals.
**Augmentation:** - Retrieved releveant chunks are combined to form a context. Used embedding query is also merged with context to form **PROMT** for LLM
**Generation** - pass the promt to LLM to generate response.

