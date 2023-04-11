 # Git
**Q: What is Git?**  
A: Git is a distributed version control system that allows developers to track changes to source code and collaborate on software projects.

**Q: What is the difference between Git and other version control systems, like SVN?**  
A: Git is a distributed version control system, which means that each developer has a complete copy of the repository on their local machine. This allows for easier collaboration and faster branching and merging. SVN, on the other hand, uses a centralized repository model, which can make it slower and more difficult to collaborate on large projects.

**Q: What is a Git repository?**  
A: A Git repository is a directory that contains all of the files and history for a project. Developers can make changes to the files in the repository and track those changes using Git.

**Q: What is a Git branch?**  
A: A Git branch is a separate line of development that diverges from the main branch of a Git repository. Developers can create branches to work on new features or bug fixes without affecting the main codebase.

**Q: How do you create a new Git branch?**  
A: To create a new Git branch, you can use the 'git branch' command followed by the name of the new branch. For example, 'git branch feature-branch' will create a new branch called 'feature-branch'.

**Q: What is a Git merge?**  
A: A Git merge is a way to combine two or more branches of a Git repository. When you merge two branches, Git combines the changes made in both branches and creates a new commit that represents the merged state.

**Q: What is a Git pull request?**  
A: A Git pull request is a way for developers to submit changes to a Git repository and ask for those changes to be merged into the main codebase. Pull requests can be reviewed by other developers and comments can be added before the changes are merged.

**Q: What is Git rebase?**  
A: Git rebase is a way to change the history of a Git repository by moving commits to a new base. This can be useful for keeping the Git history clean and easier to understand, but it can also be dangerous if not done carefully.

**Q: How do you revert a Git commit?**  
A: To revert a Git commit, you can use the 'git revert' command followed by the hash of the commit you want to revert. Git will create a new commit that undoes the changes made in the original commit.

**Q: What is Git stash?**  
A: Git stash is a way to temporarily save changes that are not yet ready to be committed to the Git repository. This can be useful if you need to switch to a different branch or pull in changes from another branch before finishing your changes. You can later apply the stash to the working directory using the 'git stash apply' command.

**Q: What is Git cherry-picking?**  
A: Git cherry-picking is a command used to apply a specific commit from one branch to another. It allows you to copy changes made in one branch and apply them to another branch without merging the entire branch.

**Q: How do you cherry-pick a commit in Git?**  
A: To cherry-pick a commit in Git, you can use the 'git cherry-pick' command followed by the hash of the commit you want to apply. For example, 'git cherry-pick abc123' will apply the changes made in commit 'abc123' to the current branch.

**Q: What is the difference between merging and cherry-picking in Git?**  
A: Merging combines changes from one branch into another, while cherry-picking applies a specific commit from one branch to another. Merging can result in conflicts if changes have been made to the same file in both branches, while cherry-picking applies a specific set of changes without affecting the rest of the branch.

**Q: Can you cherry-pick multiple commits at once?**  
A: Yes, you can cherry-pick multiple commits at once by providing a range of commit hashes to the 'git cherry-pick' command. For example, 'git cherry-pick abc123..def456' will apply all commits between 'abc123' and 'def456' to the current branch.

**Q: What happens if a cherry-picked commit conflicts with changes in the target branch?**  
A: If a cherry-picked commit conflicts with changes in the target branch, Git will mark the file as conflicted and require you to manually resolve the conflict before committing the changes.

**Q: How do you undo a cherry-pick in Git?**  
A: To undo a cherry-pick in Git, you can use the 'git cherry-pick --abort' command. This will undo the cherry-pick and return the repository to its previous state.

**Q: What is Git cherry-pick -x?**  
A: Git cherry-pick -x is a command that adds a note to the commit message indicating that the changes were cherry-picked from another branch. This can be useful for keeping track of where changes came from and why they were added to the branch.

**Q: What is a Git patch?**  
A: A Git patch is a file that contains the changes made in a commit. It can be used to apply changes from one branch to another or to share changes with other developers who do not have access to the Git repository.

**Q: How do you apply a Git patch?**  
A: To apply a Git patch, you can use the 'git apply' command followed by the path to the patch file. For example, 'git apply my-patch.patch' will apply the changes in 'my-patch.patch' to the current branch.

**Q: What is the difference between a Git patch and Git cherry-pick?**  
A: A Git patch is a file that contains the changes made in a commit, while Git cherry-pick applies a specific commit to another branch. Git patches can be used to apply changes between branches or to share changes with other developers, while Git cherry-pick is used to selectively apply changes from one branch to another.
