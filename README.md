
#  Real-Time Social Media Monitoring Dashboard — Team Edition

## 📘 Overview
This project implements a **real-time analytics dashboard** that visualizes social media engagement and sentiment trends over time.  
Developed as part of a collaborative research and data visualization initiative, it combines **Streamlit**, **Plotly**, and **Ngrok** to create an interactive web interface that can be launched directly from **Google Colab**.  

The dashboard supports both aggregated metric tracking and basic text-based insights from tweet data, allowing teams to simulate, analyze, and visualize live social media dynamics.

---

## 🚀 Key Features
- 📈 **Interactive Charts:** Real-time trends for tweet volume and average sentiment using Plotly.  
- 🧮 **Rolling Smoothing:** Configurable moving-average window for noise reduction.  
- 🕒 **Dynamic Range Selection:** View data across any time or index range.  
- 🔍 **Keyword & Mention Extraction:** Summarizes top hashtags and user mentions from text data.  
- 🗂️ **Multi-Source Data Loading:** Compatible with Google Drive or local file uploads.  
- 💻 **Colab-Compatible Deployment:** Runs seamlessly in Google Colab through Streamlit + Ngrok tunneling.  

---

## 🧩 Tech Stack
| Technology | Purpose |
|-------------|----------|
| **Python 3** | Core programming language |
| **Pandas** | Data handling and preprocessing |
| **Plotly** | Interactive data visualizations |
| **Streamlit** | Web dashboard framework |
| **Pyngrok** | Remote tunnel for hosting within Colab |

---

## 📂 Project Structure
```

real_time_social_dashboard_team/
├── collaborator_streamlit_app.py     # Streamlit app script
├── aggregates.csv                    # Aggregated social media metrics
├── tweets.csv                        # (Optional) Tweet text dataset
├── README.md                         # Documentation
└── ...                               # Colab notebook cells

````

---

## ⚙️ Setup Instructions (Google Colab)
### 1️⃣ Open a new Colab notebook
Create a new notebook and copy-paste the provided setup cells.

### 2️⃣ Install required dependencies
```bash
!pip install streamlit pyngrok pandas plotly
````

### 3️⃣ Upload or mount datasets

* Upload `aggregates.csv` (and optionally `tweets.csv`)
  **or**
* Mount Google Drive:

  ```python
  from google.colab import drive
  drive.mount('/content/drive')
  ```

### 4️⃣ Add your Ngrok authtoken

Obtain your token from [ngrok.com](https://dashboard.ngrok.com/get-started/your-authtoken):

```python
NGROK_AUTH_TOKEN = "your_token_here"
```

### 5️⃣ Run the dashboard

Execute:

```bash
!streamlit run collaborator_streamlit_app.py --server.port 8501 --server.headless true
```

A public URL will be generated (via Ngrok). Click the link to launch the live dashboard.

---

## 📊 Visual Components

* **Tweet Volume Chart:** Tracks number of tweets per time unit, with optional smoothing.
* **Sentiment Trend Chart:** Displays sentiment progression and stability over time.
* **Top Mentions & Hashtags:** Extracts frequently used tags and user handles.
* **Data Preview Panel:** Allows inspection of recent data slices interactively.

---

## 🧠 Learning Objectives

* Understand deployment of data-driven dashboards from Colab.
* Apply rolling averages for real-time signal stabilization.
* Integrate file I/O between local runtime and Google Drive.
* Automate temporary public hosting via Ngrok.

---

## 🔐 Ethical & Research Considerations

* This dashboard operates on **simulated or anonymized data** for research and educational use.
* When adapting for real-world deployment, ensure compliance with **social media platform policies**, **data privacy**, and **ethical visualization standards**.
* Avoid exposing sensitive or personally identifiable information through live dashboards.

---

## 📈 Future Improvements

* Live API stream integration (e.g., Twitter/X API).
* Sentiment classification using transformer-based NLP models.
* Real-time update loops or WebSocket integration.
* Enhanced authentication for secure remote access.

---


Would you like me to create a **compact version** of this README (for submission portals like Moodle or report appendices) — about one-third the length but still professional?
```
