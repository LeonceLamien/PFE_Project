<div align="center">

# Kicker Da Vinci

*A web platform for following foosball clubs, players and competitions*

![Angular](https://img.shields.io/badge/Angular-15-dd0031.svg?logo=angular)
![TypeScript](https://img.shields.io/badge/TypeScript-4.8-3178c6.svg?logo=typescript)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.2-7952b3.svg?logo=bootstrap)
![Project](https://img.shields.io/badge/Project-Academic-green.svg)

[About](#about) • [Features](#features) • [Tech Stack](#tech-stack) • [Getting Started](#getting-started) • [Project Structure](#project-structure)

<br/>

<img src="Frontend/src/assets/images/Babyfoot.png" alt="Foosball table used by Kicker Da Vinci" width="760"/>

</div>

---

## About

**Kicker Da Vinci** is the Angular frontend of a web platform for a foosball federation. It brings together information about clubs, players, divisions and competitions, with dedicated pages for fixtures, match recaps and archives.

The application connects to a REST API for its data and account operations. This repository contains the frontend; the API is configured separately.

### Project highlights

- Built as a single-page application with Angular and TypeScript.
- Organizes federation information into dedicated, navigable views.
- Uses Angular services and `HttpClient` to retrieve and submit data to the API.
- Includes account registration and login screens.
- Provides a responsive interface using Bootstrap and Angular Material.

---

## Features

| Area | What you can explore |
|------|----------------------|
| **Competitions** | Competition pages, divisions, club standings and fixtures |
| **Players** | Player directory with ranking and division filters |
| **Clubs** | Club directory with contact and location information |
| **Match recaps** | Recap pages associated with games |
| **Archives** | Past games and federation records |
| **Accounts** | Registration and login forms |
| **Federation information** | Game rules, useful links and an about page |

---

## Tech Stack

| Technology | Purpose |
|------------|---------|
| **Angular 15** | Frontend framework and routing |
| **TypeScript** | Application logic and data models |
| **RxJS** | Asynchronous API requests |
| **Bootstrap 5** | Responsive layout and styling |
| **Angular Material** | UI components |
| **Karma / Jasmine** | Unit test runner and framework |
| **Azure Pipelines** | Automated production build |

---

## Getting Started

### Prerequisites

- Node.js 16
- npm

### Installation

```bash
git clone https://github.com/<your-username>/<repository-name>.git
cd <repository-name>/Frontend
npm ci
```

Replace the clone URL and repository name with the public GitHub repository details.

### Run locally

```bash
npm start
```

Open [http://localhost:4200](http://localhost:4200). A development proxy for `/api` is defined in `Frontend/src/proxy.config.json`; the application also reads its API base URL from the environment configuration.

### Build and test

```bash
# Production build
npm run build

# Unit tests (non-interactive)
npm test -- --watch=false
```

The production build is written to `Frontend/dist/frontend`.

### API configuration

The frontend uses the API base URL configured in `Frontend/src/environments/environments.ts`. The checked-in configuration points to the Kicker Da Vinci API hosted on Azure. Some account and data features therefore require that service to be reachable; update the base URL when connecting to another backend.

---

## Project Structure

```text
kickerdavinci_frontend/
├── Frontend/
│   ├── src/
│   │   ├── app/
│   │   │   ├── Auths/             # Registration, login and user services
│   │   │   ├── competitions/      # Competitions, divisions and game models
│   │   │   ├── game-recaps/       # Match recap views and service
│   │   │   ├── archives/          # Archived game views
│   │   │   ├── list-players/      # Player directory and filters
│   │   │   ├── list-clubs/        # Club directory
│   │   │   ├── leader-player/     # Player leaderboard
│   │   │   ├── game-rules/        # Rules page
│   │   │   ├── important-links/   # Federation links
│   │   │   └── app-routing.module.ts
│   │   ├── assets/images/         # Foosball images
│   │   └── environments/          # API endpoint configuration
│   ├── angular.json
│   └── package.json
└── azure-pipelines.yml            # CI build pipeline
```

---

## Project Context

This project was developed as an academic project. The repository demonstrates the frontend implementation of a federation portal, including component-based UI development, routing, typed data models, API integration and unit-test setup.
