
<p align="center">
  <img src="https://github.com/user-attachments/assets/ccffa949-d0a6-4b9e-a1e8-db3b06e2ecfd" alt="GameDrop Logo" width="1000">
</p>

# GameDrop: A Comprehensive E-Commerce System for Video Games

[![Node.js Version](https://img.shields.io/badge/Node.js-v14+-green.svg)](https://nodejs.org/)
[![React Version](https://img.shields.io/badge/React-18.x-blue.svg)](https://reactjs.org/)
[![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-336791.svg)](https://www.postgresql.org/)
[![Prisma](https://img.shields.io/badge/ORM-Prisma-0c344b.svg)](https://www.prisma.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview

**GameDrop** is an enterprise-grade, full-stack e-commerce platform meticulously engineered to handle the end-to-end lifecycle of video game distribution. More than just a website, GameDrop represents a robust system architecture designed for scalability, security, and a premium user experience. It bridges the gap between avid gamers and a vast digital catalog, providing a seamless journey from discovery to checkout.

## Table of Contents

- [System Architecture](#system-architecture)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Database Schema](#database-schema)
- [API Documentation](#api-documentation)
- [Installation and Setup](#installation-and-setup)
- [Testing and Development](#testing-and-development)
- [Supplementary Documentation](#supplementary-documentation)
- [License](#license)

---

## System Architecture

GameDrop follows a modern **decoupled architecture**, separating the frontend experience from the backend business logic. This allows for independent scaling and maintenance of the two core components.

- **Frontend**: A dynamic, single-page application (SPA) built with React and Material UI, ensuring a responsive and intuitive UI.
- **Backend**: A RESTful API built with Express.js and Node.js, leveraging Prisma ORM for type-safe database interactions with PostgreSQL.
- **Security**: Stateless authentication handled via JSON Web Tokens (JWT) and industry-standard password hashing with Bcrypt.

---

## Key Features

### Customer Experience
- **Smart Catalog**: Advanced search and multi-criteria filtering (Genre, Platform, Price) to help users find their next favorite game.
- **Dynamic Cart Management**: Real-time cart updates with persistent state across sessions.
- **Seamless Checkout**: Streamlined multi-step process for order finalization and shipping details.
- **Personalized History**: Detailed order tracking and historical data for all past purchases.
- **Community Engagement**: Integrated review and rating system allowing customers to share feedback.

### Administrative Excellence
- **Inventory Control**: Comprehensive CRUD operations for managing the game catalog and stock levels.
- **Order Processing**: Centralized dashboard for monitoring and updating the status of customer orders.
- **User Oversight**: Management tools for user roles and account administration.
- **Business Insights**: Dashboard statistics providing a high-level view of platform performance.

---

## Technology Stack

### Backend Infrastructure
- **Runtime**: [Node.js](https://nodejs.org/)
- **API Framework**: [Express.js](https://expressjs.com/)
- **Database**: [PostgreSQL](https://www.postgresql.org/)
- **ORM**: [Prisma](https://www.prisma.io/)
- **Auth**: [JWT](https://jwt.io/) & [bcryptjs](https://www.npmjs.com/package/bcryptjs)

### Frontend Performance
- **UI Library**: [React](https://reactjs.org/)
- **State Management**: [Context API](https://reactjs.org/docs/context.html)
- **UI Framework**: [Material UI](https://mui.com/)
- **Navigation**: [React Router](https://reactrouter.com/)
- **Validation**: [Formik](https://formik.org/)

---

## Project Structure

```bash
.
├── backend
│   ├── prisma               # Database schema and migrations
│   ├── src
│   │   ├── config           # Environment and DB configuration
│   │   ├── controllers      # Request handlers and business logic
│   │   ├── middleware       # Auth and validation guards
│   │   ├── routes           # API endpoint definitions
│   │   └── utils            # Helper functions and constants
│   ├── tests                # Backend unit and integration tests
│   └── server.js            # API entry point
├── frontend
│   ├── src
│   │   ├── api              # API service layer (Axios)
│   │   ├── components       # Reusable UI components
│   │   ├── contexts         # Global state management
│   │   ├── layouts          # Page layouts (Header, Footer)
│   │   ├── pages            # High-level views (Home, Product, Cart)
│   │   └── index.js         # React entry point
├── documentation            # Full project documentation (PDFs)
└── README.md                # System documentation
```

---

## Database Schema

The system relies on a highly relational PostgreSQL database, managed through Prisma. Key entities include:

| Entity | Description |
| :--- | :--- |
| **Users** | Core account data with Role-Based Access Control (RBAC). |
| **Products** | Detailed game information including inventory and pricing. |
| **Orders** | Transactional records linked to users and multi-status tracking. |
| **Reviews** | User-generated content linked to specific products. |
| **Carts** | Persistent shopping session data for registered users. |

> [!NOTE]
> For a visual representation, refer to the Full Entity Relationship Diagram in the Documents Directory.

---

## API Documentation

The GameDrop API is organized into several functional modules:

### Authentication
- `POST /api/auth/register` - New user onboarding.
- `POST /api/auth/login` - Secure credentials verification.

### Product Catalog
- `GET /api/products` - Filterable game list.
- `POST /api/products` - Admin-only product creation.
- `PUT /api/products/:id` - Inventory updates.

### Cart & Orders
- `GET /api/cart` - User-specific active cart retrieval.
- `POST /api/orders` - Order finalization and payment simulation.

---

## Installation and Setup

### Prerequisites
- **Node.js** (v14.x or higher)
- **PostgreSQL** (Active instance)
- **npm** (v6.x or higher)

### Rapid Deployment

1. **Clone & Install Backend**
   ```bash
   cd backend
   npm install
   ```

2. **Environment Configuration**
   Create a `.env` in the `backend` folder:
   ```env
   DATABASE_URL="postgresql://user:pass@localhost:5432/gamedrop_db"
   JWT_SECRET="your_secure_secret_key"
   PORT=5000
   ```

3. **Database Migration**
   ```bash
   npx prisma migrate dev
   ```

4. **Frontend Initialization**
   ```bash
   cd ../frontend
   npm install
   npm start
   ```

---

## Testing and Development

Maintain code quality and system integrity with the following standard commands:

| Purpose | Command |
| :--- | :--- |
| **Run Tests** | `npm test` (Available in both root-dirs) |
| **Linting** | `npm run lint` |
| **Formatting** | `npm run format` |
| **Development** | `npm run dev` |

---

## Supplementary Documentation

For a deeper dive into the system requirements and technical specifications, please explore the `documentation/` directory:

- Project Overview
- Functional Requirements Document
- Technical Requirements Document
- Database Schema (Detailed)

---

## License

This project is licensed under the **MIT License**.

---
<p align="center">Built with ❤️ by Loay Elhattab, Youssef Sabry, Youssef Ragab, Kamal Bahaa, Keroulos Magdy, Martin Hani.</p>
