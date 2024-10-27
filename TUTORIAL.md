# Intro to Git and GitHub Tutorial

Authors: 
- [Marita Georganta](https://education.github.com/git-cheat-sheet-education.pdf)
- [ChatGPT](https://chatgpt.com)

Congratulations! Either out of choice or necessity, you are here to learn the basics of Git, a popular version control system, and GitHub, a platform for collaborative coding.

In a nutshell, Git is a version control system. That means that it allows you to track changes in your code throughout your development. Technically, you can live without it, but when your code was working fine and then it suddenly breaks, it would be great to have a tool that lets you retrace your steps. Well, that's Git!

And of course, things get very tricky when many people work on the same document, let alone a coding project. GitHub is a platform for collaborative coding, equivalent to Google Docs. 

### **Git Fundamentals**
By the end of this session, you will know how to do the actions that you will need 90% of the time:
1. Fork a repository on GitHub to create your own copy.
2. Clone the forked repository to your local machine.
3. Make changes to files, stage them, and commit them using Git.
4. Push your changes to GitHub.
5. Fetch updates from the original (upstream) repository.
6. Create and switch branches.
7. Open a pull request (PR) to propose your changes.

---

### **Prerequisites**

You need to ensure that:
1. You have git installed on your machine, google it.
2. You have set up your GitHub account on your terminal, it's like 'signing in' to your account to work with remote repositories. Google it.

* You should google it because it's a good exercise, not because the author was not bothered to include it in the resources, because they did put it. 

### **Tutorial Outline**

#### **1. Forking the Repository**
   - Begin by **forking** this repository. Forking creates a personal copy of the repository under your GitHub account.
   - **Instructions:**
     1. Navigate to the repository on GitHub.
     2. Click on the **Fork** button at the top right corner of the page.
     3. You now have a copy of the repository in your GitHub account.

#### **2. Cloning Your Forked Repository**
   - Next, clone your forked repository to your local machine so you can start working with it.
   - **Command:**
     ```bash
     git clone <your-forked-repo-URL>
     ```
   - Replace `<your-forked-repo-URL>` with the URL of your forked repository, which can be found on your GitHub repository page.

**Do I always fork a repo when I want to work on it?**
- FORK + CLONE FORKED --> When you want to test and use someone else's repo on some work they did. If you make some changes that would contribute to their work, you can let them know by opening a Pull Request and they can review and decide if they would like to merge your changes with their repo. Both Pull Requests and merging are explained later. 
- NO FORK + CLONE DIRECTLY --> When you are working together with other people, maybe as a group. Good practice says to make your own branch for your development ad let the rest of the team to review before merging with the main branch. Branches are explained later.

#### **3. Making and Committing Changes**
   - Create a file in this repository (`CONTRIBUTORS.md`) and make add your name.
   - While you are on it, you might as well look up markdown syntax and make the contributor page look a bit nicer. Embed a link to your LinkedIn or something.
   - Use the following commands to stage and commit your changes.
   - **Commands:**
     ```bash
     git add <file-name>        # Stages your changes
     git commit -m "Your message"  # Commits the staged changes
     git status                  # Checks the current status
     ```

#### **4. Pushing Changes to GitHub**
   - Push your changes to GitHub to update the remote repository on the `main` branch.
   - **Command:**
     ```bash
     git push origin main
     ```

#### **5. Fetching Updates from the Original Repository**
   - If there are updates in the original repository, fetch them to keep your fork in sync.
   - **Commands:**
     ```bash
     git fetch                             # Fetch updates 
     git merge main                       # Merge updates into your main branch
     ```

**What is the point of git status and git fetch?**
Not much if you are working alone. However, these two commands are an absolute must for when working with more people or when you go back to your code after some time or from different machines.
- `git fetch`: checks for changes on the remote repo, maybe someone has pushed something while you were working, therefore it is missing from your local repo.
- `git status`: gives you an overview of things you have changed locally and are not in sync with the remote repo.
Note that you must get into the habit of using both commands, as `git status` will not show what `git fetch` will and vice versa, leading to merging issues. 

#### **6. Branching and Creating a Pull Request**
   - Create a new branch for a small update.
   - Good practice says that in a team of many people, each task takes its own development branch. If each person on the team has their own task, then this translates to everyone having their own branch.
   - **Commands:**
     ```bash
     git checkout -b <branch-name>   # Creates and switches to a new branch
     ```
   - Make another small change, commit it, and push the branch.
   - **Commands:**
     ```bash
     git add <file-name>
     git commit -m "Your message"
     git push origin <branch-name>
     ```
   - On GitHub, navigate to your repository, find your branch, and open a **Pull Request**.
   - **Pull Request:** A PR allows you to propose your changes, get feedback, and review code before merging it.

---

### **Key Git Commands Summary**

| Action                           | Command                              |
|----------------------------------|--------------------------------------|
| Fork a repository                | Click **Fork** on GitHub             |
| Clone a repository               | `git clone <repository-URL>`         |
| Check repository status          | `git status`                         |
| Stage changes                    | `git add <file-name>`                |
| Commit staged changes            | `git commit -m "Message"`            |
| Push changes to GitHub           | `git push origin main`               |
| Create a new branch              | `git checkout -b <branch-name>`      |
| Switch branches                  | `git checkout <branch-name>`         |
| Push branch to GitHub            | `git push origin <branch-name>`      |


---

### **Additional Resources**
- [Git Cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Markdown Syntax Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
- [Install and Configure Git on Windows](https://www.youtube.com/watch?v=AdzKzlp66sQ&t=8s)

Time to break stuff! Git and GitHub are essential tools for collaborative development, use them in your projects and see how many issues you will receive and resolve.

---

Happy coding, debugging, and frustration, and welcome to the world of version control!
