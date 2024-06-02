# git-sync-automator
# Repository Synchronization Script
This script automates the process of creating repositories in one GitHub account (Account B) based on existing repositories in another account (Account A). It also synchronizes branches between the two accounts.

## Prerequisites
### 1. SSH Configuration:
- Ensure that SSH is already configured for both REMOTE_A and REMOTE_B.
- This script assumes that you can authenticate using SSH keys.
### 2. Personal Access Tokens (PATs):
- Obtain personal access tokens (PATs) for both accounts with the necessary permissions (e.g., “repo” scope).
- Set the tokens in the script as PAT_A and PAT_B.
## Usage
### 1. Clone Repositories:
- The script fetches repository names from the specified organization (%ORG%) in Account A.
- It creates corresponding private repositories in Account B.
- Clones each repository from Account A to the local machine.
### 2. Set Up Remotes:
- Adds a remote (%REMOTE_B%) for each repository pointing to the corresponding repository in Account B.
- Fetches the latest changes from the original repository.
## 3. Push Main Branch:
- Pushes the main branch to Account B.
## Synchronize Branches:
- Fetches all branches from the original repository.
- Creates and checks out each branch locally.
- Pushes the branch to Account B.
- Pulls any updates from the original repository.
- Pushes the updated branch to Account B.
### 5. Cleanup (Optional):
- Removes the local clone of each repository (optional).
## Execution
1. Run the script in a Windows command prompt or batch file.
2. Follow the prompts and monitor the progress.
3. The sync.cmd file will be generated, containing synchronization commands for each branch.
