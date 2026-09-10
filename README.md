# 🛒 Olist Marketplace — Sales & Customer Intelligence Study

[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python)](https://github.com/manthan-sagar/olist-ecommerce-analysis/blob/main/pyproject.toml)
[![Tableau](https://img.shields.io/badge/📊_Live_Dashboard-254E6B?logo=tableau&logoColor=white)](https://public.tableau.com/views/OlistPerformance/Sales?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
[![Jupyter Notebook](https://img.shields.io/badge/-Notebook-F37626?logo=jupyter&logoColor=white)](https://github.com/manthan-sagar/olist-ecommerce-analysis/blob/main/olist_deep_dive/olist_deep_dive.ipynb)

> An end-to-end exploration of Brazil's largest online marketplace dataset — turning raw transactions into growth strategy.

---

## Table of Contents

1. [Quick Links](#quick-links)
2. [Toolkit](#toolkit)
3. [What This Project Sets Out to Do](#goals)
4. [Where the Data Comes From](#data)
5. [What the Numbers Say](#findings)
6. [What to Do About It](#recommendations)
7. [Getting It Running Locally](#setup)
8. [License](#license)

---

<a id="quick-links"></a>
## 1. Quick Links

| Resource | Description |
|---|---|
| [📊 Tableau Dashboard](https://public.tableau.com/views/OlistPerformance/Sales?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link) | Interactive performance dashboard |
| [🧪 Kaggle Notebook](https://www.kaggle.com/code/manthan-sagar/deep-sales-analysis-eda-viz-rfm-nlp-geo) | Runs entirely inside Kaggle's environment |
| [📓 Source Notebook](https://github.com/manthan-sagar/olist-ecommerce-analysis/blob/main/olist_deep_dive/olist_deep_dive.ipynb) | Raw `.ipynb` — code only, outputs stripped |

[↑ Top](#table-of-contents)

---

<a id="toolkit"></a>
## 2. Toolkit

**Languages & Libraries**

| Category | Tools |
|---|---|
| Core analysis | Python, Pandas, NumPy |
| Visuals | Plotly, Tableau |
| Stats & ML | StatsModels, SciPy, Scikit-learn, Pingouin |
| Text mining | NLTK, TextBlob |

**Techniques applied**

- **EDA** — summary statistics, gap analysis, outlier flagging
- **Cleaning & feature engineering** — new metrics and derived fields built from raw tables
- **Trend analysis over time** — order/revenue trajectories, seasonal decomposition
- **RFM modeling** — segmenting buyers by Recency, Frequency, and Monetary value
- **Unsupervised clustering** — scikit-learn based behavioral grouping
- **Geo-analytics** — regional sales density and shipping-performance mapping
- **Review mining** — sentiment scoring on customer text feedback
- **Hypothesis testing** — correlation and significance checks throughout

[↑ Top](#table-of-contents)

---

<a id="goals"></a>
## 3. What This Project Sets Out to Do

Olist links independent sellers to buyers across Brazil, giving smaller merchants access to multiple marketplaces at once. This study digs into that ecosystem across five angles:

- **Commercial performance** — where revenue is growing, shrinking, or seasonal
- **Buyer psychology** — how often people come back, and what makes them stay
- **Fulfillment health** — where shipments stall and which carriers underperform
- **Checkout economics** — which payment paths convert best and which carry the most risk
- **Strategic output** — translating all of the above into concrete next steps

[↑ Top](#table-of-contents)

---

<a id="data"></a>
## 4. Where the Data Comes From

Built entirely on the **Brazilian E-Commerce Public Dataset by Olist**, sourced from [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).

[↑ Top](#table-of-contents)

---

<a id="findings"></a>
## 5. What the Numbers Say

### 📈 Momentum
- Order volume and revenue climbed steadily through 2018 before flattening at **~6–7K orders and R$1–1.2M per month**.
- Black Friday (Nov 24, 2017) triggered the single largest spike in orders, revenue, and unique buyers all year.
- **São Paulo alone accounts for 42% of total sales** and kept growing through 2018 while other regions plateaued.

### 🔁 Buyer Habits
- **97% of customers buy exactly once** — repeat purchasing is the exception, not the norm.
- Buyers who use installment plans (roughly half of all customers) spend **2x more per order** on average.
- 58% of buyers ("promoters") leave positive reviews but rarely come back; the 13% who leave critical reviews spend more per order but churn faster, usually over delivery delays.

### 🚚 Fulfillment
- Late deliveries drag average ratings down to 1–2 stars, versus 4–5 for on-time orders.
- Heavier, pricier orders take longer to arrive and are disproportionately late.
- Orders paid in installments move faster, carry higher order values, and retain customers better.

### 💳 Payments & Risk
- Credit cards drive **74% of all transactions** and carry a **35% higher average order value** than other methods.
- Installment-based orders show **2x the average order value** of one-time payments.
- Vouchers are the riskiest payment type — **16% cancellation rate vs. 5% for credit cards**, a 3x gap.

### 📦 Product & Logistics
- Electronics (27%) and furniture (18%) are the two biggest revenue categories.
- Northern-region deliveries take roughly **twice as long** as the national average.
- Carriers hold packages for **70% of total delivery time**, with Rio de Janeiro and Salvador the slowest handoff points.

### ⚠️ Recurring Problems
- Average review scores slid from **4.5 in 2017 to 3.9 in 2018**, tracking closely with rising delivery delays.
- Black Friday 2017 exposed carrier handoff bottlenecks, producing a surge in complaints and late shipments.
- Order cancellations spike every **February and August**, concentrated among high-value voucher-paid purchases.

### ⭐ Reviews at a Glance
- **58% of all reviews are 5-star.** Only 12% land at 1-star, and just 3% at 2-star.
- Roughly 15% of negative review text references "slow delivery" or "missing items" — a major drag on NPS.

### 🔍 Underlying Drivers
- Low scores correlate strongly with **longer delivery windows, higher order value, and heavier packages**.
- Fast carrier handoff (3 days or fewer) combined with installment payment options is the strongest predictor of both higher ratings and repeat business.

[↑ Top](#table-of-contents)

---

<a id="recommendations"></a>
## 6. What to Do About It

### Turn one-time buyers into repeat buyers
- Build a loyalty program aimed squarely at the 97% who never come back — second-purchase discounts or points.
- Run win-back campaigns for the top 1% of spenders, who already generate 15% of total revenue.
- Shrink the ~29-day gap before a typical second purchase using short-window incentives (e.g., a 7-day discount window).

### Sharpen the product & pricing mix
- Double down on "Beauty & Health" and "Home & Garden" — both growing ~18% YoY — via bundles or subscription-style offers.
- Revisit pricing on weak categories like "Watches & Gifts," or bundle in guaranteed faster shipping to offset delivery friction.

### Reward the highest-value customers
- Offer premium installment tiers (free shipping, priority support) to buyers averaging 3+ orders.
- Target voucher users — 3x more likely to cancel — with time-limited bundle deals to lock in the sale.

### Fix delivery friction
- Focus carrier improvement efforts on Rio de Janeiro and Salvador, where delays run ~30% above average.
- Fast-track heavy or high-value shipments (>500 R$ or >10kg) — they generate 2x more 1-star reviews.
- Pre-stock inventory and add temporary carrier capacity ahead of Black Friday to avoid a repeat of 2017's 4x delay spike.

### Double down regionally where it's working
- Use São Paulo (42% of sales, 20% faster delivery, 30% better retention) as a testbed for tactics before rolling out elsewhere.
- Subsidize shipping or add pickup points in weaker states like Maranhão and Ceará.

### Get ahead of bad reviews
- Auto-compensate customers when delivery runs past 15 days (e.g., 10% off the next order).
- Add weekend support staffing to close the gap in slower Sunday response times.

[↑ Top](#table-of-contents)

---

<a id="setup"></a>
## 7. Getting It Running Locally

### You'll need
- Python 3.11 or newer
- Git

### 1. Clone it
```bash
git clone https://github.com/manthan-sagar/olist-ecommerce-analysis.git
cd olist-ecommerce-analysis
```

### 2. Set up your environment

**No Poetry installed? → Path A**
```bash
python -m venv .venv
source .venv/bin/activate
pip install poetry
poetry config virtualenvs.in-project true --local
poetry install
jupyter lab olist_deep_dive/olist_deep_dive.ipynb
```

**Poetry already installed? → Path B**
```bash
poetry config virtualenvs.in-project true --local
poetry install
poetry run jupyter lab olist_deep_dive/olist_deep_dive.ipynb
```

[↑ Top](#table-of-contents)

---

<a id="license"></a>
## 8. License

This analysis is released under the [MIT License](LICENSE).
The underlying dataset remains subject to Olist's original [Kaggle license terms](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).
