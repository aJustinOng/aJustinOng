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

**Tools:** `Power BI | Power Query | Power Automate | Excel | Tableau | MySQL | Postman`  

**IDEs:** `Jupyter Notebook | Visual Studio Code | PyCharm | IntelliJ IDEA` 

**Soft Skills:** `Project Management | Technical Writing | Collaborative Communication | Public Speaking`

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

**Skills:** `Data Visualization | DAX | Data ETL | 3rd Party API`

**Tools:** `Power BI | Power Query`

**Overview:**  

Spotify Wrapped is probably the most popular online interests every year, but it is inherently incomplete, as data is often cut to generate the annual summary before the end of the year. In this project, I reconstructed and customized Spotify Wrapped using Spotify’s provided personal data and public Web API, producing a extensive view of the classic report that can span multiple years.

Using Power Query, tens of thousands of streaming records are ingested from raw, local JSON files and transformed into a structured semantic model. After basic cleaning, unique track and artist identifiers are grouped into controlled batches to be queried to the [Spotify Web API](https://developer.spotify.com/). Through the Web API, the model can obtain additional resources like album and artist images and genre information. To prevent exceeding rate limits, the most relavant tracks and artists are targeted and grouped for batch querying, reducing ~25000 single queries to just 33 API calls.

The result is a fully reproducible, end-to-end analytics pipeline that combines raw data, API-based enrichment, and analytical modeling to recreate — and extend — Spotify Wrapped with greater accuracy, completeness, and analytical flexibility.

**Note:** According to official Spotify documentation, API calls in the future will require a premium Spotify account.

<img src="/assets/img/recording_spotify.gif" width="100%"/>

---

### 2. Hobbit Face CNN Classifier

[GitHub Repo](https://github.com/aJustinOng/hobbit-classifier)

**Skills:** `Python | NumPy | Pandas | Matplotlib | OpenCV | PyWavelets | scikit-learn | Keras | HTML | CSS | JavaScript`

**Tools:** `Jupyter Notebook | Visual Studio Code | PyCharm | Flask`

**Overview:**

I was inspired to make this classification project when my friends started making plans to get together to watch the LOTR (Lord of the Rings) trilogy again. Hobbits are a race in the Tolkien franchise, and in the movies they are played by several well-known Hollywood actors such as Elijah Wood and Martin Freeman. I thought, since they are all male caucasian actors and played similar roles in the movies, can I build a model that can classify between them?

So I searched for and downloaded 50 images for each of the chosen five hobbit actors (Elijah Wood, Sean Astin, Billy Boyd, Dominic Monaghan, and Martin Freeman) on Google. For the preprocessing, I used OpenCV's Haar cascade classifiers to detect faces and eyes in those images, filtering out the unideal training images. I then stored the cropped facial regions into a separate folder before using PyWavelets to extract the facial regions from them. The combined images of both the original cropped image and Wavelet transformed image were split into train and test sets, which were finally used to train a SVM (support vector machine) model. I used GridSearchCV to determine the best model and parameters. After exporting the model as a Pickle file, I loaded it in a Flask server that was connected to a HTML/CSS/JavaScript webpage. The webpage allows the user to drop in an image to classify which of the five hobbits the image resembles. It also displays the confidence of the model and can detect multiple faces in a single image.

<img src="/assets/img/project-hobbit-website.gif" width="100%"/>

I was not satisfied with the model's accuracy, so I went back to the model-building process. Since SVM is considered outdated in modern image classification, I replaced it with a CNN (Convolutional Neural Network) approach. It skips the wavelet transforming process, since CNN can work directly with raw image pixels. It achieved an accuracy of 84.1% after 20-30 training epochs, a hefty 20% improvement from the SVM model.

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

<img src="/assets/img/project-kami-website.PNG" width="80%"/>

The recipe's ingredients, instructions, and AI-generated image are displayed to the user. The project utilized OpenAI's GPT-4 and DALLE-3 APIs into a Django Framework that is connected to a local database.

I fully designed the webpage using HTML, CSS, and JavaScript. I also engineered the entire database that handled the many-to-many relationships between users and their available ingredients, preferences, and generated recipes. The database was hosted on a local XAMPP MySQL database. Unfortunately, we took the demo website offline due to its costs.

<img src="/assets/img/project-kami-sql-diagram.PNG" width="100%"/>

Visit my [website](https://ajustinong.github.io) to know more about me!

[profile]: https://github.com/aJustinOng
[profilelight]: https://github.com/aJustinOng#gh-light-mode-only
[profiledark]: https://github.com/aJustinOng#gh-dark-mode-only
