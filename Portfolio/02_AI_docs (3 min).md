[⬅ Project index](00_Contents_list.md)

### 🔹 AI-documentation (Obsidian + MCP)

**SHORT:** *(40 sec)*
> "We had a common problem: a lot of knowledge lived in people's memory instead of in documentation. 
> 
> I built an AI-assisted workflow that turns raw notes, meeting summaries and code into structured documentation. The documentation is designed for both people and AI agents. This let us to include AI agents into our daily routine and keep the context switching between tasks.
> 
> I built the whole solution myself and trained our analysts to use it. Right now it's in pilot testing with the team.**"
> 
> **STACK:** Obsidian, MCP (including a sequential-thinking server), Bitbucket, JupyterLab, Jupyter-ai

**DEEP DIVE:** *(2 min 30 sec)*
> "The biggest problem wasn't writing documentation. It was keeping knowledge in one place where both people and AI could use it.
> 
> We use Obsidian as the main knowledge base for humans. It's connected to our AI agents in IDEs through MCP and synchronized with Bitbucket.
> 
> One important design decision was to make the AI work step by step. Instead of asking the agent to solve a large task at once, it breaks the work into smaller steps. If something goes wrong, we can return to the exact step where the problem happened instead of starting from scratch. That's why  I added a sequential-thinking component connected by MCP.  Prompts are structured using an approach based on Karpathy's method, adapted for this setup.
> 
> We're now extending the same approach to our cloud JupyterLab to decrease time spent for our daily tasks. The idea is to have one shared knowledge base that stays synchronized across tools and people, so both people and AI agents always work with the same information. Later we also plan to connect our SQL assistant to the same knowledge base.
> 
> And now it's a good moment to mention my **AI Philosophy**
> More generally, this is how I deal with AI agents.
> 	1. I always keep a human in the loop. To do that you need to have some appropriate background. It's a bad idea, for example, to build a Python framework if you are a UX designer, even you are a really good in UX
> 	2. I prefer breaking complex tasks into small steps
> 	3. Before starting, I define what success looks like, and afterward check the result against that criteria
> 	4. When AI works close to production systems, I always keep permissions as limited as possible.
> 	5. And I always remember that I'm responsible of the results, not an AI

---

[⬅ Project index](00_Contents_list.md) · [Next: Monitoring and model lifecycle ➡](03_Models_monitoring%20(3%20min).md)
