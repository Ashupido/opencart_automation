# OpenCart Automation Testing Framework

This project automates a test scenario on the demo e‑commerce site [demo.opencart.com](https://demo.opencart.com/) using **Selenium WebDriver** with **Python**. It demonstrates a complete automation suite following industry best practices like the **Page Object Model (POM)**, explicit waits, logging, and clean code structure.

## 📋 Test Scenario

The automated test covers the following steps:

1. **Navigate** to the OpenCart homepage.
2. **Search** for a product (e.g., "iPhone").
3. **Open** the first product from the search results.
4. **Add** the product to the shopping cart.
5. **Verify** the product is in the cart by checking the mini cart dropdown (cart total is flaky on the demo site).
6. **Proceed** to the checkout page (attempt only; payment is not completed).

## 🛠️ Tech Stack

- **Python 3.10+**
- **Selenium WebDriver** – browser automation
- **pytest** – test framework
- **pytest-html** – HTML test reports
- **undetected-chromedriver** – bypass bot detection on the demo site

## 📁 Project Structure

opencart_automation/
│
├── pages/ # Page Object classes
│ ├── init.py
│ ├── home_page.py
│ ├── search_results_page.py
│ └── product_page.py
│
├── tests/ # Test cases
│ ├── init.py
│ └── test_add_to_cart.py
│
├── utilities/ # Helper classes
│ ├── init.py
│ └── base_page.py # Common methods and waits
│
├── logs/ # (Optional) log files
├── requirements.txt # Project dependencies
├── README.md # This file
└── conftest.py # pytest configuration


## 🚀 Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/your-username/opencart_automation.git
cd opencart_automation


##   Create and activate a virtual environment

python -m venv venv


## Install dependencies

pip install -r requirements.txt



##  the tests

pytest tests/test_add_to_cart.py -v --html=report.html