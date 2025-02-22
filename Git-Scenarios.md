# Some real-word scenarios for practicing Git

## Scenario 1: Initialize a Repository and Push Code

__Objective__: Learn how to create a Git repository, add files, commit changes, and push to GitHub/GitLab.

#### Steps
1. Initialize a Git repository:
   ```sh
   mkdir my_project && cd my_project
   git init
   ```

2. Create a new README.md file:
   ```sh
   echo "# My Project" > README.md
   ```

3. Stage and commit the file:
   ```sh
   git add README.md
   git commit -m "Initial commit"
   ```

4. Link to a remote GitHub/GitLab repository:
   ```sh
   git remote add origin <repo-url>
   ```

5. Push to GitHub/GitLab:
   ```sh
   git push -u origin main
   ```

## Scenario 2: Create a New Branch and Merge Changes

__Objective__: Learn branching, making changes, and merging them.

#### Steps
1. Create a new branch:
   ```
   git checkout -b feature-branch
   ```

2. Modify a file and commit changes:
   ```
   echo "New Feature" >> feature.txt
   git add feature.txt
   git commit -m "Added new feature"
   ```

3. Switch back to `main` and merge the branch:
   ```
   git checkout main
   git merge feature-branch
   ```

4. Push the updated branch to GitHub/GitLab:
   ```
   git push origin main
   ```

## Scenario 3: Cloning a Repository and Creating a Pull Request

