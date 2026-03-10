\# 🤖 AI Automated Bug Reporter



An AI-powered bug reporting agent that automatically creates Jira tickets from plain English descriptions. Built with n8n, Google Gemini, and Jira API.



---



\## 🎯 What It Does



Instead of manually filling Jira forms, a QA engineer simply types a casual bug description like:



> \*"Login page shows an error when I enter correct credentials on Chrome"\*



And the AI agent automatically creates a fully formatted Jira ticket with:

\- ✅ Summary

\- ✅ Steps to Reproduce

\- ✅ Expected Result

\- ✅ Actual Result

\- ✅ Environment Details



\*\*No manual Jira work. No formatting. Just describe the bug and it's done.\*\*



---



\## 🛠️ Tech Stack



| Tool | Purpose | Cost |

|------|---------|------|

| \[n8n](https://n8n.io) | Workflow automation canvas | Free (self-hosted) |

| \[Google Gemini](https://aistudio.google.com) | AI brain — understands bug descriptions | Free |

| \[Jira Software](https://atlassian.com/jira) | Bug tracking \& project management | Free (up to 10 users) |



\*\*Total cost: $0\*\* 🎉



---



\## 🏗️ Workflow Architecture



```

Chat Input → AI Agent (Gemini) → Jira API

&nbsp;                ↕          ↕

&nbsp;          Simple Memory   Jira Tool

```



1\. \*\*When chat message received\*\* — triggers when a bug is described

2\. \*\*AI Agent\*\* — powered by Google Gemini, reads the message and extracts bug details

3\. \*\*Simple Memory\*\* — remembers conversation context

4\. \*\*Create Issue in Jira\*\* — automatically creates a formatted Jira ticket



---



\## 📸 Demo



\### Input (what you type):

```

The checkout button on the mobile app is not clickable 

when there are items in the cart. Tested on iPhone 14, 

iOS 16, Safari browser.

```



\### Output (Jira ticket created automatically):

```

Summary: Checkout button not clickable on mobile when cart has items



Description:

Steps to Reproduce:

1\. Open the mobile app on iPhone 14

2\. Add items to the cart

3\. Navigate to checkout

4\. Tap the checkout button



Expected Result: User should be navigated to the checkout page

Actual Result: Checkout button is unresponsive/not clickable

Environment: iPhone 14, iOS 16, Safari browser

```



---



\## 🚀 How to Run This Project



\### Prerequisites

\- Windows/Mac/Linux

\- Node.js installed (\[nodejs.org](https://nodejs.org))

\- Google account (for Gemini API)

\- Atlassian account (for Jira)



\### Step 1 — Install n8n

```bash

npm install -g n8n

npx n8n start

```

Open browser at: `http://localhost:5678`



\### Step 2 — Get Free Gemini API Key

1\. Go to \[aistudio.google.com](https://aistudio.google.com)

2\. Click \*\*"Get API Key"\*\* → \*\*"Create API key"\*\*

3\. Copy the key



\### Step 3 — Set Up Jira

1\. Create free account at \[atlassian.com](https://atlassian.com)

2\. Create a new \*\*Scrum\*\* project

3\. Go to `id.atlassian.com/manage-profile/security/api-tokens`

4\. Create an API token and copy it



\### Step 4 — Import the Workflow

1\. Download `workflow.json` from this repo

2\. In n8n → click \*\*"Import"\*\*

3\. Upload the JSON file

4\. Add your credentials:

&nbsp;  - Gemini API key

&nbsp;  - Jira email + API token + domain



\### Step 5 — Test It!

Click \*\*"Open Chat"\*\* in n8n and type any bug description!



---



\## 🧪 Test Scenarios Used



| Bug Type | Description |

|----------|-------------|

| Authentication | Login page shows error with valid credentials on Chrome |

| Mobile | Checkout button not clickable on iPhone 14, Safari |

| UI | Profile picture shows broken image on Firefox and Edge |

| Performance | Reports page takes 30+ seconds to load with 100+ records |

| Security | Password visible in plain text after show/hide toggle |



---



\## 💡 Key Learnings



\- How AI agents work with tools and memory

\- Jira REST API integration

\- Workflow automation with n8n

\- Prompt engineering for structured output

\- Real-world QA bug reporting practices



---



\## 🔮 Future Improvements



\- \[ ] Add screenshot attachment support

\- \[ ] Duplicate bug detection before creating ticket

\- \[ ] Slack notification when bug is created

\- \[ ] Auto-assign bugs based on component

\- \[ ] Weekly bug summary report



---



\## 👩‍💻 Author



\*\*Dipashree Balamurugan\*\*  

Aspiring QA Engineer  

\[GitHub](https://github.com/deepashreeee) • \[LinkedIn](#)



---



\## 📄 License



MIT License — feel free to use this project!

