# **Software Requirements Specification (SRS) Document**

## **1. Introduction**

### **1.1 Purpose**
This Software Requirements Specification (SRS) document provides a comprehensive overview of the requirements for the Zomato clone application. It includes both functional and non-functional requirements, serving as a guideline for developers, testers, and stakeholders throughout the software development lifecycle.

### **1.2 Scope**
The Zomato clone application is a food delivery and restaurant discovery platform that enables users to order food and connect with restaurants and delivery personnel. The system will handle user registration, order management, payment processing, and real-time tracking. This SRS covers all aspects of the application, including user interfaces, functional and non-functional requirements, and external interface requirements.

### **1.3 Definitions, Acronyms, and Abbreviations**
- **SRS**: Software Requirements Specification  
- **NFR**: Non-Functional Requirement  
- **UI**: User Interface  
- **API**: Application Programming Interface  
- **GPS**: Global Positioning System  

### **1.4 References**
- IEEE Std 830-1998, IEEE Recommended Practice for Software Requirements Specifications  
- SWEBOK v3.0, Software Engineering Body of Knowledge
- [Stakeholders.md](https://github.com/IIITLucknowSWEngg/CSITTeam007/blob/main/Assignment1/Stakeholder.md) 
- [User Requirements Document](https://github.com/IIITLucknowSWEngg/CSITTeam007/blob/main/Assignment1/URD.md)  

### **1.5 Overview**
This document is organized into several sections that describe the overall system, functional requirements, non-functional requirements, and other considerations relevant to the development and implementation of the Zomato clone application.

---

## **2. Overall Description**

### **2.1 Product Perspective**
The Zomato clone application is an independent system designed to operate on mobile devices and web platforms. It interfaces with external systems such as payment gateways, GPS services, and third-party APIs for map integration. The system will use a modular architecture to facilitate scalability and maintainability.

### **2.2 Product Functions**
- User registration and authentication.  
- Food and restaurant discovery.  
- Order placement and tracking.  
- Real-time delivery tracking.  
- Payment processing and history tracking.  
- Ratings and reviews system.  

### **2.3 User Classes and Characteristics**
- **Customers**: Individuals using the app to browse and order food.  
- **Delivery Partners**: Individuals using the app to fulfill delivery requests.  
- **Restaurant Partners**: Businesses managing menus, orders, and availability.  
- **Admins**: Individuals managing the platform, overseeing user and restaurant activities.

### **2.4 Operating Environment**
The application will operate on Android and iOS mobile platforms, as well as web browsers. It will require internet connectivity for real-time functionalities like food ordering, payment processing, and GPS tracking. The backend will be hosted on cloud servers with high availability and reliability.

### **2.5 Design and Implementation Constraints**
- Must comply with data protection regulations (e.g., GDPR).  
- Limited by the performance and capabilities of mobile devices.  
- Dependency on third-party services for payments and GPS tracking.  

### **2.6 Assumptions and Dependencies**
- Users have access to smartphones with stable internet connections.  
- Integration with third-party services is stable and reliable.  
- The application will initially support one currency and language.  

---

## **3. System Features**

### **3.1 User Registration and Authentication**
**Description:** Users can register using email or phone numbers. The system supports secure login and password recovery.

**Functional Requirements:**  
- The system shall allow users to register with an email or phone number.  
- The system shall send a verification code to the user for account activation.  
- The system shall support password recovery via email or SMS.  

---

### **3.2 Food Browsing and Ordering**
**Description:** Customers can browse restaurants and place orders. Restaurants manage their menu and availability.

**Functional Requirements:**  
- The system shall allow users to search for restaurants by cuisine, rating, or price range.  
- The system shall enable users to add items to a cart and place an order.  
- The system shall notify the restaurant of a new order.  
- The system shall allow users to cancel orders before preparation starts.  

---

### **3.3 Payment Processing**
**Description:** The system processes payments through various methods and records payment history.

**Functional Requirements:**  
- The system shall allow users to choose a payment method (credit/debit card, in-app wallet, or cash).  
- The system shall automatically charge users after order placement.  
- The system shall maintain a payment history for users, restaurants, and delivery partners.  

---

### **3.4 Real-Time Order Tracking**
**Description:** Users can track the order status in real-time.

**Functional Requirements:**  
- The system shall display the order status (e.g., accepted, prepared, out for delivery).  
- The system shall allow users to track the delivery partner’s location in real-time.  

---

### **3.5 Ratings and Reviews**
**Description:** Customers can rate and review restaurants and delivery partners after each order.

**Functional Requirements:**  
- The system shall allow customers to leave ratings and reviews for restaurants and delivery partners.  
- The system shall allow delivery partners and restaurants to view their ratings and reviews.  

---

## **4. External Interface Requirements**

### **4.1 User Interface Requirements**
- **Mobile Application**: Intuitive and responsive UI, optimized for different screen sizes.  
- **Web Application**: Dashboard for admin and restaurant partners to manage operations.


### **4.1.1 Search and Discovery**  
- **Features**:  
  - Prominent search bar with auto-suggestions.  
  - Filters for cuisine, location, and ratings.  
  - Infinite scroll or pagination for results.  

---

### **4.1.2 Restaurant Pages**  
- **Features**:  
  - Display restaurant details (photos, ratings, menu, hours).  
  - Clear pricing and availability of dishes.  
  - Buttons for adding items to the cart or viewing more details.  

---

### **4.1.3 Cart and Checkout**  
- **Features**:  
  - Editable cart with clear item breakdowns.  
  - Multiple payment methods and promo code application.  
  - Order confirmation screen with tracking link.  

---

### **4.1.4 Delivery Tracking**  
- **Features**:  
  - Real-time map updates for order status.  
  - Notifications for each status change (picked up, on the way, delivered).  

---

### **4.1.5 Admin Dashboard**  
- **Features**:  
  - Overview of platform metrics (orders, revenue, user activity).  
  - Tools for resolving disputes and monitoring performance.  
  - Exportable reports for analysis.  

---

### **4.1.6 Restaurant Partner Dashboard**  
- **Features**:  
  - Menu and pricing management.  
  - Real-time order updates.  
  - Sales performance graphs and metrics.  

---

### **4.2 Hardware Interfaces**
- **GPS Modules**: For tracking delivery partner locations.  
- **Cameras**: For uploading profile pictures.  

---

### **4.3 Software Interfaces**
- **Third-Party APIs**: Integration for payment processing, SMS notifications, and map services.  
- **Database**: A NoSQL database (e.g., MongoDB) for storing user and order data.  

---

### **4.4 Communication Interfaces**
- HTTPS for secure communication.  
- WebSocket for real-time notifications.  

---


## **5. Non-Functional Requirements**

### **5.1 Performance Requirements**
- The application shall load within 2 seconds under normal conditions.  
- The system shall handle up to 10,000 concurrent users without performance degradation.  

---

### **5.2 Security Requirements**
- Data shall be encrypted in transit (TLS) and at rest (AES-256).  
- The system shall enforce strong password policies and support multi-factor authentication.  

---

### **5.3 Availability and Reliability**
- The system shall achieve 99.9% uptime.  
- Data backups shall be performed daily.  

---

### **5.4 Scalability**
- The system architecture shall support horizontal scaling.  

---

### **5.5 Usability**
- The app shall follow WCAG 2.1 accessibility guidelines.  

---

## **6. Other Requirements**
- **Localization**: Support for multiple languages and currencies.  

---

## **7. Appendices**

### **Appendix A: Glossary of Terms**
- **ETA**: Estimated Time of Arrival  
- **NFR**: Non-Functional Requirements  

### **Appendix B: Diagrams**

Below are the diagrams representing the system's interactions and workflows.

#### **Use Case Diagram**  
The Use Case Diagram illustrates the main interactions between key actors (Customers, Restaurants, Delivery Partners, and Admins) and the system.  

![Use Case Diagram](https://github.com/IIITLucknowSWEngg/CSITTeam007/blob/main/Assignment2/HappyPath.jpg)

---

#### **Abuse Case Diagram**  
The Abuse Case Diagram identifies potential vulnerabilities in the system, such as fraudulent activities or unauthorized access attempts, and how they are mitigated.  

![Abuse Case Diagram](https://github.com/IIITLucknowSWEngg/CSITTeam007/blob/main/Assignment2/AbuseCase.jpg)

---

#### **Error Case Diagram**  
The Error Case Diagram highlights common error scenarios, such as payment failures or order cancellation issues, and describes how the system addresses these errors.  

![Error Case Diagram](https://github.com/IIITLucknowSWEngg/CSITTeam007/blob/main/Assignment2/ErrorCase.jpg)

---

### **Appendix C: Cross Reference Matrix**

The detailed Cross Reference Matrix is available in the following file : 
[CrossReferenceMatrix.md](https://github.com/IIITLucknowSWEngg/CSITTeam007/blob/main/Assignment2/CrossReferenceMatrix.md)    
