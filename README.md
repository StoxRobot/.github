# **StoxRobot - Comprehensive Trading Bot Management System**

StoxRobot is an advanced platform designed to manage, monitor, and optimize algorithmic trading bots. By integrating cutting-edge technologies, it provides a robust, scalable, and user-friendly solution for traders and developers looking to streamline their trading strategies.

---

## **Purpose**

The primary objectives of StoxRobot are to:
1. **Automate Trading Strategies**: Enable users to create and manage bots that execute predefined trading strategies automatically.
2. **Track Performance**: Monitor real-time profit/loss metrics and visualize trading activities.
3. **Analyze Historical Data**: Store and analyze trade history to refine strategies and evaluate performance.
4. **Provide Scalability**: Ensure the system can handle multiple bots and large volumes of trading data efficiently.

---

## **How StoxRobot Works**

### **System Flow**
1. **User Interaction**:
   - Users interact with the **frontend dashboard** to create, update, and manage bots.
   - The dashboard provides real-time insights into bot performance and trade history.

2. **Backend Processing**:
   - The **FastAPI backend** processes user requests, interacts with the database, and executes bot operations.
   - Bots are created with predefined strategies and status (e.g., active, inactive).

3. **Database Management**:
   - All bot configurations, trade data, and performance metrics are stored in **PostgreSQL**.
   - **TimescaleDB** (a PostgreSQL extension) is used for efficient handling of time-series trade data.

4. **Real-Time Updates**:
   - Bots execute trades based on strategies and fetch real-time data from integrated APIs (e.g., market data APIs).
   - Results are stored and displayed in the dashboard.

---

## **Technology Stack**

### **Frontend**
- **React**: Builds the user interface for managing bots and visualizing trade metrics.
- **Material-UI**: A modern library for styling and prebuilt components, ensuring a polished design.
- **Chart.js**: Renders performance metrics and trade history in visually appealing charts.
- **React Router**: Manages navigation between pages like dashboard, bot management, and trade history.
- **React Query**: Handles API state management for smooth data fetching and synchronization.

### **Backend**
- **FastAPI**: A high-performance framework for building the RESTful API.
- **SQLAlchemy**: Manages database operations and schema mapping using Object-Relational Mapping (ORM).
- **Pydantic**: Ensures robust validation and serialization of user input and API responses.
- **Uvicorn**: An ASGI server that runs the FastAPI application.

### **Database**
- **PostgreSQL**: Serves as the relational database for storing structured data like bot configurations and trades.
- **TimescaleDB**: A PostgreSQL extension optimized for handling time-series data like trade metrics and historical performance.

### **Infrastructure**
- **Docker**: Containerizes all services (frontend, backend, database) to ensure consistency and portability.
- **Docker Compose**: Orchestrates multi-container environments, simplifying the deployment process.
- **Flyway**: Manages database migrations, ensuring structured and versioned schema updates.

---

## **Features**

### **Bot Management**
- Create, update, delete, and view bots.
- Assign predefined strategies to bots, such as:
  - Momentum Trading
  - Mean Reversion
  - Arbitrage
- View and control the status of each bot (e.g., active, inactive).

### **Performance Monitoring**
- Real-time profit/loss metrics for each bot.
- Aggregate statistics for all bots (e.g., total profit, loss, active trades).

### **Trade History**
- Detailed logs of all trades executed by bots.
- Filter and sort trades by date, bot, or profit/loss.

### **Analytics and Visualization**
- Interactive charts powered by **Chart.js**.
- Insights into time-series data using **TimescaleDB**.

### **Scalability**
- Handle multiple bots and high-frequency trading data efficiently.
- Optimize database queries with TimescaleDB’s time-series capabilities.

---

## **Project Repositories**

### 1. **Infrastructure (`trading-bot-infra`)**
- Manages the infrastructure setup using Docker Compose.
- Services include:
  - PostgreSQL with TimescaleDB
  - Backend (FastAPI)
  - Frontend (React)

### 2. **Backend (`trading-bot-backend`)**
- Implements the FastAPI RESTful API for bots and trade management.
- Handles database interactions and business logic.

### 3. **Frontend (`trading-bot-frontend`)**
- Provides the React-based user interface for interacting with bots and viewing trade data.

### 4. **Database (`trading-bot-database`)**
- Stores migration files and schema definitions for PostgreSQL and TimescaleDB.
- Uses Flyway for version-controlled schema management.

---

## **How to Run the Project**

### **1. Clone the Repositories**
```bash
git clone https://github.com/your-username/trading-bot-infra.git
git clone https://github.com/your-username/trading-bot-backend.git
git clone https://github.com/your-username/trading-bot-frontend.git
git clone https://github.com/your-username/trading-bot-database.git
