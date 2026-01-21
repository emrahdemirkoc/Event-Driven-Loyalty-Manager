# 🛍️ Event-Driven AI Loyalty Manager

> **Turn standard Shopify orders into VIP experiences instantly. An event-driven automation system powered by n8n & OpenAI.**

![Workflow Screenshot](screenshot.png)

## 🚨 The Problem
In e-commerce, post-purchase communication is often generic and "soulless."
* Brands fail to instantly recognize **High-Value Customers (Whales)** the moment a sale happens.
* Sending a standard "Order Received" email to a VIP customer is a missed opportunity.
* Customer loyalty is lost due to a lack of immediate, personalized acknowledgement.

## ✅ The Solution
This system creates a **"Digital Store Manager"** that works in milliseconds.
Using an **Event-Driven Architecture**, it listens to Shopify webhooks. When an order arrives, it instantly analyzes the total amount. If the customer spends above a certain threshold (e.g., 1000 TL), **AI (GPT-4o)** drafts a hyper-personalized, warm, and VIP-style email with a custom discount code for the next purchase.

## 🛠 Tech Stack & Architecture

| Technology | Role |
|------------|------|
| **Event-Driven Architecture** | Replaces polling with instant Webhook triggers. |
| **Shopify Webhook API** | Streams live order data (`orders/create`) to n8n. |
| **n8n** | Data cleaning, logic routing, and API orchestration. |
| **OpenAI (GPT-4o-mini)** | Context-aware text generation based on cart value & customer name. |
| **Gmail / SMTP** | Delivery of the personalized VIP email. |

## ⚙️ Workflow Logic (How It Works)

1.  **Shopify Trigger:** The moment a customer clicks "Buy", Shopify pushes the order JSON payload to the system via Webhook.
2.  **Data Filtering:** Raw JSON is parsed to extract key metrics: Customer Name, Email, and Total Price.
3.  **AI Intelligence:** The system evaluates the order value based on a prompt rule: *"If spend > X, treat as VIP; else, send standard thanks."*
4.  **Instant Action:** AI generates a unique email body in seconds.
5.  **Delivery:** The email lands in the customer's inbox immediately, boosting LTV (Lifetime Value).

## 🚀 How to Use

1.  Import the `workflow.json` file into n8n.
2.  Configure your **Shopify Webhook** (Settings -> Notifications -> Webhooks -> Create generic webhook).
3.  Add your **OpenAI API Key**.
4.  Connect your **Gmail/SMTP** credentials.
5.  Set your "VIP Threshold" amount in the IF node.

---

### 👤 Author
**Emrah Digital** - *Automation & AI Solutions*
[Visit my Website](https://emrahdemirkoc.com)
