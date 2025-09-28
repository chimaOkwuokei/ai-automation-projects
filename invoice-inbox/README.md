# 📄 Invoice Inbox Automation

## Overview
Companies receive dozens of invoices weekly, which were previously processed manually by an admin. This automation monitors a Gmail inbox, extracts invoice data (from email body or PDFs), uses AI to parse key details, and logs the results into Google Sheets.

✅ Eliminates manual data entry  
✅ Improves accuracy  
✅ Provides real-time visibility  

---

## 🏷️ Metadata
- **Category:** Operations / Finance  
- **Size Classification:** Medium (5 tasks)  
- **Deployment Time:** 2–4 hours (basic) / 1–2 days (with AI setup)  
- **Version:** v1.0  

---

## 📊 Detailed Description
Currently, invoices are handled manually by an admin assistant, which takes hours per week and introduces errors.  
The automation solves this by:  

1. Monitoring the Gmail inbox for invoice-related emails.  
2. Extracting text from email bodies or PDF attachments.  
3. Using an LLM to parse vendor name, invoice number, dates, and amount.  
4. Logging details into Google Sheets.  
5. (Optional) Sending a Slack notification when a new invoice is logged.  

This saves ~12 hours/month and ~$200–300 in labor costs.

---

## ⚙️ How It Works
![Workflow Overview](./images/workflow.png)

1. **Trigger:** Gmail inbox monitors new emails with keywords: *invoice*, *billing*, *statement*.  
2. **Attachment Handling:** Extracts text from PDFs or email body.  
3. **AI Parsing:** LLM identifies structured invoice details.  
4. **Data Logging:** Appends details into a Google Sheet.  
5. **Notification:** Slack/Email confirmation (optional).  

---

## 🛠️ Tools Required
- Gmail API  
- n8n / Zapier / Make  
- Google Sheets API  
- LLM (e.g., OpenAI / Claude / Document AI)  
- PDF Parser tool  

---

## 🔑 Setup Requirements
- Gmail API credentials  
- Google Sheet prepared with columns: Vendor | Invoice # | Date | Due Date | Amount | Sender | File URL  
- AI API key (e.g., OpenAI)  
- Automation workspace (Zapier/Make/n8n)  

---

## 📈 Value Proposition
- **Time Saved:** ~12 hours/month  
- **Cost Saved:** ~$190 net savings (after subscriptions)  
- **Accuracy:** Reduced errors in financial reporting  

---

## 🎥 Demo Video
📌 [Insert Loom/Zoom walkthrough link here]  

---

## ⚠️ Known Limitations
- Best with standardized invoices  
- AI parsing may misread unusual formats  
- Gmail API has rate limits  
- Paid AI API may be required for high volume  

---

## 📢 Testimonials / Use Cases 
- Can be adapted for receipts, purchase orders, or expense tracking.  

---

## 🔄 Version & Updates
- **v1.0** – Gmail → AI → Google Sheets pipeline  
- **v1.1** – Added Slack notifications  
- **v1.2 (planned)** – Error-handling for malformed PDFs and duplicates  

---
