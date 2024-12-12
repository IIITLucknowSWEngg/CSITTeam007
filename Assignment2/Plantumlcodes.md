
#  Context Diagram Codes
---
## Diner Code :
```
@startuml
skinparam backgroundColor #000000

skinparam title {
    BackgroundColor #000000
    FontColor #C0FF00
    BorderColor #C0FF00
}

skinparam arrow {
    Color #B4E57C
    FontColor #FFFFFF
    Thickness 2
}

skinparam rectangle {
    BackgroundColor #FFFFCC
    BorderColor #FFD700
    FontColor #000000
}

skinparam cloud {
    BackgroundColor #FFFFE0
    BorderColor #FFD700
    FontColor #8B8000
}

skinparam actor {
    BackgroundColor transparent
    BorderColor #FFFFFF
    FontColor #FFFFFF
}

title **Context Diagram - Diner App**

actor "Diner (User)" as Diner #FFFFFF

rectangle "Diner Mobile App" as DinerApp #FFFFCC

cloud "Payment Gateway" as PaymentGateway #FFFFE0
cloud "Notification Service" as NotificationService #FFFFE0
cloud "Restaurant Service" as RestaurantService #FFFFE0
cloud "Order Service" as OrderService #FFFFE0
cloud "GPS/Map API" as MapAPI #FFFFE0
cloud "Reviews Service" as ReviewsService #FFFFE0
cloud "User Auth Service" as AuthService #FFFFE0

Diner --> DinerApp : "Register, Login, Search & Place Orders"
DinerApp --> AuthService : "User Authentication"
DinerApp --> RestaurantService : "Browse Restaurants & Menus"
DinerApp --> OrderService : "Place & Track Orders"
DinerApp --> PaymentGateway : "Make Payments"
DinerApp --> ReviewsService : "Write Reviews & Ratings"
DinerApp --> NotificationService : "Receive Real-time Notifications"
DinerApp --> MapAPI : "Real-time Delivery Tracking"

@enduml
```

## Restaurant Code :
```
@startuml
skinparam backgroundColor #000000

skinparam title {
    BackgroundColor #000000
    FontColor #C0FF00
    BorderColor #C0FF00
}

skinparam arrow {
    Color #B4E57C
    FontColor #FFFFFF
    Thickness 2
}

skinparam rectangle {
    BackgroundColor #FFFFCC
    BorderColor #FFD700
    FontColor #000000
}

skinparam cloud {
    BackgroundColor #FFFFE0
    BorderColor #FFD700
    FontColor #8B8000
}

skinparam actor {
    BackgroundColor transparent
    BorderColor #FFFFFF
    FontColor #FFFFFF
}

title **Context Diagram - Restaurant Owner App**

actor "Restaurant Owner" as RestaurantOwner #FFFFFF

rectangle "Restaurant Partner App" as RestaurantApp #FFFFCC

cloud "Order Service" as OrderService #FFFFE0
cloud "Menu Service" as MenuService #FFFFE0
cloud "Payment Gateway" as PaymentGateway #FFFFE0
cloud "Notification Service" as NotificationService #FFFFE0
cloud "Analytics Service" as AnalyticsService #FFFFE0

RestaurantOwner --> RestaurantApp : "Manage Menus, Orders & Profiles"
RestaurantApp --> MenuService : "Update Menus & Availability"
RestaurantApp --> OrderService : "View Incoming Orders"
RestaurantApp --> PaymentGateway : "Track Payments & Refunds"
RestaurantApp --> NotificationService : "Receive Order Notifications"
RestaurantApp --> AnalyticsService : "View Sales & Performance Analytics"

@enduml

```
## Delivery Executive Code :
```
@startuml
skinparam backgroundColor #000000

skinparam title {
    BackgroundColor #000000
    FontColor #C0FF00
    BorderColor #C0FF00
}

skinparam arrow {
    Color #B4E57C
    FontColor #FFFFFF
    Thickness 2
}

skinparam rectangle {
    BackgroundColor #FFFFCC
    BorderColor #FFD700
    FontColor #000000
}

skinparam cloud {
    BackgroundColor #FFFFE0
    BorderColor #FFD700
    FontColor #8B8000
}

skinparam actor {
    BackgroundColor transparent
    BorderColor #FFFFFF
    FontColor #FFFFFF
}

title **Context Diagram - Delivery Executive App**

actor "Delivery Executive" as DeliveryExecutive #FFFFFF

rectangle "Delivery Executive App" as DeliveryApp #FFFFCC

cloud "Order Service" as OrderService #FFFFE0
cloud "GPS/Map API" as MapAPI #FFFFE0
cloud "Notification Service" as NotificationService #FFFFE0
cloud "Payment Gateway" as PaymentGateway #FFFFE0

DeliveryExecutive --> DeliveryApp : "Accept & Deliver Orders"
DeliveryApp --> OrderService : "Receive Delivery Requests"
DeliveryApp --> MapAPI : "Track Routes & Optimize Delivery"
DeliveryApp --> NotificationService : "Receive Delivery Notifications"
DeliveryApp --> PaymentGateway : "Track Earnings & Payments"

@enduml

```
## Admin Code:

```
@startuml
skinparam backgroundColor #000000

skinparam title {
    BackgroundColor #000000
    FontColor #C0FF00
    BorderColor #C0FF00
}

skinparam arrow {
    Color #B4E57C
    FontColor #FFFFFF
    Thickness 2
}

skinparam rectangle {
    BackgroundColor #FFFFCC
    BorderColor #FFD700
    FontColor #000000
}

skinparam cloud {
    BackgroundColor #FFFFE0
    BorderColor #FFD700
    FontColor #8B8000
}

skinparam actor {
    BackgroundColor transparent
    BorderColor #FFFFFF
    FontColor #FFFFFF
}

title **Context Diagram - Admin App**

actor "Admin" as Admin #FFFFFF

rectangle "Admin Dashboard" as AdminDashboard #FFFFCC

cloud "User Management Service" as UserService #FFFFE0
cloud "Restaurant Service" as RestaurantService #FFFFE0
cloud "Order Service" as OrderService #FFFFE0
cloud "Analytics Service" as AnalyticsService #FFFFE0
cloud "Notification Service" as NotificationService #FFFFE0

Admin --> AdminDashboard : "Manage Users, Restaurants, Orders"
AdminDashboard --> UserService : "Manage User Profiles & Access"
AdminDashboard --> RestaurantService : "Monitor Restaurant Activities"
AdminDashboard --> OrderService : "Track Orders & Resolve Issues"
AdminDashboard --> AnalyticsService : "View Platform Metrics & Reports"
AdminDashboard --> NotificationService : "Send Notifications & Alerts"

@enduml

```
---

# Container Diagram Code 
---

---
# Deployment Diagram Code
---
```
@startuml
skinparam backgroundColor #0D0D0D

skinparam title {
    BackgroundColor #0D0D0D
    FontColor #C0FF00
    BorderColor #C0FF00
}

skinparam arrow {
    Color #B4E57C
    FontColor #FFFFFF
    Thickness 2
}

skinparam node {
    BackgroundColor #F5FFFA
    BorderColor #90EE90
    FontColor #000000
}

skinparam database {
    BackgroundColor #FFFAFA
    BorderColor #FF8C8C
    FontColor #C80000
}

skinparam cloud {
    BackgroundColor #FFFFF0
    BorderColor #FFD700
    FontColor #8B8000
}

skinparam actor {
    BackgroundColor #E0FFFF
    BorderColor #40E0D0
    FontColor #008080
}

title Deployment Diagram - Zomato Clone System

actor "User's Mobile Device" as UserDevice #E0FFFF
actor "Delivery Executive's Mobile Device" as DeliveryDevice #E0FFFF
actor "Admin's PC" as AdminDevice #E0FFFF

node "User's Mobile Device" {
    [User Mobile App] <<Mobile App>> #FFFFCC
}

node "Restaurant's System" {
    [Restaurant Web Dashboard] <<Web App>> #CCFFCC
    [Restaurant Mobile App] <<Mobile App>> #CCFFCC
}

node "Admin's PC" {
    [Admin Web Dashboard] <<Web App>> #FFFFCC
}

node "Web Server" {
    [Order Management Service] <<Microservice>> #CCFFCC
    [Payment Service] <<Microservice>> #FFCCCC
    [User Management Service] <<Microservice>> #FFFFCC
    [Real-Time Tracking Service] <<Microservice>> #CCFFCC
    [Menu Management Service] <<Microservice>> #FFCCCC
    [Notification Service] <<Microservice>> #FFFFCC
}

node "Database Server" {
    database "User Database" as UserDB #FFCCCC
    database "Order Database" as OrderDB #FFCCCC
    database "Payment Database" as PaymentDB #FFCCCC
    database "Restaurant Database" as RestaurantDB #FFCCCC
    database "Menu Database" as MenuDB #FFCCCC
}

cloud "Third-Party Services" {
    [Payment Gateway] <<External Service>> #FFFFCC
    [Map/GPS Service] <<External Service>> #FFFFCC
    [SMS Gateway] <<External Service>> #FFFFCC
}

' Connections with arrows
[User Mobile App] -[#B4E57C]-> [Order Management Service] : "Place orders"
[User Mobile App] -[#B4E57C]-> [Payment Service] : "Process payments"
[User Mobile App] -[#B4E57C]-> [Real-Time Tracking Service] : "Track delivery"
[User Mobile App] -[#B4E57C]-> [User Management Service] : "Manage profile"
[User Mobile App] -[#B4E57C]-> [Menu Management Service] : "View menus"

[Restaurant Web Dashboard] -[#B4E57C]-> [Menu Management Service] : "Update menu"
[Restaurant Web Dashboard] -[#B4E57C]-> [Order Management Service] : "Manage orders"
[Restaurant Mobile App] -[#B4E57C]-> [Order Management Service] : "Receive orders"
[Restaurant Mobile App] -[#B4E57C]-> [Menu Management Service] : "Update menu"

[Admin Web Dashboard] -[#B4E57C]-> [Order Management Service] : "Monitor orders"
[Admin Web Dashboard] -[#B4E57C]-> [User Management Service] : "Manage users"
[Admin Web Dashboard] -[#B4E57C]-> [Payment Service] : "Monitor payments"

[Order Management Service] -[#B4E57C]-> OrderDB : "Read/Write order data"
[Payment Service] -[#B4E57C]-> PaymentDB : "Read/Write payment data"
[User Management Service] -[#B4E57C]-> UserDB : "Manage user profiles"
[Menu Management Service] -[#B4E57C]-> MenuDB : "Read/Write menu data"
[Order Management Service] -[#B4E57C]-> RestaurantDB : "Access restaurant data"

[Payment Service] -[#B4E57C]-> [Payment Gateway] : "Process payment"
[Real-Time Tracking Service] -[#B4E57C]-> [Map/GPS Service] : "Access map and GPS data"
[Notification Service] -[#B4E57C]-> [SMS Gateway] : "Send notifications"

' Delivery Executive's interactions
[Delivery Executive's Mobile Device] -[#B4E57C]-> [Real-Time Tracking Service] : "Track deliveries"
[Delivery Executive's Mobile Device] -[#B4E57C]-> [Order Management Service] : "Receive delivery tasks"
[Delivery Executive's Mobile Device] -[#B4E57C]-> [Notification Service] : "Receive delivery notifications"
@enduml
```
