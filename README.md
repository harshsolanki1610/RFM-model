# RFM Customer Segmentation

A customer segmentation project built using the RFM (Recency, Frequency, Monetary) model on a real-world online retail dataset. Done as part of my AI/ML coursework to understand how businesses classify customers using transaction data.

---

## What is RFM?

RFM scores each customer on three things:
- **Recency** – how recently they bought
- **Frequency** – how often they buy
- **Monetary** – how much they spend

Each gets a score from 1–4, which are combined into a final RFM score used to place customers into segments.

---

## Dataset

[Online Retail Dataset](https://www.kaggle.com/datasets/ulrikthygepedersen/online-retail-dataset) from Kaggle — real transactional data from a UK-based store. Downloaded automatically via `kagglehub`.

---

## Setup

```bash
pip install pandas plotly kagglehub
python rfm_model.py
```

Also available on [Google Colab](https://colab.research.google.com/drive/18WZl3D22uvaHEZeQWURBzbyTYAuNKbRR).

---

## Approach

1. Dropped rows with missing `CustomerID`
2. Created `TotalAmount = Quantity x UnitPrice`
3. Calculated Recency, Frequency, and Monetary per customer
4. Scored each metric using quantiles (Recency scored inversely — recent = better)
5. Assigned segment labels based on the combined RFM score

---

## Segments

| Segment | RFM Score |
|----------------|-----------|
| VIP/Loyal | 9 – 12 |
| Potential Loyal | 6 – 8 |
| At Risk | 5 |
| Can't Lose | 4 |
| Lost | 3 |

---

## Visualizations

Built with Plotly — bar charts, treemap, box plots, correlation heatmap, and grouped bar chart comparing average R, F, M scores across segments.

---

## Tech Stack

Python, Pandas, Plotly, KaggleHub
