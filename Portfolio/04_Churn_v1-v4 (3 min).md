[⬅ Project index](00_Contents_list.md)

### 🔹 Churn — evolution v1 → v4
**SHORT:** *(1 min)*
> "This is our first model. The goal was to identify players who were likely to churn early enough to take action. At the same time, we didn't want to waste retention offers on players who would have stayed anyway.
> 
> I built the first two versions myself. After some time, we realized an important limitation: the model was good at identifying players who had already stopped playing. But for business it was  too late. Later, for versions three and four, I moved into a lead role, defining the approach and mentoring the team.
> 
> Today we're on version four. We use a survival model based on Accelerated Failure Time. The current model has an F1 score of 0.75 and helped reduce 7-day churn by 4%"
> 
> **STACK:** Python, XGBoost (v1–v3), Accelerated Failure Time survival model (v4), probability calibration

**DEEP DIVE:** *(2 min)*
> "The first version used XGBoost. We predicted whether a player would  churn within the next seven days. For this problem, precision was more important than recall. Sending unnecessary retention gifts could decrease future monetization , so we preferred to miss some churners rather than target loyal players.
>
> Version three redefined the target to include players who'd return within 3 days, then disappear for 7. The offline metrics became slightly worse, which we expected because the prediction task became harder.
> 
> More importantly, after deployment the model started degrading over time, and retraining wasn't enough to solve the problem. That's why, in version four, we moved to a survival model using Accelerated Failure Time because churn is a time-to-event problem. We don't just want to know whether someone will churn. We also want to know when they're likely to churn, so we can decide when to intervene.
>
> Instead of predicting a fixed churn probability, the model estimates the expected time until churn. From that, we can calculate the probability for any time horizon we need. We also added a probability calibration step so the predicted probabilities better matched the real churn rate. Result: F1 of 0.75, and a 4% reduction in 7-day churn overall."

---

[⬅ Project index](00_Contents_list.md) · [Next: Anti-fraud ➡](05_Cheaters%20(2%20min).md)
