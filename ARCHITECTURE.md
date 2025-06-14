# vid-gen-ai Architecture

## Overview
AI-powered platform that generates marketing videos for small businesses. Upload product info, select a theme, and get a video!

### Problem Statement
Extracted from existing codebase

### Target Audience
Development team

### Core Entities
User, Product, VideoTemplate, Job, Theme

## Design System

### Typography
- **Font**: Roboto
- **Font Stack**: ``
- **Google Fonts**: 
- **Rationale**: Roboto is a widely used and legible sans-serif font suitable for user interfaces and marketing materials.

### Color Palette


- **primary**: `#007bff` - Primary color for buttons, links, and active states. Suggests trust and reliability.
- **secondary**: `#6c757d` - Secondary color for less important elements, such as form labels and inactive states. Provides contrast and clarity.

## System Architecture

### 1. Core Components & Rationale
The system consists of several key components. The `User` component manages user authentication and authorization. The `Product` component stores information about the products the user wants to promote. The `VideoTemplate` component defines the structure and style of the generated videos. The `Job` component manages the video generation process, tracking its status and results. The `Theme` component allows the user to select the general look and feel of the video. The frontend components (`app-*`, `appearance-*`, `breadcrumbs`, etc.) are responsible for rendering the user interface and interacting with the backend API. The `Controller` manages the business logic and orchestration of different parts of the application.

### 2. Database Schema Design
The database schema includes the following tables: `users` (stores user information, likely including username, email, password, etc.), `products` (stores product information, such as name, description, images, etc.), `video_templates` (stores video template data, including layout, animations, etc.), `jobs` (stores information about video generation jobs, including status, progress, input data, etc.), `themes` (stores different themes that can be applied to the videos), and `cache` (likely used for caching API responses or other data). Relationships between tables would include: User has many Products, User has many Jobs, Job uses a VideoTemplate, Job uses a Theme, Product is associated with a Job.

### 3. API Design & Key Endpoints
The API follows a RESTful design pattern. Key endpoints include: `/api/users` (for user management), `/api/products` (for product management), `/api/videos` (for video generation and retrieval), `/api/templates` (for managing video templates), `/api/themes` (for retrieving themes). These endpoints likely support standard CRUD operations (Create, Read, Update, Delete) using HTTP methods like GET, POST, PUT, and DELETE. Authentication and authorization are likely implemented using JWT (JSON Web Tokens) or similar mechanisms.

### 4. Frontend Structure
The frontend is structured as a component-based architecture. The `app-shell` component serves as the main layout container. The `app-header` and `app-sidebar` provide navigation and branding elements. The `app-content` component displays the main content of the page. The `breadcrumbs` component provides navigation breadcrumbs. The `user-info` and `user-menu-content` components manage user profile information and settings. The `appearance-*` components handle theme and visual customizations. This structure promotes code reusability and maintainability.

## Feature Implementation Roadmap

### 1. User Authentication
Allows users to register, log in, and manage their accounts.


### 2. Product Management
Allows users to add, edit, and delete product information.


### 3. Video Generation
Generates marketing videos based on user-provided product information and selected themes.


### 4. Theme Selection
Allows users to choose from a variety of video themes.


### 5. Video Preview
Allows users to preview the generated video before downloading it.


### 6. Social Sharing
Allows users to easily share their generated videos on social media platforms.


### 7. Template Management
Allows admins to manage and create new video templates.


## Metadata
- **Generated**: 2025-06-14T15:54:20.928036+00:00
- **Project Type**: Laravel React Starter Kit
- **Architecture Version**: 1.0.0

---
*This architecture document is maintained by the CodeWebMobile AI system and should be the source of truth for all development decisions.*
