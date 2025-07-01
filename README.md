# 🎟️ Event Ticket Token System (Java + Vert.x + MongoDB)

A robust, asynchronous **Event Ticket Booking System** developed using **Java 17**, **Vert.x**, **MongoDB**, and **SMTP (Jakarta Mail API)**.  
The platform enables users to register, log in, view live event listings, and book event tokens. Secure token-based emails are sent for both registration and booking confirmations.

---

## 📌 Objective

- Design a scalable and asynchronous event ticketing backend system.
- Enable seamless user interaction through REST APIs.
- Ensure event capacity is managed automatically.
- Implement secure login and token generation workflows.
- Deliver real-time email notifications using SMTP.

---

## 🧾 System Workflow

1. **User Registration**  
   → Register with name and email. A password is auto-generated and sent via email.

2. **User Authentication**  
   → Login via email and password using secure REST endpoints.

3. **Event Listing**  
   → Fetch a list of available events and their token availability.

4. **Token Booking**  
   → Users can book an event if tokens are available. A unique booking token is generated and emailed.

---

## 🛠️ Technologies Used

- **Java 17**
- **Vert.x Web & Core** – Reactive and asynchronous backend framework.
- **MongoDB** – Stores user data, event listings, and bookings.
- **Jakarta Mail API (SMTP)** – Sends automated email notifications.
- **Maven** – Dependency management and project build system.

---

## 🚀 What’s Implemented

- 📥 REST APIs for all operations
- 🔐 User Registration & Secure Password Generation
- 🧾 User Authentication System
- 📅 Real-Time Event Listing from MongoDB
- 🎟️ Token Booking with Unique Token Generation
- ✉️ SMTP Email Notifications for Registration and Booking
- 📉 Event Capacity Management (decrements on booking)
- 🔄 Vert.x-based Asynchronous Operations

---

## 📂 API Endpoints

| Endpoint       | Method | Description                      |
|----------------|--------|----------------------------------|
| `/register`    | POST   | Register new user                |
| `/login`       | POST   | Authenticate and login           |
| `/events`      | GET    | Retrieve list of available events|
| `/book`        | POST   | Book a token for an event        |

---

## 📧 Sample Email Notifications

- **Registration Email**  
  _Subject_: "Welcome to Ticket Token System"  
  _Body_: Contains your email, auto-generated password, and login instructions.

- **Booking Confirmation Email**  
  _Subject_: "Your Event Token Booking is Confirmed"  
  _Body_: Contains your name, event name, and a unique token number.

---

## 🧩 Project Structure

- `MainVerticle.java` – Bootstraps the application and defines REST routes.
- `UserService.java` – Handles registration, login, and password generation.
- `EventService.java` – Manages event data and booking logic.
- `EmailService.java` – Sends emails via SMTP for both registration and booking.
- `MongoManager.java` – Abstracts MongoDB operations for users, events, and bookings.

---

## ✅ How to Run

1. Ensure **Java 17** and **MongoDB** (local or remote) are installed and running.
2. Clone the repository and navigate to the project directory.
3. Configure SMTP settings in `EmailService.java` (username, password, host, port).
4. Run the application using Maven :
```bash
mvn clean install
mvn exec:java
```

5. Use tools like **Postman** or **cURL** to interact with the API endpoints.

---

## 📘 Potential Enhancements

1. Admin dashboard for managing events.
2. QR code generation for booked tickets.
3. JWT-based session management.
4. Email templates using HTML.
5. Rate limiting and authentication throttling.

---
