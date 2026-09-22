# 📈 TradeHub

> A full-stack trading dashboard built with the MERN stack for managing holdings, monitoring watchlists, visualizing portfolio data, and interacting with trading-related workflows.

[![React](https://img.shields.io/badge/React-18.x-61DAFB?logo=react\&logoColor=white)](https://react.dev/)
[![Node.js](https://img.shields.io/badge/Node.js-Backend-339933?logo=node.js\&logoColor=white)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-API-000000?logo=express\&logoColor=white)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Database-47A248?logo=mongodb\&logoColor=white)](https://www.mongodb.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript\&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

---

## 📌 Overview

**TradeHub** is a full-stack web application developed to provide an interactive trading dashboard experience.

The project combines a React-based frontend with a Node.js/Express backend and MongoDB database integration. It focuses on building reusable frontend components, managing application data, creating interactive portfolio visualizations, and connecting the user interface with backend services.

The project was developed with a focus on:

* Full-stack web development
* Component-based React architecture
* REST API integration
* Database connectivity
* Portfolio and holdings management
* Interactive data visualization
* Modular and maintainable application structure

---

## ✨ Features

### 📊 Trading Dashboard

* Interactive dashboard interface
* Portfolio-oriented data presentation
* Holdings and position monitoring
* Organized trading-related components
* Reusable React components

### 💼 Holdings Management

* Display and manage portfolio holdings
* Dedicated holdings interface
* Structured presentation of position-related information
* Integration with dashboard-level application state

### ⭐ Watchlist

* Watchlist interface for monitoring selected assets
* Component-based implementation
* Integration with the overall dashboard workflow

### 💰 Trading Interface

* Buy action interface
* Dedicated buy-action component
* Structured trading workflow
* Modular UI components for trading operations

### 📈 Data Visualization

* Interactive chart components
* Bar graph visualization
* Doughnut chart visualization
* Portfolio-related data representation

### ⚙️ Backend

* Node.js backend
* Express.js server
* REST API architecture
* MongoDB integration
* Mongoose-based database models

---

# 🛠️ Tech Stack

## Frontend

| Technology | Purpose                                   |
| ---------- | ----------------------------------------- |
| React.js   | User interface and component architecture |
| JavaScript | Application logic                         |
| HTML5      | Application structure                     |
| CSS3       | Styling and responsive UI                 |

## Backend

| Technology | Purpose                         |
| ---------- | ------------------------------- |
| Node.js    | Server-side JavaScript runtime  |
| Express.js | Backend framework and REST APIs |
| Mongoose   | MongoDB object modeling         |

## Database

| Technology | Purpose              |
| ---------- | -------------------- |
| MongoDB    | Application database |

## Development Tools

| Tool    | Purpose                 |
| ------- | ----------------------- |
| Git     | Version control         |
| GitHub  | Source-code hosting     |
| VS Code | Development environment |
| npm     | Dependency management   |

---

# 🏗️ System Architecture

TradeHub follows a client-server architecture where the React application communicates with the Node.js/Express backend, which manages application logic and database interactions.

```text
                    ┌─────────────────────────┐
                    │       TradeHub UI       │
                    │        React.js         │
                    │                         │
                    │  Dashboard              │
                    │  Holdings               │
                    │  Watchlist               │
                    │  Trading Components     │
                    │  Charts                  │
                    └────────────┬────────────┘
                                 │
                                 │ HTTP / REST API
                                 ▼
                    ┌─────────────────────────┐
                    │    Node.js + Express    │
                    │        Backend          │
                    │                         │
                    │  API Routes             │
                    │  Business Logic         │
                    │  Request Handling       │
                    └────────────┬────────────┘
                                 │
                                 │ Mongoose
                                 ▼
                    ┌─────────────────────────┐
                    │        MongoDB          │
                    │                         │
                    │  Application Data       │
                    │  Trading Data           │
                    │  User/Portfolio Data    │
                    └─────────────────────────┘
```

---

# 📂 Project Structure

```text
TradeHub/
│
├── backend/
│   ├── model/
│   ├── schemas/
│   ├── index.js
│   ├── package.json
│   ├── package-lock.json
│   └── .env
│
├── dashboard/
│   ├── public/
│   ├── src/
│   │   └── components/
│   │       ├── Dashboard.js
│   │       ├── Holdings.js
│   │       ├── WatchList.js
│   │       ├── BarGraph.js
│   │       ├── DoughnutChart.js
│   │       ├── BuyActionWindow.js
│   │       ├── BuyActionWindow.css
│   │       └── GeneralContext.js
│   ├── package.json
│   └── package-lock.json
│
├── frontend/
│   └── ...
│
├── .gitignore
└── README.md
```

> **Note:** `.env` is a local configuration file and should never be committed to the repository.

---

# 🚀 Getting Started

Follow the steps below to run TradeHub locally.

## Prerequisites

Make sure the following are installed:

* Node.js
* npm
* MongoDB / MongoDB Atlas account
* Git

You can verify Node.js and npm:

```bash
node --version
npm --version
```

---

# 📥 Installation

## 1. Clone the Repository

```bash
git clone https://github.com/karanghadage807-coder/TradeHub.git
```

Navigate into the project:

```bash
cd TradeHub
```

---

## 2. Install Backend Dependencies

```bash
cd backend
npm install
```

---

## 3. Configure Environment Variables

Create a `.env` file inside the `backend` directory.

```text
backend/
└── .env
```

Add the environment variables required by the backend.

Example:

```env
MONGO_URI=your_mongodb_connection_string
PORT=3000
```

> Replace the values with your own configuration.

**Never commit your actual `.env` file to GitHub.**

---

## 4. Start the Backend

From the `backend` directory:

```bash
npm start
```

If your project uses a development script:

```bash
npm run dev
```

---

## 5. Install Dashboard Dependencies

Open another terminal:

```bash
cd TradeHub/dashboard
npm install
```

---

## 6. Start the Dashboard

```bash
npm start
```

The React application will normally be available at:

```text
http://localhost:3000
```

> The exact port may depend on the configuration of the application.

---

# 🔐 Environment Variables

TradeHub uses environment variables for configuration and sensitive credentials.

The actual `.env` file is intentionally excluded from version control.

A typical configuration may contain:

```env
MONGO_URI=your_mongodb_connection_string
PORT=your_backend_port
```

For security:

* Never commit database credentials.
* Never commit API keys.
* Never commit passwords or tokens.
* Never expose production secrets in source code.

---

# 📊 Core Components

## Dashboard

The dashboard acts as the primary interface for displaying trading and portfolio-related information.

It brings together different components such as:

* Holdings
* Watchlist
* Charts
* Trading actions
* Portfolio information

---

## Holdings

The Holdings component provides an interface for displaying portfolio positions and related information.

It is integrated into the dashboard architecture to allow portfolio information to be presented in an organized manner.

---

## Watchlist

The Watchlist component provides a dedicated interface for monitoring selected assets.

It is designed as a reusable React component that can be integrated into the dashboard.

---

## Buy Action Window

The Buy Action Window provides the user interface for initiating a buy-related workflow.

The component is separated into its own JavaScript and CSS files to maintain modularity.

---

## Data Visualization

TradeHub contains dedicated visualization components including:

### Bar Graph

Used to represent data using a bar-chart format.

### Doughnut Chart

Used to provide proportional or categorical data visualization.

These components allow portfolio-related information to be presented visually rather than relying only on tabular data.

---

# 🧩 Development Approach

The project follows a modular full-stack development approach.

### Frontend

The frontend is divided into reusable React components instead of placing the entire application logic into a single component.

### Backend

The backend separates server-side functionality from the frontend and exposes services through Express.js.

### Database

MongoDB is used for persistent application data, with Mongoose providing structured interaction between the Node.js application and MongoDB.

### Version Control

Git is used to maintain project history and support feature-based development.

---

# 🔄 Git Workflow

The project uses Git for version control.

A typical development workflow is:

```text
Create Feature Branch
        │
        ▼
Develop Feature
        │
        ▼
Test Locally
        │
        ▼
Commit Changes
        │
        ▼
Merge into main
        │
        ▼
Push to GitHub
```

Example:

```bash
git checkout -b feature/new-feature

git add <files>

git commit -m "feat: add new feature"

git push origin feature/new-feature
```

---

# 🧪 Testing & Validation

Before pushing changes to the main branch, verify:

* Frontend starts successfully
* Backend starts successfully
* Database connection works
* Dashboard loads correctly
* Components render without errors
* API requests work correctly
* No environment variables or secrets are committed

---


# 💡 Learning Outcomes

Through the development of TradeHub, the project demonstrates practical experience with:

* Full-stack web application development
* React component architecture
* Node.js backend development
* Express.js REST APIs
* MongoDB database integration
* Mongoose
* Application state management
* Data visualization
* Git and GitHub
* Modular software development
* Frontend-backend integration

---

# 🛣️ Roadmap

```text
[x] React dashboard
[x] Holdings interface
[x] Watchlist interface
[x] Trading action interface
[x] Data visualization components
[x] Node.js backend
[x] Express.js integration
[x] MongoDB integration
[ ] Authentication
[ ] Real-time market data
[ ] Advanced portfolio analytics
[ ] Automated testing
[ ] CI/CD
[ ] Cloud deployment
```

---

# 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

To contribute:

```bash
# Fork the repository

# Clone your fork
git clone <your-fork-url>

# Create a feature branch
git checkout -b feature/your-feature

# Make your changes

# Commit your changes
git commit -m "feat: describe your change"

# Push the branch
git push origin feature/your-feature
```

Then open a Pull Request.

---

# 📄 License

This project is intended as a personal portfolio and learning project.

If you plan to distribute or reuse the project, please add an appropriate open-source license to the repository.

---

# 👨‍💻 Author

**Karan Ghadage**

B.Tech Electrical Engineering
VJTI Mumbai
Minor in Data Science

### Connect

* GitHub: [karanghadage807-coder](https://github.com/karanghadage807-coder)

---

## ⭐ Support

If you find this project useful or interesting, consider giving the repository a ⭐ on GitHub.

---

<p align="center">
  Built with ❤️ using React, Node.js, Express.js and MongoDB
</p>
