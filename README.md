# Solid Meme

Final project for the Building AI course

## Summary
Solid Meme is an AI-powered decision support tool that acts as an intelligent calculator for project risk assessment and success prediction. Users input key project parameters, and the model predicts the likelihood of success while providing risk factors and mitigation recommendations. Built using Python, scikit-learn, and Streamlit, it helps teams make more informed decisions. (214 characters)

## Background
Many projects fail due to poor risk assessment and unrealistic planning. Traditional methods are often too manual or overly simplistic.

This project solves:
* Lack of accessible, data-driven project risk evaluation tools
* Difficulty in quantifying multiple risk factors simultaneously
* Limited guidance on how to improve project outcomes

My personal motivation is to apply AI to practical business problems where better decisions can save time, money, and effort. This topic is important because successful project delivery directly impacts organizations and individual careers.

## How is it used?
1. Open the web application
2. Fill in project details (budget, timeline, team size, scope complexity, stakeholder support, etc.)
3. Click “Calculate” to get an instant success probability score (0–100%)
4. Review detailed risk breakdown and personalized mitigation suggestions
5. Save or export the report for team meetings

The tool is especially useful during project planning, proposal evaluation, and quarterly reviews. It is designed for project managers, consultants, startup founders, and students working on group projects. The interface is kept simple and intuitive for non-technical users.

```python
def predict_project_success(features):
    model = joblib.load('solid_meme_model.pkl')
    probability = model.predict_proba([features])[0][1]
    return round(probability * 100, 1)
