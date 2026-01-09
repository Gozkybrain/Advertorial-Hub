# Advertorial Hub — Fullstack Application with Next.js

Advertorial Hub is a sleek and fully responsive fullstack application built with Next.js 14 using the App Router. It combines both frontend and backend into a single unified project, offering a modern platform where users can create, manage, and promote advertorial posts. The system provides user authentication, subscription plans, Paystack-powered payments, post and ad management, and an analytics dashboard, all under one integrated platform.

---

## Project Overview

Advertorial Hub allows users to describe their businesses or personal projects through posts and advertisements. Users can choose from multiple subscription plans to gain different levels of access to posts, ads, and social media promotion. Admins have full control over user management, ad approvals, and analytics.

Previously, the system used a standalone Express backend. All backend logic has now been fully migrated into the Next.js API routes, simplifying deployment, reducing maintenance, and allowing for tighter integration between frontend and backend.

Key capabilities include user authentication, secure data management, post creation, ad management, subscription plan handling, and integration with Paystack for payments.

---

## Core Features

### User Authentication

- Users can register, log in, and manage their profiles securely.

- Passwords are hashed and user sessions are maintained with JWT for authentication.

- Forgot password and reset password flows are fully implemented.

- Users can verify accounts via email links.


### User Data Management

- User profiles store first and last names, email, profile picture, phone number, gender, plan information, posts count, and ads count.

- Admins can view all users, edit any profile, and delete accounts if needed.


### Post Management

- Users can create posts describing their business, service, or project.

- Posts support text, multiple images (up to 3 depending on plan), and a single video for higher-tier plans.

- Users can edit and delete their own posts, while admins can manage all posts.

- Posts track views with device type and location.

- Users can react to posts with likes or dislikes, limited to one reaction per user per post.

- Analytics for posts are collected for insights on performance.


### Advertisement Management

- Users can promote posts as ads to specific social media platforms.

- Targeting options include age range, gender, country, and state.

- Users can view their own ads, while all ads are publicly viewable.

- Admins can approve, reject, or edit ads.

- Ads are linked to posts and integrate with user subscription plans.


### Subscription Plans

Users can choose from the following plans:

- **Personal Plan (Free)**

  - 1 post only, 1 image per post

  - No ads

  - No social sharing

- **Starter Plan (₦5,000 per month)**

  - 3 posts per month, up to 2 images per post

  - 1 ad per month

  - Social sharing on Instagram

- **Business Plan (₦30,000 per month)**

  - 10 posts per month, up to 3 images per post

  - 3 ads per month

  - Social sharing on Instagram and Facebook

- **Team Plan (₦50,000 per month)**

  - Unlimited posts, up to 3 images and 1 video per post

  - 5 ads per month

  - Social sharing on Instagram, Facebook, TikTok, and Twitter

All plans include 24/7 email support. Users can upgrade at any time. Subscription plans are verified using Paystack payments. Admins can manually change plans or user roles without payment verification.


### Security
- Passwords are hashed using bcrypt.
- Authentication is token-based via JWT.
- Sensitive routes require Bearer token authorization.
- Payment references are verified and cannot be reused.

### Frontend Features
- Built entirely in Next.js 14 with React 18.
- Responsive layout optimized for both desktop and mobile devices.
- Uses React hooks and Context API for state management.
- Post carousel and interactive components improve user engagement.
- Handles API requests efficiently using `/api/*` endpoints.

### Backend Features
- Backend APIs are fully integrated with Next.js.
- MongoDB with Mongoose is used for database management.
- Multer handles file uploads for images and videos.
- Nodemailer is used for sending emails for verification and password resets.
- Paystack SDK handles subscription payments and verification.
- Admin endpoints provide analytics, ad approval, and role management.

---


## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend Framework | Next.js 14 (React 18) |
| Styling | CSS |
| State Management | React Hooks & Context |
| HTTP Requests | Fetch API |
| Backend Communication | Next.js API Routes (Migrated from Express) |
| Payments | Paystack Inline SDK |
| Database | MongoDB |
| Authentication | JWT & bcrypt |
| File Uploads | Multer |
| Email Service | Nodemailer |
| API Testing | Postman |

---

## Key Advantages

- Single unified fullstack solution without maintaining separate backend and frontend repositories.
- Flexible subscription plans that allow both casual users and large marketing teams to scale.
- Ad management and social media promotion built directly into the platform.
- Secure authentication and data handling ensures user safety.
- Responsive design ensures accessibility on all devices.
- Full admin control over users, posts, ads, and analytics.

---

## Ideal Users

- Individual creators looking to promote a project or personal brand.
- Small businesses seeking to reach an online audience.
- Marketing teams managing multiple campaigns and posts.
- Agencies needing analytics, ad management, and cross-platform promotions.

---

## Summary

Advertorial Hub is a modern, all-in-one platform for creating and promoting advertorial content. It allows users to register, manage posts, create and manage ads, subscribe to paid plans, track analytics, and share content on multiple social media platforms. Admins have full oversight of the platform, enabling effective user management and content control.

The platform leverages the latest Next.js features with full backend integration, responsive frontend design, secure authentication, and Paystack-powered payments, making it a complete solution for personal creators, small businesses, and marketing teams alike.



