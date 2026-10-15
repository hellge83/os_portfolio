[⬅ Project index](00_Contents_list.md)

### 🔹 Monitoring and model lifecycle 

**SHORT:** *(1 min)*
> "For me, deploying a model isn't the end of the project. The goal is to detect problems before they become business problems. 
> 
> As the lead, I designed our monitoring approach. We monitor models on three levels: the model itself, the infrastructure, and the feedback loop once real outcomes become available.
> 
> This approach helped us detect that the third version of our churn model was slightly degrading in production. That was one of the reasons we redesigned it and moved to the survival model in version four.**"
> 
> **STACK:** NannyML (Confidence-Based Performance Estimation + PerformanceCalculator)

**DEEP DIVE:** *(2 min)*
> "I usually think about the ML lifecycle in three stages: design, development and deployment. Monitoring is an important part of deployment, because models naturally change over time.
> 
> The **Statistical layer** monitors the model predictions themselves. We use NannyML's Confidence-Based Performance Estimation to estimate model quality even before we have real labels. This helps us detect potential degradation much earlier.
> 
> The **Infrastructure layer** monitors the system itself: input data, request volume, latency and other operational checks. For example, we have alerts if an input table isn't updated, or if a recommendation job can't generate enough offers.
> 
> The **Feedback layer** starts working once real outcomes become available. Then we compare predictions with reality using NannyML's Performance Calculator. This is how we discovered that our third churn model was slowly degrading over time.
> 
> Mostly we monitor prediction drift and estimated performance drift. But I also pay attention to data quality, because sometimes the problem isn't the model—it's the input data. For me, monitoring isn't just about keeping a model alive. It's about making sure the business can continue trusting its predictions."

---

[⬅ Project index](00_Contents_list.md) · [Next: Churn v1 → v4 ➡](04_Churn_v1-v4%20(3%20min).md)
