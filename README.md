# CORD-19 Research Paper Explorer

## Project Overview

This project is an interactive web application built with the **Streamlit** framework to analyze and visualize the CORD-19 research dataset. It allows users to explore research papers related to COVID-19 by filtering data based on a range of publication years.

This assignment demonstrates fundamental data science skills, including data loading, cleaning, analysis, and building an interactive dashboard.

## Learning Objectives

- Practice loading, exploring, and cleaning a real-world dataset with **pandas**.
- Create meaningful and clear visualizations using **Matplotlib** and **Seaborn**.
- Build and deploy a simple, interactive web application using **Streamlit**.
- Effectively present data insights in a user-friendly format.

## How to Run the Application

Follow these steps to get the application running on your local machine.

### 1. Clone the Repository

```bash
git clone https://github.com/wondow/Frameworks_Assignment.git
cd Frameworks_Assignment
```

### 2. Install Dependencies

Ensure you have Python 3.7+ installed. Then, install the required packages using pip:

```bash
pip install pandas matplotlib seaborn streamlit wordcloud
```

### 3. Download the Dataset

Download the `metadata.csv` file from the [Kaggle CORD-19 Research Challenge page](https://www.kaggle.com/datasets/allen-institute-for-ai/CORD-19-research-challenge). Place the downloaded file in the root directory of this project.

### 4. Run the Streamlit App

Open your terminal in the project's root directory and run the following command:

```bash
streamlit run app.py
```

Your web browser should automatically open with the running application.

## Findings and Observations

- **Publication Trend**: The analysis clearly shows a massive spike in research publications in the year **2020**, which directly corresponds to the onset of the global COVID-19 pandemic.
- **Top Journals**: A small number of journals were responsible for a large portion of the publications, indicating key hubs for scientific communication during the crisis.
- **Key Research Themes**: The word cloud generated from paper titles highlights the central themes of the research, with terms like `patient`, `COVID`, `SARS`, `CoV`, and `Impact` being prominent.

## Challenges and Learning Reflections

- **Handling Large Data**: The full `metadata.csv` file is quite large. This made initial loading and processing slow with resource restrictions. Implementing Streamlit's `@st.cache_data` decorator was a crucial step to ensure the application remains performant by loading and cleaning the data only once.
- **Data Cleaning**: The `publish_time` column contained inconsistent date formats and some invalid entries. Using `pd.to_datetime` with the `errors='coerce'` parameter was essential for robustly handling these issues.
- **Building an Interactive UI**: Creating a responsive user interface with Streamlit was surprisingly straightforward. The main challenge was ensuring that all visualizations correctly updated in response to the user's input from the sidebar filters. This assignment was a great introduction to the power of frameworks for turning a data script into a shareable tool.
README.md
Displaying README.md.
