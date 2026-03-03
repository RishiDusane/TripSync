<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0EA5E9&height=200&section=header&text=TripSync&fontSize=70&fontColor=ffffff&fontAlignY=38&desc=Travel%20Management%20System%20%E2%80%94%20Microservices%20Architecture&descAlignY=58&descSize=17&descColor=e0f2fe" width="100%"/>

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Georgia&size=22&duration=3000&pause=1000&color=0EA5E9&center=true&vCenter=true&width=650&height=50&lines=Streamlining+Your+Travel+Experiences+%E2%9C%88%EF%B8%8F;Spring+Boot+Microservices+%7C+React+19+%7C+Stripe;Explore+%C2%B7+Book+%C2%B7+Travel+%C2%B7+Review" alt="Typing SVG"/>

<br/><br/>

[![Java](https://img.shields.io/badge/Java_21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.java.com/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot_3.2-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)](https://spring.io/)
[![Spring Cloud](https://img.shields.io/badge/Spring_Cloud-6DB33F?style=for-the-badge&logo=spring&logoColor=white)](https://spring.io/projects/spring-cloud)
[![React](https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite_7-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Stripe](https://img.shields.io/badge/Stripe-008CDD?style=for-the-badge&logo=stripe&logoColor=white)](https://stripe.com/)
[![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)](https://jwt.io/)
[![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)](https://maven.apache.org/)

</div>

---

## 📌 Table of Contents

- [✨ About](#-about)
- [🏗️ Architecture](#️-architecture)
- [🔹 Microservices](#-microservices)
- [🎨 Frontend](#-frontend)
- [🛠️ Tech Stack](#️-tech-stack)
- [📂 Routes & Structure](#-routes--structure)
- [✨ Features](#-features)
- [⚙️ Getting Started](#️-getting-started)
- [🎯 Learning Outcomes](#-learning-outcomes)
- [🔮 Roadmap](#-roadmap)
- [👨‍💻 Authors](#-authors)

---

## ✨ About

**TripSync** is a comprehensive travel management platform built on a **microservices architecture**. It enables users to explore travel destinations, book tour packages, complete secure payments, and share feedback on their experiences.

> 🎓 This project demonstrates real-world implementation of **Spring Boot Microservices**, **API Gateway routing**, **JWT-based security**, and modern **React 19** frontend integration.

---

## 🏗️ Architecture

```
                        ┌─────────────────────────┐
                        │    React 19 + Vite 7     │
                        │      (Frontend UI)        │
                        └────────────┬────────────┘
                                     │  HTTP / REST
                                     ▼
                        ┌─────────────────────────┐
                        │      API Gateway         │
                        │       Port: 8090         │
                        │  (Single Entry Point)    │
                        └──┬──────┬──────┬────┬───┘
                           │      │      │    │
               ┌───────────┘      │      │    └──────────────┐
               ▼                  ▼      ▼                   ▼
        ┌────────────┐  ┌──────────────┐ ┌──────────────┐  ┌──────────────┐
        │    Auth    │  │   Catalog    │ │   Booking    │  │   Feedback   │
        │  Service   │  │   Service   │ │   Service    │  │   Service    │
        │  Port:8081 │  │  Port:8082  │ │  Port:8083   │  │  Port:8084   │
        └────────────┘  └─────────────┘ └──────┬───────┘  └──────────────┘
                                                │
                                                ▼
                                        ┌──────────────┐
                                        │    Stripe    │
                                        │   Payments   │
                                        └──────────────┘
```

---

## 🔹 Microservices

<table>
<tr>
<td valign="top" width="50%">

### 🔹 API Gateway — `Port 8090`
- Single entry point for all requests
- Routes traffic to correct microservice
- Centralized request handling & filtering

### 🔹 Auth Service — `Port 8081`
- User registration & login
- JWT-based authentication & authorization
- Forgot password & reset flow with token validation

### 🔹 Catalog Service — `Port 8082`
- Manages travel destinations & tour packages
- Full CRUD for travel offerings
- Admin-controlled package management

</td>
<td valign="top" width="50%">

### 🔹 Booking Service — `Port 8083`
- Full booking lifecycle management
- Stripe payment gateway integration
- Automatic booking confirmation post-payment

### 🔹 Feedback Service — `Port 8084`
- User reviews & ratings (1–5 scale)
- View feedback by user or by package
- Review management APIs

</td>
</tr>
</table>

---

## 🎨 Frontend

Built with **React 19** + **Vite 7** for blazing-fast builds and smooth UI performance.

| Technology | Purpose |
|:-----------|:--------|
| ⚛️ React 19 | Component-based UI |
| ⚡ Vite 7 | Fast build tool & dev server |
| 🧭 React Router 7 | Client-side navigation |
| 🌐 Axios | REST API communication |
| 🎨 CSS | Styling & layouts |

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technology | Version |
|:------|:-----------|:--------|
| ☕ **Backend Language** | Java | 21 |
| 🌿 **Framework** | Spring Boot | 3.2.1 |
| ☁️ **Microservices** | Spring Cloud | 2023.0.0 |
| 🛡️ **Security** | Spring Security + JWT | — |
| ⚛️ **Frontend** | React + Vite | 19 / 7 |
| 🧭 **Routing** | React Router | 7 |
| 💳 **Payments** | Stripe | — |
| 📦 **Build** | Maven | — |
| 🌐 **HTTP Client** | Axios | — |

</div>

---

## 📂 Routes & Structure

### 🔀 Backend Routing (via API Gateway)

| Service | Route Path | Port |
|:--------|:-----------|:----:|
| 🔐 Auth Service | `/api/auth/**` | 8081 |
| 🗺️ Catalog Service | `/api/destinations/**` · `/api/packages/**` | 8082 |
| 📅 Booking Service | `/api/bookings/**` · `/api/payments/**` | 8083 |
| ⭐ Feedback Service | `/api/reviews/**` | 8084 |

### 🖥️ Frontend Pages

| Route | Page |
|:------|:-----|
| `/` | 🏠 Landing Page |
| `/login` · `/signup` | 🔐 User Authentication |
| `/dashboard` | 📊 Main User Interface |
| `/packages/:destinationId` | 🗺️ View Tour Packages |
| `/my-bookings` | 📅 Booking History |
| `/admin` | 🔒 Admin-Only Protected Routes |

---

## ✨ Features

- 🔐 **JWT Authentication** — Secure login, registration & session management
- 📧 **Forgot Password Flow** — Email-based reset token system
- 🗺️ **Tour Catalog Management** — Admin-controlled destinations & packages
- 💳 **Stripe Payment Integration** — Real-time secure payment processing
- ✅ **Automatic Booking Confirmation** — Triggered on successful payment
- ⭐ **User Feedback & Ratings** — 1–5 star review system per package
- 🛡️ **Role-Based Access Control** — Separate Admin & User permissions
- 🌐 **API Gateway Routing** — Centralized microservice communication

---

## ⚙️ Getting Started

### 📋 Prerequisites

```
✅ Java 21+        ✅ Node.js v18+
✅ Maven 3.8+      ✅ Stripe Account (for payments)
✅ Git
```

### 🖥️ Backend Setup

```bash
# 1. Clone the repository
git clone https://github.com/your-username/tripsync.git

# 2. Navigate to backend
cd backend/travel

# 3. Build all microservices
mvn clean install

# 4. Run each service individually (in separate terminals)

# Terminal 1 — Auth Service
cd auth-service && mvn spring-boot:run

# Terminal 2 — Catalog Service
cd catalog-service && mvn spring-boot:run

# Terminal 3 — Booking Service
cd booking-service && mvn spring-boot:run

# Terminal 4 — Feedback Service
cd feedback-service && mvn spring-boot:run

# Terminal 5 — API Gateway (start LAST)
cd api-gateway && mvn spring-boot:run

# ✅ Gateway live at → http://localhost:8090
```

### 🎨 Frontend Setup

```bash
# 1. Navigate to frontend
cd frontend

# 2. Install dependencies
npm install

# 3. Start development server
npm run dev

# ✅ Frontend live at → http://localhost:5173
```

---

## 🎯 Learning Outcomes

- ✅ Designed & implemented **Spring Boot microservices** from scratch
- ✅ Configured **API Gateway** with service routing
- ✅ Secured APIs using **JWT & Spring Security**
- ✅ Integrated **Stripe** payment gateway end-to-end
- ✅ Built a scalable **React 19 + REST API** system
- ✅ Followed **enterprise-grade backend architecture** patterns

---

## 🔮 Roadmap

| Status | Feature | Details |
|:------:|:--------|:--------|
| 🔵 Planned | **Docker Containerization** | Dockerize all microservices |
| 🔵 Planned | **Centralized Logging** | ELK Stack / Grafana monitoring |
| 🔵 Planned | **Config Server** | Centralized config management |
| 🔵 Planned | **Cloud Deployment** | AWS / Azure deployment |
| 🟡 In Design | **Email Notifications** | Booking confirmations via SMTP |
| 🟡 In Design | **Service Discovery** | Eureka / Consul integration |

---

## 👨‍💻 Authors

<div align="center">

<table>
<tr>
<td align="center" width="50%">

<img src="https://avatars.githubusercontent.com/AdarshMani" width="100" style="border-radius:50%"/>

### Adarsh Mani
**Java Full Stack Developer**

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AdarshMani)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/adarsh-mani)

</td>
<td align="center" width="50%">

<img src="https://avatars.githubusercontent.com/RishiDusane" width="100" style="border-radius:50%"/>

### Rishi Dattatray Dusane
**Java Full Stack Developer**

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RishiDusane)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/your-linkedin-here)

</td>
</tr>
</table>

<br/>

---

⭐ **Enjoyed TripSync? Give it a star — it really helps!** ✈️

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0EA5E9&height=120&section=footer" width="100%"/>
