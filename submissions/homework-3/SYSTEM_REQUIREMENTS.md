## Approved UN/UR Baseline
User needs
ID
Stakeholder need
UN-GIT-01
A student developer needs a way to start tracking a local project because it has no recorded history.
UN-GIT-02
A student developer needs to know which project files have changed because they may forget what they edited before recording a checkpoint.
UN-GIT-03
A student developer needs to inspect changed content before recording it because a file may contain unintended edits.
UN-GIT-04
A student developer needs to choose the file content to include in the next checkpoint because some current changes may still be unfinished.
UN-GIT-05
A student developer needs to record a meaningful checkpoint because they want to record an important project version and provide a descriptive label.
UN-GIT-06
A student developer needs to review earlier checkpoints because they want to understand how the project reached its current state.
UN-GIT-07
A student developer needs invalid commands to explain why they failed while preserving existing project files and recorded checkpoints.

User requirements
ID
User-visible capability
Need
UR-GIT-01
A student developer shall be able to initialize tracking in the current local project folder without removing existing project files.
UN-GIT-01, UN-GIT-07
UR-GIT-02
A student developer shall be able to see whether project files are untracked, staged, changed after staging, modified, deleted, or clean.
UN-GIT-02
UR-GIT-03
A student developer shall be able to view differences between current working file content and the content selected for the next checkpoint.
UN-GIT-03
UR-GIT-04
A student developer shall be able to view differences between content selected for the next checkpoint and the latest recorded checkpoint.
UN-GIT-03
UR-GIT-05
A student developer shall be able to select the current content of one existing project file for the next checkpoint without selecting unrelated files.
UN-GIT-04
UR-GIT-06
A student developer shall be able to create a checkpoint of selected content with a nonempty explanation while leaving later unselected edits in the working files.
UN-GIT-05, UN-GIT-04
UR-GIT-07
A student developer shall be able to view recorded checkpoints from newest to oldest, including their identifier and explanation.
UN-GIT-06
UR-GIT-08
A student developer shall receive a useful error when a command is invalid, a requested file is unavailable, or a path is outside the allowed project files.
UN-GIT-07
UR-GIT-09
A student developer shall be able to retry an operation after a failure without losing ordinary project files or an already recorded checkpoint.
UN-GIT-07

SR‑01 (source UR‑GIT‑01)
Given a folder with project files and no MiniGit tracking, when init is used, MiniGit shall start tracking without deleting any existing files.

SR‑02 (source UR‑GIT‑01, UR‑GIT‑09)
Given a project that is already initialized, when init is used again, MiniGit shall show a message and keep all project files unchanged.

SR‑03 (source UR‑GIT‑05)
Given an initialized project with notes.txt containing ONE, when add notes.txt is used, MiniGit shall stage a copy of notes.txt containing ONE without staging other files.

SR‑04 (source UR‑GIT‑08, UR‑GIT‑09)
Given an initialized project, when add missing.txt is used for a nonexistent file, MiniGit shall show a useful error and preserve the staged content and any existing checkpoint.

SR‑05 (source UR‑GIT‑02)
Given a project where notes.txt is staged with ONE, when status is used, MiniGit shall show notes.txt as staged and clean.

SR‑06 (source UR‑GIT‑06)
Given a project where notes.txt is staged with ONE and the user provides a nonempty explanation, when commit is used, MiniGit shall record a new checkpoint containing ONE and store the explanation.

SR‑07 (source UR‑GIT‑08, UR‑GIT‑09)
Given a project where no files are staged, when commit is used, MiniGit shall show a useful error and preserve all working files and any existing checkpoint.

SR‑08 (source UR‑GIT‑03)
Given a project where notes.txt is staged with ONE and the working file contains TWO, when diff is used, MiniGit shall show the BEFORE/AFTER difference between staged ONE and working TWO.

SR‑09 (source UR‑GIT‑04)
Given a project where notes.txt is staged with TWO and the latest checkpoint contains ONE, when diff --staged is used, MiniGit shall show the BEFORE/AFTER difference between committed ONE and staged TWO.

SR‑10 (source UR‑GIT‑07)
Given a project with two recorded checkpoints, when log is used, MiniGit shall show both checkpoints from newest to oldest, including their ID and explanation.

SR‑11 (source UR‑GIT‑06)
Given a project with a recorded checkpoint containing ONE, when checkout <ID> is used, MiniGit shall restore the working file content to ONE while keeping later uncommitted edits unstaged.

SR‑12 (source UR‑GIT‑02)
Given a project where notes.txt was previously committed but is now deleted from the working folder, when status is used, MiniGit shall show notes.txt as deleted.
