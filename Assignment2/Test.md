# Test Plan for Zomato Clone

## 1. Introduction
- The Zomato Clone is a platform connecting users with restaurants and delivery services.
- This document outlines the testing methodology to ensure quality.

---

## 2. Scope
### Components to Test:
- **Customer Module**: Registration, login, profile management, search, and favorites.
- **Restaurant Module**: Menu display, reviews, and ratings.
- **Order Management Module**: Placement, modification, and payment processing.
- **Delivery Module**: Assign orders and track deliveries.
- **Admin Module**: Manage restaurants, menus, and view reports.
- **Third-Party Integrations**: Google Maps API, notification services.

---

## 3. Modules Overview

### **1. Customer Module**
- **Features**:
  - Registration/Login: Account creation and secure login.
  - Profile Management: Update and view customer details.
  - Search: Find restaurants, cuisines, or dishes.
  - Favorites: Save favorite restaurants and dishes.

### **2. Restaurant Module**
- **Features**:
  - Menu Display: View dishes, descriptions, and prices.
  - Reviews and Ratings: Submit and view restaurant feedback.
  - Restaurant Info: Address, hours of operation, and contact details.

### **3. Order Management Module**
- **Features**:
  - Cart: Add, edit, or remove items.
  - Order Placement: Finalize and submit orders.
  - Payment Gateway: Secure payments via multiple modes.
  - Order History: View past orders and receipts.

### **4. Delivery Module**
- **Features**:
  - Assign Driver: Allocate orders to delivery personnel.
  - Real-Time Tracking: Track delivery progress.
  - Delivery Confirmation: Mark orders as delivered.

### **5. Admin Module**
- **Features**:
  - Restaurant Management: Add/update restaurant details and menus.
  - Order Monitoring: Track and manage active orders.
  - Reports: Analytics on orders, users, and revenue.

---

## 4. Objectives
- Validate functionality across all modules.
- Ensure data security, especially in payment processes.
- Test performance under high customer traffic.
- Verify customer experience on different devices.

---

## 5. Testing Strategy
### Types of Testing:
- **Unit Testing**: Individual components like login or menu display.
- **Integration Testing**: Interaction between modules, e.g., customer orders with restaurants.
- **System Testing**: Full system compliance with requirements.
- **Performance Testing**: Load testing with high traffic (e.g., 10,000 users).
- **Security Testing**: Vulnerability checks like SQL injection and authentication.
- **Usability Testing**: Ensure seamless customer experience.

---

## 6. Test Environment
- **Hardware**:
  - Customer Devices: Mobile (Android/iOS), Desktop.
  - Server: 16-core CPU, 32 GB RAM, SSD storage.

- **Software**:
  - Frontend: React/Angular.
  - Backend: Node.js or Django/Flask.
  - Database: MongoDB or PostgreSQL.

- **Configuration**:
  - Staging server mirroring production data.
  - Mock APIs for early testing.

---

## 7. Test Cases
# Feature: Customer Login

### *Scenario: Customer logs in with valid credentials*

#### Given:
The customer is on the login page.

#### When:
The customer enters valid credentials (email, password).

#### Then:
The customer should be successfully logged in.  
The customer should be redirected to the homepage.

## Chai.js Code:

```javascript
const chai = require('chai');
const expect = chai.expect;
const loginPage = require('../pages/loginPage'); 

describe('Customer Login', function() {
  it('should login customer successfully', function() {
    
    loginPage.open();
    
    loginPage.enterCredentials('validemail@domain.com', 'validPassword123');

    loginPage.submitLogin();

    expect(loginPage.getWelcomeMessage()).to.include('Welcome, Customer');

    expect(browser.getUrl()).to.include('/home');
  });
});
```

# Feature: Restaurant Search

### **Scenario: User searches for restaurants by location**

#### **Given:**
- The user is logged in and on the homepage.

#### **When:**
- The user enters a valid location (e.g., "New York") in the search bar.

#### **Then:**
- The user should see a list of relevant restaurants based in New York.


## Chai.js Code:

```javascript
const chai = require('chai');
const expect = chai.expect;
const searchPage = require('../pages/searchPage');

describe('Restaurant Search', function() {
  it('should display relevant restaurants for New York', function() {
    
    searchPage.open();
   
    searchPage.enterSearchQuery('New York');

    searchPage.submitSearch();

    expect(searchPage.getResultsCount()).to.be.greaterThan(0);

    expect(searchPage.getResultTitles()).to.include('Restaurant');
  });
});
```
# Feature: View Menu
---

### *Scenario: User views the menu of a specific restaurant*

#### *Given:*
- The user is logged in and on the restaurant’s page.

#### *When:*
- The user selects a restaurant and views the menu.

#### *Then:*
- The user should see the list of menu items with their details.


## *Chai.js Code:*
---

javascript
const chai = require('chai');
const expect = chai.expect;
const restaurantPage = require('../pages/restaurantPage'); 
object

describe('View Menu', function() {
  it('should display the menu items for a selected restaurant', function() {
   
restaurantPage.open();

  restaurantPage.selectRestaurant('The Pizza Place');

   restaurantPage.viewMenu();

 expect(restaurantPage.getMenuItemsCount()).to.be.greaterThan(0);

  expect(restaurantPage.getMenuItemNames()).to.include('Pizza Margherita');
  });
});



#Feature: Place Order

---

### *Scenario: User places an order*

#### *Given:*
- The user is logged in and has selected items from the menu.

#### *When:*
- The user adds items to the cart and proceeds to checkout.

#### *Then:*
- The order should be placed successfully.  
- The user should see an order confirmation.

---

## *Chai.js Code:*

```javascript
const chai = require('chai');
const expect = chai.expect;
const cartPage = require('../pages/cartPage'); 
describe('Place Order', function() {
  it('should place the order successfully', function() {
      cartPage.open();

   
    cartPage.addItemToCart('Pizza Margherita');

   
    cartPage.proceedToCheckout();


    cartPage.enterPaymentDetails('1234 5678 9012 3456', '12/25', '123');

   
    cartPage.submitOrder();

    
    expect(cartPage.getOrderConfirmationMessage()).to.equal('Order placed successfully');


    expect(browser.getUrl()).to.include('/order-details');
  });
});
``



