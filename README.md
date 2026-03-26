# Saving SuperStore: Data Visualization with Tableau

## Project Overview
The Superstore is in financial trouble. As a data consultant, 
I analyzed the Superstore dataset to identify profit centers, 
loss-making areas, advertising opportunities, and product 
return patterns — with the goal of providing actionable, 
data-driven recommendations to restore profitability.

## Live Dashboard
🔗 [View on Tableau Public](https://public.tableau.com/views/Saving_SuperstoreReviewed/ProductReturnRate?:language=en-US&:sid=&:redirect=auth&publish=yes&showOnboarding=true&:display_count=n&:origin=viz_share_link)

---

## Key Findings

### Part 1: Profits & Losses
- **Top profit centers:** Copiers and Phones in the West 
  and East regions generate the highest profit of any 
  Sub-Category + Region combination.
- **Biggest loss-makers:** Tables in the East and Central 
  regions consistently lose money, driven by heavy 
  discounting and poor margins.
- **Products to stop selling:** The Cubify CubeX 3D Printer, 
  GBC DocuBind P400, and Lexmark MX611 are the three 
  worst-performing products by total profit loss.
- **Subcategories to focus on:** Copiers (~$55K profit), 
  Phones (~$44K), and Accessories (~$42K).
- **Subcategories to discontinue:** Tables (~-$18K), 
  Bookcases (~-$3K), and Supplies (~-$1.5K).

### Part 2: Advertising Opportunities
The three best state + month combinations for advertising 
based on average profit per order are:

| State | Month | Avg. Profit | Recommended Max Ad Spend (1/5 rule) |
|---|---|---|---|
| Washington | March | ~$255 | ~$51 per order |
| New York | October | ~$130 | ~$26 per order |
| Washington | July | ~$85 | ~$17 per order |

California maintains steady profitability year-round 
($30–$50 avg. profit) and is a reliable secondary target.

### Part 3: Returned Items
- The `Returns` table was LEFT JOINed onto `Orders` to 
  preserve all orders including those with no returns.
- A calculated field converted `Returned` values to binary 
  (Yes = 1, null = 0) to compute return rates.
- Sub-categories with high return rates and negative profit 
  (Tables, Supplies) should be discontinued.
- Sub-categories with strong profit and manageable return 
  rates (Copiers, Phones, Accessories) should be maintained 
  and invested in.

---

## Visualizations Included
| Sheet | Purpose |
|---|---|
| Region + Sub-Category | Full profit/loss overview by dimension pair |
| Profit Centers | Top 2 Sub-Category + Region combinations |
| Loss-makers | Bottom 2 Sub-Category + Region combinations |
| Products to Stop Selling | All negative-profit products |
| Top 3 Subcategories | Best performing subcategories |
| Bottom 3 Subcategories | Worst performing subcategories |
| Advertising Opportunities | Heat map of avg profit by state + month |
| Top 3 States | Line chart of monthly avg profit for CA, NY, WA |
| Product Return Rate | Highest return rate products |
| Customers with Highest Return | Highest return rate customers |
| Avg Profit vs Avg Return Rate | Scatter plot by Sub-Category |

---

## Tools & Techniques
- **Tableau Public** — data visualization
- **Calculated fields** — binary return rate field
- **LEFT JOIN** — merging Orders and Returns tables
- **Top N filters** — isolating best/worst performers
- **Heat maps, bar charts, line charts, scatter plots**

---

## Dataset
- `Superstore.xls` — provided by TripleTen Data Science program

---

## Author
**Abena Ntim Asamoah**  
TripleTen Data Science — Sprint 4: Data Visualization with Tableau
