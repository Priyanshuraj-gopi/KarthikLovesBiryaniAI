# Data dictionary

All records are synthetic and generated in the browser.

| Dataset | Records | Main fields |
|---|---:|---|
| Customer reviews | 240 | review/customer/order IDs, date, dish, rating, text, primary complaint, delivery, order value, period, intervention flag |
| Orders | 720 | order/customer IDs, period, repeat flag, amount, delivery minutes |
| Customers | 168 | anonymised customer ID, synthetic flag, first-order date, order count |
| Menu | 10 | dish ID/name, price, availability |
| Packaging | 5 | packaging ID/name, unit cost, use, status |
| Cost assumptions | 10 | dish, selling price, estimated ingredient and packaging costs |
| Interventions | 3 | intervention ID/name/status/cohort/cost estimate/description |
| Business metrics | 1 JSON | review counts, computed averages, rating distributions, low-rating share, repeat-order share |

Review cohorts use the fixed star distributions in the project brief. Categories are synthetic labels assigned during generation, not model predictions.
