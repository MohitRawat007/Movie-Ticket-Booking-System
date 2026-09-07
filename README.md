
# 🎬 Movie Ticket Booking System

A console-based **Movie Ticket Booking System** developed in **C++17** using Object-Oriented Programming (OOP) concepts and System Design principles. The application simulates the complete ticket booking workflow for a single cinema, including movie selection, seat booking, payment processing, ticket generation, and booking cancellation.

---

## 📌 Project Overview

This project was built to demonstrate software design, UML modeling, and modular programming using C++. The system follows a clean architecture with separate entity and service classes while implementing core OOP concepts and SOLID principles.

---

## ✨ Features

- 🎞️ List all movies currently playing
- 🕒 View available shows for a selected movie
- 💺 Display seat layout (Available / Booked)
- 🎟️ Book one or more seats
- 🚫 Prevent duplicate seat bookings
- 💰 Automatic ticket pricing based on seat type
  - Silver – ₹150
  - Gold – ₹250
  - Platinum – ₹400
- 💳 Multiple payment methods
  - UPI
  - Card
  - Cash
- 🧾 Generate ticket after successful payment
- ❌ Cancel bookings and release reserved seats
- ✅ Input validation for invalid menu choices and seat numbers

---

# 🏗️ Architecture

The project is divided into entity classes and service classes to maintain modularity and separation of responsibilities.

### Entity Classes

- Cinema
- Screen
- Movie
- Seat
- Show
- ShowSeat
- Customer
- Booking

### Service Classes

- BookingService
- PriceCalculator
- TicketPrinter
- Payment (Abstract)
  - UpiPayment
  - CardPayment
  - CashPayment

---

## 📚 OOP Concepts Implemented

| Concept | Implementation |
|---------|----------------|
| Encapsulation | Private data members with controlled access methods |
| Abstraction | Abstract `Payment` class |
| Inheritance | `UpiPayment`, `CardPayment`, and `CashPayment` inherit from `Payment` |
| Runtime Polymorphism | Payment handled through base class pointers |
| Compile-Time Polymorphism | Constructor overloading |
| Static Members | Auto-generated Booking IDs |
| Composition | Cinema → Screen, Screen → Seat, Show → ShowSeat |
| Aggregation | Show → Movie, Booking → ShowSeat |
| Association | Booking → Customer, Show → Screen |

---

## 🧩 SOLID Principles

- **Single Responsibility Principle (SRP)** – Each class has one well-defined responsibility.
- **Open/Closed Principle (OCP)** – New payment methods can be added without modifying existing booking logic.
- **Liskov Substitution Principle (LSP)** – Any payment implementation can replace the base `Payment` class.
- **Interface Segregation Principle (ISP)** – `Payment` exposes only the operations required by all payment types.
- **Dependency Inversion Principle (DIP)** – `BookingService` depends on the `Payment` abstraction instead of concrete payment classes.

---

## 📊 UML & System Design

The project includes complete software design documentation:

- Requirement Analysis
- Noun–Verb Analysis
- Class Responsibility Analysis
- Relationship Analysis
- UML Class Diagram
- Sequence Diagram
- SOLID Principle Mapping

---

## 📁 Project Structure

```text
Movie-Ticket-Booking-System/
│
├── main.cpp
├── Cinema.cpp
├── Movie.cpp
├── Screen.cpp
├── Seat.cpp
├── Show.cpp
├── ShowSeat.cpp
├── Customer.cpp
├── Booking.cpp
├── BookingService.cpp
├── Payment.cpp
├── UpiPayment.cpp
├── CardPayment.cpp
├── CashPayment.cpp
├── PriceCalculator.cpp
├── TicketPrinter.cpp
├── diagrams/
│   ├── ClassDiagram.png
│   ├── SequenceDiagram.png
│   ├── RelationshipDiagram.png
│   └── SOLIDMapping.png
└── README.md
```

---

## 🚀 Build & Run

Compile the project using **g++**:

```bash
g++ -std=c++17 -Wall -Wextra *.cpp -o movie-booking
```

Run the executable:

```bash
./movie-booking
```

---

## 🖥️ Sample Output

```text
===== MOVIE TICKET BOOKING SYSTEM =====

1. List Movies
2. View Shows
3. Book Ticket
4. Print Ticket
5. Cancel Booking
6. Exit

Movies Currently Playing

1. Avengers: Endgame
2. Interstellar

Seat Layout

A1  AVAILABLE
B1  AVAILABLE
C1  AVAILABLE

Payment Successful via UPI

=============== TICKET ===============

Booking ID : B1001
Movie      : Avengers: Endgame
Screen     : Screen 1
Time       : 06:00 PM
Seats      : A1
Amount     : ₹150
Status     : CONFIRMED

======================================
```

---

## 🛠️ Tech Stack

- C++17
- Object-Oriented Programming (OOP)
- UML
- PlantUML
- draw.io

---

## 🎯 Future Improvements

- User authentication
- Database integration
- Online payment gateway
- GUI version
- Multiple cinema support
- File-based data persistence

---

## 👨‍💻 Author

**Mohit Rawat**

B.Tech Computer Science & Engineering

System Design (TCS-504)
