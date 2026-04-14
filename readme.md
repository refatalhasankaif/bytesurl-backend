# BytesURL — Backend

A production-ready URL shortener API with analytics, subscription plans, payment integration, and AI-powered assistance.

## Live URLs

| Service   | Link |
|----------|------|
| Backend  | https://bytesurl.onrender.com |
| Frontend | https://bytesurl.vercel.app |

## Repositories

| Service   | Link |
|----------|------|
| Backend  | https://github.com/refatalhasankaif/bytesurl-backend |
| Frontend | https://github.com/refatalhasankaif/bytesurl-frontend |

![Page](https://i.ibb.co.com/NddPjJYp/Screenshot-From-2026-04-09-13-34-57.png)

## Overview

BytesURL is a full-stack URL shortener platform that enables users to create short links, track detailed analytics, and manage usage through subscription plans.

The backend is built with a modular and scalable architecture using Node.js, Express, and TypeScript, with PostgreSQL managed via Prisma ORM. It provides core services such as unique URL generation using nanoid, real-time analytics (device, browser, operating system, geolocation, and referrer), and secure authentication using Firebase.

The system includes role-based access control for administrative operations and integrates Stripe for payment processing and subscription upgrades. AI capabilities are integrated via the Groq API to support backend-driven assistance and intelligent features.

## Notice

The system design diagram below does not include the recently integrated AI components. AI functionality was added after the initial system design and is not reflected in that diagram. The Entity Relationship Diagram (ERD) is up to date.

## System Overview Diagram

![System Overview](https://i.ibb.co.com/QFq3DDwC/Screenshot-From-2026-03-23-21-09-43.png)

## Entity Relationship Diagram

![ERD Diagram](https://i.ibb.co.com/Z6krRVGp/Untitled-Diagram.webp)

## Tech Stack

| Layer | Technology |
|-------|----------|
| Runtime | Node.js |
| Framework | Express.js |
| Language | TypeScript |
| Database | PostgreSQL (NeonDB) |
| ORM | Prisma |
| Authentication | Firebase |
| Payments | Stripe |
| AI Integration | Groq API |
| Backend Deployment | Render |
| Frontend Deployment | Vercel |

## Libraries & Packages

| Package | Purpose |
|---------|--------|
| express | Core HTTP server and routing framework |
| prisma + @prisma/client | Type-safe database ORM and query builder |
| @prisma/adapter-pg | PostgreSQL adapter for Prisma |
| firebase-admin | Server-side Firebase token verification and user management |
| stripe | Payment processing and webhook handling |
| nanoid | Generates unique, URL-safe short codes |
| zod | Runtime schema validation |
| ua-parser-js | Device, browser, and OS detection |
| geoip-lite | IP-based geolocation for analytics |
| helmet | Security headers |
| cors | Cross-Origin Resource Sharing configuration |
| express-rate-limit | Rate limiting and abuse prevention |
| compression | Response compression |
| morgan | HTTP request logging |
| dotenv | Environment variable management |
| http-status | HTTP status code constants |
| pg | PostgreSQL client |
| tsx | Run TypeScript without compilation |

## Features

- URL shortening with optional custom aliases
- Unique URL generation using nanoid
- Click analytics including device, browser, OS, country, city, and referrer
- Firebase authentication (email/password and Google)
- Role-based access control for admin and user operations
- Subscription plans with usage limits and upgrade support
- Stripe integration for one-time payments and webhook handling
- Administrative controls for managing users, URLs, analytics, and payments
- Security features including validation, rate limiting, and HTTP protection
- AI integration using the Groq API for backend-powered assistance

## Subscription Plans

| Plan | Price | URL Limit | Reset |
|------|-------|-----------|-------|
| FREE | Free | 10 URLs | Lifetime total |
| PRO | 66 BDT once | 500 URLs | Monthly auto-reset |
| ULTIMATE | 199 BDT once | Unlimited | No limit |