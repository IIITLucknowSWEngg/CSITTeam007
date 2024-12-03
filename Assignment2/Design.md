# Zomato Project Design Documentation  

## Introduction  

## Purpose  
This project intends to deliver a seamless food-ordering and delivery experience for users while supporting restaurants and delivery agents with robust tools to optimize operations.  

## Scope  
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

## Database Design  
![Screenshot 2024-12-03 194425](https://github.com/user-attachments/assets/bdf4d4ad-01a4-42e3-bc28-0142f39a26d2)


**Relationships:**  
- One-to-Many: Restaurants → Menu_Items.  
- One
-to-Many: Users → Orders.  

---

## API Design Diagram  
### Key Endpoints  
![api endpoints](https://github.com/user-attachments/assets/f4df1b2d-73c3-4476-9f02-9f217accbb8e)
