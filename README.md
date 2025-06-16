# ⚽ FIFA 21 Data Science & Machine Learning Project

This project goes far beyond basic data cleaning — it showcases full-stack problem-solving, automation, and machine learning on a real-world football dataset. I independently built a custom data enrichment API, automated the cleaning pipeline, and delivered predictive insights using regression models — all in Python.

## 🔍 Trying To Find a Solution

I worked with a real-life FIFA 21 player dataset (`Fifa21_dirty.csv`) that was filled with missing, inconsistent, and corrupted data. Rather than dropping incomplete records, I:

- 🔎 Explored public APIs (e.g., SoFIFA, Futbin, TransferMarket) for data enrichment
- 🔐 Found them restricted or rate-limited
- 💡 Built and deployed my own REST API from scratch using Flask, hosted on Vercel, to automatically fill in the gaps
- 🧠 After 4.5 hours of automated enrichment, achieved 0% missing values

## 🌐 Custom-Built FIFA 21 API

When scraping failed and no free APIs were available, I built and deployed my own:

- 🛠️ **Built with**: Flask (Python), Vercel (Deployment)
- 📦 **Input**: Player ID
- 📤 **Output**: Structured player data in JSON format
- 🔄 **Used to**: Automatically enrich the dataset with missing attributes like nationality, club, age, and more

**Sample Endpoint:**  
[https://fifa21api.vercel.app/player/20801](https://fifa21api.vercel.app/player/20801) → Cristiano Ronaldo

## 🧹 Data Cleaning & Preprocessing

The dataset went through a full transformation pipeline:

- ✅ **Deduplication**: Removed duplicate entries using Player IDs
- 🔁 **Data Type Fixes**: Converted numeric columns and reformatted dates
- 📏 **Unit Standardization**: Feet/inches → centimeters, pounds → kilograms
- 💰 **Monetary Parsing**: Converted "€5M", "€500K" strings to floats
- 🧩 **Column Splitting**: Separated mixed fields like “Team & Contract”
- 🧠 **Feature Engineering**: Created flags for loans, cleaned skill ratings
- 🌍 **Encoding Fixes**: Ensured UTF-8 for special characters in names
- 🔄 **API Integration**: Automated enrichment of missing values

## 📊 Visual Analysis

After cleaning, I explored the data using Matplotlib, Seaborn, and Plotly. Key insights included:

- England Has The Most Talented Players with High Potential (>85)

 ![image](https://github.com/user-attachments/assets/1d0e36d2-a2ed-407f-b317-179c00c10e85)


- Best Potential PLayers in each Position

![image](https://github.com/user-attachments/assets/8ae80078-20a1-45c8-9b08-151e67f0ccbb)


- 📈 Prefered foot per Position
  
  ![image](https://github.com/user-attachments/assets/33466822-8879-47d6-9cf1-fb876403180b)

- who has higher shot power (left or right footed players)?

  ![image](https://github.com/user-attachments/assets/fcaf4ca5-1b7b-495a-86ea-d5e135cbb27e)


- most wages paid

  ![image](https://github.com/user-attachments/assets/eb99f7bb-b405-415d-92bb-d55d94c6edce)


- 💸 higher salary means higher rating?

  ![image](https://github.com/user-attachments/assets/169acd2d-fc96-4535-96fb-c2c97dd12c05)


- Players Market Values for each Country (top 100 player)

  ![image](https://github.com/user-attachments/assets/b89e6626-3bf6-4618-83cc-79876da87686)

- 🧠 Hieghts Across Positions

   ![image](https://github.com/user-attachments/assets/ca3fb2cb-3203-42c6-92bb-552d981ccfd8)

- Top 10 Comparison

  ![image](https://github.com/user-attachments/assets/c5fc8bdd-170a-4ced-9f4a-b3e4d4e64dbc)



- 🦶 Foot Preference distribution (pie chart)

## 🤖 Machine Learning: OVA Rating Prediction 

- 🎯 **Target**: OVA "Overall Rating"
- 🔢 **Features Used**: Age, wage, total stats, etc
- 📈 **Model**: Linear Regression (Scikit-learn)
- ✅ **Performance**:
  - R² Score: 0.85
  - Trained on the fully enriched and cleaned dataset
    
    ![image](https://github.com/user-attachments/assets/1dc47a49-9821-4256-9885-e989d09f8dbb)


## 🧰 Tools & Tech Stack

- **Languages & Frameworks**: Python, Flask
- **Data Handling**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn, Plotly
- **Modeling**: Scikit-learn
- **Deployment**: Vercel
- **Environment**: Jupyter Notebook, VS Code


## 📌 Summary

This project is a showcase of resourcefulness, technical breadth, and data storytelling — applied to one of the world’s most loved sports. From raw, messy CSVs to clean, interactive insights and predictive models, this end-to-end workflow demonstrates production-ready skills in data science, software development, and analytics.
