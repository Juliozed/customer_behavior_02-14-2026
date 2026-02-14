# customer_behavior_02-14-2026
customer analysis for loyalty programs (Python, SQL, Power Bi)
# Customer Shopping Behavior Analysis

## 📊 Project Overview

This project analyzes customer shopping behavior using transactional data to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior. The analysis combines Python for data processing, SQL for business analysis, and Power BI for visualization to deliver actionable business recommendations.

---

## 📁 Dataset

- **Source:** Customer transaction data
- **Size:** 3,900 rows × 18 columns
- **Key Features:**
  - Customer demographics (Age, Gender, Location, Subscription Status)
  - Purchase details (Item, Category, Amount, Season, Size, Color)
  - Shopping behavior (Discounts, Previous Purchases, Review Ratings, Shipping Type)

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Python** | Data cleaning, EDA, feature engineering |
| **Pandas** | Data manipulation and analysis |
| **PostgreSQL** | Database management and SQL queries |
| **Power BI** | Interactive dashboard creation |
| **Gamma** | Professional presentation design |
| **Jupyter Notebook** | Code development and documentation |

---

## 📋 Project Steps

### 1️⃣ Data Loading & Exploration (Python)
- Imported dataset using Pandas
- Performed initial exploration with `.info()` and `.describe()`
- Identified data types and missing values

### 2️⃣ Data Cleaning & Preparation
- Handled missing values in Review Rating column (median imputation)
- Standardized column names to snake_case
- Removed redundant columns (promo_code_used)

### 3️⃣ Feature Engineering
- Created `age_group` column by binning ages
- Generated `purchase_frequency_days` from purchase history
- Validated data consistency across features

### 4️⃣ Database Integration
- Connected Python to PostgreSQL database
- Loaded cleaned DataFrame into SQL database
- Enabled SQL-based analysis

### 5️⃣ SQL Analysis
Performed structured queries to answer business questions:
- Revenue comparison by gender
- High-spending discount users identification
- Top-rated products analysis
- Shipping type preferences
- Subscriber vs. non-subscriber behavior
- Customer segmentation (New, Returning, Loyal)
- Product performance by category
- Age group revenue contribution

### 6️⃣ Dashboard Development (Power BI)
- Built interactive visualizations
- Created KPI cards for key metrics
- Designed category-wise revenue and sales charts
- Implemented filters for dynamic exploration

### 7️⃣ Reporting & Presentation
- Compiled analysis results into a comprehensive report
- Created professional presentation using Gamma
- Developed business recommendations

---

## 📊 Dashboard

The Power BI dashboard includes:

- **KPIs:** Total customers, average purchase amount, average review rating
- **Visualizations:**
  - Revenue by category
  - Sales by age group
  - Subscription status distribution
  - Shipping type preferences
- **Interactive Filters:** Gender, Category, Subscription Status, Shipping Type

![Dashboard Preview](dashboard_screenshot.png) *(Add your screenshot here)*

---

## 💡 Key Results

### Findings:
- **Gender Revenue:** Male customers generated 2.1x more revenue than female customers
- **Subscription Impact:** Only 27% of customers are subscribers despite similar spending patterns
- **Discount Dependency:** Products like hats (50%) and sneakers (49.7%) are highly discount-driven
- **Customer Loyalty:** 80% of customers are classified as "Loyal" based on purchase history
- **High-Value Segments:** Young adults contribute the most revenue across age groups

### Business Recommendations:
1. **Boost Subscriptions:** Promote exclusive benefits to increase subscriber base
2. **Loyalty Programs:** Reward repeat buyers to enhance retention
3. **Review Discount Strategy:** Balance promotions with margin protection
4. **Targeted Marketing:** Focus on high-revenue segments and express shipping users
5. **Product Positioning:** Highlight top-rated products in marketing campaigns

---

## 🚀 How to Run This Project

### Prerequisites
```bash
- Python 3.8+
- PostgreSQL/MySQL/SQL Server
- Power BI Desktop
- Jupyter Notebook
```

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/customer-shopping-analysis.git
cd customer-shopping-analysis
```

### Step 2: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 3: Run Data Cleaning & EDA
```bash
jupyter notebook notebooks/data_cleaning.ipynb
```

### Step 4: Set Up Database
```sql
-- Create database
CREATE DATABASE shopping_analysis;

-- Run the Python script to load data
python scripts/load_to_database.py
```

### Step 5: Execute SQL Queries
```bash
-- Navigate to SQL folder and run queries
psql -U username -d shopping_analysis -f queries/analysis_queries.sql
```

### Step 6: Open Power BI Dashboard
- Open `dashboard/shopping_dashboard.pbix` in Power BI Desktop
- Refresh data connections
- Explore interactive visualizations

---

## 📂 Project Structure

```
customer-shopping-analysis/
│
├── data/
│   ├── raw/                    # Original dataset
│   └── cleaned/                # Processed data
│
├── notebooks/
│   ├── data_cleaning.ipynb     # Data preparation
│   └── eda.ipynb               # Exploratory analysis
│
├── scripts/
│   ├── load_to_database.py     # Database loading script
│   └── feature_engineering.py  # Feature creation
│
├── queries/
│   └── analysis_queries.sql    # SQL business queries
│
├── dashboard/
│   └── shopping_dashboard.pbix # Power BI dashboard
│
├── reports/
│   ├── analysis_report.pdf     # Detailed findings
│   └── presentation.pdf        # Gamma presentation
│
├── README.md
└── requirements.txt
```

---

## 👤 Author

**Your Name**
- LinkedIn: [your-linkedin-profile](https://linkedin.com/in/yourprofile)
- GitHub: [@yourusername](https://github.com/yourusername)
- Email: your.email@example.com

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Dataset source: [Mention source if applicable]
- Special thanks to [any contributors or resources]

---

**⭐ If you found this project helpful, please consider giving it a star!**
