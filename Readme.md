# Project Workflow Guidelines

## 1. Branch Management

### 1.1 Main Branches
- **Main (or Master) Branch**
  - Always in a deployable state.
  - Only tested and reviewed code is merged here.
- **Develop Branch**
  - Integration branch for features.
  - Code is merged here after it passes initial testing.

### 1.2 Feature Branches
- **Feature Branches (`feat`)**
  - Named using the format: `feat/short-description` (e.g., `feat/user-authentication`).
  - Created for new features, enhancements, or large refactors.

### 1.3 Bugfix Branches
- **Bugfix Branches (`bugfix`)**
  - Named using the format: `bugfix/short-description` (e.g., `bugfix/login-issue`).
  - Created for resolving bugs identified during development.

### 1.4 Hotfix Branches
- **Hotfix Branches (`hotfix`)**
  - Named using the format: `hotfix/short-description` (e.g., `hotfix/login-bug`).
  - Created for urgent fixes that need to go directly to the main branch during code freeze.

### 1.5 Release Branches
- **Release Branches (`release`)**
  - Named using the format: `release/version-number` (e.g., `release/1.2.0`).
  - Created when preparing for a new production release or QA testing.

## 2. Code Pushing Guidelines

### 2.1 Commit Messages
- Use meaningful commit messages.
  - **Good**: `Fix issue with user login on mobile devices`
  - **Bad**: `Fixed stuff`
- Use the present tense (e.g., "Add feature" not "Added feature").

### 2.2 Pushing Code
- **Feature Branch**
  - Work on the feature branch locally.
  - Push code to the corresponding remote feature branch.
- **Bugfix Branch**
  - Work on the bugfix branch locally.
  - Push code to the corresponding remote bugfix branch.
- **Hotfix Branch**
  - Work on the hotfix branch locally.
  - Push code to the corresponding remote hotfix branch.

## 3. Creating Pull Requests (PRs)

### 3.1 Before Creating a Pull Request
- Ensure your code is well-tested.
- Run linting tools to check for code quality issues.
- Rebase or merge the latest changes from the develop branch to your feature branch to avoid conflicts.
- **Update Release Notes**
  - Update the release note in Fastlane.
  - If building an APK, update the changelog file based on the release note and other changes.
- **Documentation**
  - Document each and every code change except for widgets.

### 3.2 Creating the Pull Request
- **Title**
  - Use descriptive titles (e.g., `Add user authentication feature`).
- **Description**
  - Provide a detailed description of the changes.
  - Include any relevant ticket numbers (e.g., `Fixes #123`).
  - Mention any dependencies or steps required for testing.

### 3.3 Pull Request Checklist
- Ensure all automated tests pass.
- Verify there are no linting errors.
- Confirm the branch is up-to-date with the develop branch.

## 4. Code Reviews

### 4.1 Requesting a Review
- Assign reviewers who are knowledgeable about the code.
- Address any questions or feedback from reviewers promptly.

### 4.2 Reviewing Code
- Check for code quality, readability, and maintainability.
- Ensure code follows the project’s style guide.
- Verify that all new code is covered by unit tests.

## 5. Merging Code

### 5.1 Merging Pull Requests
- **Feature Branch**
  - Merge into the develop branch after approval.
  - Ensure the develop branch is stable before merging.
- **Bugfix Branch**
  - Merge into the develop branch after approval.
- **Hotfix Branch**
  - Merge into both the develop and main branches after approval.

### 5.2 Post-Merge
- Delete the feature, bugfix, or hotfix branch after merging.
- Notify the team about the merged changes.


