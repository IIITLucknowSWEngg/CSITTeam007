# 1. C4 Diagrams 🚀
## 1.1 System Context Diagram 🔥


<img width="1440" alt="Screenshot 2024-12-03 at 6 44 33 PM" src="https://github.com/user-attachments/assets/c5c8ff92-effb-40d2-b726-9dda1378ee15">

### Context Level:
This is depicted in the diagram. It illustrates the Zomato Clone Platform as the central system interacting with various external actors and systems:
#### Primary Actors:
Customers, Restaurant Owners, Delivery Partners, and Admins interact with the platform for different functionalities like browsing, managing menus, and delivery.
#### External Systems:
Services like Payment Gateways, CDNs, Map Services, Analytics, and Ad Networks support the platform through APIs or HTTPS.

## 1.2 Container Diagram 🔥
<img width="801" alt="Screenshot 2024-12-03 at 7 18 29 PM" src="https://github.com/user-attachments/assets/a86968fe-a05d-4178-8dba-1d666bf12dbf">

### *Containers:*

#### **Zomato Clone App**: 
- **Description**: Central application that handles browsing, ordering, and delivery tracking for customers.
- **Responsibilities**:
  - Displays restaurant menus and available dishes.
  - Allows customers to place orders and track delivery status.
  - Integrates with payment systems for seamless transactions.

#### **API Gateway**: 
- **Description**: Routes incoming requests from the front-end to the appropriate service (order, payment, restaurant, delivery).
- **Responsibilities**:
  - Manages API calls from customers and other system components.
  - Ensures proper routing of requests based on their type (order-related, payment, etc.).

#### **Order Service**: 
- **Description**: Manages the creation and management of customer orders.
- **Responsibilities**:
  - Handles the ordering process, including confirmation and status updates.
  - Tracks order details like items, customer info, and delivery instructions.

#### **Payment Service**: 
- **Description**: Processes payments via integrated third-party services.
- **Responsibilities**:
  - Handles payment processing using services like Stripe or PayPal.
  - Ensures secure payment transactions and confirms successful payments.

#### **Restaurant Service**: 
- **Description**: Manages restaurant menus and processes order confirmations.
- **Responsibilities**:
  - Handles restaurant menu management, updates, and synchronization.
  - Confirms orders placed by customers and triggers necessary actions for delivery.

#### **Delivery Service**: 
- **Description**: Coordinates deliveries and provides tracking features for delivery partners.
- **Responsibilities**:
  - Tracks delivery status and updates customers on the progress of their orders.
  - Coordinates with delivery partners for timely delivery.
  - Uses mapping services (e.g., Google Maps) for route optimization.
 
  - <img width="801" alt="Screenshot 2024-12-03 at 7 18 29 PM" src="https://github.com/IIITLucknowSWEngg/CSITTeam007/edit/main/Assignment2/DeployZomato.png">

#### **Analytics Service**:
- **Description**: Provides insights into user behavior to improve the platform.
- **Responsibilities**:
  - Tracks user activity and generates analytics for marketing, UX improvements, etc.
  - Monitors customer interactions, order patterns, and service usage.

#### **Zomato Database**: 
- **Description**: Stores data such as orders, menus, and user information.
- **Responsibilities**:
  - Acts as the central repository for all essential data (e.g., user accounts, menu items, orders, payment details).
  - Ensures data consistency and availability across all services.

 ## 1.3 Component Diagram 🔥

### 1.3.1 Customer feature:
 
<img width="819" alt="Screenshot 2024-12-03 at 7 56 40 PM" src="https://github.com/user-attachments/assets/118e7bc7-e06f-4968-9c60-78e331ce70a6">

#### Components:

1. **User Interface**: 
   - Interacts with various services such as authentication, search, and order services.
   
2. **Restaurant Interface**: 
   - Represents the service that allows restaurants to interact with the platform.
   
3. **Order Service**: 
   - Manages the user's order.
   - Communicates with the payment service to handle transactions.
   - Interacts with the restaurant service to notify the restaurant about new orders.
   
4. **Payment Service**: 
   - Handles the financial transactions during the ordering process, ensuring that payments are processed securely.

5. **Order Management**: 
   - Helps in managing the state and notifications related to orders.
   - Notifies both the user and restaurant about the order's status.

### 1.3.2 Restaurant Interface:





<img width="671" alt="Screenshot 2024-12-03 at 8 03 00 PM" src="https://github.com/user-attachments/assets/acbd9514-f73b-4feb-9363-4b23890f748d">

#### Components:

1. **Restaurant Interface**: 
   - Represents the service that allows restaurants to interact with the platform.
   - Handles restaurant-side functionalities like viewing orders and updating the status of orders.
   
2. **Restaurant Service**: 
   - Responsible for managing restaurant-specific data, such as menus and available food items.
   - Interacts with the search service to display restaurants to users and with the order service to notify about new orders.

3. **Order Management**: 
   - Helps in managing the state and notifications related to orders from restaurants.
   - Notifies the restaurant when a new order is placed and tracks the status of orders during their lifecycle.
  
### Delivery Excutive interface:

<img width="692" alt="Screenshot 2024-12-03 at 8 08 18 PM" src="https://github.com/user-attachments/assets/4d804316-df79-48a0-b245-8a83785288ea">

### Components:

1. **Delivery Partner Interface**: 
   - Represents the service that allows delivery partners to interact with the platform.
   - Handles delivery partner-specific functionalities like accepting orders, updating order status, and tracking delivery progress.
   
2. **Delivery Management Service**: 
   - Responsible for managing the state of deliveries, such as assigning orders to available delivery partners.
   - Updates the status of deliveries, including when they are in transit, delivered, or canceled.

3. **Order Management**: 
   - Helps in managing the state and notifications related to orders, including communicating with delivery partners to update them about new orders that need to be delivered.







 
 
 


