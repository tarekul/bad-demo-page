# AI Code Review GitHub Action

Automatically runs AI-powered code reviews on pull requests using **Gemini 2.5 Flash**. Lints JS/JSX files and posts review comments on PRs.

---

## Setup

1. **Add Workflow**

Create `.github/workflows/code-review.yml` in your repo and paste the workflow YAML.

2. **Add Secrets**

- `GCP_API_KEY` – Gemini 2.5 Flash API key.
- `GITHUB_TOKEN` – Already available in GitHub Actions.

3. **Optional: Install ESLint**

npm install eslint --save-dev
npx eslint --init

4. **Open a pull request to main.**

The action will:

- Checkout code
- Install dependencies
- Lint changed JS/JSX files
- Send diff to Gemini 2.5 Flash
- Post AI review as PR comment

## Notes

- Only works on pull requests.
- For best results, keep PRs small.
