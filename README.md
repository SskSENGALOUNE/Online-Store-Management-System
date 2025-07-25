# 🛍️ Online Store Management System

A complete **Online Store Management System** built using **AppSheet**, **Google Sheets**, **Telegram**, and **Google Apps Script**. Designed to help manage finances, stock, COD status, and monthly reporting — all accessible on mobile.

---

## 🖼️ App Screenshot

![App Screenshot](images/store-app-demo.png)

> _Place your screenshot in the `/images` folder and name it `store-app-demo.png`._

---

## ✅ Key Features

- 💰 **Money Management**
  - Track income, expenses, and net profit
  - View daily/weekly/monthly summaries
  - Integrated with Google Sheets for real-time updates

- 📦 **Stock Management**
  - View real-time stock quantity
  - Add or update stock with barcode or name
  - Notify when stock is low (optional)

- 📮 **COD Status**
  - Track Cash on Delivery (COD) status by customer
  - View pending / delivered / canceled orders

- 📊 **Monthly Report**
  - Auto-generated reports for sales, profit, stock, and more
  - Visualized with charts and summaries

- 📢 **Telegram Notification**
  - Send order alerts or stock updates to Telegram groups
  - Apps Script integration with Telegram Bot API

- 🖼️ **Image Support**
  - Upload product images or receipts
  - Display images directly inside the app

- 👥 **Multi-user Roles**
  - Admin: Full access (money, stock, reports)
  - Staff: Add/update stock and orders
  - Viewer: Read-only reports

---

## 📁 App Pages Overview

| Page Name            | Description                                              |
|----------------------|----------------------------------------------------------|
| **Dashboard**         | Summary of income, orders, and notifications            |
| **Money Tracker**     | View & manage cash flow (income/expenses)               |
| **Stock**             | Product inventory with quantity and image               |
| **Orders (COD)**      | Order list with customer name, amount, and COD status   |
| **Monthly Report**    | Charts + summary by month (sales, expenses, balance)    |
| **Telegram Settings** | Link to Telegram Bot for notifications                  |
| **Product Images**    | Upload and view product or receipt images               |
| **User Access**       | Manage user roles and permissions                       |

---

## 🚀 Getting Started

### 1. Copy the Google Sheets Template

- [Click here to copy the sheet](https://docs.google.com/spreadsheets/your-template-link)

### 2. Open AppSheet and Create Your App

1. Go to [AppSheet](https://www.appsheet.com)
2. Click “Start from your own data”
3. Select the Google Sheet you copied
4. Customize app views and permissions

### 3. Setup Telegram Integration (Optional)

1. Create a Telegram bot via [@BotFather](https://t.me/BotFather)
2. Copy the Bot Token
3. Create a Google Apps Script project
4. Use the script below to send messages:

```javascript
function sendTelegram(text) {
  var token = 'YOUR_BOT_TOKEN';
  var chat_id = 'YOUR_CHAT_ID';
  var url = 'https://api.telegram.org/bot' + token + '/sendMessage?chat_id=' + chat_id + '&text=' + encodeURIComponent(text);
  UrlFetchApp.fetch(url);
}
