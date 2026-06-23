# Cheta

> Remember. Plan. Grow.

---

# 🏗️ System Architecture and Folder Structure

## Overview

Cheta is designed using a feature-based architecture.

The goal is to:

* Keep features isolated.
* Improve maintainability.
* Support future growth.
* Make onboarding easier.
* Reduce coupling between modules.

---

# High-Level Architecture

```text
Frontend (Next.js)

↓

API Layer

↓

Services

↓

Database (Supabase)

↓

OpenAI + Memory Layer
```

---

# Tech Stack

## Frontend

* Next.js
* TypeScript
* Tailwind CSS
* shadcn/ui

---

## Backend

* Next.js Route Handlers

---

## Database

* PostgreSQL
* Supabase

---

## AI

* OpenAI API

---

## Hosting

* Vercel

---

## Authentication

* Supabase Auth

---

# Folder Structure

```text
src/

├── app/
│
├── components/
│
├── features/
│
├── hooks/
│
├── services/
│
├── types/
│
├── lib/
│
├── constants/
│
├── providers/
│
├── store/
│
├── styles/
│
├── public/
│
└── docs/
```

---

# App Directory

Contains:

```text
app/

dashboard/

chat/

planner/

goals/

projects/

memory/

career/

notes/

settings/
```

Purpose:

Routes and layouts.

---

# Components Directory

Contains reusable UI.

```text
components/

ui/

layout/

navigation/

cards/

forms/

tables/

dialogs/
```

Purpose:

Shared components.

Examples:

* Button
* Card
* Modal
* Sidebar
* Header

---

# Features Directory

This is where most business logic lives.

```text
features/

auth/

dashboard/

planner/

chat/

memory/

projects/

goals/

career/

notes/

notifications/
```

Each feature owns:

* components
* hooks
* services
* types

Example:

```text
features/planner/

components/

hooks/

services/

types/
```

---

# Hooks Directory

Reusable hooks.

Examples:

```text
useTheme()

useDebounce()

useMediaQuery()

useLocalStorage()
```

---

# Services Directory

Handles external communication.

Examples:

```text
services/

supabase/

openai/

memory/

notifications/
```

Purpose:

Separate business logic from UI.

---

# Types Directory

Stores TypeScript types.

Examples:

```text
task.ts

goal.ts

memory.ts

project.ts

user.ts
```

---

# Constants Directory

Stores:

```text
routes.ts

themes.ts

priorities.ts

categories.ts
```

---

# Providers Directory

Application-wide providers.

Examples:

```text
ThemeProvider

AuthProvider

QueryProvider
```

---

# Store Directory

Global state.

Possible tools:

* Zustand
* React Query

Examples:

```text
authStore

themeStore

sidebarStore
```

---

# Styles Directory

Contains:

```text
globals.css

themes.css
```

---

# Public Directory

Assets:

```text
logo/

icons/

images/

illustrations/
```

---

# API Layer

```text
api/

chat/

tasks/

goals/

projects/

memory/

notifications/
```

Purpose:

Handle communication between frontend and services.

---

# AI Layer

Responsible for:

* Chat
* Suggestions
* Summaries
* Reflection
* Task generation

Future agents:

* Career Agent
* Project Agent
* Learning Agent
* Fitness Agent

---

# Memory Layer

Responsibilities:

* Store memories
* Retrieve memories
* Rank memories
* Pin memories
* Delete memories

Future:

Vector search with pgvector.

---

# State Management

## Local State

React state.

---

## Server State

React Query.

---

## Global State

Zustand.

Used for:

* Theme
* Sidebar
* User preferences

---

# Authentication Flow

```text
User

↓

Supabase Auth

↓

Session

↓

Protected Routes
```

---

# Data Flow

```text
UI

↓

API Route

↓

Service

↓

Database

↓

Response

↓

UI Update
```

---

# Logging and Monitoring

Future:

* Sentry
* Vercel Analytics

---

# Future Mobile Architecture

React Native + Expo

Shared:

* Types
* Services
* API contracts

Goal:

Single backend supporting:

* Web
* Mobile
* Extensions

---

# Design Principles

## Feature First

Group by feature.

---

## Keep Components Dumb

Business logic belongs in services.

---

## Separation of Concerns

UI should not know database details.

---

## Reuse

Prefer shared components.

---

## Simplicity

Avoid premature complexity.

---

## Scale Gradually

Build for v0.1.

Design for v1.0.
