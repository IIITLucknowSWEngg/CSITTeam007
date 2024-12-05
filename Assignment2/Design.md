# Zomato Project Design Documentation

## Introduction  

### Purpose  
This project intends to deliver a seamless food-ordering and delivery experience for users while supporting restaurants and delivery agents with robust tools to optimize operations.

### Scope  
The Zomato clone system enables users to request, order, and pay for food via a mobile app and web app. Restaurants are able to offer services through the same platform. The system includes:  
- Mobile application and web application interfaces.  
- Backend API services.  
- Payment processing integration.  
- Real-time communication.  
- External integrations with services like maps and SMS gateways.

---

## Frontend Design  

### Web  
- **Framework:** React.js  
- **Features:**  
  - Restaurant search and filtering.  
  - Menu display and ordering.  
  - Real-time order tracking.  
  - User profile management.  

### Mobile  
- **Framework:** Flutter  
- **Features:**  
  - Location-based restaurant suggestions.  
  - Interactive maps for delivery tracking.  
  - Push notifications for order status updates.  
  - Intuitive UI for easy navigation.

---

## Backend Design  

### Web  
- **Framework:** Node.js (Express.js)  
- **Services:**  
  - Authentication (JWT-based).  
  - Search and filter restaurants.  
  - Order management and status updates.  

### Mobile  
- **Framework:** Django REST Framework  
- **Services:**  
  - User-specific data (preferences, past orders).  
  - Real-time notifications (via Firebase or Kafka).  
  - API integration with 3rd-party delivery systems.  

---

## Module Design  

### Overview  
The module design describes how the different components of the system interact to form the complete solution. These modules cover both the frontend and backend systems and their interdependencies.

### Frontend Modules  
The frontend is designed to be modular, each responsible for a specific feature of the application.  

1. **Restaurant Module**  
   - **Features:** Search restaurants, display restaurant menu, order food.  
   - **Technology:** React.js, Redux for state management.

2. **User Module**  
   - **Features:** Manage user profile, preferences, order history.  
   - **Technology:** React.js, Redux for user state management.  

3. **Order Module**  
   - **Features:** Add items to the cart, proceed to checkout, track order status.  
   - **Technology:** React.js, Redux for order state management.

4. **Payment Module**  
   - **Features:** Handle payment transactions via different methods (Card, UPI, Wallet).  
   - **Technology:** React.js, integrate with Payment Gateway API.

### Frontend Architecture  
![frontend architecture](https://github.com/user-attachments/assets/38b69204-26d9-40e2-9b89-c5b887d79921)

### Backend Modules  
The backend consists of several services that manage business logic, data processing, and interaction with external services.  

1. **Authentication Module**  
   - **Features:** User registration, login, JWT token management.  
   - **Technology:** Node.js, Express.js.

2. **Restaurant Management Module**  
   - **Features:** Restaurant registration, menu management, order management.  
   - **Technology:** Node.js, Express.js, MongoDB.

3. **Order Management Module**  
   - **Features:** Process orders, update status, handle cancellations.  
   - **Technology:** Node.js, Express.js, MongoDB.

4. **Payment Gateway Integration Module**  
   - **Features:** Process payments, handle different payment methods, update transaction status.  
   - **Technology:** Node.js, integrate with Payment Gateway API (e.g., Razorpay, Stripe).

5. **Notification Module**  
   - **Features:** Send real-time notifications to users for order updates, restaurant offers.  
   - **Technology:** Firebase or Kafka for real-time notifications.

### Backend Architecture  
![backend architecture](https://github.com/user-attachments/assets/6463618a-7567-491b-8564-f456afb40eab)

---

## Database Design  
![Screenshot 2024-12-03 194425](https://github.com/user-attachments/assets/bdf4d4ad-01a4-42e3-bc28-0142f39a26d2)

**Relationships:**  
- One-to-Many: Restaurants → Menu_Items.  
- One-to-Many: Users → Orders.  

---

## API Design  

### Overview  
APIs facilitate communication between the frontend, backend, and third-party services. They are organized around REST principles for simplicity and consistency.  

### Key Endpoints  
1. **Authentication Service:**  
   - `POST /api/login` - User authentication.  
   - `POST /api/register` - User registration.  

2. **Restaurant Management:**  
   - `GET /api/restaurants` - Fetch a list of restaurants.  
   - `POST /api/restaurants` - Add a new restaurant.  

3. **Order Management:**  
   - `POST /api/orders` - Create a new order.  
   - `GET /api/orders/:id` - Get order details.  

4. **Payment Service:**  
   - `POST /api/payment` - Initiate a payment.  
   - `GET /api/payment/status` - Check payment status.  

### API Design Diagram  
![API Design UML](https://github.com/user-attachments/assets/f4df1b2d-73c3-4476-9f02-9f217accbb8e)

---

## Non-Functional Requirements  

- **Scalability:** The app should handle a large number of concurrent users and orders.  
- **Performance:** The app should have low latency, with fast loading times and smooth interactions.  
- **Security:** User data, particularly payment information, must be securely handled and stored.  
- **Reliability:** The app should have high availability, with minimal downtime and robust error handling.  
- **Usability:** The app should be user-friendly, with an intuitive interface and easy navigation.  
- **Compliance:** The app must comply with relevant regulations (e.g., PCI-DSS for payment processing).  

---

## Conclusion  

This Software Design Description outlines the architecture, modules, database, and interfaces for the Zomato-like food delivery system, ensuring the application is robust, scalable, and secure. The use of modular design and external system integration ensures that the system is capable of efficiently handling a large number of users, restaurants, and orders, while providing a seamless and reliable user experience.

---
