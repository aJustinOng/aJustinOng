# **Hey there, I'm Justin! :v::shit:**

### **`Data Analyst`**



Visit my [website](https://ajustinong.github.io) to know more about me!

### Find me on:

[![website](./assets/img/globe-light.svg)](https://ajustinong.github.io#gh-light-mode-only)
[![website](./assets/img/globe-dark.svg)](https://ajustinong.github.io#gh-dark-mode-only)
&nbsp;&nbsp;
[![website](./assets/img/linkedin-light.svg)](https://linkedin.com/in/a-justin-ong#gh-light-mode-only)
[![website](./assets/img/linkedin-dark.svg)](https://linkedin.com/in/a-justin-ong#gh-dark-mode-only)
<!-- &nbsp;&nbsp;
[![website](./assets/img/instagram-light.svg)](https://instagram.com/idrawshizzle#gh-light-mode-only)
[![website](./assets/img/instagram-dark.svg)](https://instagram.com/idrawshizzle#gh-dark-mode-only)
-->

## Summary of Skills

**Programming Languages:** `Python | DAX | Java | SQL | C++ | HTML | CSS | JavaScript | TypeScript`  

**Frameworks:** `Pandas | NumPy | scikit-learn | Keras | Matplotlib | Spring Boot`  

**Tools:** `Power BI | Power Query | Power Automate | Excel | Visio | Tableau | MySQL | Postman`  

**IDEs:** `Jupyter Notebook | Visual Studio Code | PyCharm | IntelliJ IDEA | Code::Blocks`

**Soft Skills:** `Project Management | Technical Writing | Collaboratiion | Transformation & Automation`

---

# **Projects**

### **Table of Contents**

1. [Spotify Wrapped in PowerBI](#1-spotify-wrapped-in-power-bi) | [GitHub Repo](https://github.com/aJustinOng/spotify-wrapped-power-bi)
2. [Hobbit Face Classifier](#2-hobbit-face-cnn-classifier) | [GitHub Repo](https://github.com/aJustinOng/hobbit-classifier)
3. [Real Estate Price Prediction](#3-real-estate-price-prediction) | [GitHub Repo](https://github.com/aJustinOng/real-estate-price-prediction)
4. [AI Recipe Generator](#4-kami-kitchen-assistant-and-meal-innovator---ai-recipe-generator)

<br>

### 1. Spotify Wrapped in Power BI

[GitHub Repo](https://github.com/aJustinOng/spotify-wrapped-power-bi)

**Skills:** `Data ETL | Data Visualization | DAX | 3rd Party Web API`

**Tools:** `Power BI | Power Query`

**Overview:**  

Spotify Wrapped is a popular online phenomenon that pops up every year, but it is inherently incomplete, as data is often cut by mid November to generate the summary before the year ends. In this project, I reconstructed and customized Spotify Wrapped using Spotify’s provided personal data and public Web API, producing a extensive view of the classic report that can span multiple years.

<img src="/assets/img/project-spotify-wrapped-power-bi-dashboard.gif" width="100%"/>

Using Power Query, tens of thousands of streaming records are ingested from raw, local JSON files and transformed into a structured semantic model. After basic cleaning, unique track and artist identifiers are grouped into controlled batches to be queried to the [Spotify Web API](https://developer.spotify.com/). Through the Web API, the model can obtain additional resources like album and artist images and genre information. To prevent exceeding rate limits, the most relavant tracks and artists are targeted and grouped for batch querying, reducing ~25000 single queries to just 33 API calls.

<img src="/assets/img/project-spotify-wrapped-power-bi-power-query.png" width="100%"/>

The result is a fully reproducible, end-to-end analytics pipeline that combines raw data, API-based enrichment, and analytical modeling to recreate — and extend — Spotify Wrapped with greater accuracy, completeness, and analytical flexibility.

**Note:** According to [official Spotify documentation](https://developer.spotify.com/documentation/web-api), API calls in the future will require a premium Spotify account.

---

### 2. Hobbit Face CNN Classifier

> If most of us valued food and cheer and song above hoarded gold it would be a merrier world. — J.R.R. Tolkien

[GitHub Repo](https://github.com/aJustinOng/hobbit-classifier)

**Skills:** `Python | NumPy | Pandas | Matplotlib | OpenCV | PyWavelets | scikit-learn | Keras | HTML | CSS | JavaScript`

**Tools:** `Jupyter Notebook | Visual Studio Code | PyCharm | Flask`

**Overview:**

This project explores whether a machine learning model can distinguish between actors who portrayed Hobbits in The Lord of the Rings. Because the actors share similar visual traits, the task serves as a fine-grained face classification challenge.

I scraped images online of Elijah Wood, Sean Astin, Billy Boyd, Dominic Monaghan, and Martin Freeman that were ingested into a Jupyter Notebook setup. Faces were detected and cropped using OpenCV Haar cascades, and low-quality images were filtered out. The initial model used a traditional pipeline with wavelet feature extraction and an SVM classifier, tuned using GridSearchCV. The trained model was deployed via a Flask backend and a simple web interface that supports image uploads, multiple face detection, and confidence-based predictions.

<img src="/assets/img/project-hobbit-website.gif" width="100%"/>

To improve performance, the SVM was replaced with a Convolutional Neural Network trained directly on raw face images. After 20–30 epochs, the CNN achieved a ~20% improvement in accuracy over the original approach.

The final system demonstrates the effectiveness of CNNs for distinguishing visually similar faces in a real-world classification setting.

---

### 3. Real Estate Price Prediction

[GitHub Repo](https://github.com/aJustinOng/real-estate-price-prediction)

**Skills:** `Python | NumPy | Pandas | Matplotlib | scikit-learn | HTML | CSS | JavaScript`

**Tools:** `Jupyter Notebook | Visual Studio Code | PyCharm | Flask | Postman`

**Overview:**

In this regression project, I used a U.S. real estate dataset (2.2M+ entries) on Kaggle that was extracted from Realtor.com to create a prediction model that estimates the price of a property based on house area (square feet), number of bedrooms and bathrooms, and state.

I started by preprocessing the dataset and used it to build a model with scikit-learn using linear regression. The model was then exported as a Pickle file. Next, I created a Python Flask server to run the model and receive GET and POST requests, which I tested using Postman. Lastly, I made a webpage using HTML, CSS, and JavaScript with a user-friendly UI, where the user can enter their desired inputs to get a predicted price.

<img src="/assets/img/project-real-estate-price-prediction-website.gif" width="100%"/>

The model building section covers a majority of data science concepts like data cleaning, outlier removal, feature engineering, dimensionality reduction, one hot encoding, and K-Fold cross-validation.

---

### 4. KAMI (Kitchen Assistant and Meal Innovator) - AI Recipe Generator

[Project Report](https://ajustinong.github.io/assets/pdfs/KAMIReport.pdf) | [Project Poster](https://ajustinong.github.io/assets/pdfs/KAMIPoster.pdf)

**Skills:** `Project Management | Python | SQL | Data Modeling | AI Prompt Modeling | HTML | CSS | JavaScript`

**Tools:** `Django | XAMPP MySQL | GPT-4 | DALLE-3`

**Overview:**  

This senior capstone project was carried out across two semesters (roughly 9 months) with two of my buddies. We met twice a week physically to discuss our individual and collaborative progress with our senior project advisor. Other forms of communication and collaboration was done through Discord, Google Docs, and Google Slides.

The main focus of the project was to make an AI-based recipe generator that functions by feeding it with available ingredients and establishing limits or constraints to the dish. We integrated this into a website that 'invents' new recipes by considering the user's dietary needs and choice of cuisine.

<img src="/assets/img/project-kami-website.PNG" width="100%"/>

The recipe's ingredients, instructions, and AI-generated image are displayed to the user. The project utilized OpenAI's GPT-4 and DALLE-3 APIs into a Django Framework that is connected to a local database.

I fully designed the webpage using HTML, CSS, and JavaScript. I also engineered the entire database that handled the many-to-many relationships between users and their available ingredients, preferences, and generated recipes. The database was hosted on a local XAMPP MySQL database. Unfortunately, we took the demo website offline due to its costs.

<img src="/assets/img/project-kami-sql-diagram.PNG" width="100%"/>

Visit my [website](https://ajustinong.github.io) to know more about me!

[profile]: https://github.com/aJustinOng
[profilelight]: https://github.com/aJustinOng#gh-light-mode-only
[profiledark]: https://github.com/aJustinOng#gh-dark-mode-only
