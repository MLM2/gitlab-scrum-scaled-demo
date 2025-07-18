# Sprint Planning Flow in GitLab Scrum

This guide outlines how to facilitate sprint planning using GitLab, whether synchronously (live meeting) or asynchronously (issue-based). It covers backlog preparation, story sizing, and transitioning issues into sprint-ready status.

## 🎯 Objective

Enable distributed or cross-functional teams to plan and execute 2-week sprints consistently using GitLab’s:

- Issue Boards
- Iteration Cadences
- Scoped Labels
- Story Weights
- Comment threads and checklists

---

## 🛠️ Prerequisites

- You’ve configured a `Backlog` issue board scoped by upcoming iterations
- You’ve applied labels such as:
  - `status::refine`
  - `status::ready`
  - `type::story`
  - `priority::now`

- Your stories are grouped by their corresponding epics
- You’ve created a 2-week **iteration cadence** at the group level

---

## 🧱 Backlog Grooming Before Sprint Planning

Before the sprint planning ceremony:

1. **Break down features (epics) into user stories (issues)**
2. Apply `status::refine` label to stories needing review
3. Draft **acceptance criteria** in the issue description
4. Estimate **Weight** (story points) or leave blank for team to estimate
5. Assign stories to an upcoming iteration (e.g., Sprint 3)

---

## 👥 Sprint Planning – Synchronous Flow

Use a live meeting to review stories for the upcoming iteration.

### Step-by-Step

1. Open the `Backlog` board, scoped to the target iteration
2. Review each issue:
   - Check clarity of the title and description
   - Confirm or refine acceptance criteria
   - Discuss technical complexity
3. Assign:
   - `Weight` (story points)
   - `status::ready` label
4. If needed, break story into **checklist of tasks** in the issue
5. Repeat for all issues in the iteration column

✅ Sprint planning is complete once all selected stories are `status::ready` and estimated.

---

## 📬 Sprint Planning – Asynchronous Flow

Ideal for distributed or hybrid teams with different time zones or limited availability.

### Step-by-Step

1. Create a **planning issue** titled:  
   `Sprint Planning – Sprint 3`

2. Mention team members to create a GitLab To-Do for each

3. For each story in the upcoming sprint:
   - Start a comment thread using this template:
     ```markdown
     ## [Story Title – Link]
     - [ ] Acceptance criteria reviewed
     - [ ] Weight assigned
     - [ ] Tasks defined
     ```

4. Ask team members to:
   - React with emoji (e.g., `:two:`, `:three:`) to vote on story points
   - Propose edits to description and checklist
   - Mark as `status::ready` when aligned

5. Once each thread is resolved, the planning issue is considered complete.

---

## 📊 Using Story Weights for Velocity

Each issue’s **Weight** field represents its complexity (1 = simple, 5 = complex). At the top of each iteration column, GitLab shows total story points committed.

Track team velocity over time by:
- Summing story points completed per sprint
- Adjusting future commitments accordingly

---

## ✅ Post-Planning Checklist

- [ ] All stories assigned to iteration
- [ ] Acceptance criteria defined
- [ ] Status label is `status::ready`
- [ ] Story points (weights) are applied
- [ ] Tasks/checklists created as needed
- [ ] Planning issue closed (if async)

---

## 📈 Related GitLab Features

- [Iterations](https://docs.gitlab.com/ee/user/group/iterations/)
- [Story Weights](https://docs.gitlab.com/ee/user/project/issues/issue_weights.html)
- [Scoped Labels](https://docs.gitlab.com/ee/user/project/labels.html#scoped-labels)
- [Issue Boards](https://docs.gitlab.com/ee/user/project/issue_board.html)

---

## 🧠 Summary

Sprint planning in GitLab can be structured and transparent using boards, weights, and labels — and can flex to fit distributed, multi-team delivery environments. Whether real-time or async, these workflows help ensure stories are clear, sized, and sprint-ready.
