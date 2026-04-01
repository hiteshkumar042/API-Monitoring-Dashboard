# API Monitoring Dashboard (Angular)

## Overview

This project is a **real-time API Monitoring Dashboard** built using Angular. It allows users to monitor the health and performance of different services, view status updates, and track failure logs in a clean and scalable architecture.

---

## Features

**Authentication System**

  * Login functionality
  * Route protection using Auth Guard
  * Token-based authentication (localStorage)

**HTTP Interceptor**

  * Automatically attaches auth token to requests
  * Handles global HTTP errors (e.g., 401 Unauthorized)

**Dashboard**

  * Displays list of APIs/services
  * Shows real-time status (UP/DOWN)
  * Visual indicators with colors

**Charts Integration**

  * Line charts using Chart.js
  * Displays simulated response time trends

**Real-Time Simulation**

  * Uses interval-based updates to simulate live API status changes

**Logs Module**

  * Tracks API failures
  * Displays timestamped logs in a separate page

**Sidebar Navigation**

  * Navigate between Dashboard and Logs
  * Clean layout with header and sidebar

**Search & Filter**

  * Filter APIs dynamically based on user input

---

## Project Structure

```
src/
 ├── app/
 │    ├── core/              # Services, guards, interceptors
 │    │    ├── services/
 │    │    ├── guards/
 │    │    └── interceptors/
 │    │
 │    ├── features/          # Feature modules
 │    │    ├── dashboard/
 │    │    ├── auth/
 │    │    └── logs/
 │    │
 │    ├── layout/            # Layout components
 │    │    ├── header/
 │    │    └── sidebar/
 │    │
 │    └── shared/            # Reusable components (cards, etc.)
```

---

## Architecture

The project follows a **feature-based architecture**:

* **Core** → Singleton services (Auth, API, Interceptor)
* **Layout** → Application structure (Header, Sidebar)
* **Features** → Independent modules (Dashboard, Logs, Auth)
* **Shared** → Reusable UI components

---

## Tech Stack

* Angular (Standalone Components)
* TypeScript
* RxJS
* Chart.js
* HTML / CSS

---

## How It Works

1. User logs in → token stored in localStorage
2. Auth Guard protects routes
3. Dashboard fetches API data via service
4. Interceptor attaches token to requests
5. Status updates simulated using `setInterval`
6. Logs are generated when API status is DOWN
7. Charts visualize API performance trends

---

## Getting Started

### 1. Install dependencies

```
npm install
```

### 2. Run the app

```
ng serve
```

### 3. Open in browser

```
http://localhost:4200
```

---

##  Demo Credentials

(No real authentication backend — simulated login)

---

##  Future Improvements

* Real backend integration (Node.js)
* WebSocket-based real-time updates
* Role-based authentication
* Dark mode UI
* Advanced analytics dashboard

---

## Key Learnings

* Angular standalone architecture
* Component-based design
* State updates and change detection
* Integration with third-party libraries (Chart.js)
* Authentication & route protection
* Scalable folder structure

---

## Author

**Hitesh Kumar**

---

## Conclusion

This project demonstrates a **production-like Angular application** with real-world features such as authentication, monitoring dashboard, logging, and modular architecture.

---
