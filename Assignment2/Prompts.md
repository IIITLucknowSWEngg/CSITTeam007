# AI Usage Documentation

This document outlines how AI systems were utilized during the development of the **Zomato** project, detailing the prompts used to gather ideas, resolve challenges, and streamline various aspects of software development.

---

## Purpose of Using AI

1. **Feature Inspiration and Brainstorming**: Generating innovative features for the food delivery platform.
2. **Software Engineering Documentation**: Assisting with the creation of essential documents like SRS (Software Requirements Specification), URD (User Requirements Document), and stakeholder analysis.
3. **Complex Functional Implementations**: Implementing functionalities such as secure user authentication, real-time order tracking, and payment gateway integration.
4. **Code Optimization and Debugging**: Offering solutions for code optimization and bug fixing.
5. **Project Structuring and Task Prioritization**: Providing suggestions on project structure and task management.
6. **Diagram Design**: Creating UML diagrams for platform architecture and use cases.
7. **Testing and Quality Assurance**: Assisting in designing test cases and ensuring the platform meets quality standards.

---

## Prompts Used

### 1. Project Overview
- **Prompt**: "Suggest advanced features for a food delivery platform similar to Zomato."
- **AI Response**:
  - Personalized restaurant recommendations.
  - Real-time order tracking.
  - In-app chat support.
  - Loyalty and rewards program.
  - Integration with multiple payment gateways.
  - AI-powered food suggestions based on user preferences.

### 2. Stakeholders Document
- **Prompt**: "List potential stakeholders for a food delivery platform and their roles."
- **AI Response**:
  - **Primary Stakeholders**: End users (customers), Restaurant partners, Delivery personnel.
  - **Secondary Stakeholders**: Payment gateway providers, Platform administrators.
  - **Tertiary Stakeholders**: Advertisers, Technology partners, Investors.

### 3. User Requirements Document (URD)
- **Prompt**: "What user requirements should be included in a URD for a food delivery platform?"
- **AI Response**:
  - Users must register/login securely.
  - Users can browse restaurants with advanced filters (cuisine, location, price, etc.).
  - Users can track orders in real-time.
  - Support for multiple payment gateways.
  - Easy access to order history and receipts.
  - Users can provide ratings and reviews for restaurants and delivery personnel.

### 4. Software Requirements Specification (SRS)
- **Prompt**: "Provide a template and example for an SRS document tailored for a food delivery system."
- **AI Response**:
  - **Functional Requirements**: User authentication, Order management, Payment processing, Notification system.
  - **Non-Functional Requirements**: Scalability, multi-language support, high availability, security.
  - **Interfaces**: Web and mobile compatibility.

### 5. UML Diagrams
#### 5.1. Use Case Diagram
- **Prompt**: "Generate a use case diagram for a food delivery platform like Zomato."
- **AI Response**:
  - Diagram Syntax:
    ```text
    @startuml

    actor "User" as User
    actor "Restaurant" as Restaurant
    actor "Delivery Person" as DeliveryPerson
    actor "Admin" as Admin

    rectangle "Zomato Platform" as System {
        usecase "Browse Restaurants" as UC_Browse
        usecase "Place Order" as UC_Order
        usecase "Track Order" as UC_Track
        usecase "Manage Menu" as UC_Menu
        usecase "Deliver Order" as UC_Deliver
        usecase "Process Payment" as UC_Payment
        usecase "Handle Support" as UC_Support
        usecase "Manage Platform" as UC_Manage
    }

    User --> UC_Browse
    User --> UC_Order
    User --> UC_Track
    User --> UC_Payment
    User --> UC_Support

    Restaurant --> UC_Menu
    Restaurant --> UC_Order

    DeliveryPerson --> UC_Track
    DeliveryPerson --> UC_Deliver

    Admin --> UC_Manage
    Admin --> UC_Support

    @enduml
    ```

#### 5.2. Component Diagram
- **Prompt**: "Create a component diagram showing the core modules of a food delivery platform."
- **AI Response**:
  - Components:
    - **Frontend**: React-based UI for users.
    - **Backend**: Node.js API for managing orders and user data.
    - **Database**: MongoDB for restaurant and user data storage.
    - **Payment Gateway**: Integration module for multiple providers.
    - **Notification Service**: Real-time notifications for order updates.
    - **Admin Panel**: Dashboard for managing platform operations and analytics.

### 6. Testing and Quality Assurance
- **Prompt**: "Suggest test cases for a food delivery platform."
- **AI Response**:
  - **User Registration and Login**: Ensure users can register and log in securely.
  - **Order Placement**: Verify that orders can be placed and processed correctly.
  - **Payment Processing**: Test various payment methods for successful transactions.
  - **Order Tracking**: Check the accuracy of real-time order tracking.
  - **Notification System**: Ensure notifications are sent at appropriate stages.
  - **Platform Performance**: Test for scalability and response times under load.

### 7. Documentation Assistance
- **Prompt**: "How do I structure a software engineering project folder in GitHub?"
- **AI Response**:
  - **Root Directory**:
    - `README.md` (Project overview).
    - `docs/` (Documentation files like SRS, URD, etc.).
    - `src/` (Source code).
    - `tests/` (Unit and integration tests).

---

## Impact of AI

- **Time Saved**: AI significantly reduced the time needed for brainstorming, writing documentation, and designing diagrams.
- **Clarity**: The suggestions improved the structure and coverage of requirements and implementation plans.
- **Technical Support**: AI provided solutions for complex functionalities like real-time order tracking and secure payments.
- **Quality Assurance**: AI-assisted testing ensured the platform met high-quality standards before deployment.

---
