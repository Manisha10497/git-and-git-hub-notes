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
