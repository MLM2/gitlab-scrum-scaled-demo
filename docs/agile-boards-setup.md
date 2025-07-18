# Agile Boards Setup for Scaled Scrum in GitLab

This document explains how to configure GitLab’s epic, issue, and sprint boards using a consistent, group-level structure to support scaled Scrum delivery across multiple teams and projects.

## 🧭 Overview

In scaled environments—such as federated DevSecOps platforms or multi-agency coalitions—Scrum boards must support:

- Prioritization of high-level features (epics)
- Breakdown of work into user stories (issues)
- Sequencing across multiple upcoming sprints (iterations)

GitLab allows you to do this using **three core board types**, all of which can be configured at the **group level** and inherited by child projects.

---

## 📌 Key Boards to Set Up

| Board Name       | Purpose                                          |
|------------------|--------------------------------------------------|
| **Release Planning (Epic Board)** | Manage and prioritize high-level features (epics) |
| **Backlog (Issue Board)**         | Sequence stories across upcoming sprints         |
| **Current Sprint (Issue Board)**  | Track sprint progress with status-based swimlanes |

---

## 🗂️ 1. Release Planning Board (Epic-Level)

This board helps your product owners and business leads prioritize high-level deliverables.

### ✅ Steps:
- Navigate to your group → **Plan > Epic Boards**
- Create a new board: `Release Planning`
- Add lists for:
  - `priority::later`
  - `priority::next`
  - `priority::now`
  - `Closed`

### 🔖 Labels to Use:
- `priority::now`
- `priority::next`
- `priority::later`

These scoped labels allow mutual exclusivity — only one priority label per epic.

---

## 🗃️ 2. Backlog Board (Issue-Level)

This board lets teams break epics into granular, vertically sliced user stories and assign them to future sprints.

### ✅ Steps:
- Go to **Plan > Issue Boards**
- Create a new board: `Backlog`
- Add one list for each **upcoming iteration** (e.g., Sprint 1, Sprint 2, Sprint 3)
- Enable **Group by Epic** to link stories to parent features

### 📌 Tip:
Add a list with `status::refine` label to hold stories that need grooming before sprint planning.

---

## 🚦 3. Current Sprint Board

Visualize in-flight work and identify bottlenecks during sprint execution.

### ✅ Steps:
- Create another Issue Board: `Current Sprint`
- Filter it to only show issues assigned to the **current iteration**
- Add lists based on **status labels**:
  - `status::refine`
  - `status::ready`
  - `status::in progress`
  - `status::review`
  - `status::acceptance`
  - `status::done`

### 🔖 Scoped Labels to Use:

| Scope     | Values                             |
|-----------|-------------------------------------|
| `status::` | refine, ready, in progress, review, acceptance, done |
| `type::`   | story, bug, maintenance            |

Using scoped labels ensures clarity during sprint ceremonies and daily standups.

---

## 🧠 Why Group-Level Setup Matters

When you create these boards and labels **at the group level**, every project beneath it inherits:

- The same backlog structure
- Shared understanding of story types and sprint stages
- Consistent terminology for cross-team coordination

This avoids duplication and helps large programs operate with agility and clarity.

---

## 🧪 Example Workflow

1. **PO creates an epic** in the Release Planning board
2. **Team breaks epic into issues** using vertical slicing
3. **Stories are tagged** (`type::story`, `status::refine`)
4. **Refined stories are added to Backlog** and assigned to future iterations
5. **During Sprint**, stories move across the Current Sprint board:  
   `ready` → `in progress` → `review` → `done`
6. **Burndown charts** reflect velocity and progress automatically

---

## 📎 References

- [GitLab Issue Boards](https://docs.gitlab.com/ee/user/project/issue_board.html)
- [Epic Boards](https://docs.gitlab.com/ee/user/group/epics/#epic-boards)
- [Scoped Labels](https://docs.gitlab.com/ee/user/project/labels.html#scoped-labels)
- [Iteration Reports](https://docs.gitlab.com/ee/user/group/iterations/#view-the-iteration-report)

---

## ✅ Summary

With these boards in place, GitLab enables structured, transparent, and flexible Scrum workflows that scale across distributed teams. This is especially valuable in complex programs where multiple systems, vendors, or agency teams must collaborate without friction.
