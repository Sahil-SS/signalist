# Signalist

## Introduction

Signalist is a modern stock market signal and analytics platform designed to help traders monitor real-time market movements, analyze trends, and generate meaningful insights for smarter decision-making. The platform is engineered with scalability, automation, and professional UI/UX standards, making it ideal for retail traders, analysts, financial researchers, and developers working with structured market data.

With Signalist, users gain access to high-performance charting, real-time updates, secure authentication, automated workflows, and visually rich dashboards powered by advanced event-driven architecture.

---

## 🚀 Live Deployment

**https://signalist-two-tan.vercel.app/sign-up**  
_The hosted deployment link will be attached once published._

---

## ✨ Features

- Real-time stock signal visualization & analytics
- **TradingView Advanced Chart & Widget** integration for professional-grade charting
- Secure authentication system powered by **Better Auth**
- Automated background jobs & scheduled tasks using **Inngest**
- Email notifications & alerts using **Nodemailer**
- Modern component architecture using **ShadCN UI**
- Clean and scalable styling using **Tailwind CSS**
- Full-stack support with **Next.js App Router** & API routes
- Structured database persistence with **MongoDB**
- Developer-friendly tooling including:
  - `npx inngest-cli@latest dev` for workflow testing
  - Modular and maintainable TypeScript setup
- Responsive & optimized UI/UX for all devices

---
## 🧰 Technology Stack

| Category | Technologies Used |
|----------|-------------------|
| Framework | **Next.js (App Router)** |
| Language | **TypeScript** |
| Styling | **Tailwind CSS**, **ShadCN UI** |
| Charts & Market Data | **TradingView Widgets** |
| Authentication | **Better Auth** |
| Background Jobs & Workflow Engine | **Inngest** |
| Email Service | **Nodemailer** |
| Database | **MongoDB** |
| Version Control | **Git & GitHub** |
| Package Manager | npm / pnpm / yarn |

---

## 📦 Installation Guide

### **Prerequisites**
Ensure you have the following installed:

- Node.js (v18+ recommended)
- npm / yarn / pnpm
- MongoDB locally or MongoDB Atlas
- Internet connection for TradingView widget resources

---

### **Clone the Repository**
```bash
git clone https://github.com/Sahil-SS/signalist.git
cd signalist
```
```bash
npm install
# or
yarn install
# or
pnpm install
```
---

## ⚙️ Environment Configuration

Create a `.env.local` file in the root directory and add the following:
```ini
MONGODB_URI=your_mongodb_connection_string
NEXT_PUBLIC_INGEST_API_KEY=your_ingest_key
AUTH_SECRET=your_auth_secret_key
EMAIL_SERVER_USER=your_email@example.com

EMAIL_SERVER_PASSWORD=your_email_password
```
## ▶️ Running the Development Server
```bash
npm run dev
http://localhost:3000
```
---

## 🔧 Setup & Configuration Guide

### **Inngest Setup (Background Jobs & Event Workflows)**

Inngest is used for creating scheduled tasks, event-driven functions, automated summaries, alerts, etc.

#### Install Inngest CLI (if not installed)
```bash
npm install inngest --save
npx inngest-cli@latest dev
```
### Basic example of an Inngest function:
```ts
import { inngest } from "@/lib/inngest";

export const summaryJob = inngest.createFunction(
  { id: "generate-market-summary" },
  { cron: "0 18 * * 1-5" }, // runs at 6pm Mon–Fri
  async () => {
    console.log("Market summary generated");
  }
);
```
### To run workflows locally:
```bash
npx inngest-cli@latest dev
```

### Nodemailer Setup (Email Notifications & Alerts)
```bash
npm install nodemailer
```
---

## 🧠 Future Scope

Signalist is continuously evolving, and several advanced features are planned for upcoming releases:

- **AI-Powered Market Summary**
  - Automatic generation of stock insights, sentiment-based summaries, and pattern detection.
- **Stock Watchlist Feature**
  - Add and track selected stocks with personalized alerts.
- Real-time WebSocket based live streaming updates
- Portfolio tracking and performance analytics
- Push notifications (email / browser alerts)
- Mobile app version (iOS & Android)

---

## 🤝 Contributing

Signalist is an open project, and **contributors are warmly welcomed!**  
Whether it's fixing bugs, improving documentation, designing UI, or adding new features — your contributions are highly valued.

### 🔧 How to Contribute

```bash
# 1. Fork the repository
# 2. Create a feature branch
git checkout -b feature/your-feature-name

# 3. Make your changes and commit
git commit -m "Added new feature"

# 4. Push your branch to GitHub
git push origin feature/your-feature-name

# 5. Create a Pull Request and describe your changes
```
---

## ❤️ Created With Love

Signalist is built with dedication, continuous learning, and passion for technology + financial markets.  
If you find this project useful, inspiring, or worth supporting, please consider:

- ⭐ Giving the repository a star on GitHub
- 🛠 Contributing improvements or ideas
- 💬 Sharing feedback to help it grow

Together, we can make something truly impactful.  
**Thank you for being part of the journey! 🚀**
