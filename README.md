# Inventory Management System

Welcome to the **Inventory Management System** project! 🎉 This project is split into two primary directories:

1. **Inventory Dashboard**: This is the frontend, built using Next.js for an interactive, responsive UI.
2. **Inventory Server**: This is the backend, built using Express.js, with Prisma ORM to communicate with a PostgreSQL database.

Let's dive into the installation, setup, and architecture of this project! 🚀

---

## 🏗️ Architecture Design

This section covers the architecture of the Inventory Management System. Below is a placeholder where you can add an image that depicts the structure and flow of the application.

![img.png](img.png)

---

## 📂 Directory Structure

- **`inventory-dashboard/`**: Frontend (Next.js)
- **`inventory-server/`**: Backend (Express.js with Prisma)

---

## 🖥️ Frontend Setup (Inventory Dashboard)

To get the frontend up and running, follow these steps:

1. Navigate to the frontend directory:
    ```bash
    cd inventory-dashboard
    ```

2. Install the required dependencies:
    ```bash
    npm install
    ```

3. Run the development server:
    ```bash
    npm run dev
    ```

4. To build the production-ready version:
    ```bash
    npm run build
    ```

5. Run the production build:
    ```bash
    npm run start
    ```

---

## 🛠️ Backend Setup (Inventory Server)

To set up the backend, follow these steps:

1. Navigate to the backend directory:
    ```bash
    cd inventory-server
    ```

2. Initialize the project and install Prisma and required packages:
    ```bash
    npm init -y
    npm install prisma @prisma/client
    ```

3. Set up TypeScript for the project:
    ```bash
    npm install typescript
    npx tsc --init
    npm install -D ts-node typescript @types/node
    ```

4. Install additional dependencies:
    ```bash
    npm install express body-parser cors dotenv helmet morgan concurrently
    npm install -D nodemon @types/cors @types/express @types/morgan
    npm install rimraf
    ```

5. Set up Prisma:
    ```bash
    npx prisma generate
    npx prisma migrate dev --name init
    ```

6. Seed the database with dummy data:
    ```bash
    npm run seed
    ```

---

## 🌱 Database Setup & Seeding

1. After setting up the Prisma models and seed data, run the following commands to sync the database and seed data:
    ```bash
    npx prisma generate
    npx prisma migrate dev --name init
    npm run seed
    ```

2. Example of adding a PostgreSQL connection in the `.env` file:
    ```
    DATABASE_URL="postgresql://postgres:root@localhost:5433/inventorymanagement?schema=public"
    ```

3. Ensure the PostgreSQL user has the correct credentials:
    ```sql
    ALTER USER postgres WITH PASSWORD 'root';
    ```

---

## 🎉 You're All Set!

Both the frontend and backend should now be running successfully. Feel free to contribute, report issues, or ask questions. Happy coding! 😊
