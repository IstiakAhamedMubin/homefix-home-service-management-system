# HomeFix – A Web-Based Home Service Management System

HomeFix is a web-based platform that lets customers book common home maintenance services — Electrician, Plumber, AC Repair, Carpenter, and Home Cleaning — and lets an admin manage customers, service providers, service categories, bookings, and payments from a central dashboard.

This repository contains the **frontend implementation** of the system: a fully working HTML/CSS/JavaScript prototype covering the complete customer and admin user flow.


**Team Members**

| SL No | Name | Student ID |
|---|---|---|
| 01 | Istiak Ahamed | 2024100000273 |
| 02 | MD. Shahedur Rahman Sajid | 2023100000589 |
| 03 | Mir Nafiul Islam Nirjhor | 2023100000599 |

## Project Info

| | |
|---|---|
| **University** | Southeast University |
| **Department** | Computer Science & Engineering |
| **Course** | Information System Design & Software Engineering Lab (CSE346.17) |
| **Semester** | Summer 2026 |
| **Faculty** | Shimul Dey Katha (SDK) |

## Features

### Customer
- Register / Login
- View available services and service details
- Book a service (address, phone, preferred date, problem description)
- Live booking summary before payment
- Payment with method selection (Cash on Service / Mobile Banking / Card) and confirmation screen
- Booking status tracking (Pending → Assigned → Completed)
- Booking history
- View / edit profile

### Admin
- Admin login
- Dashboard overview (customers, providers, bookings, payments at a glance)
- Manage customers
- Manage service providers (add / edit / delete)
- Manage service categories (add / edit / delete)
- View all bookings, view booking details
- Assign a service provider to a booking
- Update booking status
- View payment information

## Tech Stack

- HTML5, CSS3, vanilla JavaScript — no frameworks, no build step
- Browser `sessionStorage` to simulate the booking → payment → dashboard data flow
- Google Fonts (Manrope, Inter)

## Project Structure

```
homefix/
├── index.html              # Homepage
├── login.html               # Customer login
├── register.html            # Customer registration
├── services.html             # Browse all services
├── service-details.html       # Service detail (dynamic via ?service=)
├── booking.html               # Booking form + live summary
├── payment.html                # Payment + confirmation
├── dashboard.html               # Customer dashboard
├── profile.html                  # Customer profile
├── admin.html                     # Admin panel
├── admin-login.html                # Admin login
├── css/
│   └── style.css                    # Shared stylesheet
└── js/
    └── script.js                     # Shared JavaScript
```

## Getting Started

No installation or build step required.

1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/homefix.git
   ```
2. Open the folder in VS Code and run `index.html` with the **Live Server** extension (recommended), or open `index.html` directly in a browser.

## Deployment

This project is static and works on GitHub Pages with no configuration changes — all file paths are relative.

## Scope & Limitations

This is a **frontend-only prototype** built for a university Information System Design & Software Engineering lab project. There is no backend, no database, and no real payment gateway:

- Booking and payment data is stored in the browser's `sessionStorage` and is cleared when the tab is closed.
- Login, registration, and payment forms perform frontend validation only — no real authentication or transactions occur.
- Admin actions (add/edit/delete/assign) update in-memory demo data and reset on page refresh.
