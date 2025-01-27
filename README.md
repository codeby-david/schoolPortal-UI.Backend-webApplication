School Web App

-Welcome to the School Web App! This project is a modern, responsive, and scalable web application built for managing and enhancing school operations. It leverages the latest web technologies to provide a seamless experience for both administrators and students.

Features

-User Authentication and Authorization: Powered by Clerk for secure, customizable, and robust user management.

Role-Based Access Control:

-Admin: Full CRUD operations for managing users, assignments, and school data.

-Teacher: Can add assignments and marks but cannot access admin pages.

-Student: Can view assignments and marks but cannot access admin or teacher pages.

-Parent: Can view his/her student(s) results and events.

-Routing with React Routes: Enables dynamic and protected navigation between roles and features.

-Responsive Design: Built with Tailwind CSS for a mobile-first, visually appealing UI.

-Type-Safe Development: Implemented using TypeScript for a safer and more predictable codebase.

-Database Management: Integrated with Prisma for efficient and scalable database interactions.

-Dockerized Deployment: Seamlessly containerized using Docker for portability and consistency.

-Built with Next.js: Utilizes Next.js for server-side rendering, static site generation, and optimal performance.

Tech Stack

-Frontend: Next.js, TypeScript, Tailwind CSS

-Backend: Prisma ORM, Clerk Authentication

-Database: PostgreSQL (or other supported relational databases)

-Deployment: Docker for containerization

Installation and Setup

-To run the project locally, follow these steps:

-Clone the Repository:

-git clone https://github.com/codeby-david/schoolPortal-Ui.Backend-webApplication.git
cd school-web-app

Install Dependencies:

``npm install

Set Up Environment Variables:
Create a .env file in the root directory and add the required environment variables:

DATABASE_URL=your-database-connection-string
NEXT_PUBLIC_CLERK_FRONTEND_API=your-clerk-frontend-api
CLERK_API_KEY=your-clerk-api-key

Run Database Migrations:

`npx prisma migrate dev

Start the Development Server:

``npm run dev

The application will be available at http://localhost:3000.

Docker Setup (Optional):
If you prefer to run the application in a Docker container:

docker-compose up --build

Project Structure

pages/: Contains all the Next.js pages.

components/: Reusable UI components.

styles/: Global and module-specific styles using Tailwind CSS.

prisma/: Database schema and migrations.

utils/: Utility functions and helper classes.

routes/: Contains React route definitions with role-based access control.

docker-compose.yml: Configuration for Docker services.

Role-Based Access Control

The application implements role-based access control to ensure a secure and user-specific experience:

Admin:

Access to all CRUD operations for managing users, assignments, and school data.

Can navigate to admin-specific pages and dashboards.

Teacher:

Can add assignments and marks.

Cannot access admin-specific pages.

Student:

Can view assignments and marks.

Cannot access admin or teacher-specific pages.

These roles are enforced through protected routes in the application, ensuring that each user only accesses the features they are authorized to use.

