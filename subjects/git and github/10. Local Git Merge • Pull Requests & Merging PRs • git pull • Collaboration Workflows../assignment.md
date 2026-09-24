```text
ASSIGNMENT 1 – LOCAL MERGE

1. What is a local merge?

ANSWER

A local merge combines the changes from one Git branch into another branch on the computer.
It allows us to bring the work from a feature branch into the main branch.


2. Create a new branch.

ANSWER

git checkout -b feature-local-merge


3. What should be written in local-merge.txt?

ANSWER

Today I learned how to merge a feature branch into the main branch locally.
A local merge combines changes from one branch into another on my computer.
The feature branch can be tested before merging it into main.
After merging, the updated main branch can be pushed to GitHub.


4. Stage and commit the changes.

ANSWER

git add .
git commit -m "Add local-merge notes"


5. Switch back to main.

ANSWER

git checkout main


6. Merge the feature branch into main.

ANSWER

git merge feature-local-merge


7. Push main to GitHub.

ANSWER

git push origin main


8. Check the commit history.

ANSWER

git log --oneline -5

[SCREENSHOT REQUIRED HERE]


9. Confirm that local-merge.txt is on GitHub main.

ANSWER

Open the GitHub repository and select the main branch.
Confirm that local-merge.txt is visible.

[SCREENSHOT REQUIRED HERE]



==================================================

ASSIGNMENT 2 – PULL REQUEST WORKFLOW

1. Create a new branch.

ANSWER

git checkout -b feature-pr-practice


2. What should be written in pr-practice.txt?

ANSWER

A Pull Request is a request to merge changes from one branch into another.
It allows team members to review the code before it is merged.
Pull Requests help find mistakes and improve code quality.
They make collaboration easier when many people work on the same project.
Teams use Pull Requests to discuss, review, and safely merge changes.


3. Stage and commit the changes.

ANSWER

git add .
git commit -m "Add PR practice notes"


4. Push the branch to GitHub.

ANSWER

git push -u origin feature-pr-practice


5. Create a Pull Request on GitHub.

ANSWER

PR Title:

Add PR practice notes

PR Description:

This Pull Request adds notes explaining what a Pull Request is and why teams use it.
It demonstrates the basic Pull Request workflow.


[SCREENSHOT REQUIRED HERE – Pull Request]


6. Merge the Pull Request.

ANSWER

On GitHub, select:

Create a merge commit

Then click the merge button.


[SCREENSHOT REQUIRED HERE – Merged Pull Request]


7. Update the local main branch.

ANSWER

git checkout main
git pull origin main


8. Confirm that pr-practice.txt is present.

ANSWER

Check your local repository and confirm that pr-practice.txt is present.

[SCREENSHOT REQUIRED HERE – Successful git pull]



==================================================

ASSIGNMENT 3 – COMPARE BOTH WORKFLOWS

1. What is the main difference between local merge and PR merge?

ANSWER

A local merge is performed directly on the computer using Git commands.
A Pull Request merge is performed through GitHub after pushing the branch to the remote repository.


2. When would you prefer a local merge?

ANSWER

I would prefer a local merge when working alone or when the changes do not require team review.


3. When is a Pull Request better?

ANSWER

A Pull Request is better when working with a team because other developers can review, discuss, and approve the changes before merging.


4. After merging a PR on GitHub, which command brings the changes to your computer?

ANSWER

git pull origin main


5. What does git pull actually do?

ANSWER

git pull first fetches the latest changes from the remote repository.
Then it merges those changes into the current local branch.


6. Create comparison.txt.

ANSWER

The main difference between a local merge and a PR merge is where the merge is performed.
A local merge is performed on the computer, while a PR merge is performed through GitHub.

I would prefer a local merge when working alone or when team review is not required.

A Pull Request is better when working with a team because the changes can be reviewed and discussed before merging.

After merging a PR on GitHub, the command git pull origin main brings the changes to my computer.

Git pull performs two main steps: it fetches changes from the remote repository and then merges them into the current local branch.


7. Commit and push comparison.txt.

ANSWER

git add comparison.txt
git commit -m "Add workflow comparison"
git push origin main


[SCREENSHOT REQUIRED HERE – comparison.txt or commit/PR]



==================================================

ASSIGNMENT 4 – GIT PULL PRACTICE

1. Make sure you are on main.

ANSWER

git checkout main


2. Run git pull.

ANSWER

git pull origin main


3. Make a small change directly on GitHub.

ANSWER

Open any file on GitHub.
Click the Edit button.
Add this line:

Git pull helps keep my local repository synchronized with the remote repository.

Commit the change directly to the main branch.


4. Pull the GitHub change to your computer.

ANSWER

git pull origin main


5. Confirm that the web change is present locally.

ANSWER

Open the edited file on your computer and confirm that the new GitHub change is present.


[SCREENSHOT REQUIRED HERE – Successful git pull showing the GitHub change]



==================================================

BONUS ASSIGNMENT – MINI COLLABORATION SIMULATION

PERSON A

ANSWER

git checkout -b feature-A
git add .
git commit -m "Add feature A"
git push -u origin feature-A


PERSON B

ANSWER

git checkout -b feature-B
git add .
git commit -m "Add feature B"
git push -u origin feature-B


After both Pull Requests are merged:

ANSWER

git checkout main
git pull origin main


BONUS OBSERVATION

ANSWER

After multiple Pull Requests were merged, git pull downloaded the latest changes from GitHub to my local main branch.
Both feature files were available locally after pulling.


[SCREENSHOT REQUIRED HERE – Both merged PRs and final git log]
```
