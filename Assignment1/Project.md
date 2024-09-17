# Zomato Clone Project

## Overview

| Section            | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| **Project Name**    | Zomato Clone                                                               |
| **Objective**       | A food delivery web and mobile app, similar to Zomato.                     |
| **Users**           | General users (customers), restaurant owners, admin                        |

---

## Features

| Feature Category       | Features                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------|
| **User Features**       | - User Authentication <br> - Restaurant Search <br> - Menu Browsing <br> - Order Placement <br> - Order Tracking <br> - Review & Rating |
| **Restaurant Features** | - Restaurant Registration <br> - Menu Management <br> - Order Management <br> - Analytics Dashboard |
| **Admin Features**      | - User Management <br> - Restaurant Management <br> - Order Monitoring <br> - Reports & Analytics |

---

## Tech Stack

| Layer             | Technologies                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------|
| **Frontend**       | React.js, React Native, Redux, Tailwind CSS/Bootstrap                                                     |
| **Backend**        | Node.js, Express.js, MongoDB, Firebase                                                                    |
| **Tools**          | Stripe, Google Maps API, AWS S3, Socket.IO                                                                |

---

## Setup Instructions

| Step               | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| **1. Clone Repo**   | `git clone https://github.com/username/zomato-clone.git`                   |
| **2. Install Backend** | `npm install`                                                            |
| **3. Install Frontend** | `cd client && npm install`                                              |
| **4. Configure Env** | Set environment variables in `.env`                                        |
| **5. Start Backend** | `npm run server`                                                           |
| **6. Start Frontend** | `cd client && npm start`                                                  |

---

## Usage Guide

| Task                   | URL/Action                                                      |
|------------------------|-----------------------------------------------------------------|
| **User Registration**   | `/signup`                                                      |
| **Explore Restaurants** | Use search bar on homepage                                     |
| **Place an Order**      | Browse menu, add to cart, and checkout                         |
| **Track Order**         | Real-time updates from confirmation to delivery                |
| **Restaurant Dashboard**| Manage menus, view orders, update order status                 |

---
## API Documentation

| Endpoint               | Description                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| *POST /auth/register* | Register a new user.                                                                            |
| *POST /auth/login*    | Authenticate a user.                                                                            |
| *GET /restaurants*    | Get a list of restaurants.                                                                      |
| *GET /restaurants/:id*| Get detailed info of a specific restaurant.                                                     |
| *POST /orders*        | Place a new order.                                                                              |
| *GET /orders/:id*     | Get order details.                                                                              |

---

## Database Schema

| Collection           | Structure                                                                                          |
|----------------------|---------------------------------------------------------------------------------------------------|
| *User Collection*   | { "_id": "ObjectId", "name": "string", "email": "string", "password": "string", "role": "string", "orders": ["OrderId"], "created_at": "Date" } |
| *Restaurant Collection* | { "_id": "ObjectId", "name": "string", "location": "string", "menu": ["MenuItemId"], "owner": "UserId", "created_at": "Date" } |
| *Order Collection*  | { "_id": "ObjectId", "user": "UserId", "restaurant": "RestaurantId", "items": ["MenuItemId"], "total": "number", "status": "string", "created_at": "Date" } |

---

## Contributing

| Step                   | Description                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| *1. Fork Repo*        | Fork the repository.                                                                            |
| *2. Create Branch*    | Create a new branch for your feature/bugfix.                                                    |
| *3. Commit Changes*   | Commit your changes.                                                                            |
| *4. Submit PR*        | Submit a pull request with a detailed description of changes.                                   |

---

## License

| License               | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| *MIT License*        | The project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details. |

---

## Contact

| Role                  | Contact Information                                                       |
|-----------------------|---------------------------------------------------------------------------|
| *Project Maintainer* | email@example.com                                                      |
