# GitHub Publishing Guide

This guide walks through the fastest public-release path for this repository.

## Option A: Publish using the GitHub web interface

### 1. Create the repository
1. Sign in to GitHub.
2. Click **New repository**.
3. Repository name: `prompt-guidance-suite`
4. Description: `Reusable ChatGPT skills for structured conversations, research, coding, executive writing, academic writing, and workflow-style automation.`
5. Choose **Public**.
6. Do **not** add a README, license, or gitignore here if you are uploading this prepared repository bundle as-is.
7. Click **Create repository**.

### 2. Upload the repository files
1. In the new empty repository, click **uploading an existing file** or **Add file** -> **Upload files**.
2. Extract this bundle on your computer.
3. Open the extracted folder.
4. Drag all files and folders from the repository root into GitHub.
5. Commit to the `main` branch with a message like: `Initial public release scaffold`.

### 3. Verify the repository landing page
1. Confirm that `README.md` renders correctly.
2. Confirm that these files are visible in the repository root:
   - `LICENSE`
   - `SECURITY.md`
   - `.gitignore`
   - `CONTRIBUTING.md`
3. Confirm that `skills/` and `release-assets/` are both present.

### 4. Add repository metadata
1. Click the gear icon in the **About** section.
2. Set the website or homepage if you have one.
3. Paste the short description from `GITHUB_METADATA.md`.
4. Add topics such as:
   `chatgpt`, `skills`, `prompting`, `research`, `coding`, `writing`, `automation`, `executive-writing`, `academic-writing`, `agentic-workflows`

### 5. Create the first release
1. On the repository page, click **Releases**.
2. Click **Draft a new release**.
3. Create tag: `v1.0.0`
4. Release title: `v1.0.0 - Initial public release`
5. Paste the release notes from `RELEASE_NOTES/v1.0.0.md`.
6. Upload every ZIP file from `release-assets/` as release assets.
7. Publish the release.

### 6. Add a visible security policy
You already have a `SECURITY.md` file in the repository root. GitHub can surface this policy in the **Security** tab when the file is present in a supported location.

### 7. Final public check
Before sharing the repository:
1. Open the README in an incognito window.
2. Open the release page and confirm all ZIP assets download correctly.
3. Open one ZIP locally and confirm `SKILL.md` is at the package root.
4. Confirm there are no personal, company-specific, or private notes anywhere in the repo.

## Option B: Publish locally with Git

### 1. Create a new repository on GitHub
Create an empty public repository named `prompt-guidance-suite`.

### 2. Extract this bundle locally
Unzip the repository bundle into a local folder.

### 3. Initialize and push
Run the following commands from the repository root:

```bash
git init
git branch -M main
git add .
git commit -m "Initial public release scaffold"
git remote add origin https://github.com/<your-username>/prompt-guidance-suite.git
git push -u origin main
```

### 4. Create a release on GitHub
After pushing, open the GitHub repository in your browser and create the release from the **Releases** page.

## Suggested first public workflow

1. Publish repository contents.
2. Publish `v1.0.0` with all six ZIP assets.
3. Share the repository link.
4. Collect feedback through GitHub Issues.
5. Ship `v1.0.1` only after install and usability feedback.
