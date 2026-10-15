[⬅ Project index](00_Contents_list.md)

### 🔹 1-year ROAS/payback prediction — Amazon Chronos 
**SHORT:** *(1 min)*
> "The goal was to estimate 1-year return on marketing spends much earlier instead of waiting a full year. This helped the business make investment decisions much faster.
> 
> I built and integrated the first version myself. Later, for version two, I moved into a lead role and worked closely with our A/B testing principal on the statistical part.
> 
> We used Amazon Chronos, a foundation model for time series forecasting, and after fine-tuning it on our own data we achieved a MAPE between 12% and 20%, depending mainly on the cohort size."
> 
> **STACK:** Python, Amazon Chronos, AWS SageMaker, bootstrap resampling

**DEEP DIVE:** *(2 min)*
> "We wanted to predict long-term revenue much earlier. Instead of building a forecasting model from scratch, I decided to try Amazon Chronos, which is a pretrained foundation model for time series and fine-tuned it on our own cohorts
> 
> Training required much more GPU memory than I had locally, so I used a rented SageMaker instance. My local machine could only handle the smallest Chronos model
>
> Our goal wasn't to reproduce the whole revenue curve perfectly. What really mattered was the predicted value around day 360, because that's what the business used for decision making. That's why I evaluated the model mainly on the last part of the prediction array instead of the whole time series. I used MAPE because it's easy to explain to business stakeholders, and in our case divide-by-zero wasn't a problem since we only worked with paying users.
>
> One interesting challenge was confidence intervals. Small cohorts are much noisier than large ones, so using the same confidence interval for every prediction could be wrong. Together with our A/B testing principal, we used bootstrap sampling to estimate prediction errors for different cohort sizes. Then we adjusted the interval width based on the cohort size (scaled the interval approximately by 1 over the natural logarithm of the cohort size.). Smaller cohorts received wider confidence intervals, while larger cohorts had much narrower ones."

---

[⬅ Project index](00_Contents_list.md) · [Next: Offers / RecSys ➡](09_Offers_RecSys%20(2%20min%2030%20sec).md)
