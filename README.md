# 🐞 Bugscope Panel - Jira Issue Manager

**Bugscope** is a feature-rich custom Jira Issue Panel built using **Atlassian Forge** and **Custom UI**. It empowers users to manage Jira issues directly within the issue view—add, update, delete issues, and labels like `bug`, `priority`, and more. The panel also features a weather widget powered by geolocation-based APIs.

---

## 🚀 Features

### 🔧 Issue Management

* View issues with their summary and labels
* Create new issues with summary and label input
* Delete issues with a single click
* Filter issues based on label (e.g., show only `bug` or `priority` issues)

### 🏷️ Label Management

* View current labels of the selected issue
* Add new labels via input
* Delete existing labels instantly

### 🌤️ Weather Panel

* Fetch weather by default location (Delhi)
* Option to fetch weather by user’s live location (via IP geolocation)

---

## 📦 Tech Stack & Tools

* **Atlassian Forge** (Serverless App Platform)
* **Custom UI** with **React**
* **AWS Lambda-style functions** via `resolver.define`
* **Jira REST API** via `@forge/api`
* **@forge/bridge** for frontend-backend communication
* **OpenWeatherMap API** for weather data
* **IP-based geolocation** via `ipapi.co`

---

## 🧠 What I Learned

* ✅ Understanding of Forge's **serverless architecture**
* ✅ Implementing **backend logic using Lambda-style resolvers**
* ✅ Communicating with **Jira APIs** securely via scopes
* ✅ Building **Custom UI** inside the Jira Issue Panel
* ✅ Handling **CORS, sandboxing, and geolocation constraints**
* ✅ Using **Forge CLI** effectively: `forge deploy`, `forge install`, `forge uninstall`, `forge logs`
* ✅ Architecting a modular app with backend + frontend components
* ✅ The potential of GPT-based tools to extend app usability

---

## 📁 Project Structure

```
bugscope_panel/
├── manifest.yml
├── src/
│   ├── resolvers/index.js         # Lambda functions (e.g. fetchIssuesWithLabels)
│   └── frontend/index.jsx         # Custom UI using React
└── static/
    └── index.html
```

---

## 🏁 Getting Started

### 🔧 Prerequisites

* Node.js 18 or 20
* Atlassian Forge CLI
* A Jira Cloud instance

### 🔄 Install & Deploy

```bash
forge login
forge register
forge deploy
forge install
```

---

## 🔐 Permissions Required

```yaml
permissions:
  scopes:
    - read:jira-work
    - write:jira-work
  external:
    fetch:
      backend:
        - https://ipapi.co
        - https://api.openweathermap.org
```

---

## 📸 Screenshots

*Include screenshots of the panel, filtering, label actions, and weather widget.*
![image](https://github.com/user-attachments/assets/59a8b820-25c0-4a3f-9b63-1150b54d2e14)
![image](https://github.com/user-attachments/assets/914376ae-2316-4e60-a1b3-96e973345c97)
![image](https://github.com/user-attachments/assets/457a5b7e-ab98-49fd-b0d5-350057f3a48f)
![image](https://github.com/user-attachments/assets/42106754-c64e-418c-9f6f-0ffb18137e77)



