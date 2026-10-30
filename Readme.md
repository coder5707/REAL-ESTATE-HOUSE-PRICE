# Real Estate Market Analysis & Investment Evaluator

Welcome to the **Real Estate Market Analysis** repository! This project is a comprehensive toolkit and data-driven framework designed to evaluate residential and commercial real estate properties, analyze market trends, and calculate key investment metrics.

## 🚀 Project Overview

Navigating the real estate market requires deep insights into historical pricing, neighborhood trends, cash flow potential, and risk factors. This repository provides scripts, notebooks, and configuration files to help investors, analysts, and data scientists perform rigorous quantitative assessments of properties.

### Key Features
* **Market Trend Analysis:** Track historical price-per-square-foot trends, inventory levels, and days-on-market across different zip codes.
* **Investment Calculator:** Compute critical real estate metrics including Net Operating Income (NOI), Capitalization Rate (Cap Rate), Cash-on-Cash Return, and Internal Rate of Return (IRR).
* **Comparative Market Analysis (CMA):** Automate the selection of comparable properties using spatial distance and feature matching.
* **Interactive Visualizations:** Generate clear, publication-ready charts illustrating appreciation forecasts and mortgage amortization schedules.

---

## 📂 Repository Structure

```text
├── data/
│   ├── raw/                 # Unprocessed MLS data and public datasets
│   └── processed/           # Cleaned datasets ready for modeling
├── notebooks/
│   ├── 01_data_cleaning.ipynb      # Initial data preprocessing and EDA
│   ├── 02_market_trends.ipynb      # Macro and micro market trend analysis
│   └── 03_investment_model.ipynb   # Financial modeling and valuation
├── src/
│   ├── __init__.py
│   ├── metrics.py           # Financial and valuation formulas (Cap Rate, NOI, etc.)
│   ├── spatial.py           # Geospatial utilities for finding comps
│   └── visualization.py     # Plotting functions for reports
├── requirements.txt         # Python dependencies
└── README.md                # Project documentation
```

---

## ⚙️ Getting Started

### Prerequisites
Ensure you have Python 3.8 or higher installed on your system.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/real-estate-analysis.git
   cd real-estate-analysis
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## 📊 Core Financial Metrics Used

The analysis relies on standard institutional real estate formulas:

* **Net Operating Income (NOI):**
  $$\text{NOI} = \text{Gross Operating Income} - \text{Operating Expenses}$$

* **Capitalization Rate:**
  $$\text{Cap Rate} = \frac{\text{NOI}}{\text{Current Market Value (Purchase Price)}}$$

* **Cash-on-Cash Return:**
  $$\text{Cash-on-Cash Return} = \frac{\text{Annual Pre-Tax Cash Flow}}{\text{Total Cash Invested}}$$

---

## 🛠️ Usage Example

You can run the core investment calculator programmatically via the `metrics.py` module:

```python
from src.metrics import calculate_noi, calculate_cap_rate

# Example property financials
gross_income = 120000  # Annual
operating_expenses = 35000  # Annual
purchase_price = 850000

noi = calculate_noi(gross_income, operating_expenses)
cap_rate = calculate_cap_rate(noi, purchase_price)

print(f"Net Operating Income: ${noi:,.2f}")
print(f"Capitalization Rate: {cap_rate * 100:.2f}%")
```

---

## 🤝 Contributing

Contributions are welcome! If you have suggestions for improving the valuation models or adding new data sources, please fork the repository and submit a pull request.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
