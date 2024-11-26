# Admin Dashboard - Role-Based Access Control (RBAC)

This project is a frontend application for an Admin Dashboard. It allows an admin to manage users, assign roles (creator or user), and enable creators to write and manage posts. Users can view posts and follow their favorite creators. The project demonstrates Role-Based Access Control (RBAC) using React.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [State Management](#state-management)
- [Routing & Permissions](#routing--permissions)
- [How to Run the Project](#how-to-run-the-project)
- [Conclusion](#conclusion)

---

## Project Overview

This Admin Dashboard supports the following features:

### Admin Features:
- View and manage users and creators.
- Assign roles or toggle between user and creator roles.
- Add new members to the system.

### Creator Features:
- Write new posts using a rich text editor.
- View and manage previously created posts.

### User Features:
- Browse and view posts created by creators.
- Follow and unfollow creators.

---

## Features

### Admin Features:
- **Role Management**: Change user roles to either "user" or "creator."
- **User Management**: Add or remove users from the system.

### Creator Features:
- **Post Creation**: Write, edit, and manage posts using a text editor (TinyMCE).
- **Post History**: View a list of previously published posts.

### User Features:
- **Post Viewing**: Browse posts written by creators.
- **Follow Creators**: Follow or unfollow creators to view their content.

### Shared Features:
- **Protected Routes**: Users can only access pages based on their roles. Unauthorized users are redirected.
- **Optimized UI**: Includes a loading effect (shimmer) for better user experience and debounce for smoother input handling.
- **Responsive Design**: The layout works well on both desktop and mobile devices, with a sidebar that can toggle on smaller screens.

---

## Technologies Used
- **React**: For building user interfaces.
- **React Context API**: For managing global state like user roles and posts.
- **React Router**: For navigation and protected routes.
- **Reducer**: For centralized state management.
- **Tailwind CSS**: For styling and responsive design.
- **TinyMCE**: A rich text editor for post creation.
- **Shimmer Effect**: For skeleton loading during data fetching.
- **Debounce**: For efficient handling of input events like search or form submissions.

---

## Project Structure


src/
├── components/
│   ├── forms/          # Login and add-user forms
│   ├── CreatorNav/     # Navigation bar for creators
│   ├── Shimmer/        # Loading effect component
│   ├── UserNav/        # Navigation bar for users
├── context/
│   ├── AuthContext/    # Handles login and authentication logic
│   ├── BlogContext/    # Manages posts and related actions
├── pages/
│   ├── Dashboard/      # Admin dashboard for managing users and roles
│   ├── Following/      # Page for users to follow/unfollow creators
│   ├── PastBlogs/      # Page for creators to view their past posts
│   ├── UnAuthorized/   # Page shown when access is denied
│   ├── UserDashboard/  # User dashboard for viewing posts
│   ├── Write/          # Page for creators to write posts
├── utils/
│   ├── reducer.js      # Functions for managing global state
├── App.jsx             # Main application routes
├── protectedRoute.jsx  # Logic for role-based protected routes
