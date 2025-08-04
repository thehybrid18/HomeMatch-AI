# <span style="color:blue">HomeMatch Real Estate Semantic Search</span>

## <span style="color:blue">Project Overview</span>
HomeMatch is a demonstration application using **LangChain**, **OpenAI GPT models**, and a **vector database (FAISS/Chroma)** to create and search real estate listings semantically. 
This approach allows matching user preferences (e.g., number of bedrooms, neighborhood vibe, amenities) with synthetically generated property listings.

The application simulates how future **chatbox integrations** could personalize real estate searches by combining **retrieval-augmented generation (RAG)** with LLMs.

---

## <span style="color:blue">Features</span>
- **Synthetic Listing Generation:** Creates realistic real estate property descriptions using GPT.
- **Vector Storage with FAISS/Chroma:** Converts listings into embeddings for semantic search.
- **Preference-Based Search:** Matches user responses to property listings based on cosine similarity.
- **Personalized Augmentation:** Tailors property descriptions to emphasize user-specific preferences.

---

## <span style="color:blue">Workflow</span>
1. **Generate Listings:** Use GPT to create 10+ synthetic property listings with neighborhood details.
2. **Store in Vector Database:** Convert each listing to embeddings and store in FAISS or Chroma.
3. **Collect Buyer Preferences:** Gather buyer responses via predefined questions or free-form input.
4. **Semantic Search:** Perform nearest-neighbor search to find the most relevant property listings.
5. **Personalize Results:** Enhance top-matching listings using GPT to highlight features important to the buyer.

---

## <span style="color:blue">Requirements</span>
- Python 3.8+
- Jupyter Notebook
- Installed libraries (requirements.txt):
  ```bash
  pip install langchain openai chromadb pandas tiktoken pydantic sentence-transformers transformers
  ```

---

## <span style="color:blue">How to Run</span>
1. Clone this repository or download the project files.
2. Open the Jupyter Notebook (`HomeMatch.ipynb`) in your environment.
3. Ensure your **OpenAI API key** is set:
   ```python
   import os
   os.environ["OPENAI_API_KEY"] = "your-api-key"
   os.environ["OPENAI_API_BASE"] = "https://openai.vocareum.com/v1"
   ```
4. Run each notebook cell step-by-step to:
   - Generate listings
   - Build vector index
   - Input buyer preferences
   - Query and personalize search results

---

## <span style="color:blue">Example Use Case</span>
This project can be adapted into a **real-time chatbox** for real estate dashboards. 
A buyer could chat with the system about their preferences, and the app would retrieve and personalize property matches instantly.

---

## <span style="color:blue">Files Included</span>
- `listings.txt`: Generated property listings
- `HomeMatch.ipynb`: Full project notebook
- `README.md`: Project documentation

---

## <span style="color:blue">Future Improvements</span>
- Integrate live real estate data APIs
- Add user authentication and saved searches
- Support multi-turn conversation for evolving preferences
