[⬅ Story index](00_Contents_list.md)

## Story 8. A production failure — recommendation system

> We had a project with a recommendation system that had been working well for quite a long time. But after about a year, we had a production failure. The system was supposed to select five offers from dozens of available options, but only three were left in the interaction history logs.
>
> The problem happened because the LiveOps Manager didn't notice that the offers had stopped running. As a result, there were fewer and fewer player interactions in the logs. But I also see this as my responsibility because I was responsible for the system. I hadn't considered this scenario in the code, and I hadn't set up an alert to warn us when the number of available offers became lower than the minimum required.
>
> At the time, I thought it was very unlikely that this situation would ever happen. But technically, the system could get into that state, and that alone was a good enough reason to plan for it.
>
> That was my main takeaway. If a system can technically fail because of a particular state of the data or infrastructure, we should account for it in both the code and the monitoring, even if the scenario seems unlikely from a business point of view.
>
> Following the same logic, we also introduced monitoring for data freshness in the tables we use. Sometimes upstream systems fail and stop sending fresh logs.
>
> This experience changed the way I think about these kinds of problems. It's not enough to check that a model or an algorithm works well under normal conditions. You also need to think about what will happen if the input data is different from what you expect.
>
> Of course, it's impossible to predict every corner case or prepare fixes for every future bug in advance. But at the very least, it's worth thinking about logging at important stages and setting up different levels of alerts beforehand.

---

*See also: [Offers / RecSys](../../Portfolio/09_Offers_RecSys%20(2%20min%2030%20sec).md) and [Monitoring and model lifecycle](../../Portfolio/03_Models_monitoring%20(3%20min).md) in the Portfolio — same project, more detail on the stack and monitoring.*

[⬅ Story index](00_Contents_list.md) · [← Previous: A DS mistake — churn](07_DS_mistake_churn.md) · [Next: Mentoring ➡](09_Mentoring.md)
