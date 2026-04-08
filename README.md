Simple CI/CD demo

This is a minimal static site used to demonstrate a basic CI/CD workflow with GitHub Actions.

What’s included
- public/index.html — the static site
- .github/workflows/ci.yml — workflow: test (grep) and deploy to GitHub Pages

Quick start (zsh)
1. Initialize and commit
   cd /Users/ratnakarchakkapalli/Documents/CICD/simple-webapp-ci
   git init
   git add .
   git commit -m "Initial commit: CI/CD demo"

2. Create a GitHub repo (web UI) named `simple-webapp-ci`, then:
   git branch -M main
   git remote add origin https://github.com/<your-username>/simple-webapp-ci.git
   git push -u origin main

Or create & push with GitHub CLI (if installed):
   gh repo create simple-webapp-ci --public --source=. --remote=origin --push

3. Watch Actions tab on GitHub. After deploy, site is at:
   https://<your-username>.github.io/simple-webapp-ci/

Notes
- The workflow looks for the text "Hello World" in `public/index.html` as a simple test.
- To change the test, edit `.github/workflows/ci.yml` or `public/index.html` and push.
