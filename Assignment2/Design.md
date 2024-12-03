# Zomato Project Design Documentation  

## Introduction  
This project aims to create a platform for users to discover restaurants, order food, and track deliveries in real time. It also provides tools for restaurants to manage their menu and orders, and delivery agents to fulfill orders efficiently.  

## Purpose  
The primary goal is to offer a seamless food delivery and restaurant discovery experience for users. It also focuses on scalability and ease of use for restaurants and delivery partners, ensuring all stakeholders benefit from the platform.  

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
### ER Diagram  
**Main Entities:**  
1. **Users**: `user_id`, `name`, `email`, `password`, `address`.  
2. **Restaurants**: `restaurant_id`, `name`, `location`, `cuisine`.  
3. **Menu_Items**: `item_id`, `restaurant_id`, `name`, `price`.  
4. **Orders**: `order_id`, `user_id`, `restaurant_id`, `status`.  

**Relationships:**  
- One-to-Many: Restaurants → Menu_Items.  
- One-to-Many: Users → Orders.  

---

## API Design Diagram  
### Key Endpoints  
1. **User Module:**  
   - `POST /users/register`  
   - `GET /users/profile`  
2. **Restaurant Module:**  
   - `GET /restaurants/search`  
   - `POST /restaurants/add-menu-item`  
3. **Order Module:**  
   - `POST /orders/create`  
   - `GET /orders/track`  

**Diagram:**  
```plaintext  
[Frontend (Web/Mobile)]  
    ↕  
[API Gateway]  
    ↕  
[Backend Services] -> [Database]  
