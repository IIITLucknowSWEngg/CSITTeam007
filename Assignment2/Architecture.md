# C4 Diagrams 🚀

## 1.1 System Context Diagram 🔥

### Diner App
![Diner App Context Diagram](https://github.com/user-attachments/assets/da05f862-e253-4f7e-885f-cd5f3c31fd46)
**Description**: The Diner App enables customers to browse menus, place orders, and make payments. It offers features like personalized recommendations, real-time delivery tracking, and user reviews.


### Restaurant App
![Restaurant App Context Diagram](https://github.com/user-attachments/assets/a99fe2ac-0a70-4920-abd7-d4ae1b606b64)
**Description**: The Restaurant App helps restaurant owners manage their menus, update availability, process incoming orders, and view performance analytics.


### Delivery Executive App
![Delivery Executive Context Diagram](https://github.com/user-attachments/assets/23b27071-7a2d-4458-bec2-42051b87da0c)
**Description**: The Delivery Executive App allows delivery partners to accept delivery requests, navigate through GPS-based routing, and update delivery statuses in real-time.


### Admin App
![Admin App Context Diagram](https://github.com/user-attachments/assets/884f140f-ba7d-429e-bbe6-37dcff2a5d2e)
**Description**: The Admin App provides tools for platform administrators to monitor system operations, handle escalations, and oversee user management and platform analytics.


### Context Level Description
The **System Context Diagram** illustrates the Zomato platform as the central system interacting with various external actors and systems.

#### Primary Actors
1. **Diners**: Browse, order, and make payments for food deliveries.  
2. **Restaurant Owners**: Manage menus, orders, and restaurant profiles.  
3. **Delivery Partners**: Accept and deliver orders with GPS support.  
4. **Admins**: Manage platform operations and monitor performance.

#### External Systems  
- **Payment Gateways** (e.g., Razorpay, PayPal): For secure payments.  
- **Map Services (GPS APIs)**: For real-time delivery tracking.  
- **Notification Services**: Send alerts to users (SMS, email, app push notifications).  
- **Analytics Services**: Provide insights into business performance.  
- **Ad Networks & CDNs**: Optimize app performance and advertisements.  

---
## 1.2 Container Diagram 🔥


### 1.2.1 Diner App :

<img width="904" alt="Screenshot 2024-12-12 at 1 34 41 PM" src="https://github.com/user-attachments/assets/24ba4fbc-8682-424b-8e7e-f2082243498c" />



This diagram shows the high-level architecture of the **Diner App** and its interactions with core backend services.

##### Components:

- **Diner App**: The mobile application used by diners to browse restaurants, place orders, and make payments. It interacts with backend services through API calls.
  
- **API Gateway**: The entry point for all requests from the Diner App. It routes requests to the appropriate backend services such as order management and payment processing.

- **Order Service**: Handles all operations related to managing diner orders, including creating new orders, updating their status, and tracking progress until delivery.

- **Payment Service**: Manages all payment transactions, processing payments through various external gateways like GPay, PayPal, or others. It ensures secure payment handling and stores payment-related data.

- **Restaurant Service**: Manages restaurant-specific data such as menus, order confirmation, and restaurant profiles. It interacts with both the Zomato database and external services.

- **Zomato Database**: A central database that stores and manages all application data, including diner orders, payment transactions, restaurant details, and customer profiles.

### 1.2.2 Restaurant Owner 

<img width="638" alt="Screenshot 2024-12-12 at 1 53 06 PM" src="https://github.com/user-attachments/assets/9299e2d3-164b-40f7-bfd3-9b07a86dd003" />


This diagram depicts the architecture for the **Restaurant Owner** system. It includes the following components:

- **Restaurant Owner App**: Mobile/web app for restaurant management.
- **API Gateway**: Routes requests from the app to backend services.
- **Order Service**: Manages orders.
- **Restaurant Service**: Handles restaurant operations (menu, orders).
- **Payment Service**: Processes payments via external gateways (e.g., GPay, PayPal).
- **Analytics Service**: Provides insights on restaurant performance.
- **Zomato Database**: Stores all data (orders, restaurant details).
- **Payment Gateway**: External payment processor.

The app communicates with backend services through the **API Gateway**, and data is managed in the **Zomato Database**.

### 1.2.3 Delivery Executive :

<img width="705" alt="Screenshot 2024-12-12 at 1 59 59 PM" src="https://github.com/user-attachments/assets/87ba2603-c99e-4279-8316-25aea44f96f4" />


This diagram illustrates the architecture of the **Delivery Executive** system, including the following components:

- **Delivery Executive App**: Mobile app used by delivery executives to manage orders and deliveries.
- **API Gateway**: Routes requests from the app to backend services.
- **Order Service**: Manages order details and updates.
- **Delivery Service**: Handles delivery assignments and tracking.
- **Zomato Database**: Stores all data (orders, deliveries, payments).
- **Analytics Service**: Provides delivery-related performance insights.
- **Payment Gateway**: External service for processing payments.

The app communicates with the backend through the **API Gateway**, with data managed in the **Zomato Database**.



---


 



 ## 1.3 Component Diagram 🔥

### 1.3.1 Diner feature:
 
<img width="819" alt="Screenshot 2024-12-03 at 7 56 40 PM" src="https://github.com/user-attachments/assets/118e7bc7-e06f-4968-9c60-78e331ce70a6">

#### Components:

1. **Diner Interface**: 
   - Interacts with various services such as authentication, search, and order services.
   
2. **Restaurant Interface**: 
   - Represents the service that allows restaurants to interact with the platform.
   
3. **Order Service**: 
   - Manages the Diner's order.
   - Communicates with the payment service to handle transactions.
   - Interacts with the restaurant service to notify the restaurant about new orders.
   
4. **Payment Service**: 
   - Handles the financial transactions during the ordering process, ensuring that payments are processed securely.

5. **Order Management**: 
   - Helps in managing the state and notifications related to orders.
   - Notifies both the Diner and restaurant about the order's status.

### 1.3.2 Restaurant Interface:





<img width="671" alt="Screenshot 2024-12-03 at 8 03 00 PM" src="https://github.com/user-attachments/assets/acbd9514-f73b-4feb-9363-4b23890f748d">

#### Components:

1. **Restaurant Interface**: 
   - Represents the service that allows restaurants to interact with the platform.
   - Handles restaurant-side functionalities like viewing orders and updating the status of orders.
   
2. **Restaurant Service**: 
   - Responsible for managing restaurant-specific data, such as menus and available food items.
   - Interacts with the search service to display restaurants to Diners and with the order service to notify about new orders.

3. **Order Management**: 
   - Helps in managing the state and notifications related to orders from restaurants.
   - Notifies the restaurant when a new order is placed and tracks the status of orders during their lifecycle.
  
### 1.3.3 Delivery Excutive interface:

<img width="692" alt="Screenshot 2024-12-03 at 8 08 18 PM" src="https://github.com/user-attachments/assets/4d804316-df79-48a0-b245-8a83785288ea">

#### Components:

1. **Delivery Partner Interface**: 
   - Represents the service that allows delivery partners to interact with the platform.
   - Handles delivery partner-specific functionalities like accepting orders, updating order status, and tracking delivery progress.
   
2. **Delivery Management Service**: 
   - Responsible for managing the state of deliveries, such as assigning orders to available delivery partners.
   - Updates the status of deliveries, including when they are in transit, delivered, or canceled.

3. **Order Management**: 
   - Helps in managing the state and notifications related to orders, including communicating with delivery partners to update them about new orders that need to be delivered.


## 1.4 Deployment Diagram 🚀
![Deployment3](https://github.com/user-attachments/assets/abbc54b5-fccb-43f9-ab12-cd6aef569a07)

  
### Diner's Device

- **Functionality**:
  - Access the Zomato app or website.
  - Browse restaurants, menus, and offers.
  - Place orders and track deliveries.

### Delivery Person Device
- **Functionality**:
  - Accept and manage order deliveries.
  - Track delivery routes with GPS.
  - Update delivery status in real-time.

### Zomato Backend Server
- **Functionality**:
  - Process API requests and handle business logic.
  - Authenticate Diners and manage database operations.
  - Coordinate communication between Diner and delivery modules.

### Diner Service Component
- **Functionality**:
  - Manage Diner queries and complaints.
  - Enable Diner feedback, reviews, and ratings.
  - Integrate live chat for real-time assistance.

### Order Processing Component
- **Functionality**:
  - Handle cart management, order placement, and checkout.
  - Process payments (credit card, wallet, COD).
  - Notify Diners of order confirmation and updates.

### Driver Management Component
- **Functionality**:
  - Assign delivery partners based on location and availability.
  - Track delivery progress and optimize routes.
  - Update Diner on real-time delivery status.

### Restaurant Database Admin
- **Functionality**:
  - Maintain restaurant details and menu updates.
  - Manage restaurant-side order processing.
  - Provide analytics on restaurant performance and sales trends.

### Payment Gateway Component
- **Functionality**:
  - Integrates with multiple payment providers like Razorpay, PayPal, and Stripe.
  - Supports various payment methods: 
    - Credit/Debit Cards
    - Wallets
    - UPI
    - Net Banking
  - Manages:
    - Payment authorization and verification.
    - Refunds and failed transaction handling.
    - Sending payment confirmations to Diners and Zomato backend.
  - Ensures:
    - PCI-DSS compliance for secure data handling.
    - Encryption for sensitive information.

### Frontend Component
  - Provides an engaging and responsive Diner interface for Diners, delivery partners, and restaurant admins.
- **Functionality**:
  - **Diner Interface**:
    - Browse restaurants, menus, and offers.
    - Place orders and track delivery in real-time.
  - **Delivery Partner Interface**:
    - View assigned orders and routes.
    - Update delivery statuses (e.g., order picked, delivered).
  - **Restaurant Admin Interface**:
    - Manage menu details, order acceptance, and reports.
  - **General Features**:
    - Real-time updates via WebSockets or APIs.
    - Cross-platform compatibility (Web, Android, iOS).
    - Responsive design for all device types (mobile, tablet, desktop).
    - Accessibility support for diverse Diner needs.




### Additional Insights:  
- **Security Measures**: The system ensures end-to-end encryption for sensitive data like payment details and Diner credentials to prevent unauthorized access.  
- **Scalability**: Designed with a microservices architecture, the platform supports horizontal scaling to handle a growing Diner base efficiently.  
- **Performance Optimization**: Incorporates caching mechanisms and CDNs to deliver a seamless Diner experience with minimal latency.
 
 
 


