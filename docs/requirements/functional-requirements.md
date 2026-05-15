# Functional Requirements

## RF-01 - User Authentication

The system must allow authentication using email and password.

---

## RF-02 - Professionals Registration

The system must allow the registration of professionals containing:
- full name
- nickname
- CPF
- one or multiple roles

---

## RF-03 - Professionals Editing

The system must allow editing registered professionals.

---

## RF-04 - Professionals Deletion

The system must allow deletion of professionals.

---

## RF-05 - Professionals Search

The system must allow searching professionals by:
- name
- nickname
- role

---

## RF-06 - Teams Creation

The system must allow creating production teams.

---

## RF-07 - Team Management

The system must allow:
- adding members
- removing members
- editing team roles

---

## RF-08 - Team Role Override

The system must allow changing a professional role inside a team without modifying the original professional registration.

---

## RF-09 - Teams Export

The system must allow exporting teams organized by roles.

---

## RF-10 - Access Control

The system must support:
- master users
- common users

---

## RF-11 - Master Permissions

Master users must be able to:
- register professionals
- edit professionals
- delete professionals
- manage users

---

## RF-12 - Common User Permissions

Common users must be able to:
- create teams
- edit teams
- export teams# Product Backlog

| ID | Task | Priority |
|----|------|-----------|
| TASK-01 | Configure project structure | High |
| TASK-02 | Configure React application | High |
| TASK-03 | Configure Supabase | High |
| TASK-04 | Create database model | High |
| TASK-05 | Create employees entity | High |
| TASK-06 | Create teams entity | Medium |
| TASK-07 | Create productions entity | Medium |
| TASK-08 | Create reports module | Medium |# Guerrilha Manager

## Objective

Guerrilha Manager is a workforce and production management system designed for audiovisual operations.

The system aims to manage:
- employees
- teams
- productions
- operational reports
- workforce allocation

---

## Technologies

- React
- PostgreSQL
- Supabase
- Git/GitHub

---

## Engineering Practices

- Scrum
- UML
- Requirements Engineering
- GitFlow
