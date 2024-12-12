# Software Design Description (SDD)

## 1. Introduction

### 1.1 Purpose
The purpose of this Software Design Description (SDD) is to provide a detailed design for the Zomato food-ordering and delivery application. This document describes the system's architecture, components, interfaces, and their interactions to ensure that the implementation meets the functional and non-functional requirements.

### 1.2 Scope
The Zomato system enables users to browse restaurants, place food orders, and make payments through a mobile or web app. Restaurants can manage menus and orders, while delivery partners fulfill requests. The system includes:
- Mobile and web applications.
- Backend API services.
- Payment processing integration.
- Real-time communication.
- External services like maps and SMS gateways.

---

## 2. System Overview

The Zomato system is composed of three main modules:

- **User Interface**: Mobile/Web apps for customers, restaurants, and delivery agents.
- **Backend System**: API and business logic for order processing and user management.
- **External Services**: Third-party integrations for payment gateways, maps, and SMS.

The system operates across Android, iOS, and web platforms and communicates with a backend via REST APIs, employing scalable cloud-based architecture for high performance and availability.

---

## 3. Architecture Design

### 3.1 Architecture Components

#### User Interfaces
- **Customer App and Web Interface**
  - Search and filter restaurants.
  - View menus and place orders.
  - Track orders in real-time.
  - Integrated payment options.
  - Review and rate restaurants/delivery partners.

- **Restaurant Dashboard**
  - Menu and order management.
  - Insights into performance and customer reviews.
  - Integration with promotions and offers.

- **Delivery Partner App**
  - Real-time delivery requests.
  - Navigation for delivery routes.
  - Earnings tracking.


#### Backend Services
- **Authentication**  
  Secure user authentication using JWT tokens for customers, restaurants, and delivery agents.

- **Order Management**  
  Handles the lifecycle of food orders, including placement, status updates, and cancellations.

- **Real-time Communication**  
  WebSocket-based real-time updates for order tracking and delivery progress.

- **Payment Processing**  
  Integrates with external payment gateways like Razorpay or Stripe for secure transactions.

- **Notification Service**  
  Sends notifications for order confirmations, updates, and promotional offers.

#### Databases
- **PostgreSQL**  
  Stores structured data (user profiles, restaurant details, orders, payments).

- **Redis**  
  Caches real-time data (active orders, delivery partner locations).

#### External APIs
- **Google Maps API**  
  Enables location services for restaurant search, delivery routing, and order tracking.

- **Payment Gateways**  
  Secure payment processing and refunds.

- **SMS Gateway**  
  Sends real-time notifications to customers and delivery agents.

---

### 3.6 Workflow Overview
1. **Customer places an order**
   - Browses menu, selects items, and completes the checkout process.
   - Backend creates an order and assigns it to a nearby restaurant.

2. **Restaurant prepares the order**
   - Updates the status to "ready for pickup."

3. **Delivery partner picks up the order**
   - Receives delivery request and navigates to the restaurant.

4. **Order is delivered**
   - Updates the status to "delivered," and payment is processed.

5. **Admin and analytics**
   - Admin dashboard monitors performance metrics and manages the system.

---

## 4. Module Design

### 4.1 Mobile/Web Application (Frontend)

#### 4.1.1 User Interface
Designed to be simple, intuitive, and responsive. Key components:
- Restaurant Search
- Menu Display
- Order Tracking
- Payment Screen
- User Profile Management

#### 4.1.2 Controller Layer
Handles customer, restaurant, and delivery partner requests and communicates with the service layer.

#### 4.1.3 Service Layer
Implements core business logic, such as order placement, payment processing, and notifications.

### Frontend Architecture  
![frontend architecture](https://github.com/user-attachments/assets/38b69204-26d9-40e2-9b89-c5b887d79921)


---

### 4.2 Backend System (Server-side)

#### 4.2.1 API Gateway
Serves as the single entry point for all requests, routing them to appropriate backend services.

#### 4.2.2 Authentication Service
Handles user login, registration, and account management.

#### 4.2.3 Order Management Service
- **Order Placement**: Links customers with restaurants.
- **Order Tracking**: Tracks order status in real-time.
- **Order Cancellation**: Handles customer-initiated cancellations.

#### 4.2.4 Payment Service
Manages payment transactions, maintains order payment history, and processes refunds.

#### 4.2.5 Notification Service
Sends notifications for order updates, promotions, and reminders.

---

### Backend Architecture  
![backend architecture](https://github.com/user-attachments/assets/6463618a-7567-491b-8564-f456afb40eab)

---

## 5. Database Design
- **Users**: Stores details of customers, restaurants, and delivery partners.
- **Orders**: Contains order-specific information, including status, payment, and delivery details.
- **Restaurants**: Stores menu items, restaurant details, and reviews.
- **Payments**: Maintains transaction records and payment statuses.

![Screenshot 2024-12-03 194425](https://github.com/user-attachments/assets/bdf4d4ad-01a4-42e3-bc28-0142f39a26d2)

---

## 6. Interface Design

### 6.1 API Design
- **Authentication:**
  - `POST /api/login`
  - `POST /api/register`

- **Order Management:**
  - `POST /api/orders`
  - `GET /api/orders/:id`

- **Restaurant Management:**
  - `GET /api/restaurants`
  - `POST /api/restaurants/menu`

- **Payment Processing:**
  - `POST /api/payments`
  - `GET /api/payments/status`

### API Design Diagram  
![API Design UML](https://github.com/user-attachments/assets/f4df1b2d-73c3-4476-9f02-9f217accbb8e)

---

### 6.2 External System Interfaces
- **Payment Gateways**: Processes payments and refunds.
- **Google Maps API**: Facilitates navigation and delivery tracking.
- **SMS Gateway**: Sends order status updates to users.

---

## 7. Conclusion
This Software Design Description for the Zomato platform ensures a robust, scalable, and secure food-ordering and delivery system. The modular architecture and external service integrations provide an efficient and seamless experience for customers, restaurants, and delivery partners alike.

### ChatGPT Prompt

> **Prompt 1:**  
> Generate a Software Design Description (SDD) for a food-ordering and delivery platform like Zomato. Include sections for introduction, system overview, frontend and backend architecture, module design, database design, API endpoints, and external service integration. Ensure the design supports scalability, real-time communication, and secure payment processing.  

---  

> **Prompt 2:**  
> Create a detailed module design for a platform like Zomato, focusing on the following modules: Authentication, Restaurant Management, Order Management, Payment Integration, and Notification Service. Provide a brief description, features, and the technologies involved for each module.  

---  

> **Prompt 3:**  
> Draft a database schema for a food delivery system similar to Zomato. Include key entities such as Users, Restaurants, Menu Items, Orders, Payments, and Reviews. Specify the relationships between these entities and provide an explanation of
