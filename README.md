# DineMatch

**A Personalized Restaurant Recommendation Platform**

Software Engineering Project — Deliverable 1

---

## Team Members

| # | Name | Role |
|---|------|------|
| 1 | Fathima Bint-Khalid | Project Coordinator |
| 2 | Umar A. Hasan | Systems Architect |
| 3 | Saumya Aditya Patel | Software Engineer & QA Lead |
| 4 | David Huynh | Front End & UX/UI |

## Task Delegation

- **Fathima Bint-Khalid** — Report writing, requirements, research, submission. Tasks: 1.1 & 1.6. Report sections: 1–5, 6.
- **Umar A. Hasan** — System architecture, sequence diagrams, process model. Tasks: 1.1 & 1.5. Report sections: 7d, 9.
- **Saumya Aditya Patel** — Use case diagram, class diagram, GitHub management. Tasks: 1.1–3. Report sections: 7a, b, & c.
- **David Huynh** — UI design, frontend components, Google Maps integration. Tasks: 1.1 & 1.4. Report sections: 8.

## Project Overview

DineMatch is a full-stack web application that allows users to discover restaurants tailored to their personal preferences. The platform accepts multi-dimensional search inputs — including cuisine type, price range, dining vibe, and geographic location — and returns ranked, relevant restaurant results. Users can create accounts, save favorite restaurants, leave reviews, and interact with an embedded map view for a seamless discovery experience.

## Technology Stack

| Layer | Technology | Purpose |
|-------|------------|---------|
| Frontend | React.js | Dynamic, component-based UI |
| Styling | Tailwind CSS | Responsive, mobile-friendly design |
| Backend | Java / Spring Boot | RESTful API, business logic, auth |
| Database | PostgreSQL | Relational data: users, restaurants, reviews |
| Authentication | Spring Security + JWT | Secure user login and session management |
| Maps | Google Maps API | Location-based search and map display |
| Version Control | Git / GitHub | Source control, CI/CD pipeline |
| Prototyping | Figma | UI/UX wireframes and interactive prototype |

## Core Features

### Smart Search & Filtering
- Filter restaurants by cuisine type (Italian, Mexican, Thai, etc.)
- Price range filter using a budget selector ($ to $$$$)
- Vibe/atmosphere tags: casual, date night, family-friendly, rooftop, etc.
- Location-aware search using geolocation or manual address entry
- Results ranked by relevance score computed server-side

### User Accounts & Saved Favorites
- Secure registration and login with email/password via JWT authentication
- User profile page displaying saved restaurants and review history
- One-click save/unsave restaurants to a personal favorites list
- Personalized recommendation feed based on past searches and favorites

### Reviews & Ratings
- Authenticated users can post text reviews and a 1–5 star rating
- Each restaurant displays an aggregate rating and review count
- Users can edit or delete their own reviews
- Review feed sorted by most recent or highest rated

### Google Maps Integration
- Interactive embedded map on the search results page
- Restaurant pins on the map link to their detail page
- Distance from user's current location displayed on each result card
- Directions link opens Google Maps for turn-by-turn navigation

### Mobile-Friendly & Responsive Design
- Responsive layout built with React + Tailwind CSS for all screen sizes
- Touch-optimized filter controls and map interactions on mobile
- Fast load times via lazy loading of restaurant images and map tiles

## Software Process Model

The team follows Agile/Scrum with two-week sprints. Each sprint delivers a working, testable increment of the platform. Sprint planning, async standups, sprint reviews, and retrospectives are conducted throughout the project lifecycle. GitHub Issues and a Kanban board serve as the primary backlog and progress tracking tools.

## Software Requirements

### Functional Requirements

- **FR1:** Users can filter restaurants by cuisine, price, location, and vibe.
- **FR2:** The system ranks restaurants by a relevance score based on the user's filters.
- **FR3:** Users can create an account and log in using secure JWT authentication.
- **FR4:** Logged-in users can bookmark restaurants and view their saved list.
- **FR5:** Logged-in users can leave a star rating and text review on any restaurant.
- **FR6:** Restaurant search results include an embedded Google Maps view.
- **FR7:** The system suggests restaurants based on a user's past searches and bookmarks.

### Non-Functional Requirements

**Product Requirements:**
- Performance: Search results load in under 3 seconds.
- Space: The app uses no more than 500MB of server storage.
- Usability: A new user can search for a restaurant without any tutorial.
- Dependability: The system stays up 99% of the time during peak hours.
- Security: Passwords are stored securely and JWT tokens expire after 24 hours.

**Organizational Requirements:**
- Environmental: The app can be deployed on standard cloud infrastructure like AWS.
- Operational: The system follows Google Maps API usage guidelines.
- Development: All code changes are committed to the team's GitHub repo.

**External Requirements:**
- Accounting: The system logs all bookmark and review activity.
- Safety/Security: The system is protected against SQL injection and XSS attacks.
- Ethical: User data is only used for recommendations, nothing else.
- Legislative: Users must opt in before their data is used for personalized recommendations.

## High-Level Architecture

The system follows a three-tier architecture:

| Tier | Description |
|------|-------------|
| Presentation | React.js single-page application served via a CDN. Communicates with the backend exclusively through RESTful API calls over HTTPS. |
| Application | Spring Boot application exposing REST endpoints for auth, search, user profiles, favorites, and reviews. Hosts the recommendation scoring logic. |
| Data | PostgreSQL database storing users, restaurants, reviews, and favorites. Indexed on location coordinates and cuisine tags for fast queries. |

## Repository

This repository contains all source code, documentation, and deliverables for the DineMatch project.
