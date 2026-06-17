# ShopEZ - Full Stack E-Commerce Microservices Application

ShopEZ is a full-stack e-commerce platform built using **ASP.NET Core 8 Microservices**, **Angular 18**, **SQL Server**, **Docker**, **JWT Authentication**, and **Ocelot API Gateway**.

The application follows a microservices architecture where independent services handle user management, product catalog, shopping cart, and order processing. All client requests are routed through a centralized API Gateway, while the Angular frontend provides a responsive user experience.

---

## Features

### Customer Features

* User Registration and Login
* JWT-Based Authentication
* Product Browsing and Search
* Product Details View
* Shopping Cart Management
* Checkout and Order Placement
* Order History Tracking
* Secure Role-Based Access Control

### Admin Features

* Product Creation
* Product Update
* Product Deletion
* Product Inventory Management
* Protected Admin Routes

---

## Architecture

### Backend Microservices

| Service               | Responsibility                           |
| --------------------- | ---------------------------------------- |
| ShopEZ.UserService    | User registration, login, JWT generation |
| ShopEZ.ProductService | Product catalog and inventory management |
| ShopEZ.CartService    | Cart synchronization and storage         |
| ShopEZ.OrderService   | Order placement and order history        |
| ShopEZ.API Gateway    | Centralized routing and authentication   |

### Frontend

| Technology     | Purpose                 |
| -------------- | ----------------------- |
| Angular 18     | Single Page Application |
| TypeScript     | Frontend Development    |
| Angular Router | Client-side Routing     |
| Reactive Forms | Form Validation         |
| RxJS           | State and Data Handling |
| Bootstrap      | Responsive UI           |

---

## Technology Stack

### Backend

* ASP.NET Core 8
* C#
* Entity Framework Core
* Dapper
* SQL Server
* JWT Authentication
* Ocelot API Gateway
* REST APIs
* Docker & Docker Compose
* xUnit Testing

### Frontend

* Angular 18
* TypeScript
* HTML5
* CSS3
* Bootstrap
* RxJS

### DevOps & Tools

* Git
* GitHub
* Docker
* Visual Studio 2022
* VS Code
* Postman

---

## System Workflow

1. User accesses Angular Frontend.
2. Frontend communicates only with the API Gateway.
3. API Gateway routes requests to respective microservices.
4. UserService authenticates users and issues JWT tokens.
5. ProductService manages product catalog and stock.
6. CartService manages shopping cart operations.
7. OrderService processes orders and updates stock.
8. Responses are returned through the API Gateway to the frontend.

---

## Security Features

* JWT Authentication
* Role-Based Authorization

  * Admin
  * Customer
* Protected API Endpoints
* Angular Route Guards

  * authGuard
  * adminGuard
  * customerGuard
* Internal Service Communication Protection using `X-Internal-Key`

---

## Core API Endpoints

### Authentication

```http
POST /api/auth/register
POST /api/auth/login
```

### Products

```http
GET    /api/products
GET    /api/products/{id}
POST   /api/products
PUT    /api/products/{id}
DELETE /api/products/{id}
```

### Cart

```http
GET    /api/cart
POST   /api/cart/sync
DELETE /api/cart
```

### Orders

```http
POST /api/orders
GET  /api/orders
GET  /api/orders/{id}
```

---

## Project Structure

```text
E-Commerce-Shop-EZ-Application
│
├── Frontend Angular
│   ├── src
│   ├── angular.json
│   ├── package.json
│   └── Dockerfile
│
├── ShopEZ.Microservices
│   ├── ShopEZ.API Gateway
│   ├── ShopEZUserService
│   ├── ShopEZProductService
│   ├── ShopEZCartService
│   ├── ShopEZOrderService
│   ├── tests
│   └── docker-compose.yml
│
└── README.md
```

---

## Running the Application

### Prerequisites

* .NET 8 SDK
* Node.js 20+
* Angular CLI
* SQL Server
* Docker Desktop

---

### Run Using Docker (Recommended)

Clone the repository:

```bash
git clone https://github.com/lalahmed632/E-Commerce-Shop-EZ-Application.git
```

Navigate to project:

```bash
cd E-Commerce-Shop-EZ-Application
```

Start all services:

```bash
docker compose up --build -d
```

Verify running containers:

```bash
docker compose ps
```

---

## Application URLs

### Frontend

```text
http://localhost:4200
```

### API Gateway

```text
http://localhost:7201
```

### Health Check

```text
http://localhost:7201/health
```

---

## Demo Credentials

```text
Customer
Email: customer@shopez.com
Password: Pass@123
```

```text
Admin
Email: admin@shopez.com
Password: Admin@123
```

---

## Testing

Run all tests:

```powershell
dotnet test
```

Or run individual service tests:

```powershell
dotnet test tests\ShopEZ.ProductService.Tests
dotnet test tests\ShopEZ.CartService.Tests
dotnet test tests\ShopEZ.OrderService.Tests
dotnet test tests\ShopEZ.UserService.Tests
```

---

## Screenshots

Add screenshots for:

* Home Page
* Login Page
* Registration Page
* Product Listing
* Product Details
* Shopping Cart
* Checkout
* Orders History
* Admin Dashboard
* Docker Containers Running
* API Gateway Health Endpoint

---

## Key Highlights

* Microservices Architecture
* API Gateway Pattern
* JWT Authentication & Authorization
* Angular Single Page Application
* Dockerized Deployment
* SQL Server Integration
* Entity Framework Core & Dapper
* RESTful API Design
* Role-Based Access Control
* Unit Testing with xUnit

---

## Author

**Shaik Lal Ahmed**

B.Tech Computer Science & Engineering (2025)

Full Stack .NET Developer | ASP.NET Core | Angular | SQL Server | Docker
