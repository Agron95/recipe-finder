# Recipe Finder

## Project idea

Build a small recipe browsing website with local sample recipes. Visitors can search by name, filter by category, read ingredients and cooking steps, and save favorites. No account, backend, or external API is needed.

## Technology and scope

Use plain HTML, CSS, and JavaScript. No frameworks, packages, build tools, backend, or external services are required. This initial repository contains the assignment only; students build the application through the tasks below.

The finished application should run by opening `index.html` in a modern browser. Use the same browser and file location when checking saved data; browser storage behavior for local files can vary. If needed, use your editor's local preview server consistently.

## Team assignments

- **student1**: tasks 01, 04, 07.
- **student2**: tasks 02, 05, 08, 10.
- **student3**: tasks 03, 06, 09.

There are exactly 10 tasks and each task has one owner. One student has four tasks and the other two have three each. Teammates review each other's pull requests.

## GitHub setup and pull request workflow

The teacher should create an empty GitHub repository for this project, push this local repository's `main` branch, and give all three students access. Replace the placeholders below with that repository's URL:

```sh
git remote add origin <github-repository-url>
git push -u origin main
```

Students then clone the GitHub repository. Complete the numbered tasks in order, merging each task before starting the next; later tasks build on earlier work. For every task, its owner must:

1. Update their local `main` branch and create a new task branch.
2. Implement only that task and manually check its completion criteria.
3. Commit and push the branch, then open one GitHub pull request targeting `main`.
4. Put the task number, changes, and manual-check results in the PR description; add a screenshot for visible UI changes.
5. Ask another team member to review, address feedback, and merge after approval. Mark the task checkbox complete in the same PR.

Example for task 01 (replace the student and task number for your own assignment):

```sh
git switch main
git pull --ff-only origin main
git switch -c student1/task-01
# Make and check your changes, then stage the files you changed.
git add .
git commit -m "Complete task 01: create page structure"
git push -u origin student1/task-01
```

Use GitHub's **Compare & pull request** button after pushing. Suggested PR title: `[Task 01] Create page structure (student1)`. Do not push task work directly to `main`. The finished project should have **10 task PRs**, one per task. PRs are submitted when students implement their tasks.

## Tasks

### 01. Create the page structure

- [ ] Complete and merge this task.
- **Owner:** student1
- **Branch:** `student1/task-01`
- **Work:** Create index.html with a heading, labeled search input, category controls, a recipe-grid container, and a status-message area. Link styles.css and a deferred script.js; create those files.
- **Done when:** The page opens without missing-file errors and the search field has a visible label.
- **Deliverable:** One GitHub PR for this task, reviewed by another team member.

### 02. Style recipe cards and controls

- [ ] Complete and merge this task.
- **Owner:** student2
- **Branch:** `student2/task-02`
- **Work:** Style the page, search controls, recipe cards, buttons, and visible keyboard focus in styles.css. Use a responsive grid; recipe images are optional.
- **Done when:** Cards fit a 360px screen without horizontal scrolling and form a readable grid on desktop.
- **Deliverable:** One GitHub PR for this task, reviewed by another team member.

### 03. Add sample data and render recipes

- [ ] Complete and merge this task.
- **Owner:** student3
- **Branch:** `student3/task-03`
- **Work:** In script.js, define at least six recipes with unique id, name, category, cooking time, ingredients array, and steps array. Use at least three categories. Render cards with name, category, and time using safe text insertion.
- **Done when:** All six recipes appear, have unique ids, and contain enough information to cook the dish.
- **Deliverable:** One GitHub PR for this task, reviewed by another team member.

### 04. Search recipes by name

- [ ] Complete and merge this task.
- **Owner:** student1
- **Branch:** `student1/task-04`
- **Work:** Listen for search input, trim whitespace, and filter recipe names case-insensitively. Keep the original data unchanged.
- **Done when:** Partial names match; capitalization does not matter; clearing the search restores all recipes.
- **Deliverable:** One GitHub PR for this task, reviewed by another team member.

### 05. Filter recipes by category

- [ ] Complete and merge this task.
- **Owner:** student2
- **Branch:** `student2/task-05`
- **Work:** Populate category controls from the recipe data and include All. Combine the category selection with the current search text and visibly mark the selected category.
- **Done when:** Only recipes matching both controls are shown, and All removes the category restriction.
- **Deliverable:** One GitHub PR for this task, reviewed by another team member.

### 06. Show recipe details

- [ ] Complete and merge this task.
- **Owner:** student3
- **Branch:** `student3/task-06`
- **Work:** Add a View recipe button to each card. Display the selected recipe's ingredients and numbered steps in an inline details panel with a close button. Move focus to the panel heading on open and return it to the trigger on close.
- **Done when:** Opening different recipes shows the correct details; opening and closing works using only the keyboard.
- **Deliverable:** One GitHub PR for this task, reviewed by another team member.

### 07. Toggle favorite recipes

- [ ] Complete and merge this task.
- **Owner:** student1
- **Branch:** `student1/task-07`
- **Work:** Add an accessible favorite toggle to each card and track favorite recipe ids in a Set or array. Reflect the state visually and with aria-pressed.
- **Done when:** Toggling a recipe updates only that recipe and never creates duplicate favorite ids.
- **Deliverable:** One GitHub PR for this task, reviewed by another team member.

### 08. Add a favorites-only view

- [ ] Complete and merge this task.
- **Owner:** student2
- **Branch:** `student2/task-08`
- **Work:** Add a favorites-only control that works together with search and category filters. Show an appropriate empty-state message when there are no matches or no saved favorites.
- **Done when:** Combined filters show the correct cards; removing the final matching favorite updates the view immediately.
- **Deliverable:** One GitHub PR for this task, reviewed by another team member.

### 09. Persist favorites

- [ ] Complete and merge this task.
- **Owner:** student3
- **Branch:** `student3/task-09`
- **Work:** Store favorite ids in a project-specific localStorage key and restore them on load. Ignore unknown recipe ids and handle malformed JSON or unavailable storage without crashing.
- **Done when:** Favorites survive refresh when storage is available; invalid saved content does not break browsing.
- **Deliverable:** One GitHub PR for this task, reviewed by another team member.

### 10. Verify and document the complete experience

- [ ] Complete and merge this task.
- **Owner:** student2
- **Branch:** `student2/task-10`
- **Work:** Check search, combined filters, details-panel focus, favorites, persistence, empty states, and responsive layout. Fix issues and add a Manual testing section to this README.
- **Done when:** Record actual results and browser used; keyboard navigation and the 360px layout work for all core actions.
- **Deliverable:** One GitHub PR for this task, reviewed by another team member.
