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
[![JUnit5](https://img.shields.io/badge/JUnit_5-25A162?style=for-the-badge&logo=junit5&logoColor=white)](https://junit.org/junit5/)
[![Mockito](https://img.shields.io/badge/Mockito-78A641?style=for-the-badge&logoColor=white)](https://site.mockito.org/)

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
- [🧪 Testing Approach](#-testing-approach)
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
| 🧪 **Unit Testing** | JUnit 5 + Mockito | — |
| 🔬 **Integration Testing** | JUnit 5 + Spring Boot Test | — |
| 📮 **API Testing** | Postman | — |

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

## 🧪 Testing Approach

In a microservices system, reliability requires testing at multiple levels — service isolation, integration boundaries, and API contracts. Testing was applied across all services using **JUnit 5**, **Mockito**, and **Postman**.

---

### 🔬 Unit Testing — Service Layer (Per Microservice)

Each microservice's service layer was tested in isolation. Repositories and external service clients were mocked using **Mockito** to focus tests purely on business logic.

**What was tested:**
- Booking creation, cancellation, and status transitions (Booking Service)
- JWT token generation and validation logic (Auth Service)
- Tour package and destination CRUD operations (Catalog Service)
- Review submission and retrieval rules (Feedback Service)
- Input validation, constraint enforcement, and exception paths across all services

**Example — Booking Service:**
```java
@ExtendWith(MockitoExtension.class)
class BookingServiceTest {

    @Mock
    private BookingRepository bookingRepository;

    @Mock
    private CatalogClient catalogClient;

    @InjectMocks
    private BookingServiceImpl bookingService;

    @Test
    void shouldCreateBookingWhenPackageIsAvailable() {
        BookingRequest request = new BookingRequest(1L, 2L, LocalDate.now());
        PackageDto mockPackage = new PackageDto(1L, "Goa Tour", 5999.0, true);

        when(catalogClient.getPackageById(1L)).thenReturn(mockPackage);
        when(bookingRepository.save(any(Booking.class))).thenAnswer(i -> i.getArgument(0));

        BookingResponse response = bookingService.createBooking(request);

        assertNotNull(response);
        assertEquals("PENDING", response.getStatus());
        verify(bookingRepository, times(1)).save(any(Booking.class));
    }

    @Test
    void shouldThrowExceptionWhenPackageNotFound() {
        when(catalogClient.getPackageById(99L))
            .thenThrow(new ResourceNotFoundException("Package not found"));

        assertThrows(ResourceNotFoundException.class,
            () -> bookingService.createBooking(new BookingRequest(99L, 1L, LocalDate.now())));
    }
}
```

---

### 🔗 Integration Testing — API Layer (Per Microservice)

Integration tests validated complete request-response cycles through the Controller → Service → Repository stack using **Spring Boot Test** with `MockMvc`.

**What was tested across all services:**
- Auth Service — registration, login, invalid credentials, token expiry
- Catalog Service — package CRUD with Admin vs User role enforcement
- Booking Service — booking creation, listing, and payment state transitions
- Feedback Service — review submission and retrieval per package
- HTTP status codes: 200, 201, 400, 401, 403, 404 across all endpoints
- Response payload structure — field presence, data types, error message format

**Example — Auth Service:**
```java
@SpringBootTest
@AutoConfigureMockMvc
class AuthControllerIntegrationTest {

    @Autowired
    private MockMvc mockMvc;

    @Autowired
    private ObjectMapper objectMapper;

    @Test
    void shouldReturn200AndTokenOnValidLogin() throws Exception {
        LoginRequest request = new LoginRequest("user@example.com", "password123");

        mockMvc.perform(post("/api/auth/login")
                .contentType(MediaType.APPLICATION_JSON)
                .content(objectMapper.writeValueAsString(request)))
            .andExpect(status().isOk())
            .andExpect(jsonPath("$.token").isNotEmpty());
    }

    @Test
    void shouldReturn401OnInvalidCredentials() throws Exception {
        LoginRequest request = new LoginRequest("user@example.com", "wrongpassword");

        mockMvc.perform(post("/api/auth/login")
                .contentType(MediaType.APPLICATION_JSON)
                .content(objectMapper.writeValueAsString(request)))
            .andExpect(status().isUnauthorized());
    }
}
```

---

### 🔐 Security & RBAC Testing

Authorization boundaries were explicitly tested to ensure role enforcement was correct across all services.

**Scenarios validated:**
- Admin-only endpoints return `403 Forbidden` when accessed with a User token
- Protected endpoints return `401 Unauthorized` when no token is provided
- Expired or malformed JWT tokens are correctly rejected at the gateway
- Each role (Admin, User) can only access permitted endpoints and data

```java
@Test
void shouldReturn403WhenUserAccessesAdminCatalogEndpoint() throws Exception {
    String userToken = generateToken("ROLE_USER");

    mockMvc.perform(post("/api/packages")
            .header("Authorization", "Bearer " + userToken)
            .contentType(MediaType.APPLICATION_JSON)
            .content("{ \"name\": \"Manali Tour\", \"price\": 7999 }"))
        .andExpect(status().isForbidden());
}
```

---

### 🌐 API Gateway — Routing Verification

The API Gateway was verified as the single entry point for all traffic, confirming correct routing to each downstream service.

**What was tested:**
- `/api/auth/**` routes correctly to Auth Service (Port 8081)
- `/api/packages/**` routes correctly to Catalog Service (Port 8082)
- `/api/bookings/**` routes correctly to Booking Service (Port 8083)
- `/api/reviews/**` routes correctly to Feedback Service (Port 8084)
- JWT Authorization headers are forwarded correctly to all downstream services

---

### 📮 API Testing — Postman

All 20+ REST endpoints across all five services were manually validated using **Postman**, covering the complete end-to-end user journey.

| Service | Test Scenarios Covered |
|:--------|:----------------------|
| 🔐 Auth | Register, login, invalid credentials, token expiry, password reset |
| 🗺️ Catalog | Browse destinations, CRUD packages (Admin), invalid payloads |
| 📅 Booking | Create booking, payment flow, booking history, cancellation |
| ⭐ Feedback | Submit review, view by package, view by user, duplicate review |
| 🌐 Gateway | Route verification per service, auth header forwarding |

---

### 📊 Test Coverage Summary

| Layer | Tool | Scope |
|:------|:-----|:------|
| Service (Unit) | JUnit 5 + Mockito | Business logic, validation, exceptions — per microservice |
| Controller (Integration) | JUnit 5 + Spring Boot Test | HTTP status, RBAC, payload structure — per microservice |
| Security | MockMvc + JWT | Auth boundaries, role enforcement, token validation |
| Gateway | Integration Tests | Route forwarding, header propagation |
| API (Manual) | Postman | End-to-end user journey across all services |

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
git clone https://github.com/RishiDusane/TripSync.git

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

### 🧪 Run Tests

```bash
# Run all tests across all microservices (from root)
mvn test

# Run tests for a specific service
cd auth-service && mvn test
cd booking-service && mvn test

# Run with coverage report
mvn test jacoco:report
```

---

## 🎯 Learning Outcomes

- ✅ Designed & implemented **Spring Boot microservices** from scratch
- ✅ Configured **API Gateway** with service routing
- ✅ Secured APIs using **JWT & Spring Security**
- ✅ Integrated **Stripe** payment gateway end-to-end
- ✅ Built a scalable **React 19 + REST API** system
- ✅ Applied **unit and integration testing** across distributed services using JUnit 5 and Mockito
- ✅ Validated API contracts and cross-service flows using Postman
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
| 🔵 Planned | **Automated UI Tests** | Selenium / Playwright test suite |

---

## 👨‍💻 Authors

<div align="center">

<table>
<tr>
<td align="center" width="50%">

<img src="https://avatars.githubusercontent.com/AdarshMani" width="100" style="border-radius:50%"/>

### Adarsh Mani
**Java Full Stack Developer**

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/frostAdarsh)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/adarsh-mani-95b216254/)

</td>
<td align="center" width="50%">

<img src="https://avatars.githubusercontent.com/RishiDusane" width="100" style="border-radius:50%"/>

### Rishi Dattatray Dusane
**Software Development Engineer in Test (SDET)**

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RishiDusane)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/rishidusane)

</td>
</tr>
</table>

<br/>

---

⭐ **Enjoyed TripSync? Give it a star — it really helps!** ✈️

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0EA5E9&height=120&section=footer" width="100%"/>
