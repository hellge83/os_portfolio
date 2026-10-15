[⬅ Project index](00_Contents_list.md)

### 🔹 Offers / RecSys

**SHORT:** *(1 min)*
> "The goal was to increase revenue by showing players more relevant offers. At the same time, we wanted to avoid some system problems, like giving unnecessary discounts or shifting revenue from one channel to another.
> 
> For the first version, I designed the solution, built the model and integrated it into production myself. Later, for version two, I moved into a lead role and coordinated the development.
> 
> The first version increased incremental revenue by 8% in A/B testing. The second version reduced the average discount by 2%, which meant real cost savings."
> 
> **STACK:** Python, Implicit (ALS + cosine similarity for v1), LightFM (for v2)

**DEEP DIVE:** *(1 min 30 sec)*
> "The first version was based on Implicit library using ALS and cosine similarity. Overall, it worked well and gave us the 8% revenue increase, but we found two important issues.
> 
> The first was cannibalization. On some projects the recommendation with creating new revenue shifted it from one channel to another.
> 
> The second was the cold-start problem. For new players, we used a daily calculated top list of offers. It worked, but it wasn't personalized.
> 
> In the second version, we switched to LightFM because it could use both user and offer features. This gave us better personalization and solved the cold-start problem by looking at similar players instead of using a fixed list. It also helped us reduce the average discount by 2%.
> 
> But honestly, the machine learning part wasn't the hardest. The biggest challenge was the product logic: deciding which offers to recommend, how many to show, how to rank them, how to avoid filter bubble and how to balance personalization with business goals."

---

[⬅ Project index](00_Contents_list.md) · [Next: Stack and process ➡](10_Stack_and_process%20(30%20sec).md)
