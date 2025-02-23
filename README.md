My first dive into the RAG for AI applications

I used the book "The Great Gatsby" as the document to feed my model. 

Along with playing with the project, I applied several techniques, such as:

1. Decoupling which  means separating the query embedding process from retrieving search results, allowing each part to be optimized independently
2. Contextual Query Rewriting where I added the hypothetical chat history regarding the book. This helped the model to get a richer context and thus improving the results
3. HyDE-rag where the model generates a hypothetical answer to my query. This hypothetical answer is then embedded and used for the similarity search.
4. Fusion search where the model is tasked to break down a "complex" query into subqueries. Then, for each subquery the answer is generated and combined for the final one

First, I wanted to run the application locally but when I feed the model with the chunks(no matter what values I assigned to chunk_size and chunk_overlap), my kernel died constantly.
That is why I switched to Google collab :)

The libraries I used:

1. ChromaDB
2. Langchain
3. OpenAI(for sure)
4. Requests
