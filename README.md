# Airbnb Clone Project

Welcome to the Airbnb Clone Project!

This project aims to recreate a simplified version of Airbnb’s core functionality, focusing on an intuitive user interface, clean backend integration, and efficient user experience.

## Project Goals

- Build a dynamic, responsive platform for property listings and bookings.
- Practice full-stack development skills.
- Collaborate effectively using GitHub workflows.

## Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (React.js optional later)
- **Backend**: Python (Flask/Django), Node.js (optional)
- **Database**: MySQL / PostgreSQL
- **Version Control**: Git & GitHub
- **Design**: Figma

---

## UI/UX Design Planning

### Design Goals

- Keep the interface clean, simple, and easy to navigate.
- Ensure responsiveness for mobile and desktop users.
- Create visually attractive pages without overwhelming the user.

### Key Features

- Easy property browsing
- Detailed property views
- Simple and fast checkout flow

| Page Name               | Description                                                                  |
|--------------------------|------------------------------------------------------------------------------|
| Property Listing View    | Displays a list of available properties with thumbnails and key details.    |
| Listing Detailed View    | Shows full property details, amenities, pricing, and booking option.        |
| Simple Checkout View     | A straightforward booking form with payment integration (later phase).      |

### Importance of User-Friendly Design

A user-friendly design is critical in a booking system because it directly impacts the user's trust, ease of navigation, and likelihood to complete a booking.
A confusing layout = users running away faster than a cat avoiding bath time.

---

## More UI/UX Design Planning

### Color Styles

- **Primary Color**:`#00A699` (Airbnb Teal)
- **Secondary Color**: `#FFFFFF` (White)
- **Accent Colors**:  `#FF5A5F` (Red),`#484848` (Grey)

### Typography

- **Font Family**: Circular, "Helvetica Neue", Helvetica, Arial, sans-serif
- **Font Weights**: Regular (400), Medium (500), Bold (700)
- **Font Sizes**:
  - Headings: 24px, 18px
  - Body: 14px
  - Buttons: 16px

### Importance of Identifying Design Properties

Identifying design properties early ensures consistency across the app and reduces the chances of a UI looking like it got dressed in the dark.  
It helps developers, designers, and testers stay on the same page.

---

## Team Roles

| Role                  | Responsibilities |
|------------------------|------------------|
| Project Manager        | Plan, coordinate, and track project progress. |
| Frontend Developers    | Build the user interface and make it dynamic. |
| Backend Developers     | Develop APIs, manage server-side logic and databases. |
| Designers              | Create mockups, wireframes, and ensure visual consistency. |
| QA/Testers             | Test the product rigorously to catch bugs early. |
| DevOps Engineers       | Manage deployment, CI/CD pipelines, and infrastructure. |
| Product Owner          | Define project requirements and prioritize tasks. |
| Scrum Master           | Facilitate Agile processes, remove blockers, and keep the team on track. |

---

## UI Component Patterns

### Planned Components

- **Navbar**: Top navigation menu with branding and links.
- **Property Card**: Clickable cards showing thumbnail, title, price, and rating.
- **Footer**: Standard bottom navigation with links and information.

---

## Database Design

The database will revolve around the following key entities:

| Entity | Key Fields | Relationships |
|--------|------------|---------------|
| **User** | id, name, email, password, phone_number | A user can have multiple properties and bookings. |
| **Property** | id, title, description, location, price_per_night | Belongs to a user (host). Can have many bookings and reviews. |
| **Booking** | id, user_id, property_id, start_date, end_date | Linked to a user and a property. |
| **Review** | id, user_id, property_id, rating, comment | Tied to both a user and a property. |
| **Payment** | id, booking_id, payment_method, amount, payment_status | Connected to a booking record. |

**Relationships Overview**:

- A user can own multiple properties.
- A property can have many bookings.
- A booking belongs to one user and one property.
- A review is posted by a user for a property.
- Payments are linked to bookings.

---

## Feature Breakdown

- **User Management**: Users can sign up, log in, and manage their profiles securely.
- **Property Management**: Hosts can list properties, edit details, upload photos, and set prices.
- **Booking System**: Users can browse listings, book properties, and view their booking history.
- **Payment Integration**: Seamless, secure payment processing for bookings.
- **Review System**: Guests can leave reviews and ratings for properties after stays.
- **Search and Filtering**: Users can search for properties based on location, date, and price range.
- **Admin Dashboard**: For site administrators to oversee all user activities and property listings.

---

## API Security

Key Security Measures:

- **Authentication**: Users must verify identity (e.g., token-based authentication like JWT).
- **Authorization**: Users can only access and modify their own resources.
- **Input Validation**: All input is validated and sanitized to prevent SQL injection and XSS attacks.
- **Rate Limiting**: To prevent API abuse and DoS attacks.
- **Data Encryption**: Sensitive information (e.g., passwords, payment info) will be securely encrypted.

**Why Security Matters**:

- **User Data Protection**: Keeping personal and financial data secure builds trust.
- **Payment Security**: Ensures users' transactions are safe and prevents financial fraud.
- **System Integrity**: Protects against malicious activities that could disrupt operations.

---

## CI/CD Pipeline

**What is CI/CD?**

- **Continuous Integration (CI)**: Automatically testing and merging code changes into the main branch.
- **Continuous Deployment (CD)**: Automatically deploying the application after successful integration and testing.

**Why is CI/CD Important?**

- Speeds up the development process with automated builds and tests.
- Ensures higher code quality and faster deployment with less human error.

**Tools to be Used**:

- **GitHub Actions**: For automating tests, builds, and deployments.
- **Docker**: To containerize applications and ensure consistency across environments.

---
