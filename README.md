# git-and-git-hub-notes
Step 0: Create Repository on GitHub
On GitHub:
•	Create a new repository
•	Select Add README file
•	Click Create repository
•	Copy the repository URL
🔹 Step 1: Clone Repository to Local (VS Code)
git clone <repository-URL>
📌 This creates a local copy of the GitHub repository.
Then in VS Code:
•	File → Open Folder
•	Select the cloned repository folder
🔹 Step 2: Modify File (Working Directory)
•	Edit README.md
•	Add content
•	Save the file
📌 File is now in the Working Directory
🔹 Step 3: Check File Status
git status
✔ Shows:
•	Modified files
•	Untracked files
📌 Confirms file is changed but not staged
🔹 Step 4: Add File to Staging Area
git add .
📌 Moves file from:
Working Directory → Staging Area
🔹 Step 5: Verify Staged Changes
git status
✔ Confirms file is now in staging
🔹 Step 6: Commit Changes
git commit -m "Added project description to README"
📌 Moves changes from:
Staging Area → Local Repository (Commit History)
🔹 Step 7: Push Changes to GitHub
git push
done
Feature / Hotfix Branch Strategy (ChatGPT)
This strategy ensures that main (or master) branch remains stable, while new work is done in separate branches.
🔹 Step-by-Step Feature Branch Workflow
1️⃣ Check current branch
git branch
➡ Shows all branches and highlights the current branch (main).
2️⃣ Create and switch to a feature branch
git checkout -b feature/editing-readme-file
✔ Creates a new feature branch
✔ Automatically switches to it
✔ Naming convention: feature/<short-description>
3️⃣ Make code changes
•	Edit README.md
•	Save the changes
4️⃣ Check file status
git status
➡ Shows modified files in working directory
5️⃣ Add changes to staging area
git add .
➡ Moves files from working directory → staging area
6️⃣ Verify staging status
git status
➡ Confirms files are ready to commit
7️⃣ Commit the changes
git commit -m "Updated README with project details"
➡ Saves changes locally in the feature branch
8️⃣ Push feature branch to remote
git push --set-upstream origin feature/editing-readme-file
✔ Pushes code to remote feature branch
✔ Still does NOT affect main branch
🔀 Why Pull Request (PR) Is Required?
At this stage:
•	Code exists only in feature branch
•	main branch is untouched
•	To merge feature → main safely, we use a Pull Request (PR)
9️⃣ Raise a Pull Request
•	Source branch: feature/editing-readme-file
•	Target branch: main
•	Add description & reviewers
✔ Enables code review
✔ CI/CD checks can run
✔ Ensures quality & safety
🔟 Merge the Pull Request
•	Once reviews pass
•	Merge button becomes active
•	Click Merge PR
🎉 Now the feature branch code is merged into main
🧯 Hotfix Branch Strategy (Production Issues)
Used for urgent production bugs
git checkout -b hotfix/fix-login-issue main
•	Fix critical issue
•	Commit changes
•	Raise PR → main
•	Merge immediately
✔ Faster than feature branches
✔ Used only for emergencies
Best Practices (Very Important)
1.	Keep PRs small & focused
2.	Write clear commit messages
3.	Add proper description (what & why)
4.	Assign reviewers
5.	Fix CI/CD pipeline failures before merge
6.	Rebase or resolve conflicts if needed

