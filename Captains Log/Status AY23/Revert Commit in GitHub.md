---
title: Revert Commit in GitHub
created: 2023-10-02 11:10
modified: 2023-10-02 11:10
---

# Revert Commit in GitHub

Certainly! Below is a summary of the steps you can take for various tasks in git and GitHub, tailored for one specific repository. Each section addresses a different issue or operation.

---

### To Revert a Commit (Before Syncing with GitHub)

1. Open project in Visual Studio Code.
2. Open the terminal.

    ```bash
    git log
    git revert <commit_hash>
    git commit -m "Reverting commit"
    git push
    ```

🛑 Press `q` to exit the git log in the terminal.

---

### To Exit a Stuck Commit Prompt

1. In the terminal, press `Ctrl + C`.

---

### To Sync Local and Remote Repositories

1. In the terminal:

    ```bash
    git status
    git checkout -b temp
    git commit -m "Temp commit"
    git checkout main
    git pull --rebase
    git push
    ```

---

### To Recover Deleted Files

1. If you're on a temporary branch:

    ```bash
    git checkout temp
    git log
    git checkout <commit_hash> -- path/to/deleted/file
    git commit -m "Restored files"
    git checkout main
    git merge temp
    git push
    ```

🛑 Use `git log --pretty=oneline` if the log is too long to read easily.

---

### To Wipe Local Repo and Clone Fresh from Remote

1. Navigate to your project directory (`2023-olc-html-hacks`) in the terminal.

    ```bash
    cd 2023-olc-html-hacks
    rm -rf .git
    ```

2. Re-clone the repository:

    ```bash
    git clone https://github.com/mundorfd/2023-olc-html-hacks.git
    ```

🛑 Be sure to use the correct repository URL. Do not include `/tree/main` or similar subpaths.


## Related Ideas

[[GitHub]]

## References

## Linked files

```dataview
LIST FROM [[]]
sort file.name ASC
```

