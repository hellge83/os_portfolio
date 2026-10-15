[⬅ Project index](00_Contents_list.md)

### 🔹 ARPU clusterization / content personalization
**SHORT:** *(1 min)*
> "The goal was to personalize content based not only on how much a player spends, but also on their behavior. We wanted to avoid treating all players in the same payment segment the same way. As the team lead, my role was to define the business problem, to design the approach and coordinate the work. The implementation was done by the team, and the system is now used in production.
> Today, each player has two labels: one based on actual spending, and another based on predicted behavior."
> 
> **STACK:** Python, K-means, multiclass classification (softmax)

**DEEP DIVE:** *(1 m 30 s)*
> "The main idea was that spending alone doesn't tell the whole story. Spending tells us the player's value today, while behavior helps us understand how the player got his value. 
> 
> To define the behavioral segments, we first used K-means clustering. One important product decision was not to recompute the clusters every day to avoid constantly reshuffling people between segments, making personalization unstable.
> 
> The payment segment is based on actual spending, so there's no prediction there. The behavioral segment is predicted by a multiclass classification model. It outputs probabilities for all behavioral segments, and we assign the player to the most likely one.
> 
> Because the classes are imbalanced, we evaluated the model using weighted F1 with a one-vs-rest approach to make sure smaller segments were also predicted well.
> 
> For me, the most interesting part wasn't choosing the algorithm. It was designing a segmentation that was both accurate and enough to be used in production."

---

[⬅ Project index](00_Contents_list.md) · [Next: Chronos / ROAS ➡](08_Chronos_payback_prediction%20(3%20min).md)
