# E-Commerce Project Overview

This repository contains a full-stack e-commerce platform divided into three main parts:

- **backend-nest**: Backend microservices built with NestJS  
- **frontend-react**: React-based user-facing frontend application  
- **frontend-vue**: Vue.js-based admin dashboard for management  

---

## Backend (NestJS Microservices)

The backend is a microservices architecture implemented in NestJS, covering core e-commerce functionalities:

- **Microservices include**: Authentication, Cart, Category, Payment, Products, User Profile, and API Gateway  
- **Communication**: Services communicate over TCP transport with the API Gateway as the single entry point  
- **Security**: JWT authentication, role-based guards, input validation with DTOs and class-validator, and Zod validation at the gateway  
- **Project structure**: Organized under `apps/` for each microservice, with shared libraries in `libs/` and utilities in `utils/`  
- **Docker support**: Basic Dockerfile included for containerization  
- **Core dependencies**: NestJS modules, Passport JWT, bcrypt, multer, nodemailer, Jest for testing, ESLint, and Prettier for linting and formatting  

Run backend services with:

```bash
npm install
npm run start:dev
npm run test
```

---

## Frontend React Application

The React frontend is a modular TypeScript project using Redux Toolkit for state management:

- **Folder structure**:  
  - `app/`: Redux store configuration  
  - `components/`: Shared UI components (Navbar, Footer, Toasts, etc.)  
  - `features/`: Domain-specific slices and UI modules (auth, cart, payment, products)  
  - `types/`: TypeScript type definitions  
  - `App.tsx` and `index.tsx`: Root components and entry point  

- **State management**: Redux slices for authentication, cart, products, and payment  
- **Validation**: Zod schemas for form validation in auth modules  
- **UI features**: Login, signup, password reset, product listing/detail, cart management, payment processing  
- **Best practices**: Feature-based modular architecture, separation of concerns, reusable hooks and components  

---

## Frontend Vue.js Admin Dashboard

The Vue.js admin dashboard is designed for managing the e-commerce platform with:

- **Folder structure**:  
  - `public/`: Static assets like logo  
  - `src/assets/`: Tailwind CSS styles  
  - `src/components/`: Reusable layout and chart components (BarChart, PieChart, NavBar, SideBar, etc.)  
  - `src/routes/`: Vue Router configuration  
  - `src/services/`: API service layer for auth, categories, products, users  
  - `src/stores/`: Pinia stores for state management (auth, products, users, payments)  
  - `src/views/`: Main pages like Dashboard, AddProducts, Categories, Transactions  

- **Features**: Admin control over products, categories, users, transactions with data visualization charts  
- **State management**: Pinia for reactive state handling  
- **UI/UX**: Tailwind CSS for styling, modular components for layout and functionality  

---

This README provides a high-level overview of your e-commerce platform's architecture, key technologies, and project structure across backend and frontend components. It can be used as the main project README to orient developers and contributors.

---