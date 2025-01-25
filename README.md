# Hey there, I'm Justin!

**`Data Engineering/Data Modeling/Data Analysis`**

I am an aspiring data scientist with entry-level professional experience in application development. I mainly work with Python, Java, and SQL in various personal and academic projects. I graduated from Southern Arkansas University with a major in Computer Science and a minor in Mathematics. I enjoy collaborating with people and creating ideas!

### Find me on:

[![website](./assets/img/globe-light.svg)](https://ajustinong.github.io#gh-light-mode-only)
[![website](./assets/img/globe-dark.svg)](https://ajustinong.github.io#gh-dark-mode-only)
&nbsp;&nbsp;
[![website](./assets/img/linkedin-light.svg)](https://linkedin.com/in/a-justin-ong#gh-light-mode-only)
[![website](./assets/img/linkedin-dark.svg)](https://linkedin.com/in/a-justin-ong#gh-dark-mode-only)
&nbsp;&nbsp;
[![website](./assets/img/instagram-light.svg)](https://instagram.com/idrawshizzle#gh-light-mode-only)
[![website](./assets/img/instagram-dark.svg)](https://instagram.com/idrawshizzle#gh-dark-mode-only)

### Core skills:
Python | SQL | Data Modeling | Data Analysis

---

## **Projects**

1. [Hobbit Face Classifier](#1-hobbit-face-classifier) | [GitHub Repo](https://github.com/aJustinOng/hobbit-classifier)
2. [Real Estate Price Prediction](#2-real-estate-price-prediction) | [GitHub Repo](https://github.com/aJustinOng/real-estate-price-prediction)
3. [Sales Insights using PowerBI](#3-sales-insights-using-powerbi) | [GitHub Repo](https://github.com/aJustinOng/sales-insights-powerbi)
4. [AI Recipe Generator](#4-kami-kitchen-assistant-and-meal-innovator---ai-recipe-generator)

---

### 1. Hobbit Face Classifier

[GitHub Repo](https://github.com/aJustinOng/hobbit-classifier)

**Skills:** `Python | NumPy | Pandas | Matplotlib | OpenCV | PyWavelets | scikit-learn | HTML | CSS | JavaScript`

**Tools:** `Jupyter Notebook | VS Code | PyCharm | Flask`

**Overview:**

I was inspired to make this classification project when my friends started making plans to get together to watch the LOTR (Lord of the Rings) trilogy again. Hobbits are a race in the Tolkien franchise, and in the movies they are played by several well-known Hollywood actors such as Elijah Wood and Martin Freeman. I thought, since they are all male caucasian actors and played similar roles in the movies, can I build a model that can classify between them?

So I searched for and downloaded 50 images for each of the chosen five hobbit actors (Elijah Wood, Sean Astin, Billy Boyd, Dominic Monaghan, and Martin Freeman) on Google. For the preprocessing, I used OpenCV's Haar cascade classifiers to detect faces and eyes in those images, filtering out the unideal training images. I then stored the cropped facial regions into a separate folder before using PyWavelets to extract the facial regions from them. The combined images of both the original cropped image and Wavelet transformed image were split into train and test sets, which were finally used to train a SVM (support vector machine) model. I used GridSearchCV to determine the best model and parameters. After exporting the model as a Pickle file, I loaded it in a Flask server that was connected to a HTML/CSS/JavaScript webpage. The webpage allows the user to drop in an image to classify which of the five hobbits the image resembles. It also displays the confidence of the model and can detect multiple faces in a single image.

<img src="/assets/img/project-hobbit-website.png" width="100%"/>

---

### 2. Real Estate Price Prediction

[GitHub Repo](https://github.com/aJustinOng/real-estate-price-prediction)

**Skills:** `Python | NumPy | Pandas | Matplotlib | scikit-learn | HTML | CSS | JavaScript`

**Tools:** `Jupyter Notebook | VS Code | PyCharm | Flask | Postman`

**Overview:**

In this regression project, I used a U.S. real estate dataset (2.2M+ entries) on Kaggle that was extracted from Realtor.com to create a prediction model that estimates the price of a property based on house area (square feet), number of bedrooms and bathrooms, and state.

I started by preprocessing the dataset and used it to build a model with scikit-learn using linear regression. The model was then exported as a Pickle file. Next, I created a Python Flask server to run the model and receive GET and POST requests, which I tested using Postman. Lastly, I made a webpage using HTML, CSS, and JavaScript with a user-friendly UI, where the user can enter their desired inputs to get a predicted price.

The model building section covers a majority of data science concepts like data cleaning, outlier removal, feature engineering, dimensionality reduction, one hot encoding, and K-Fold cross-validation.

<img src="/assets/img/project-real-estate-price-prediction.png" width="100%"/>

---

### 3. Sales Insights using PowerBI

[GitHub Repo](https://github.com/aJustinOng/sales-insights-powerbi)

**Skills:** `SQL | DAX | Data Visualization`

**Tools:** `MySQL Workbench | Microsoft Excel | PowerBI`

**Overview:**  

As a data analysis project, I took a sales dataset and used it to create a dashboard in PowerBI. I first used MySQL Workbench and Excel to clean and ETL a sales dataset. I then used PowerBI to analyze and visualize the revenue and profit across different regions, customers, and markets. I learned to focus on the critical areas (profit rather than revenue, etc.) that a sales manager would be interested in to answer and tackle sales problems.

I used basic DAX to return specific data aggregates that could be used in visualizations. I also learned how to integrate the powerful interactive tools in PowerBI to allow my stakeholders to conveniently isolate data within specific conditions. I also took additional feedback to drastically improve my initial dashboard.

<img src="/assets/img/project-sales-insights.png" width="100%"/>

---

### 4. KAMI (Kitchen Assistant and Meal Innovator) - AI Recipe Generator

**Skills:** `Project Management | Python | SQL | Data Modeling | AI Prompt Modeling | HTML | CSS | JavaScript`

**Tools:** `Django | XAMPP MySQL | GPT-4 | DALLE-3`

**Overview:**  

This senior capstone project was carried out across two semesters (roughly 9 months) with two of my buddies. We met twice a week physically to discuss our individual and collaborative progress with our senior project advisor. Other forms of communication and collaboration was done through Discord, Google Docs, and Google Slides.

The main focus of the project was to make an AI-based recipe generator that functions by feeding it with available ingredients and establishing limits or constraints to the dish. We integrated this into a website that 'invents' new recipes by considering the user's dietary needs and choice of cuisine.

<img src="/assets/img/project-kami-website.PNG" width="80%"/>

The recipe's ingredients, instructions, and AI-generated image are displayed to the user. The project utilized OpenAI's GPT-4 and DALLE-3 APIs into a Django Framework that is connected to a local database.

I fully designed the webpage using HTML, CSS, and JavaScript. I also engineered the entire database that handled the many-to-many relationships between users and their available ingredients, preferences, and generated recipes. The database was hosted on a local XAMPP MySQL database. Unfortunately, we took the demo website offline due to its costs.

<img src="/assets/img/project-kami-sql-diagram.PNG" width="100%"/>

View my [website](https://ajustinong.github.io) to know more about me!

[profile]: https://github.com/aJustinOng
[profilelight]: https://github.com/aJustinOng#gh-light-mode-only
[profiledark]: https://github.com/aJustinOng#gh-dark-mode-only
