# **Recipe Genie: Using Machine Learning to Find Recipes Based on Ingredients You Already Have**

**Recipe Genie** is a web application designed to help users discover recipes based on the ingredients they already have on hand. Just enter your ingredients, and Recipe Genie will provide a list of delicious recipes to try!

---

## **Table of Contents**

1. [Introduction](#introduction)
2. [Project Objective](#project-objective)
3. [Datasets](#datasets)
4. [Features](#features)
5. [Technologies Used](#technologies-used)
6. [Project Details](#project-details)
   - [Data Collection](#data-collection)
   - [Data Preprocessing](#data-preprocessing)
   - [Text Vectorisation & Similarity Calculation](#text-vectorisation--similarity-calculation)
7. [Building the Web Application](#building-the-web-application)
8. [Summary of Results](#summary-of-results)
9. [Usage](#usage)
10. [Acknowledgements](#acknowledgements)

---

## **Introduction**

People often stick to a limited set of recipes in their weekly routines, sometimes due to the risk of trying new dishes that may not suit their tastes, potentially leading to wasted ingredients. Recipe Genie aims to make meal planning easier and less repetitive by helping users discover new recipes based on the ingredients they already have.

---

## **Project Objective**

The objective of Recipe Genie is to diversify users' meal options by recommending dishes that align with their available ingredients and preferences. This helps users expand their weekly menus without extra shopping or complex preparation.

---

## **Datasets**

- **Recipe Data**: Sourced from [Pinch of Yum](https://pinchofyum.com/) using Beautiful Soup for web scraping.
- **Ingredient Data**: Preprocessed to optimize recommendation quality.
- **Vectorization and Similarity Analysis**: Ingredient data is vectorized using a TF-IDF model, enabling effective matching with user inputs.

---

## **Features**

- **Ingredient-Based Recommendations**: Input your ingredients, and Recipe Genie will suggest recipes that use what you already have.
- **Flexible Search**: Supports a wide range of ingredients for almost any pantry combination.
- **Detailed Recipe Information**: Provides titles, descriptions, prep time, ingredients, and instructions for each recipe.
- **Interactive User Interface**: Designed for ease of use, allowing seamless recipe exploration and discovery.

---

## **Technologies Used**

- **Python**: Backend development
- **Flask**: Web framework for backend server
- **Pandas**: Data manipulation and analysis
- **scikit-learn**: Text vectorization and similarity calculations
- **HTML/CSS**: Frontend design and styling
- **JavaScript**: Client-side scripting for dynamic interactions
- **Render**: Application deployment platform

---

## **Project Details**

### **Data Collection**

Recipe data was sourced from [Pinch of Yum](https://pinchofyum.com/) using Beautiful Soup:

1. **Identify the Data**: Key recipe attributes, such as title, ingredients, and instructions, were identified.
2. **Scraping Process**: Scripts were created to crawl the website, parse HTML content, and extract the required information.
3. **Save the Data**: Extracted data was stored in CSV format for processing.

---

### **Data Preprocessing**

Collected data required cleaning and preprocessing steps:

- **Tokenization**: Ingredient text was split into individual words.
- **Stopwords Removal**: Common English words that don’t add meaning were removed.
- **Stemming**: Words were reduced to their root form.
- **Unwanted Words and Measurements Removal**: Unnecessary words and measurements were excluded.
- **Regex Cleaning**: Non-alphabetic characters and extraneous information were removed.

---

### **Text Vectorisation & Similarity Calculation**

For recommending recipes:

1. **TF-IDF Vectorization**: Ingredient lists were converted into numerical vectors, with unique ingredients given more weight.
2. **Cosine Similarity**: Calculated the similarity between user-provided ingredients and recipes, ranking recommendations based on similarity.

---

## **Building the Web Application**

- **Backend Setup**: A Flask application handles user requests, calculates similarity scores, and returns the top 5 recipe recommendations.
- **Frontend Design**: HTML and CSS were used for the UI, with JavaScript enabling dynamic interactions, such as modal displays for recipe details.

---

## **Summary of Results**

Recipe Genie generates personalized recipe recommendations using cosine similarity, helping users make the most of their available ingredients, saving both time and effort.

---

## **Usage**

1. Clone the repository: git clone <repository-url>
2. pip3 install -r requirements.txt
3. python3 api/app.py

