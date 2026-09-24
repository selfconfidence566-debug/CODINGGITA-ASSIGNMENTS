# GIT CHERRY-PICK — COMPLETE ASSIGNMENT

==================================================
Q1. THEORY — UNDERSTANDING CHERRY-PICK
==================================================

Q1.1 What is git cherry-pick?

Answer:
git cherry-pick applies the changes from a specific commit to the current branch. It allows us to select specific commits without merging the entire branch.

Command:
git cherry-pick <commit_id>


Q1.2 Difference between cherry-pick and merge?

Answer:
Merge combines the changes of an entire branch, while cherry-pick applies only selected commit(s) to the current branch.


Q1.3 Does cherry-pick move the original commit?

Answer:
No. The original commit remains on the source branch. Cherry-pick creates a new commit on the target branch.


Q1.4 Why does cherry-pick create a new commit?

Answer:
Because the changes are being applied to another branch, Git creates a new commit with a different commit ID.


Q1.5 Purpose of the commands:

git cherry-pick --continue
Answer:
Continues cherry-pick after resolving a conflict.

git cherry-pick --abort
Answer:
Cancels the current cherry-pick operation.

git cherry-pick --skip
Answer:
Skips the current commit during an ongoing cherry-pick operation.


Q1.6 Difference between:

git cherry-pick <start_commit>..<end_commit>

and

git cherry-pick <start_commit>^..<end_commit>

Answer:
A..D excludes A and selects B, C, D.

A^..D includes A and selects A, B, C, D.

<img width="1917" height="1077" alt="Git   GitHub Day 22 Assignment-02-02" src="https://github.com/user-attachments/assets/b8d0bd40-772e-42ba-acde-c2538bf4df4d" />

<img width="1917" height="1077" alt="Git   GitHub Day 22 Assignment-02-03" src="https://github.com/user-attachments/assets/1e34edf9-ae6c-4640-906e-b3a072fb45f8" />

<img width="1917" height="1078" alt="image" src="https://github.com/user-attachments/assets/31aa7440-d9df-464e-8253-be7340fe5c39" />

<img width="1917" height="1075" alt="image" src="https://github.com/user-attachments/assets/5644ecf4-9671-4ba5-af0b-b9bc6069edcb" />









==================================================
Q2. PRACTICAL — CHERRY-PICK A SPECIFIC COMMIT
==================================================

SCENARIO: Student Management System

STEP 1:
Create folder:
Student-Management-System

Open it in VS Code.

STEP 2:
Run:

git init
git branch -M main

[SCREENSHOT REQUIRED HERE]


STEP 3:
Create Student.txt with:

Student Management System

Run:

git add Student.txt
git commit -m "Create student management system"


STEP 4:
Create branch:

git checkout -b student-information

[SCREENSHOT REQUIRED HERE]


STEP 5:
Edit Student.txt:

Student Management System
Rahul - Student

Run:

git add Student.txt
git commit -m "Add Rahul student information"


STEP 6:
Add Amit:

Student Management System
Rahul - Student
Amit - Student

Run:

git add Student.txt
git commit -m "Add Amit student information"

[SCREENSHOT REQUIRED HERE]


STEP 7:
Switch to main:

git checkout main


STEP 8:
Find Amit's commit:

git log student-information --oneline

Copy the ID beside:
Add Amit student information


STEP 9:
Cherry-pick Amit:

git cherry-pick <AMIT_COMMIT_ID>

Replace <AMIT_COMMIT_ID> with your real ID.

[SCREENSHOT REQUIRED HERE]


STEP 10:
Check history:

git log --oneline --graph --all

Expected:
The original Amit commit remains on student-information, while a new cherry-picked commit appears on main.

[SCREENSHOT REQUIRED HERE]


==================================================
Q3. PRACTICAL — CHERRY-PICK MULTIPLE COMMITS
==================================================

SCENARIO: E-Commerce Website

STEP 1:
Create folder:
E-Commerce-Git

Run:

git init
git branch -M main


STEP 2:
Create README.md:

E-Commerce Website

Run:

git add README.md
git commit -m "Create e-commerce website project"


STEP 3:
Create branch:

git checkout -b product-features


STEP 4 — Commit 1:

Create products.txt:

Product List

Run:

git add products.txt
git commit -m "Add product listing"


STEP 5 — Commit 2:

Edit products.txt:

Product List
Laptop
Mobile

Run:

git add products.txt
git commit -m "Add laptop and mobile products"


STEP 6 — Commit 3:

Edit products.txt:

Product List
Laptop - 50000
Mobile - 25000

Run:

git add products.txt
git commit -m "Add product prices"

[SCREENSHOT REQUIRED HERE]


STEP 7:
Find commit IDs:

git log --oneline

Copy the IDs of any TWO commits.


STEP 8:
Switch to main:

git checkout main


STEP 9:
Cherry-pick the two commits:

git cherry-pick <COMMIT_ID1> <COMMIT_ID2>

[SCREENSHOT REQUIRED HERE]


STEP 10:
Check history:

git log --oneline --graph --all

[SCREENSHOT REQUIRED HERE]


Answer:
Two selected commits were copied from the feature branch into main without merging the entire branch.


==================================================
Q4. PRACTICAL — CHERRY-PICK COMMIT RANGE
==================================================

Create four commits:

A = Create homepage
B = Add navigation bar
C = Add login page
D = Fix login validation

STEP 1:

git init
git branch -M main


STEP 2:
Create index.html:

Homepage

git add index.html
git commit -m "Create homepage"


STEP 3:
Add:

Navigation Bar

git add index.html
git commit -m "Add navigation bar"


STEP 4:
Add:

Login Page

git add index.html
git commit -m "Add login page"


STEP 5:
Add:

Login Validation

git add index.html
git commit -m "Fix login validation"


STEP 6:
Check commits:

git log --oneline

[SCREENSHOT REQUIRED HERE]


Q4 TASK 1 — EXCLUDING STARTING COMMIT

Command:

git cherry-pick <START_COMMIT>..<END_COMMIT>

If:

A → B → C → D

Then:

A..D = B, C, D

Answer:
The starting commit is excluded.


[SCREENSHOT REQUIRED HERE]


Q4 TASK 2 — INCLUDING STARTING COMMIT

Command:

git cherry-pick <START_COMMIT>^..<END_COMMIT>

If:

A → B → C → D

Then:

A^..D = A, B, C, D

Answer:
The starting commit is included.


[SCREENSHOT REQUIRED HERE]


Q4 FINAL ANSWER:

A..D = B, C, D
A^..D = A, B, C, D

Easy rule:
A..D → starts AFTER A
A^..D → starts FROM A


==================================================
Q5. PRACTICAL — RESOLVE CHERRY-PICK CONFLICT
==================================================

STEP 1:
Create folder:
Cherry-Pick-Conflict

Run:

git init
git branch -M main


STEP 2:
Create Student.txt:

Student Name: Student

Run:

git add Student.txt
git commit -m "Create student file"


STEP 3:
Create feature branch:

git checkout -b feature


STEP 4:
Change Student.txt to:

Student Name: Rahul

Run:

git add Student.txt
git commit -m "Add Rahul as student"

[SCREENSHOT REQUIRED HERE]


STEP 5:
Switch to main:

git checkout main


STEP 6:
Change the SAME line to:

Student Name: Amit

Run:

git add Student.txt
git commit -m "Add Amit as student"


STEP 7:
Find Rahul commit:

git log feature --oneline

Copy the ID beside:
Add Rahul as student


STEP 8:
Cherry-pick it:

git cherry-pick <RAHUL_COMMIT_ID>

A conflict should occur because both branches changed the same line.

[SCREENSHOT REQUIRED HERE]


STEP 9:
Open Student.txt.

You may see:

<<<<<<< HEAD
Student Name: Amit
=======
Student Name: Rahul
>>>>>>> <commit>

Remove the conflict markers and choose the final content, for example:

Student Name: Rahul and Amit

Save the file.


STEP 10:
Run:

git add Student.txt
git cherry-pick --continue

[SCREENSHOT REQUIRED HERE]


STEP 11:
Check history:

git log --oneline --graph --all

[SCREENSHOT REQUIRED HERE]


Q5 ANSWER:

The conflict occurred because main and feature modified the same line. I resolved the conflict manually, staged the file, and completed the cherry-pick using git cherry-pick --continue.


Q5 — ABORT

To demonstrate abort, start a cherry-pick that causes a conflict:

git cherry-pick <RAHUL_COMMIT_ID>

Then run:

git cherry-pick --abort

Answer:
It cancels the current cherry-pick and returns the repository to its previous state.

[SCREENSHOT REQUIRED HERE]


Q5 — SKIP

During an ongoing multi-commit cherry-pick, use:

git cherry-pick --skip

Answer:
It skips the current commit and continues with the next commit.

[SCREENSHOT REQUIRED HERE]


==================================================
Q6. SHORT PRACTICAL + THEORY
==================================================

Q6.1 Find commit history

Command:
git log --oneline

Answer:
Displays commit history in a short format with commit IDs and messages.

[SCREENSHOT REQUIRED HERE]


Q6.2 Cherry-pick one commit

Command:
git cherry-pick <commit_id>

Answer:
Applies one specific commit to the current branch and creates a new commit.

[SCREENSHOT REQUIRED HERE]


Q6.3 Cherry-pick multiple commits

Command:
git cherry-pick <commit_id1> <commit_id2>

Answer:
Applies multiple selected commits to the current branch.

[SCREENSHOT REQUIRED HERE]


Q6.4 Cherry-pick a range

Command:
git cherry-pick <start_commit>..<end_commit>

Answer:
Selects commits after the starting commit up to the ending commit.

Example:
A..D = B, C, D

[SCREENSHOT REQUIRED HERE]


Q6.5 Range including starting commit

Command:
git cherry-pick <start_commit>^..<end_commit>

Answer:
Includes the starting commit and all commits up to the ending commit.

Example:
A^..D = A, B, C, D

[SCREENSHOT REQUIRED HERE]


Q6.6 Continue after conflict

Command:
git cherry-pick --continue

Answer:
Continues the cherry-pick after resolving and staging a conflict.

[SCREENSHOT REQUIRED HERE]


Q6.7 Cancel cherry-pick

Command:
git cherry-pick --abort

Answer:
Cancels the current cherry-pick operation.

[SCREENSHOT REQUIRED HERE]


Q6.8 Skip current commit

Command:
git cherry-pick --skip

Answer:
Skips the current commit during an ongoing cherry-pick operation.

[SCREENSHOT REQUIRED HERE]


==================================================
SUBMISSION CHECKLIST
==================================================

[ ] Created Git repository
[ ] Created meaningful branches
[ ] Used meaningful commit messages
[ ] Cherry-picked one commit
[ ] Cherry-picked multiple commits
[ ] Used commit range
[ ] Used <start_commit>^..<end_commit>
[ ] Resolved cherry-pick conflict
[ ] Used --continue
[ ] Used --abort
[ ] Used --skip
[ ] Used git log --oneline --graph --all
[ ] Took required screenshots
[ ] Added screenshots to CodingGita_assignment
[ ] Added GitHub repository link


==================================================
QUICK REVISION
==================================================

One commit:
git cherry-pick <commit_id>

Multiple commits:
git cherry-pick <id1> <id2>

Range excluding start:
git cherry-pick <start>..<end>

Range including start:
git cherry-pick <start>^..<end>

Continue:
git cherry-pick --continue

Cancel:
git cherry-pick --abort

Skip:
git cherry-pick --skip

History:
git log --oneline --graph --all


IMPORTANT:
Never copy example commit IDs.

Always use the REAL commit ID from:

git log --oneline

Cherry-pick selects specific commit changes. It does not merge the entire branch.
