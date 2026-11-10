# Fun with LLMs

Collection of notebooks relating to LLMs. Built January to March 2024.

## 1) AirBnB similarity search
[similarity.ipynb](notebooks/similarity.ipynb) - Creating embeddings from previously ingested AirBnB data and storing them in Postgres using the PGVector extension. We perform a test by describing our ideal listing, create embeddings from the description, then finding existing listings that closely match our description.
- For example, the query 'A cute secluded place with a laid back vibe. A small place, preferably a closet' returns 'Private room in quite area. quite, nice size private room' as its closest listing.

## 2) Chat with your data
[sql_agent_trino.ipynb](notebooks/sql_agent_trino.ipynb) - Utilize LangChain and ChatGPT 3.5 to build a simple SQL Agent that lets a user ask questions like "Which neighborhood has the best reviews?" for our AirBnB data, and get an answer from the SQL agent.

## Running
- The data is the Kaggle Seattle Airbnb dataset (airbnb/seattle), loaded into a Trino lakehouse on localhost:8082 by a separate pipeline.
- Start Postgres with pgvector: `docker compose -f databases/pgvector-airbnb-listings.yaml up -d`. The credentials in `databases/.env.pgvector` are local-only container defaults.
- Install the packages with `pip install -r requirements.txt`. I used Python 3.9.
- The SQL agent needs `OPENAI_API_KEY` set.
