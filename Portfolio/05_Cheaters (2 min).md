[⬅ Project index](00_Contents_list.md)

### 🔹 Cheaters classification

**SHORT:** *(1 min)*
> "The goal was to detect cheaters early, so we could keep our dashboards, game balance analysis and business metrics clean. Without filtering them out, they could seriously distort the data.
> 
> I built the whole solution myself, from feature engineering to model validation. We used CatBoost, and on the test set the model achieved 0.98 precision, 0.91 recall and a ROC-AUC of 0.953.
> 
> The model was ready for production, but it wasn't deployed because the client changed priorities before rollout."
> 
> **STACK:** Python, CatBoost

**DEEP DIVE:** *(1 min)*
> "The main goal wasn't to punish cheaters. It was to keep our analytics clean. Cheaters can significantly distort dashboards and business metrics, so identifying them early improves the quality of many downstream analyses
> Technically, it was a CatBoost classifier on tabular data. One of the most important feature  was geography, which we encoded using revenue tiers instead of raw country names.
> 
> The only thing I should mention is that the model never reached production. Before deployment, the client changed priorities, so the project was stopped. Because of that, I don't have production monitoring experience for this particular model.
> 
> Even though this model wasn't deployed, the problem itself is very similar to fraud detection: highly imbalanced data, careful feature engineering, and balancing precision against recall. That's one of the reasons I'm interested in this role"

---

[⬅ Project index](00_Contents_list.md) · [Next: Non-payers ➡](06_Non-payers%20(2%20min).md)
