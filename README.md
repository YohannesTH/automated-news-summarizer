# ml-news-summarizer(n8n + Google Gemini)
An automated workflow built with n8n that monitors multiple RSS feeds for Machine Learning and AI news, uses the Google Gemini Chat Model to generate concise summaries, and stores the structured results for quick review.

✨ Features
Fully Automated: Runs on a scheduled trigger (e.g., daily or hourly).

Targeted Content: Monitors specific RSS feeds related to ML, AI, and Data Science.

AI-Powered Summarization: Utilizes the Google Gemini API via the n8n Basic LLM Chain node to create high-quality, actionable summaries.

Data Cleaning: Automatically fetches full article content and converts HTML to clean Markdown before sending to the LLM.

Conditional Logic: Filters articles based on predefined criteria (e.g., keyword, date).

Structured Output: Delivers clean, structured data (Title, Summary, Link) to a final system (e.g., Google Sheets, Notion, or a database).

🛠️ Prerequisites
To run this workflow, you will need:

n8n Instance: A self-hosted or cloud-based n8n instance (version 1.0.0 or higher).

Google Gemini API Key: Access to the Google AI Studio / Gemini API.

Target Destination Credentials: Credentials for your chosen output system (e.g., Google Sheets, a database, or Slack webhook).

RSS Feed URLs: A list of relevant ML/AI news RSS feeds.

🚀 Setup & Installation
1. Import the Workflow
- Download the ml-news-summarizer.json file from the workflows directory in this repository.
- In your n8n instance, go to Workflows and click Import from JSON.
- Paste the contents or upload the file.

2. Configure Credentials
Gemini AI:
- Find the Basic LLM Chain node.
- Create a new Gemini (or similar) credential using your API Key.

Output System:
- Find the final Create a record node (e.g., Google Sheets, Notion, Database).
- Add the required credentials for that service and configure the sheet/database ID.

3. Customize Inputs
- RSS Feeds: Update the RSS Feeds node with your desired ML news sources.
- Filtering: Review the If node to adjust any keyword or date-based filtering logic.
- Summarization Prompt: Modify the prompt in the Basic LLM Chain node to adjust the summary style (e.g., "Provide a 3-bullet point summary focused on technical applications.").

4. Activate
Toggle the workflow Active and test it manually before relying on the Schedule Trigger.
