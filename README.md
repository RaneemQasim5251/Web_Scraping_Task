# Books Scraper & Analysis

A simple, end-to-end Python project that:

1. **Scrapes** book data from [Books to Scrape](https://books.toscrape.com).
2. **Cleans** and structures the data into a tabular format.
3. **Visualizes** key patterns (price distribution, availability..etc).

---

## Project Files

* **`Raneem_Web_Scraping.ipynb`**

  * Colab notebook that:

    * Loops through pages 1–50 of the catalogue.
    * Visits each book's detail page.
    * Extracts **Title**, **Description**, **Price**, **UPC**, and **Availability**.
    * Cleans fields (removes `£`, strips `(XX available)`, trims whitespace).
    * Saves the cleaned data to **`Raneem_Web_Books_Scraped.csv`**.
    * Demonstrates visualizations:

      * Book Price Distribution
      * ![تنزيل](https://github.com/user-attachments/assets/cde9f553-8b58-4821-98eb-886b8d67a592)

      * Violin Distribution
        ![تنزيل (1)](https://github.com/user-attachments/assets/084b32e6-dab4-4928-8741-dd5c91886b17)

      * KDE Price distribution
        ![تنزيل (2)](https://github.com/user-attachments/assets/0afa96ee-67fd-4e5c-93a8-592d7f9b8a9b)

      * Word clouds
     ![تنزيل (3)](https://github.com/user-attachments/assets/3887c390-0ff4-4058-9621-a544be9d6958)

      * TF-IDF top-term charts for descriptions
![تنزيل (4)](https://github.com/user-attachments/assets/3d872c5c-9790-4f11-bcb3-8c3ea3dab155)

* **`Raneem_Web_Books_Scraped.csv`**

  * The final CSV containing all scraped records with columns:

    1. `Title`
    2. `Description`
    3. `Price` (numeric, no currency symbol)
    4. `UPC`
    5. `Availability` (cleaned text)

* **`README.md`**

  * This document.

---

## Setup & Dependencies

1. **Create a virtual environment** (optional but recommended):

   ```bash
   python3 -m venv venv
   source venv/bin/activate   # on macOS/Linux
   venv\Scripts\activate    # on Windows
   ```

2. **Install required packages**:

   ```bash
   pip install requests beautifulsoup4 pandas matplotlib seaborn scikit-learn wordcloud
   ```

3. **Run the notebook**:

   ```bash
   jupyter notebook "Raneem_Web_Scraping.ipynb"
   ```

   * Execute cells in order to scrape, clean, save, and visualize the data.

---

## What You’ll Learn

* **Web scraping patterns**: pagination, detail-page extraction, error-handling with `try`/`except`.
* **Data cleaning**: stripping currency symbols, parsing availability text, trimming whitespace.
* **Basic EDA & visualization** with Matplotlib/Seaborn and WordCloud.
* **Notebook-driven workflow**: embed code, data, and charts in one place for easy sharing.

---

## Contributing & Customization

* Feel free to extend the notebook:

  * Add **Plotly** for interactivity.
  * Build a **Streamlit** dashboard.
  * Scrape additional fields (e.g., number of reviews, tax, star ratings raw).
* Open an issue or PR if you find bugs or edge cases.

---

*Happy scraping & analyzing!*
