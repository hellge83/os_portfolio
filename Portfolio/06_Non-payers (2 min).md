[⬅ Project index](00_Contents_list.md)

### 🔹 Non-payers prediction

**SHORT:** *(1 min)*
> "The goal was to identify players who were unlikely to make a purchase, so we could start showing them ads earlier. At the same time, we wanted to avoid showing ads to players who might still become paying users.
> 
> I built the model, integrated it into production, and later helped another team integrate it into their own pipeline. 
> 
> We used CatBoost, but in production we only acted on the predicted non-payer class. That made the system much more conservative and reduced the risk of making wrong decisions for new players"
> 
> **STACK:** Python, CatBoost

**DEEP DIVE:** *(1 min)*
> "Technically, the model predicts whether a player will make a purchase. But from a business point of view, the real question was when it's safe to start showing ads.
> 
> In production, we only act when the model predicts that a player is a non-payer. This conservative approach helps avoid showing ads to players who might still become paying users.
> 
> One interesting challenge was that non-paying players don't have a first payment day, because they never make a purchase. Instead of leaving this feature empty, I generated synthetic values using a log-normal distribution fitted on the upper percentiles of real paying users. This allowed us to keep the helpful information from these data and to increase offline metrics
> 
> The interesting part wasn't training the classifier. It was deciding how to use its predictions safely in production."

---

[⬅ Project index](00_Contents_list.md) · [Next: ARPU clusterization ➡](07_ARPU_clusterization%20(2%20min%2030%20sec).md)
