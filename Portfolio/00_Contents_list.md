[⬅ Portfolio home](../00_Index.md)

# Projects

1. [Analytics RAG](01_Analytics_RAG%20(4%20min).md) — Gen AI RAG
2. [AI-documentation (Obsidian + MCP)](02_AI_docs%20(3%20min).md) — Gen AI
3. [Monitoring and model lifecycle](03_Models_monitoring%20(3%20min).md) — model risk management and governance
4. [Churn evolution v1 → v4](04_Churn_v1-v4%20(3%20min).md) — model evolution
5. [Cheaters classification](05_Cheaters%20(2%20min).md) — anti-fraud
6. [Non-payers prediction](06_Non-payers%20(2%20min).md) — feature engineering
7. [ARPU clusterization / personalization](07_ARPU_clusterization%20(2%20min%2030%20sec).md) — user behavior
8. [1-year ROAS/payback — Amazon Chronos](08_Chronos_payback_prediction%20(3%20min).md) — Innovate to Grow
9. [Offers / RecSys](09_Offers_RecSys%20(2%20min%2030%20sec).md) — +8% rev increase
10. [Stack and development process](10_Stack_and_process%20(30%20sec).md)
11. [Bonus: meeting recordings transcription](11_Meeting_transcription%20(1%20min).md) — Gen AI

---

## Code samples

My production work is under NDA, so these two public case studies illustrate two kinds of work that often matter more than training the model itself: **building the business logic around an ML model and taking ownership of undocumented legacy systems.**

- [**Loan Applications**](https://github.com/hellge83/loan-applications) — **Turning model predictions into business decisions.** A credit risk model is only one component of a lending decision process. The real challenge is designing the logic around it: translating default probabilities into approval decisions using the actual cost of false approvals and false rejections, explaining individual decisions, checking for potential bias, and defining how the system should be deployed, monitored and governed. The result is a business-oriented design for a credit decision system, not just a model with an AUC score.

- [**YSDA Contest**](https://github.com/hellge83/YSDA_contest) — **Reverse-engineering and reworking undocumented legacy ML.** Take over an existing pipeline with no documentation, 24 anonymous features and a seemingly impressive ROC-AUC of 0.97. Before improving anything, establish what the system actually does: reconstruct the features from raw transaction data, trace data leakage, verify the original results and identify how the underlying patterns change over time. The result is a rebuilt feature pipeline and a more realistic validation setup that accounts for temporal drift and previously unseen clients and merchants.

---

[Next: Analytics RAG ➡](01_Analytics_RAG%20(4%20min).md)
