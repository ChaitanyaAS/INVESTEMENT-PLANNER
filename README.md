# Investment Planner using Google Gemini & Streamlit

This is an **AI-powered Investment Planner** built using **Google Gemini (Generative AI API)** and **Streamlit** for the UI. It helps users build a customized investment plan based on their financial goals, risk tolerance, income, and investment horizon.

## Features
- **Personalized Investment Plans**: Generate customized investment plans based on user input.
- **Secure API Key Input**: Supports .streamlit/secrets.toml or manual entry for secure Google API key integration.
- **Google Gemini for Financial Advice**: Uses the Gemini (gemini-pro or gemini-1.5-pro) model to generate detailed financial advice.
- **Stylish Dark UI**: Clean, responsive, and modern UI for an optimal user experience.
- **Investment Allocation & Considerations**: Provides investment allocation suggestions, important considerations, and disclaimers.
- **Error Handling**: Safe error handling for API, JSON parsing, and model selection issues.

## Technologies Used
- **Streamlit**: For building the frontend interface.
- **Google Generative AI API**: For generating personalized investment advice.
- **Python 3.8+**: Backend programming language.
- **HTML/CSS**: For custom styling inside Streamlit.

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/investment-planner.git
cd investment-planner
```

### 2. Create a Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # For Windows: `venv\Scripts\activate`
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Add Your Google API Key
You have two options for adding your Google API key:

#### Option A: Add to `secrets.toml` (Recommended)
- Create a file `.streamlit/secrets.toml` with the following content:
  ```toml
  GOOGLE_API_KEY = "your_google_api_key"
  ```

#### Option B: Enter It Manually
- You can also enter the API key manually when prompted in the app.

## Running the App

To run the app, use the following command:
```bash
streamlit run investment_planner.py
```

Then open your browser and visit:
```
http://localhost:8501
```

## How It Works
1. **User Input**: Enter your financial details such as goal, income, debt, risk appetite, etc.
2. **API Interaction**: The app formats the input into a structured prompt.
3. **Investment Plan Generation**: The **Gemini API** generates a JSON-formatted investment plan.
4. **Display Results**: The app parses the generated JSON and displays it in a user-friendly manner using Streamlit components.

### Example Output
The app will generate a structured output like this:
```json
{
  "Understanding Your Situation": "...",
  "Investment Options & Potential Allocation": "...",
  "Important Considerations": "...",
  "Disclaimer": "I'm an AI chatbot, not a financial advisor..."
}
```

## Disclaimer
This tool is intended for **educational purposes only**. It does not replace professional financial advice. Always consult a certified financial planner for real investment decisions.
