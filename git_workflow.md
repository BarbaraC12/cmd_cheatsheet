# GIT WORKFLOW

## 🌳 BRANCHES

- master
- development
- one branch per feature

## 1️⃣ GIT COMMANDS

- `git checkout -b name-of-your-feature`
- `git push --set-upstream origin name-of-your-feature`
- code...
- `git add <file_name>` or `git add -p` and `y` for the files you want to commit

  **NB 1:** Never use `git add .`

  **NB 2:** `git add -p` doesn't add new or deleted files but only already committed files

- `git commit -m 'title of your commit'`

  **NB 3:** The title of your commit should be concise, in English, and in the present tense

  **NB 4:** Commit your work regularly

- `git checkout development`
- `git pull --prune`
- `git checkout -`
- `git merge development`
- `git push -u origin name-of-your-feature`

## 2️⃣ PULL REQUEST

- Go to your GitHub repository
- Go to **Pull requests** tab
- Click **New pull request**
- Choose **base: development** and **compare: name-of-your-feature**
- Type a title and description for your pull request
- Click **Create pull request**

  *You can request a pull request review in __Reviewers__ by clicking __Request__ next to the username of your teammate*

- Click **Merge pull request**
- Type a commit message
- Click **Confirm merge**

If your feature is finished, you can delete your branch:

- Click **Closed** to see the list of closed pull requests
- Click the pull request that's associated with the branch that you want to delete
- Click **Delete branch**

  *You can restore a deleted branch by clicking __Restore branch__*

## 3️⃣ ISSUES

- Use GitHub Issues to track and manage tasks, bugs, and enhancements.
- Click **Issues** tab in your GitHub repository to view and create issues.
- Clearly describe the issue, including steps to reproduce for bugs.
- Use labels (e.g., bug, enhancement, task) to categorize issues.
- Assign issues to team members responsible for resolution.
- Mention issues in commit messages using keywords like `closes #issue_number`.
- Keep discussions on issues constructive and focused on problem-solving.

## 4️⃣ ADDITIONAL PRACTICES

- **Configuration Git:** Configure Git settings, especially if your team uses specific configurations or aliases for frequently used commands.
- **Git Ignore:** Use a `.gitignore` file to exclude specific files or directories from version control.
- **Branches to Avoid:** Follow team conventions regarding branch usage, especially branches to avoid (e.g., direct commits on `master`).
- **Conflict Resolution:** Learn effective conflict resolution strategies during merges to handle conflicts efficiently.
- **Custom Scripts and Tools:** Utilize custom scripts or tools that your team may have developed to streamline the Git workflow.
- **Best Practices:** Follow Git best practices, such as avoiding overly large commits and writing meaningful commit messages.
- **Useful Links:** Keep a section with useful links to online resources, tutorials, and reference documents.

These additional practices are meant to enhance your Git/GitHub workflow based on specific needs. Customize the document further based on your team's environment and development requirements.

## 5️⃣ UNDO MISTAKES

If you made a mistake, don't panic:

- **Undo the local merge:**
  If the merge hasn't been pushed to the remote repository yet, you can undo the local merge using the `git reset --hard HEAD` command to go back to the state before the merge, discarding local changes.
  ```bash
  git reset --hard HEAD
  ```

- **Check for uncommitted changes:**
  If you've already committed the merge changes, you can view the recent commits using `git log`. Note the commit hash of the commit you want to revert.
  ```bash
  git log
  ```

- **Revert to a previous commit:**
  Use the `git reset --hard <commit_hash>` command to revert to the state of the repository at a specific commit, discarding all subsequent commits, including the unintentional deletions.
  ```bash
  git reset --hard <commit_hash>
  ```

- **Force push to update the remote repository (if necessary):**
  If you've already pushed these changes to the remote repository, you'll need to force push after locally undoing the changes.
  ```bash
  git push origin <branch_name> --force
  ```
  Replace `<branch_name>` with the name of your branch.

  Note: Using `--force` to push can lead to loss of history on the remote repository, so use it with caution. Inform others working on the same branch to avoid complications.
