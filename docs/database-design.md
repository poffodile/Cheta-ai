# Cheta

> Remember. Plan. Grow.

---

# 🗄️ Database Design and Domain Model

## Overview

Cheta uses PostgreSQL (Supabase) as its primary database.

The database is designed around several domains:

* User Domain
* Planning Domain
* AI Domain
* Memory Domain
* Projects Domain
* Goals Domain
* Career Domain
* Notification Domain

The architecture should support growth while remaining simple during the MVP phase.

---

# 👤 User Domain

## profiles

Stores user information.

### Purpose

Provide personalisation and account settings.

### Attributes

* id
* user_id
* full_name
* username
* email
* timezone
* avatar_url
* onboarding_completed
* created_at
* updated_at

---

## settings

Stores user preferences.

### Purpose

Configure the application.

### Attributes

* id
* user_id
* theme
* language
* ai_personality
* notification_enabled
* memory_enabled
* created_at

---

# ✅ Planning Domain

## tasks

Stores tasks.

### Purpose

Convert intentions into actions.

### Attributes

* id
* user_id
* title
* description
* priority
* category
* status
* due_date
* completed_at
* created_at

---

## subtasks

Stores child tasks.

### Purpose

Break work into smaller actions.

### Attributes

* id
* task_id
* title
* completed
* created_at

---

# 🎯 Goals Domain

## goals

Stores long-term goals.

### Purpose

Track progress.

### Attributes

* id
* user_id
* title
* description
* target_date
* progress_percentage
* status
* created_at

---

## goal_milestones

Stores milestones for goals.

### Purpose

Break goals into stages.

### Attributes

* id
* goal_id
* title
* completed
* created_at

---

# 📂 Project Domain

## projects

Stores project ideas and active projects.

### Attributes

* id
* user_id
* title
* description
* status
* difficulty
* tech_stack
* github_url
* created_at

---

## project_milestones

Stores project milestones.

### Attributes

* id
* project_id
* title
* status
* created_at

---

# 🤖 AI Domain

## chat_sessions

Represents conversations.

### Attributes

* id
* user_id
* title
* created_at

---

## chat_messages

Stores messages.

### Attributes

* id
* session_id
* role
* content
* timestamp

Role values:

* user
* assistant
* system

---

# 🧠 Memory Domain

Memory is one of the most important parts of Cheta.

---

## memories

Stores important facts.

Examples:

* User is preparing for graduate jobs.
* User dislikes eggs.
* User wants to learn Spring Boot.

### Attributes

* id
* user_id
* category
* content
* importance_score
* pinned
* source
* created_at

---

## memory_embeddings

Stores vector embeddings.

Purpose:

Semantic search.

### Attributes

* id
* memory_id
* embedding_vector

Future implementation using pgvector.

---

# 📝 Notes Domain

## notes

Stores brain dumps and ideas.

### Attributes

* id
* user_id
* title
* content
* archived
* created_at

---

# 🔔 Notification Domain

## notifications

Stores notifications.

### Types

* Reminder
* AI Suggestion
* Weekly Review

### Attributes

* id
* user_id
* title
* type
* read
* created_at

---

# 💼 Career Domain

## applications

Stores job applications.

### Attributes

* id
* user_id
* company
* role
* status
* applied_date

---

## interviews

Stores interviews.

### Attributes

* id
* application_id
* interview_date
* notes

---

# 📚 Learning Domain

## learning_paths

Stores learning goals.

### Attributes

* id
* user_id
* title
* progress_percentage

---

## resources

Stores resources.

### Attributes

* id
* learning_path_id
* type
* url
* title

---

# ❤️ Health Domain

Future Version

## workouts

## meals

## health_logs

## weight_entries

## sleep_records

---

# Relationships

User

↓

Tasks

↓

Subtasks

---

User

↓

Goals

↓

Goal Milestones

---

User

↓

Projects

↓

Project Milestones

---

User

↓

Chat Sessions

↓

Chat Messages

---

User

↓

Memories

↓

Embeddings

---

User

↓

Applications

↓

Interviews

---

User

↓

Notes

---

User

↓

Notifications

---

# MVP Tables

Version 0.1 only requires:

* profiles
* settings
* tasks
* subtasks
* chat_sessions
* chat_messages
* memories
* notes
* notifications

Everything else can be introduced later.

---

# Design Principles

### Build Simple

Avoid unnecessary complexity.

### Design for Growth

Prepare for future modules.

### Separate Domains

Keep responsibilities clear.

### Memory First

Memory is a core feature.

### AI Everywhere

AI should integrate naturally across all domains.
