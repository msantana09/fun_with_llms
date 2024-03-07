# Fun with LLMs


Collection of notes, notebooks, scripts relating to LLMs

## 1) AirBnB similarity search
[similarity.ipynb](notebooks/similarity.ipynb) - Creating embeddings from previously ingested AirBnB data and storing them in Postgres using the PGVector extension. We perform a test by describing our ideal listing, create embeddings from the description, then finding existing listings that closely match our description. 
- For example, say you want a 'small quiet location to help clear my mind'.  The matching listings might be a cabin in the woods, or a house with dedicated meditation space. 


## 2) Chat with your data
[sql_agent_trino.ipynb](notebooks/sql_agent_trino.ipynb) - Utilize LangChain and ChatGPT 3.5 to build a simple SQL Agent allow a user to ask questions like "Which neighborhood has the best reviews?" for our AirBnB data, and get a valid response from the SQL agent. 