# 🛍️ NOIRE – E-commerce Automation with n8n

An end-to-end automation system for a fashion store (**NOIRE**) built with
**n8n**, **Google Sheets**, **Telegram**, **Gmail**, and **Google Gemini AI**.

🔗 [LinkedIn Post](https://www.linkedin.com/posts/shimaa-el-zaidey_automation-n8n-workflowautomation-ugcPost-7487904886701895681-FKVt/) ·
🎥 [Demo Video](YOUR_DEMO_LINK) ·
🤖 [Telegram Bot](https://t.me/Orders_Managementtt_bot) ·
📊 [Google Sheet](https://docs.google.com/spreadsheets/d/1syFuYK5-ch-ol7RnVvqX1eVyWsnhZYn6olsqz-5Fb5c/edit?usp=sharing)

---

## ✨ Features
| Module | What it does |
|---|---|
| 🤖 **AI Chatbot** | Answers customers about products, prices, stock, and their orders (Arabic & English) |
| 📦 **Orders Management** | Receives orders from the website, saves them to Google Sheets, and notifies via Telegram |
| 🗃️ **Inventory Management** | Automatically deducts stock after each order |
| ⏰ **Daily Low Stock Alert** | Every day at 12 AM, emails the inventory manager the low-stock items |

## 🧰 Tech Stack
n8n · Google Gemini · Google Sheets · Telegram Bot API · Gmail · Webhooks · JavaScript

---

## 1️⃣ AI Chatbot
Webhook → AI Agent (Gemini + Simple Memory) → reads Orders & Inventory sheets → Respond to Webhook

![Workflow](ChatBot/Workflow%20of%20ChatBot.png)

<p>
  <img src="ChatBot/chat1.png" width="24%">
  <img src="ChatBot/chat2.png" width="24%">
  <img src="ChatBot/chat3.png" width="24%">
  <img src="ChatBot/chat4.png" width="24%">
</p>

## 2️⃣ Orders Management
Website checkout → Webhook → Save order in Google Sheets → Telegram notification

![Workflow](Order/Workflow.png)

**Website UI**
<p>
  <img src="Order/UI%201.png" width="24%">
  <img src="Order/UI%202.png" width="24%">
  <img src="Order/UI%203.png" width="24%">
  <img src="Order/UI%204.png" width="24%">
</p>

**Cart & Checkout**

![Cart](Order/CART.png)
![Checkout](Order/Check%20out.png)

**Saving the order**

![Commit](Order/Commit%20order.png)
![Save](Order/Save-%20order%20in%20sheet.png)
![Append](Order/Append%20the%20new%20orders.png)

**Telegram notification**

![Bot 1](Order/bot%20message%201.png)
![Bot 2](Order/bot%20message%202.png)

## 3️⃣ Inventory Management
Receive Order → Separate items → Get Current Stock → Calculate New Stock → Update Inventory

![Workflow](Inventory/Workflow.png)
![Get stock](Inventory/Get%20current%20stock.png)
![Calculate](Inventory/calculate%20new%20stock.png)
![Update](Inventory/update%20%20inventory.png)

| Before | After |
|---|---|
| ![Before](Inventory/Inventory%20sheet%20befor%20update.png) | ![After](Inventory/Inventory%20sheet%20after%20update.png) |

## 4️⃣ Daily Low Stock Alert
Schedule (12 AM) → Read Inventory → Filter low stock → Summarize → Email the manager

![Workflow](Daily%20Alert/Workflow.png)
![Sheet](Daily%20Alert/sheet.png)
![Filter](Daily%20Alert/Filter.png)
![Email](Daily%20Alert/email.png)

---

## 🚀 How to Run
1. Import `Final Project.json` into your n8n instance.
2. Connect your credentials (Google Sheets, Gemini, Telegram, Gmail).
3. Create a Google Sheet with two tabs: **Inventory** and **Orders**.
4. Update the Webhook URLs in the website code.
5. Activate the workflow.

## 👩‍💻 Author
**Shimaa El-Zaidey** – [LinkedIn](https://www.linkedin.com/in/shimaa-el-zaidey/)
