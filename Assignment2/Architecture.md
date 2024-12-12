# 1. C4 Diagrams 🚀
## 1.1 System Context Diagram 🔥


<img width="1440" alt="Screenshot 2024-12-03 at 6 44 33 PM" src="https://github.com/user-attachments/assets/c5c8ff92-effb-40d2-b726-9dda1378ee15">

### Context Level:
This is depicted in the diagram. It illustrates the Zomato Platform as the central system interacting with various external actors and systems:
#### Primary Actors:
Customers, Restaurant Owners, Delivery Partners, and Admins interact with the platform for different functionalities like browsing, managing menus, and delivery.
#### External Systems:
Services like Payment Gateways, CDNs, Map Services, Analytics, and Ad Networks support the platform through APIs or HTTPS.

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
<img width="801" alt="Screenshot 2024-12-03 at 8 09 18 PM" src="https://github.com/IIITLucknowSWEngg/CSITTeam007/blob/main/Assignment2/DeployZomato.png">


### Customer Device
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
  - Authenticate users and manage database operations.
  - Coordinate communication between customer and delivery modules.

### Customer Service Component
- **Functionality**:
  - Manage customer queries and complaints.
  - Enable customer feedback, reviews, and ratings.
  - Integrate live chat for real-time assistance.

### Order Processing Component
- **Functionality**:
  - Handle cart management, order placement, and checkout.
  - Process payments (credit card, wallet, COD).
  - Notify users of order confirmation and updates.

### Driver Management Component
- **Functionality**:
  - Assign delivery partners based on location and availability.
  - Track delivery progress and optimize routes.
  - Update customer on real-time delivery status.

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
    - Sending payment confirmations to customers and Zomato backend.
  - Ensures:
    - PCI-DSS compliance for secure data handling.
    - Encryption for sensitive information.

### Frontend Component
  - Provides an engaging and responsive user interface for customers, delivery partners, and restaurant admins.
- **Functionality**:
  - **Customer Interface**:
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
    - Accessibility support for diverse user needs.

### 1.4.1 Swimlane Diagram 
A swimlane diagram is a type of flowchart that organizes processes into lanes to show responsibilities and interactions between participants (teams, departments, or systems). Each lane represents a participant, and the steps are aligned in their respective lanes.

<img width="801" alt="Screenshot 2024-12-03 at 8 09 18 PM" src="https://github.com/user-attachments/assets/fa974e42-f78f-42e1-be00-d7c892ff26a3">

- **Flow Summary**:
1. Customer Interaction:

   - Customers interact with the app (via User Interface Package) to place orders.Orders are routed to the Order Processing Component through the backend.Payment is processed via the Payment Gateway.

2. Restaurant Admin:

   - Admins manage orders and update menus using their respective components.

3. Delivery Workflow:

   - Delivery personnel receive orders and navigate via the Delivery Device, which is updated by Google Maps API and the Driver Management Component.

4. Backend Centralization:

   - All components communicate via the Zomato Backend Server.

CODE:
```
@startuml
|Customer|
start
:Place Order;
:Payment Process;
|Backend Server|
:Validate Order;
:Fetch Data from Customer Database;
:Send Confirmation;
|Order Processing|
:Process Order;
|Admin|
:Update Restaurant Database;
|Driver Management|
:Assign Delivery Person;
|Delivery Person|
:Receive Order Details;
:Navigate using Google Maps API;
:Deliver Order;
stop
@enduml
```



### Additional Insights:  
- **Security Measures**: The system ensures end-to-end encryption for sensitive data like payment details and user credentials to prevent unauthorized access.  
- **Scalability**: Designed with a microservices architecture, the platform supports horizontal scaling to handle a growing user base efficiently.  
- **Performance Optimization**: Incorporates caching mechanisms and CDNs to deliver a seamless user experience with minimal latency.
 
 
 


