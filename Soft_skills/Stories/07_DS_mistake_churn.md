[⬅ Story index](00_Contents_list.md)

## Story 7. A DS mistake — churn target definition

> When I was building my first churn model, the initial results looked very good. The model had strong metrics, so at first it seemed like we had built a really good model.
>
> But at some point, I started looking more closely at why the model metrics were good while the actual reduction in churn was very small. That's when I found a problem with the way the target had been defined.
>
> The positive class included users who had already churned recently because the data loader was also pulling historical logs for them. So, in a way, the model was very good at predicting something that had already happened. And, of course, we couldn't do anything to prevent churn for those users.
>
> So technically, the model looked very good based on its ML metrics, but from a business perspective, we were solving the wrong problem because the target was defined incorrectly.
>
> In the end, we had to rebuild the target.
>
> This was an important lesson for me: good ML metrics alone don't mean that a model is solving the right problem. You need to keep checking what exactly you are predicting, which data you are using, at what point in time you are making the prediction, and whether you can actually do something with the result.

---

*See also: [Churn v1→v4](../../Portfolio/04_Churn_v1-v4%20(3%20min).md) in the Portfolio — same project, more technical detail (v1–v4, AFT).*

[⬅ Story index](00_Contents_list.md) · [← Previous: A rejected idea — KPI](06_Rejected_idea_KPI.md) · [Next: A production failure ➡](08_Production_failure_reco.md)
