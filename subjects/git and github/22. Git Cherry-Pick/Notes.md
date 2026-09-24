GIT CHERRY-PICK — ASSIGNMENT

1. What is Git Cherry-Pick?

Question:
What is git cherry-pick? Explain in simple words.

Answer:
git cherry-pick is used to apply the changes of a specific commit from one branch to another branch. It allows us to select only the commit we need instead of merging the entire branch.

Easy meaning:
Cherry-pick means selecting a specific commit and applying its changes to another branch.


2. What is the basic cherry-pick command?

Question:
Write the basic command used to cherry-pick a commit.

Answer:
git cherry-pick <commit_id>

Example:
git cherry-pick 7a82f91


3. How do you find a commit ID?

Question:
Which command is used to find the commit ID before cherry-picking?

Answer:
git log --oneline

Example:
7a82f91 Add Amit
42bc921 Add Rahul
15de721 Create Student file


4. What happens when we cherry-pick a commit?

Question:
What happens when a commit is cherry-picked to another branch?

Answer:
Git applies the changes from the selected commit to the current branch and creates a new commit. The original commit remains on the original branch.


5. Does cherry-pick move the original commit?

Question:
Does cherry-pick move the original commit from one branch to another?

Answer:
No. Cherry-pick does not move the original commit. It creates a new commit containing the same changes.

Therefore:
Original commit ≠ New cherry-picked commit


6. Cherry-Pick Multiple Commits

Question:
How can we cherry-pick multiple specific commits?

Answer:
We can provide multiple commit IDs in the same command.

Command:
git cherry-pick <commit_id1> <commit_id2>

Example:
git cherry-pick 42bc921 7a82f91


7. Cherry-Pick a Range of Commits

Question:
How can we cherry-pick a range of commits?

Answer:
Use:

git cherry-pick <start_commit>..<end_commit>

The first commit is not included.

Example:
git cherry-pick A..D

If the history is:

A---B---C---D

The commits picked are:

B, C, D


8. How do you include the starting commit?

Question:
How can we include the starting commit when cherry-picking a range?

Answer:
Use:

git cherry-pick <start_commit>^..<end_commit>

Example:
git cherry-pick A^..D

This includes:

A, B, C, D


9. Difference Between Cherry-Pick Range Commands

Question:
What is the difference between A..D and A^..D?

Answer:

git cherry-pick A..D
→ Picks B, C, D

git cherry-pick A^..D
→ Picks A, B, C, D

Easy memory:
A..D → Start after A
A^..D → Include A


10. What is a Cherry-Pick Conflict?

Question:
What is a cherry-pick conflict?

Answer:
A cherry-pick conflict happens when the commit being cherry-picked changes the same part of a file that has already been changed in the current branch. Git then asks us to manually resolve the conflict.


11. How do you continue after resolving a conflict?

Question:
Which commands are used after fixing a cherry-pick conflict?

Answer:

First stage the resolved files:

git add .

Then continue:

git cherry-pick --continue


12. How do you cancel a cherry-pick?

Question:
Which command is used to cancel an ongoing cherry-pick?

Answer:

git cherry-pick --abort

It cancels the cherry-pick operation and returns the branch to its previous state.


13. How do you skip a commit?

Question:
Which command is used to skip the current commit during cherry-picking?

Answer:

git cherry-pick --skip

Easy memory:

--continue → Continue
--abort → Cancel
--skip → Skip


14. Useful Git Commands

Question:
Write some useful commands related to cherry-pick.

Answer:

Check commit history:
git log --oneline

Check current status:
git status

Cherry-pick one commit:
git cherry-pick <commit_id>

Cherry-pick multiple commits:
git cherry-pick <commit_id1> <commit_id2>

Cherry-pick a range:
git cherry-pick <start_commit>..<end_commit>

Cherry-pick a range including the first commit:
git cherry-pick <start_commit>^..<end_commit>

Continue after resolving conflict:
git cherry-pick --continue

Cancel cherry-pick:
git cherry-pick --abort

Skip current commit:
git cherry-pick --skip

See complete branch history:
git log --oneline --graph --all


15. Real-Life Example

Question:
Give a simple real-life example of using cherry-pick.

Answer:
Suppose the student-info branch contains three commits:

Add Rahul
Add Amit
Add Priya

But the main branch needs only the changes from Add Amit.

We can switch to main:

git switch main

Then find the commit ID:

git log --oneline

Then cherry-pick the required commit:

git cherry-pick <Add-Amit-commit-id>

Only the changes from the selected commit are applied to main.


16. Difference Between Merge, Rebase and Cherry-Pick

Question:
What is the difference between merge, rebase and cherry-pick?

Answer:

Merge:
Combines changes from branches.

Rebase:
Replays commits onto another base.

Cherry-pick:
Applies selected commits to another branch.


Easy memory:

Merge → Bring branches together

Rebase → Replay branch commits

Cherry-pick → Select specific commits


17. Cherry-Pick Workflow

Question:
Write the basic cherry-pick workflow.

Answer:

Step 1: Go to the target branch.

git switch main

Step 2: Find the required commit.

git log --oneline

Step 3: Apply the required commit.

git cherry-pick <commit_id>

Step 4: If there is a conflict, fix the file.

Step 5: Stage the resolved file.

git add .

Step 6: Continue the cherry-pick.

git cherry-pick --continue

If you want to cancel:

git cherry-pick --abort


18. Quick Revision

Question:
What is the most important thing to remember about Git Cherry-Pick?

Answer:
git cherry-pick applies the changes from a specific commit to the current branch and creates a new commit.

Most important command:

git cherry-pick <commit_id>

Remember:

Merge → Bring branches together

Rebase → Replay commits

Cherry-pick → Select specific commits


SCREENSHOT SPACE

📸 Screenshot 1:
Take a screenshot of the cherry-pick command being used.


📸 Screenshot 2:
Take a screenshot showing git log --oneline.


📸 Screenshot 3:
Take a screenshot showing the successful cherry-picked commit.


📸 Screenshot 4:
Take a screenshot of the final Git history if required.
