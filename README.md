# My_First_Project
It's about my work on ai automation

# Automated Lead Enrichment 

An AI-powered automation built with Zapier that captures new leads, enriches them with company data from Apollo, scores them by priority, and automatically notifies the sales team and follows up with the client. It replaces manual lead research with a fully automated workflow.

##  Workflow Overview
![Zap workflow](<img width="1834" height="810" alt="Project #3 Lead Enrichment" src="https://github.com/user-attachments/assets/420104f8-2e7b-4504-bab8-ff2114ee8671" />
/zap-workflow.png)

##  Features
- **Instant lead capture**: new leads are received through a webhook.
- **Automatic data cleanup**: extracts the company URL/domain from the lead's information.
- **Lead enrichment**: pulls company and contact details using the Apollo API.
- **Smart prioritization**: splits leads into **High Priority** and **Low Priority** paths based on set conditions.
- **Lead tracking**: saves high-priority leads to Google Sheets.
- **Team alerts**: notifies the sales team on Slack (high priority) or Gmail (low priority).
- **AI-written emails**: AI by Zapier drafts a personalized email for the client.
- **Automated follow-up**: sends the email to the client through Gmail.

##  How It Works

| Step | App | Action |
|------|-----|--------|
| 1 | Webhooks by Zapier | Lead comes in |
| 2 | Formatter by Zapier | Get company URL |
| 3 | Webhooks by Zapier | Lead enrichment using Apollo |
| 4 | Paths | Split into High / Low priority |

**High Priority path**
| Step | App | Action |
|------|-----|--------|
| 5 | Paths | Check path conditions |
| 6 | Google Sheets | Save high-priority leads |
| 7 | Slack | Send a notification to the sales team |
| 8 | AI by Zapier | Create email draft for the client |
| 9 | Gmail | Send email to the client |

**Low Priority path**
| Step | App | Action |
|------|-----|--------|
| 10 | Paths | Check path conditions |
| 11 | Gmail | Send notification to the sales team |

##  Tools Used
![Zapier](https://img.shields.io/badge/Zapier-FF4F00?style=for-the-badge&logo=zapier&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google_Sheets-34A853?style=for-the-badge&logo=googlesheets&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white)
![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)

Also: Apollo (lead enrichment API), Webhooks by Zapier, Formatter, Paths, AI by Zapier.

##  How to Run / Set It Up
1. Create a free account at [zapier.com](https://zapier.com).
2. Create a new Zap and add the steps in the table above in the same order.
3. **Step 1:** choose *Webhooks by Zapier* > *Catch Hook* and copy the webhook URL.
4. **Step 3:** connect your own Apollo account and API key.
5. **Step 4:** set the rules for High vs Low priority (for example, company size or job title).
6. Connect your own Google Sheets, Slack, and Gmail accounts.
7. Click **Test run** to check each step, then **Publish**.
8. Send a test lead to your webhook URL:
```json
   {
     "name": "Jane Doe",
     "email": "jane@example.com",
     "company": "Example Inc",
     "website": "https://example.com"
   }
```

##  Use Cases
- Sales teams that want to qualify leads faster
- Agencies handling inbound inquiries
- Small businesses with no CRM automation yet

##  What I Learned
- Building multi-step automations with webhooks and API calls
- Using Paths for conditional logic
- Using AI to generate personalized emails
- Connecting several apps into one workflow

##  Future Improvements
- Add a CRM integration (HubSpot or Salesforce)
- Add error handling and retry steps
- Add lead scoring based on more data points

##  Contact
[![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/angelo.daniel.913706/about/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/feed/)
