# Challenge 5- Generate Embeddings and export them to Azure Search

**Objective**

Use OpenAI to generate embeddings from documents and export to Azure
Search.

**Steps:**

1.  In Azure OpenAI-\> Azure AI Foundry:

    - Deploy text-embedding-ada-002 manually

2.  Create search index( name : **Fleet_index** )manually with fields:

**id: String (Key)**

**filename: String (Searchable)**

**content: String (Searchable)**

**embedding: Collection(Edm.Single)**

3.  Run the notebook: **export_embeddings_to_search.ipynb**

**Success Criteria:**

- Index is populated with document content + embedding vectors

- Can search vector index from Azure portal
