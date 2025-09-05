## Phishing-Mail-Analyzer Overview
The **Phishing Mail Analyzer Agent** is a simple AI-powered tool built with [Relevance AI](https://relevanceai.com) that helps users detect phishing emails. It analyzes the content of an email, identifies suspicious indicators, estimates the likelihood of phishing, and provides actionable security advice. This project is ideal for cybersecurity awareness, small-scale SOC testing, or as a learning project for building AI agents in cybersecurity.
---
## Features
Detects common phishing indicators such as:
- Suspicious sender addresses
- Urgency or threatening language
- Fake/mismatched links
- Unexpected attachments
- Spelling or grammar mistakes
- Requests for sensitive information
- Provides a **Phishing Probability Score** (0% = safe, 100% = phishing)
- Offers **clear security advice** to users
- Fully **English-language** support
- Built with Relevance AI’s **Knowledge Base** and **Prompt Agent**
---
## Knowledge Base
The agent uses a **SANS Institute phishing red flags document** as its knowledge base. This ensures that phishing detection is aligned with cybersecurity best practices.
---
## Example Input 1 

From: it-support@yourbank-secure.com
Subject: Password Reset Required
Click the link to reset your password immediately: http://bank-secure-update.com

## Example Output 1 

1. Suspicious Indicators:
- Sender domain: "yourbank-secure.com" is not a standard bank domain and could be spoofed.
- Urgency: The email demands immediate action ("reset your password immediately").
- Link mismatch: The link ("http://bank-secure-update.com") does not match the sender's domain and is not a typical bank URL.
- Generic message: No personal greeting or details.
- Unsolicited password reset: You did not request a password reset.
- 
2. Phishing Probability Score: 95% (Very likely to be phishing)

3. Security Advice:
- Do not click the link or enter any information.
- Do not reply to the email.
- Contact your bank directly using their official website or phone number to verify any account issues.
- Report the email to your IT/security team or your bank’s fraud department.

## Example Input 2

From: notifications@amazon.com
Subject: Order Shipped
Your recent order #12345 has been shipped. Track it here: https://www.amazon.com/trackorder

## Example Output 2

1. Suspicious Indicators:

- The sender address (notifications@amazon.com) appears legitimate, but this can be easily spoofed.
- The message is very generic—no personal greeting or order details.
- The link appears to be a valid Amazon URL, but without hovering or inspecting, it’s impossible to confirm if it’s genuine or masked.
- No spelling or grammar issues, but the email is very brief and lacks typical Amazon formatting or branding.
- No attachments, which is good, but the main action is to click a link.

2. Phishing Probability Score:
30% (Low to moderate risk, but caution is still advised due to the generic nature and potential for link spoofing.)

3. Security Advice:
- Do not click the link directly from the email.
- Instead, log in to your Amazon account by typing www.amazon.com into your browser to check your order status.
- Always verify order numbers and details in your official Amazon account.
- If you receive unexpected shipping notifications, be extra cautious.
- Report suspicious emails to Amazon (stop-spoofing@amazon.com).
- If you have any doubts, contact Amazon support directly through their official website.
---

## License
This project is for educational and cybersecurity awareness purposes. The knowledge base uses publicly available material from the SANS Institute.
---

## Future Improvements
- Can be added automated email ingestion via webhooks
- Can be integrated with link extraction and domain verification tools
- Expand the knowledge base with real-world phishing samples
- Add multi-language support
---
