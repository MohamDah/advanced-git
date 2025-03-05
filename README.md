
# Part 1: Refining Git History (10 Challenges)

## 1. Missing File Fix:
```bash
git status
git log
git add test4.md
git commit --amend --no-edit
```

## 2. Editing Commit History:
```bash
git rebase -i HEAD~2
```

## 8. Cherry-Picking Commits:
```bash
git branch ft/branch
git checkout ft/branch
echo "content" > test5.md
git add test5.md
git commit -m "feat: Implemented test 5"
git checkout main
git log ft/branch --oneline
git cherry-pick 13376c6
```

## 9. Visualizing Commit History (Bonus):
```bash
git log --graph
git log --graph --oneline
```

## 10. Understanding Reflogs (Bonus):
```bash
git reflog
```


# Part 2: Branching Basics (10 Challenges)

## 1. Feature Branch Creation:
```bash
git branch ft/new-feature
git checkout ft/new-feature
```

## 2. Working on the Feature Branch:
```bash
echo "some content" > feature.txt
git add feature.txt
git commit -m "Implemented core functionality for new feature"
```

## 3. Switching Back and Making More Changes:
```bash
git checkout main
echo "some introductory content" > readme.txt
git add readme.txt
git commit -m "Updated project readme"
```

## 4. Local vs. Remote Branches:
```bash
git remote add origin git@github.com:MohamDah/advanced-git.git
git push origin main
```

## 5. Branch Deletion:
```bash
git checkout ft/new-feature
git rebase main
git checkout main
git merge ft/new-feature
git branch -d ft/new-feature
```

## 6. Creating a Branch from a Commit:
```bash
git checkout -b ft/new-branch-from-commit HEAD~2
```

## 7. Branch Merging:
```bash 
git checkout ft/new-branch-from-commit
echo "other feature" > feature.txt
git add feature.txt 
git commit -m "feat: new feature"
git checkout main
git merge ft/new-branch-from-commit 
# CONFLICT (add/add): Merge conflict in feature.txt
git add feature.txt 
git commit -m "resolve merge"
```
## 8. Branch Rebasing:
```bash
echo "changes on main" > feature.txt
git add feature.txt
git commit -m "feat: main feature"
git checkout ft/new-branch-from-commit
echo "changes on ft" > feature.txt
git add feature.txt
git commit -m "feat: feature feature"
git rebase main
git add feature.txt
git rebase --continue
git checkout main
git merge ft/new-branch-from-commit 
```

## 9. Renaming Branches:
```bash
git branch -m ft/new-branch-from-commit ft/improved-branch-name
```

## 10. Checking Out Detached HEAD:
```bash
git checkout 10ce372
```


# Part 3: Advanced Workflows (10+ Challenges)

## 1. Stashing Changes:
```bash
git stash
```

## 2. Retrieving Stashed Changes:
```bash
git stash pop
```

## 3. Branch Merging Conflicts (Continued):
```bash
git checkout -b ft/conflict-branch
echo "line 1" > conflict-file.txt
git add conflict-file.txt
git commit -m "feat: added conflict-file with two lines"

git checkout main
echo "line 3" > conflict-file.txt
git add conflict-file.txt
git commit -m "feat: added conflict-file with different second line"

git merge ft/conflict-branch
git add conflict-file.txt
git commit -m "fix: resolved merge conflict in conflict-file.txt"
```

## 4. Resolving Merge Conflicts with a Merge Tool:
```bash
git mergetool
```

## 5. Understanding Detached HEAD State:
```bash
git checkout main
```

## 6. Ignoring Files/Directories:
```bash
echo "/tmp" >> .gitignore
```

## 7. Working with Tags:
```bash
git tag v1.0
```

## 8. Listing and Deleting Tags:
```bash
git tag
git tag -d v1.0
```

## 9. Pushing Local Work to Remote Repositories:
```bash
git push origin main
```

## 10. Pulling Changes from Remote Repositories:
```bash
git fetch origin main
git diff origin/main
git rebase origin/main
```
