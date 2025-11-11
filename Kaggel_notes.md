👉🏻Kaggle Setup & API Key Guide
Quick reference for setting up Google Gemini API access in Kaggle notebooks.

Adding API Key as Kaggle Secret
Step-by-Step
Get your API key from Google AI Studio
Open your Kaggle notebook
Click Settings (gear icon in the right sidebar)
Navigate to Secrets section
Click Add a new secret
Set:
Label: GOOGLE_API_KEY
Value: Your API key from AI Studio
Toggle ON to enable the secret for your notebook
Click Add
Using the API Key in Code
Standard Setup
import os
import google.generativeai as genai

# Configure the API
genai.configure(api_key=os.environ["GOOGLE_API_KEY"])

# Verify it works
print("API configured successfully")
Quick Model Test
# List available models
for model in genai.list_models():
    if 'generateContent' in model.supported_generation_methods:
        print(f"- {model.name}")
Basic Usage Example
# Initialize the model
model = genai.GenerativeModel('gemini-1.5-flash')

# Generate content
response = model.generate_content("Explain AI agents in one sentence.")
print(response.text)
Model Selection Tips
Recommended Models
gemini-1.5-flash (Recommended for course)

Fast and cost-effective
Great for learning and experimentation
Often free for light usage
gemini-1.5-pro

More powerful but costs more
Use for complex tasks requiring higher quality
Cost Awareness
Flash model: ~$0 for typical course usage (free tier)
Pro model: ~$0.0025/1K input tokens, ~$0.01/1K output tokens
Check tools/estimate_cost.py for more details
Monitor actual usage in Google Cloud Console
Security Best Practices
Never hardcode API keys in notebook cells
Always use Kaggle Secrets for sensitive credentials
Never print or log your API key
Don't commit notebooks with exposed keys to GitHub
Review notebook outputs before sharing publicly
Troubleshooting
Error: "GOOGLE_API_KEY not found"
Solution: Make sure the secret is toggled ON in notebook settings.

Error: "API key invalid"
Solutions:

Verify the key is correct in AI Studio
Check for extra spaces when copying
Regenerate the key if needed
Rate Limiting
If you hit rate limits:

Wait a few seconds between requests
Use gemini-1.5-flash instead of Pro
Batch requests when possible
Additional Resources
Gemini API Documentation
Kaggle Secrets Documentation
Google AI Studio
