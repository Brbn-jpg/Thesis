# Design and Implementation of a Culinary Recipe Management System

**Engineering Thesis** **Author:** Jakub Kuźnicki  
**University:** Vistula University of Finance and Business  
**Year:** 2026

## Project Overview

This repository contains the source code for the engineering thesis "Design and Implementation of a Culinary Recipe Management System". The primary objective of this project was to create a comprehensive web application ("Cibaria") that allows users to manage, browse, and share culinary recipes.

The system addresses the problem of cluttered and non-intuitive recipe platforms by providing a clean, responsive interface and a robust filtering system. The application is built using a modern full-stack architecture, utilizing Java/Spring Boot for the backend and Angular for the frontend.

**Note:** The engineering thesis document associated with this project is written in **Polish**.

**Application Demo:** [here](https://cibaria.vercel.app/)
_(It might take a while for backend to run since its on a free hosting)_

_[Link to repository with code](<(https://github.com/Brbn-jpg/Recipe-management-app)>)_

## Key Features

The system is divided into modules catering to different user roles (Guest, User, Administrator):

- **Authentication & Authorization:** Secure user registration and login system based on JWT (JSON Web Tokens) with BCrypt password hashing.
- **Recipe Management:** Users can create, update, and delete their own recipes.
- **Multimedia Support:** Integration with Cloudinary API for storing and optimizing recipe images and user avatars.
- **Advanced Search & Filtering:** Filtering recipes by category, preparation time, difficulty level, number of servings, language, and ingredients.
- **Social Interactions:** Functionality for rating recipes (1-5 scale) and adding them to a "Favorites" list.
- **User Profiles:** Profile management including avatar changes, background images, and password updates.
- **Administration Panel:** Dedicated dashboard for administrators to manage users (ban/delete/promote) and moderate content.

## Technology Stack

The project utilizes a layered architecture with the following technologies:

### Backend

- **Language:** Java 21
- **Framework:** Spring Boot 3
- **Database:** PostgreSQL 15
- **ORM:** Hibernate / Spring Data JPA
- **Security:** Spring Security, JWT
- **Testing:** JUnit 5, Mockito

### Frontend

- **Framework:** Angular 18
- **Architecture:** Standalone Components
- **State Management:** RxJS (Reactive programming)
- **Styling:** CSS3, Responsive Design
- **Testing:** Jasmine, Karma

### Infrastructure & DevOps

- **Containerization:** Docker, Docker Compose
- **Web Server:** Nginx (serving the Angular application)
- **Performance Testing:** K6

## Architecture

The system follows a RESTful architecture pattern. The application is fully containerized, ensuring consistency across different environments.

- **Database Layer:** PostgreSQL container storing relational data.
- **Backend Layer:** Spring Boot application running on JRE 21 Alpine, exposing REST endpoints.
- **Frontend Layer:** Angular application built and served via Nginx container.

## Installation and Setup

### Prerequisites

- Docker and Docker Compose installed on the host machine.
- Git for cloning the repository.

### Build and Run

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/Brbn-jpg/Recipe-management-app
    cd Recipe-management-app
    ```

2.  **Configuration:** Create a `.env` file in the root directory and populate it with the required environment variables (Database credentials, Cloudinary API keys, JWT secret).

3.  **Run the application using Docker Compose:**

    ```bash
    docker-compose up --build
    ```

4.  **Access the application:**

    _Frontend: http://localhost:4200_

    _Backend API: http://localhost:8080/api_

## Testing

The project includes a comprehensive testing suite:

- **Unit Tests:** Verifying business logic in isolation.
- **Integration Tests:** Verifying the interaction between Spring Boot components and the database (using H2 in-memory DB).
- **Performance Tests:** K6 scripts located in the `/performance-tests` directory to simulate load.
