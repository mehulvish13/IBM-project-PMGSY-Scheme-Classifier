# 🚧 PMGSY Scheme Classifier – IBM SkillsBuild Project

A robust machine learning solution developed with IBM Watson Studio and AutoAI to classify rural infrastructure projects under the Pradhan Mantri Gram Sadak Yojana (PMGSY) schemes.  
The project automates the prediction of project scheme types (e.g., PMGSY-I, PMGSY-II, RCPLWEA) based on key infrastructure attributes, supporting data-driven rural development and efficient resource allocation.

---

## 📊 Dataset Overview

The model leverages the official AI-KOSH dataset containing comprehensive rural infrastructure project data across India.  
- 📥 Dataset source: [AI-Kosh PMGSY Dataset](https://aikosh.indiaai.gov.in/web/datasets/details/pradhan_mantri_gram_sadak_yojna_pmgsy.html)  
- 🔑 Key features include:  
  - Number and length of road works sanctioned and completed  
  - Number of bridges sanctioned and constructed  
  - Project expenditure and pending works  
- 🎯 Target variable: The PMGSY scheme type under which each project falls  
- 🧹 Data cleaning: Missing values handled, column names standardized

---

## 🔧 Tools and Technologies

- 🧠 **IBM Watson Studio & AutoAI** – automated ML pipeline generation  
- ☁️ **IBM Watsonx Runtime (Cloud Lite)** – model deployment and testing  
- 🐍 **Python** – data preprocessing (optional)  
- 🐙 **GitHub** – for sharing and collaboration

---

## 🧠 Machine Learning Pipeline

- **ML Task:** Multi-class classification  
- **Pipeline:** AutoAI generates and ranks models (e.g., XGBoost, Random Forest, Logistic Regression)  
- **Selection:** Best model selected based on F1-score and accuracy  
- **Deployment:** Online endpoint created using IBM Watsonx for real-time predictions

---

## 🧪 Sample Prediction Input

Use this JSON format in the deployed API test interface:

```json
{
  "input_data": [{
    "fields": [
      "STATE_NAME",
      "DISTRICT_NAME",
      "NO_OF_ROAD_WORK_SANCTIONED",
      "LENGTH_OF_ROAD_WORK_SANCTIONED",
      "NO_OF_BRIDGES_SANCTIONED",
      "COST_OF_WORKS_SANCTIONED",
      "NO_OF_ROAD_WORKS_COMPLETED",
      "LENGTH_OF_ROAD_WORK_COMPLETED",
      "NO_OF_BRIDGES_COMPLETED",
      "EXPENDITURE_OCCURED",
      "NO_OF_ROAD_WORKS_BALANCE",
      "LENGTH_OF_ROAD_WORK_BALANCE",
      "NO_OF_BRIDGES_BALANCE"
    ],
    "values": [
      ["Odisha", "Cuttack", 5, 11.2, 1, 1800000, 4, 10.4, 1, 1700000, 1, 0.8, 0]
    ]
  }]
}
```

---

## 🚀 Project Deliverables

* ✅ Cleaned dataset in CSV format
* ✅ AutoAI-generated model with leaderboard insights
* ✅ Deployed online model via Watsonx API
* ✅ Sample input JSON and testing documentation
* ✅ Screenshots of training, deployment, and predictions

---

## 🔍 Project Structure

```
PMGSY-Project/
│
├── dataset/               # Cleaned PMGSY dataset CSV file(s)
├── notebooks/             # Data exploration and preprocessing notebooks
├── model/                 # Saved model assets and metadata
├── images/                # Screenshots (model training, predictions, error fixes)
├── input_sample.json      # Example JSON payload for model testing
├── requirements.txt       # Python dependencies for data prep
└── README.md              # This detailed project documentation
```

---

## 📌 How to Use

1. **Clone this repository** to your local system
2. Explore the dataset and notebooks in the `notebooks/` folder
3. (Optional) Use IBM Watson Studio to recreate AutoAI experiments
4. Use the `input_sample.json` file to test deployed model on IBM Cloud
5. Adapt this project for related government schemes or rural project classification

---

## 🗂 Tags

`machine-learning` `ibm-watson` `skillsbuild` `autoai` `classification` `ai-kosh` `infrastructure` `rural-development`

---

## 📞 Contact

For questions, improvements, or collaborations, feel free to:
📬 Open an issue on GitHub
📧 Email: [mehulvinodv@gmail.com](mailto:mehulvinodv@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/mehul-vishwakarma/)

---

Made with 💡 during IBM SkillsBuild Challenge – Empowering India's Rural Intelligence through AI 🇮🇳