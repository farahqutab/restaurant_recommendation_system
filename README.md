# 🍽️ Restaurant Recommendation System

An AI-powered restaurant recommendation system built with Machine Learning, offering personalized restaurant suggestions for Makkah and Madinah.

## 🚀 Features
✅ **Machine Learning Recommendations** - Uses Content-Based Filtering  
✅ **Sentiment Analysis** - Extracts insights from restaurant reviews  
✅ **Travel Time Estimation** - Estimates travel time based on location  
✅ **Web-based Interface** - Simple, user-friendly interface for quick recommendations  

---

## 📂 Project Structure

```
Restaurant-Recommendation-System/
│── ML_Restaurant_Recommendation.ipynb    # Jupyter Notebook (Google Colab)
│── restaurant_recommendation_dynamic.html # Frontend Web Interface
│── README.md                               # Project Documentation
│── .gitignore                              # Ignore unnecessary files
```

---

## 🛠️ Setup & Installation (Google Colab)

### **1️⃣ Open the Google Colab Notebook**
1. **Go to Colab** and open `ML_Restaurant_Recommendation.ipynb`  
2. Make sure the runtime is set to **Python 3 (with GPU/CPU support as needed)**  

### **2️⃣ Install Required Packages**
Inside the Colab notebook, the following command installs all required libraries:
```python
!pip install pandas numpy geopy nltk vaderSentiment scikit-learn scipy flask flask-cors pyngrok
```

### **3️⃣ Install & Authenticate ngrok**
Since the Flask API runs inside **Google Colab**, we need `ngrok` for public access:
```python
!curl -sSL https://ngrok-agent.s3.amazonaws.com/ngrok.asc \
	| sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null \
	&& echo "deb https://ngrok-agent.s3.amazonaws.com buster main" \
	| sudo tee /etc/apt/sources.list.d/ngrok.list \
	&& sudo apt update \
	&& sudo apt install ngrok
```

Now, add your **ngrok authentication token**:
```python
!ngrok config add-authtoken YOUR_AUTH_TOKEN
```
(Replace `YOUR_AUTH_TOKEN` with your actual token from [ngrok](https://dashboard.ngrok.com/get-started/setup)).

---

## 🚀 Running the Project in Colab

### **1️⃣ Run All Cells in the Notebook**
Inside `ML_Restaurant_Recommendation.ipynb`, run all the cells.  
One of the cells will **start the Flask API**, and you should see an output like this:
```
Running on http://127.0.0.1:5000/
 * Running on public URL: https://xxxx.ngrok-free.app
```

### **2️⃣ Get the Public ngrok URL**
The notebook will print an **ngrok-generated public URL** (e.g., `https://xxxx.ngrok-free.app`).  

### **3️⃣ Update the Web Interface (`restaurant_recommendation_dynamic.html`)**
Inside `restaurant_recommendation_dynamic.html`, update the **ngrok URL** in this script:
```html
<script>
    let NGROK_URL = "https://xxxx.ngrok-free.app";
</script>
```
(Replace `xxxx.ngrok-free.app` with your actual ngrok link.)

### **4️⃣ Open the Web Interface**
1. Open `restaurant_recommendation_dynamic.html` in your browser.
2. Select **cuisine, rating, distance, etc.**
3. Click **"Get Recommendations"** to receive suggestions.
4. Click the **Google Maps link** to view restaurant locations.

---

## 📦 Dependencies

| Package       | Version |
|--------------|---------|
| Python       | 3.8+    |
| pandas       | Latest  |
| numpy        | Latest  |
| scikit-learn | Latest  |
| nltk         | Latest  |
| geopy        | Latest  |
| Flask        | Latest  |
| Flask-CORS   | Latest  |
| scipy        | Latest  |
| pyngrok      | Latest  |

---

## 🚀 Future Improvements
- ✅ Implement a user query input box with NLP processing to extract relevant information for finding restaurants based on natural language queries.
- ✅ API Integration for real-time restaurant data  
- ✅ Advanced NLP for sentiment analysis  
- ✅ Enhanced UI for better user experience  

---

## 🤝 Contribution
Want to improve this project?  
- Fork the repository  
- Create a new branch:  
  ```bash
  git checkout -b feature-branch
  ```
- Commit changes:  
  ```bash
  git commit -m "Your Changes"
  ```
- Push:  
  ```bash
  git push origin feature-branch
  ```
- Open a **Pull Request**  

---

## 📜 License
This project is licensed under the MIT License.

---

### 🎯 **Developed by [Farah Qutab]**
🔗 GitHub: [Your GitHub Profile](https://github.com/farahqutab)  

