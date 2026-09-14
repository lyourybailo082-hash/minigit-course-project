# Homework 2 — Part 2 Submission

Student name: Oury Ly

GitHub username:lyourybailo082-hash

## 1. Git Command Observations

| Command or workflow | What did you observe? | What was the user trying to accomplish? | What problem or risk did it address? |
|---|---|---|---|
|1. git status | It showed which files were modified, staged, or untracked. | The user wanted to understand the current state of their work. | It helps prevent forgetting changes or committing the wrong files. |
| 2.git diff | It showed the changes made to files before staging them. | The user wanted to review their changes before selecting them for a commit. | It helps catch unwanted changes or mistakes. |
| 3.git add <file> + git diff --staged | The file was selected for the next commit, and the staged changes could be reviewed. | The user wanted to choose and verify what would be included in the next commit. | It helps prevent committing changes that were not intended. |
| 4.git commit -m "<message>" + git log --oneline -3 | The changes were saved in the repository history, and recent commits were displayed. | The user wanted to preserve their work and review recent versions. | It helps keep a clear history of the project. |

## 2. User Needs

### UN-GIT-01 — 

>A student working on a shared software project needs a way to understand the current state of their work because they need to avoid forgetting changes or including the wrong files.
 
### UN-GIT-02 — 
> A student working on a shared software project needs a way to review and select their changes because they need to avoid including unwanted changes or mistakes.



### UN-GIT-03 — 
> A student working on a shared software project needs a way to preserve and review previous versions because they need to keep track of how the project changes over time.

## 3. User Requirements

| ID and short title | User requirement | Source user need | Rationale |
|---|---|---|---|
| UR-GIT-01 — View current work | A student shall be able to view the current state of their project changes before saving a version. | UN-GIT-01 | This helps the student know what has changed and avoid forgetting files. |
| UR-GIT-02 — Review changes | A student shall be able to review changes before including them in a saved version. | UN-GIT-02 | This helps the student identify unwanted changes or mistakes. |
| UR-GIT-03 — Select changes | A student shall be able to select which changes will be included in the next saved version. | UN-GIT-02 | This helps prevent unwanted changes from being included. |
| UR-GIT-04 — Review project history | A student shall be able to view previous versions of the project. | UN-GIT-03 | This helps the student keep track of how the project has changed over time. |

