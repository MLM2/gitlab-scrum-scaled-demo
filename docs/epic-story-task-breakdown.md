# Epic → Story → Task Breakdown in GitLab Scrum

In scaled agile delivery, breaking work into the right-sized components is critical. GitLab supports a natural hierarchy of:

- **Epic** = Feature (high-level capability)
- **Issue** = User Story (delivers user value)
- **Checklist / Comments** = Tasks (implementation steps)

This document shows how to decompose complex features into deliverable stories and discrete engineering tasks, using GitLab’s built-in tools.

---

## 🧱 1. Define a Feature Epic

An **epic** represents a business feature that delivers tangible value — e.g., “Enable secure user registration”.

### Example Epic:
> **Epic Title**: As a user, I want to create an account so I can access the platform.

---

## 🧩 2. Break Epic into Vertically Sliced User Stories

Each **issue (story)** should:
- Be independently testable
- Contain acceptance criteria
- Take 1–3 days to complete
- Be valuable to the user, not just a backend step

### Example Stories:
- `As a user, I need to enter my email address to register`
- `As a user, I need to create a password to secure my account`
- `As a user, I need to submit my information to complete registration`

Each story is a thin, functional slice of the end-to-end feature.

---

## 🧱 3. Further Break Each Story into Tasks (Optional)

For complex stories, add implementation steps as a checklist in the issue body or as linked sub-tasks (if using Enterprise features).

### Example (Story: Enter email address)

```markdown
### Acceptance Criteria
- User can enter email address in form field
- Field validates proper email format
- Invalid email shows helpful error

### Tasks
- [ ] Frontend: Create email input field
- [ ] Frontend: Style form with error state
- [ ] Backend: Validate email format on POST
- [ ] Backend: Store email in database
