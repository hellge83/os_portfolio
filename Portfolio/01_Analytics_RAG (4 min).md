[⬅ Project index](00_Contents_list.md)

### 🔹 Analytics RAG

**SHORT:** *(50 sec)*
> "Over the years, our team produced a lot of valuable research, but it was spread across hundreds of Confluence pages. People often spent more time looking for information than using it. To solve this, I built a RAG system that lets anyone ask a question in natural language and get an answer based on our own research.
> 
> I built the MVP myself using Gemini to prototype the solution. After we validated the idea, I worked together with our Big Data Engineer to prepare the production version. The first version is now live, and we are collecting the feedback.**"
> 
> **STACK:** Python, LangChain, MongoDB (as vector store), BeautifulSoup, Amazon ECS, Gemini for prototyping

**DEEP DIVE:** *(3 min)*
> "The biggest challenge wasn't retrieval itself. It was the quality of the source documents. Our Confluence pages had very different structures, nested sections and interactive plots that couldn't simply be converted to PDF or MD.
> 
> I parsed the pages with BeautifulSoup. Large pages were split into logical sections, and then into smaller semantic chunks. For interactive plots, I converted the data into tables, compressed and split anything too big into numbered parts, saved this numbers in metadata to reassemble it
> 
> One design decision we made was to keep both the original document and the chunks together. That's why we chose MongoDB instead of a traditional vector database. It helped us keep the source document, the chunks and the metadata synchronized.
> 
> The retrieval pipeline uses LangChain. Depending on the user's question, the system understands the intent, rewrites the query if needed, retrieves relevant chunks using MMR, reranks them, and then generates the final answer using retrieved context and conversation history.
> 
> We also added logging through Amazon ECS so with my own log parser we could analyze query history.
> 
> Right now we're collecting user feedback. The next step is hybrid search, and later we'd like to let an LLM interpret charts automatically instead of converting them manually because it's a real hard job to parse the layout of every type of Plotly plot
> 
> The hardest part wasn't learning how RAG works. There are many good courses and examples online. The real challenge was turning those ideas into a production-ready solution that worked well with our own data and gave good retrieval quality. That meant spending a lot of time on document parsing, chunking, adding metadata, and retrieval quality. I learned that the quality of a RAG system depends much more on the data and information architecture than on the LLM itself."

*See also: [AI-documentation](02_AI_docs%20(3%20min).md) — more on how I work with AI agents in general.*

---

[⬅ Project index](00_Contents_list.md) · [Next: AI-documentation ➡](02_AI_docs%20(3%20min).md)
