# GitLab Group/Project Inheritance Model for Scaled Scrum

GitLab uses a hierarchical structure where **groups** contain one or more **projects**. This model enables consistent configuration, standardized labels, and scalable planning across multiple teams working under a single initiative.

## 🔧 Core Concepts

| Layer        | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| **Group**    | The parent container for related projects. Controls global settings, boards, and labels. |
| **Project**  | The working space for specific components, services, or team deliverables. Inherits from the group. |
| **Issues**   | Work items (e.g., user stories, bugs) tracked at the project level.         |
| **Labels**   | Tagging system that cascades from group → project. Scoped labels enforce consistency. |
| **Boards**   | Visual planning boards. Group-level boards allow cross-project planning.    |
| **Iterations** | Timeboxes for sprints, created at the group level and applied across projects. |

---

## 🧬 How Inheritance Works

Settings and assets created at the **group level** cascade down to all child projects:

- ✅ **Scoped Labels**: Standardize workflows like `status::in progress`, `type::bug`, `priority::now`.
- ✅ **Epics & Boards**: Enable planning across multiple projects with a shared backlog.
- ✅ **Iteration Cadences**: Apply sprint planning cycles consistently across all child teams.
- ✅ **Roadmaps & Milestones**: Aggregate progress reporting at the program level.

This allows a centralized PMO, governance office, or DevSecOps lead to define key agile structures that all participating teams use.

---

## 📘 Example Use Case (Fictional)

**Program Name**: `InterGov-Federated-Platform`  
**Group URL**: `gitlab.com/intergov-federated-platform`

| Group                 | Project                      | Description                                  |
|-----------------------|------------------------------|----------------------------------------------|
| `intergov-federated-platform` | `data-api-service`              | Backend component managed by Team A          |
|                        | `geospatial-ui`              | Frontend mapping UI managed by Team B        |
|                        | `policy-audit-module`        | Governance logic managed by Team C           |

All projects inherit:
- A shared **release planning epic board**
- Sprint iteration cadence (2 weeks)
- Standard labels like `type::story`, `status::done`, `priority::next`

---

## 🧠 Benefits for Multi-Team Delivery

- **Consistency**: Ensures common Agile language across all teams
- **Transparency**: Shared boards and sprints create visibility for leadership
- **Efficiency**: No need to recreate the same labels/boards per project
- **Traceability**: Link epics → issues → merge requests across teams

---

## 📎 Related GitLab Features

- [Scoped Labels](https://docs.gitlab.com/ee/user/project/labels.html#scoped-labels)
- [Epics and Roadmaps](https://docs.gitlab.com/ee/user/group/epics/)
- [Iteration Cadences](https://docs.gitlab.com/ee/user/group/iterations/)
- [Issue Boards](https://docs.gitlab.com/ee/user/project/issue_board.html)

---

## Diagram## 🖼️ GitLab Inheritance Structure

![GitLab Inheritance](../gitlab-inheritance-structure.png)



## ✅ Summary

GitLab’s inheritance model is ideal for managing scaled Scrum delivery in environments with:

- Multiple teams or partners
- Program-wide release cycles
- Shared backlogs and planning boards
- Need for governance, traceability, and DevSecOps alignment

This structure enables modern product delivery workflows — even in highly segmented or federated ecosystems.
