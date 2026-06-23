# Cheta

> Remember. Plan. Grow.

---

# 📐 Wireframes and Page Specifications

## Overview

This document defines the layout and functionality of every page in Cheta.

The goal is to create a consistent, calm, and premium experience inspired by:

* Apple
* Arc Browser
* Notion
* Linear

---

# 🏠 Dashboard

## Purpose

Provide a central overview of life and progress.

---

## Layout

```text
-------------------------------------------------------
Sidebar | Main Content Area           | Context Panel
-------------------------------------------------------

Today's Focus

Weekly Tasks

AI Suggestions

Recent Activity

Quick Notes

Recent Memories

Upcoming Items
```

---

## Components

### Today's Focus

Shows:

* Priority tasks
* Overdue tasks

---

### Weekly Tasks

Shows:

* Progress bar
* Upcoming tasks

---

### AI Suggestions

Examples:

* Update CV
* Finish Spring Boot course
* Continue inventory project

---

### Recent Activity

Shows:

* Completed tasks
* Recent chats
* New memories

---

### Context Panel

Contains:

* Quick Notes
* Recent Memories
* Upcoming Events

---

# 🤖 Chat Page

## Purpose

Natural conversations with Cheta.

---

## Layout

```text
-----------------------------------------
Header

Conversation Area

Suggestions

Input Area
-----------------------------------------
```

---

## Components

### Conversation

Chat bubbles

---

### Suggestions

Examples:

* What should I focus on this week?
* Summarise my goals.
* Have I forgotten anything?

---

### Input Area

Supports:

* Text
* Voice (future)
* Attachments (future)

---

# ✅ Planner

## Purpose

Turn intentions into actions.

---

## Tabs

### Today

Tasks due today.

---

### This Week

Weekly overview.

---

### Upcoming

Future tasks.

---

### Completed

Finished tasks.

---

## Components

Task Card

Contains:

* Checkbox
* Title
* Priority
* Due Date

---

# 🎯 Goals Page

## Purpose

Track long-term goals.

---

## Sections

### Annual Goals

Examples:

* Become Software Engineer

---

### Monthly Goals

Examples:

* Finish Spring Boot

---

### Weekly Goals

Examples:

* Complete 5 applications

---

## Components

Goal Card

Contains:

* Progress bar
* Deadline
* Milestones

---

# 📂 Projects Page

## Purpose

Manage ideas and projects.

---

## Views

### Grid View

Project cards.

---

### Kanban View

Ideas

In Progress

Completed

---

## Project Card

Contains:

* Title
* Description
* Difficulty
* Tech Stack
* Progress

---

# 🧠 Memory Page

## Purpose

Show what Cheta remembers.

---

## Categories

Goals

Projects

Career

Habits

Preferences

---

## Memory Card

Contains:

* Memory
* Importance
* Date
* Source

Actions:

* Pin
* Edit
* Delete

---

# 💼 Career Page

## Purpose

Support career development.

---

## Tabs

Applications

Interviews

Achievements

CV

LinkedIn

---

## Application Card

Contains:

* Company
* Role
* Status
* Date Applied

---

## Interview Card

Contains:

* Company
* Date
* Notes

---

# 📝 Notes Page

## Purpose

Quick idea capture.

---

## Layout

Simple editor.

---

## Sections

Recent Notes

Pinned Notes

Archived Notes

---

# 🔔 Notifications

## Types

Task Reminder

AI Suggestion

Weekly Review

Memory Reminder

---

# ⚙️ Settings

## Sections

### Profile

Name

Email

Timezone

---

### Appearance

Theme

Light Mode

Dark Mode

---

### AI

Memory Settings

Personality

Response Style

---

### Security

Password

Sessions

Privacy

---

# 🌙 Dark Mode

Uses:

* Deep earth tones
* Warm contrast
* Soft shadows

---

# 📱 Mobile Layout

Bottom Navigation:

```text
Home

Chat

Tasks

Profile
```

Additional pages accessible through menu.

---

# Floating AI

Cheta is available globally.

Floating button appears on every page.

Examples:

> What should I do next?

> Have I forgotten anything?

> Summarise this page.

---

# UX Principles

## Calm

Avoid clutter.

---

## Memory First

Important information should remain visible.

---

## AI Everywhere

Users should never feel disconnected from Cheta.

---

## Progressive Disclosure

Advanced features should appear gradually.

---

## Consistency

Interactions should feel familiar across pages.

--------------------





I would actually recommend creating a dedicated folder structure like this:
docs/
│
├── images/
│     ├── logo.png
│     ├── cheta-african-theme.png
│     ├── dashboard-light.png
│     ├── dashboard-dark.png
│     ├── sidebar.png
│     └── chat-page.png
│
├── vision.md
├── prd.md
├── information-architecture.md
├── database-design.md
├── system-architecture.md
├── design-system.md
├── backlog.md
├── sprint-plan.md
└── roadmap.md

Then inside your markdown files, use:

![Cheta Theme](images/cheta-african-theme.png)

GitHub will render the image beautifully.

My suggestion is that as we continue with Documents 7–12, we should also start creating:

dashboard-light.png
dashboard-dark.png
chat-page.png
planner-page.png
memory-page.png
project-page.png

so that by the time we're done, you'll have not just documentation but almost a complete startup blueprint with diagrams and UI mockups, similar to what a product team would produce before development starts.