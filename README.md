# 💪 FitNexis: AI-Powered Smart Fitness & Diet Planner

[![Live Preview](https://img.shields.io/badge/Live%20Preview-Streamlit-blue?logo=streamlit)](https://fitnexis-tm.streamlit.app/)

A personalized fitness and diet plan generator powered by Google's Gemini AI, built with Streamlit. This application helps users calculate key health metrics (BMI, BMR, TDEE) and generates tailored workout and diet plans, which can be viewed directly in the app or downloaded as a PDF.

---

## ✨ Features

- **Personalized Plan Generation**  
  Generates unique fitness and diet plans based on user input (age, gender, weight, height, fitness goal, activity level, diet type, workout type).

- **Health Metric Calculations**  
  Automatically calculates and displays:
  - **BMI (Body Mass Index):** Assesses weight in proportion to height.  
  - **BMR (Basal Metabolic Rate):** Estimates calories burned at rest.  
  - **TDEE (Total Daily Energy Expenditure):** Calculates total daily calorie needs based on activity.

- **AI-Powered Plans**  
  Leverages Google's **Gemini 1.5 Flash** model for intelligent and adaptive plan creation.

- **Structured Workout Plan Display**  
  Workout plans are presented in a clear, "box-like" markdown format, making them easy to read and follow.

- **PDF Export**  
  Download your complete personalized plan, including metrics and generated content, as a well-formatted PDF document.

- **History Tracking**  
  All generated plans are saved locally, allowing users to revisit and review their past plans.

- **Intuitive Navigation**  
  A clean sidebar provides easy access to the **Home**, **Dashboard**, and **History** sections.

---

## 🚀 Technologies Used

- **Python** – Core programming language  
- **Streamlit** – Interactive UI and deployment  
- **Google Gemini API** – AI-powered plan generation  
- **ReportLab** – PDF generation  
- **JSON** – Plan history storage  
- **Regex (re)** – Markdown parsing and formatting

---

## ⚙️ Setup and Local Development

### Prerequisites

- Python 3.9+ (recommended: 3.10 or 3.11)  
- Git (optional but helpful)

---

### 1. Clone the Repository

```bash
git clone https://github.com/turja1347/fitnexis.git
cd fitnexis
```

Alternatively, download the ZIP and extract manually.

---

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

---

### 3. Activate the Virtual Environment

- **macOS/Linux:**

```bash
source venv/bin/activate
```

- **Windows (Command Prompt):**

```cmd
venv\Scripts\activate.bat
```

- **Windows (PowerShell):**

```powershell
.\venv\Scripts\Activate.ps1
```

---

### 4. Install Dependencies

Create a `requirements.txt` file with:

```txt
streamlit
google-generativeai
reportlab
```

Install with:

```bash
pip install -r requirements.txt
```

---

### 5. Set Up Google Gemini API Key

1. Go to [Google AI Studio](https://aistudio.google.com/)  
2. Create a new API key

#### Option A: `.streamlit/secrets.toml` (Recommended)

Create `.streamlit/secrets.toml` and add:

```toml
GEMINI_API_KEY = "YOUR_ACTUAL_GEMINI_API_KEY"
```

#### Option B: Environment Variable

- **macOS/Linux:**

```bash
export GEMINI_API_KEY="YOUR_ACTUAL_GEMINI_API_KEY"
```

- **Windows CMD:**

```cmd
set GEMINI_API_KEY="YOUR_ACTUAL_GEMINI_API_KEY"
```

- **Windows PowerShell:**

```powershell
$env:GEMINI_API_KEY="YOUR_ACTUAL_GEMINI_API_KEY"
```

---

### 6. Create `instance/` Directory

```bash
mkdir instance
```

This folder stores `history.json` and exported PDFs.

---

### 7. Run the Application

```bash
streamlit run streamlit_app.py
```

Your browser will open the app automatically.

---

## ☁️ Deployment (Streamlit Cloud)

1. Push the project to GitHub (`turja1347/fitnexis`)
2. Visit [FitNexis]( https://fitnexis-tm.streamlit.app/)
3. Connect your GitHub repo
4. Set main file path to `streamlit_app.py`
5. Add a **Secret**:
   - Key: `GEMINI_API_KEY`
   - Value: Your API key
6. Click **Deploy**

---

## 💡 Usage

### 🏠 Home Page

- Input your personal details
- Choose goal, activity level, diet type, and workout preference
- Click **Generate Plan 💪**

### 📊 Dashboard

- View BMI, BMR, TDEE with explanations
- Review your AI-generated workout and diet plans
- Click **📥 Download Plan as PDF**

### 🕒 History

- View all past plans in the **History** section
- Expand to review any previously generated result

---

## 📂 Project Structure

```
.
├── instance/
│   └── history.json         # Generated on use
├── app.py                   # Main app logic
└── requirements.txt         # Dependencies
```

---

## 🤝 Contributing

1. Fork this repo  
2. Create a new branch:

```bash
git checkout -b feature/YourFeature
```

3. Make changes and commit:

```bash
git commit -m "Add YourFeature"
```

4. Push and open a pull request:

```bash
git push origin feature/YourFeature
```


## ✉️ Contact

Feel free to reach out:

- LinkedIn: [Turja Mondal](https://www.linkedin.com/in/turjamondal01/)
