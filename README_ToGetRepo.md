# WebSite
WebSite of Appartements Azur

# Use GitHub Desktop or add a ssh key :

## 1. Generate a New SSH Key
(in Git Bash app):

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

When prompted to "Enter file in which to save the key," type a custom path and unique name, for example:

 - /users/yourusername/.ssh/id_ed25519 (macOS/Linux)
 - C:\Users\yourusername\.ssh\id_ed25519 (Windows)
 
## 2. Add the New Key to Your GitHub Account

- Copy the contents of your brand new public key to your clipboard:
```bash
cat ~/.ssh/id_ed25519.pub
```

- Log into your GitHub account.
- Navigate to Settings > SSH and GPG keys > New SSH Key.
- Provide a descriptive title (e.g., "Laptop") and paste the public key into the field.

## 3. To Clone and Push Repositories Correctly

Because your primary account maps directly to github.com, you can interact with it normally. However, for repositories belonging to your second account, you must substitute github.com with your custom alias (github.com-second) inside the SSH URL when cloning or setting up remotes.
- To clone a repository for your second account (in COMMAND PROMPT):
 
``` bash
# Standard URL: git@github.com:username/repo.git
# Modified URL using your alias:
git clone git@github.com:username/repo.git
```
- To PUSH a repository for your second account (in COMMAND PROMPT):
 
``` bash
git push origin main
```

## 4. Create a new branch 
- Do not work directly on the main branch.
- Create a new branch
``` bash
git checkout -b your-new-branch-name
```