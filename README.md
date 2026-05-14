# 🗺️ GitHub Basics: Choose Your Own Adventure Exercises

Welcome! After today's session, pick the adventures that match where you want to grow. Each one builds real, practical skills you can apply to your projects right away.

---

## ⚔️ Adventure 1: Introduction to GitHub

> **Start here if you're new to GitHub — or want a solid refresher.**

### Your Path

**Part A — Microsoft Learn: Introduction to GitHub**
📖 [learn.microsoft.com — Introduction to GitHub](https://learn.microsoft.com/en-us/training/modules/introduction-to-github/1-introduction)

Work through this guided reading module. It covers the core concepts:
- What GitHub is and how it fits into your workflow
- Repositories, branches, commits, and pull requests
- The GitHub Flow

> At the end of the module, it links directly to the GitHub Skills hands-on exercise. Follow it!

**Part B — GitHub Skills: Introduction to GitHub**
🛠️ [github.com/skills/introduction-to-github](https://github.com/skills/introduction-to-github)

A browser-based, hands-on exercise. You'll practice:
1. Creating a branch
2. Committing a file
3. Opening a pull request
4. Merging your changes

No local tools required — everything happens in the browser.

---

## 🔑 Adventure 2: Configure SSH for GitHub

> **Set up secure, passwordless authentication to GitHub from your local machine.**

### Requirements
- A GitHub account
- Git installed locally
- A terminal (Terminal on Mac/Linux · Git Bash or WSL on Windows)

### Your Path

The GitHub docs walk you through the full process with step-by-step instructions. Use the **platform toggle** at the top of each page to switch between Mac, Windows, and Linux instructions.

1. **Generate a new SSH key & add it to the SSH agent**
   📄 [docs.github.com — Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

2. **Add your public key to your GitHub account**
   📄 [docs.github.com — Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

3. **Test your connection** — the docs include a verification step to confirm everything is working.

---

## 🛡️ Adventure 3: Explore Repo Rulesets & CODEOWNERS

> **Discover how to govern your repositories and automate code ownership.**

### Requirements
- A GitHub account
- Admin access to at least one repository (either create one, or access one you already have access to)

### Your Path

**Part A — Repository Rulesets**
📄 [About rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets)

1. Review the About Rulesets docs above.
2. Navigate to a repository → **Settings** → **Rules** → **Rulesets**
3. Create a new ruleset and explore the options:
   - Restrict who can push to a branch
   - Require pull request reviews before merging
   - Require status checks to pass
   - Block force pushes
4. Consider: *Which of these rules would improve how your team ships code today?*

**Part B — CODEOWNERS**
📄 [About code owners](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)

1. Review the About code owners doc above.
2. Navigate to (or create) a `CODEOWNERS` file in the root, `docs/`, or `.github/` folder of a repo
3. Add a pattern to assign ownership, for example:
   ```
   # All .js files owned by the frontend team
   *.js   @your-org/frontend-team
   ```
4. Consider: *Which directories or critical files in your existing projects should have designated owners? Who should be auto-requested for review?*

---

## 🤖 Adventure 4: Build with GitHub Copilot (Cloud Agent, Code Review Agent)

> **Let Copilot scaffold, build, review, and iterate on a real project — from scratch.**

### Requirements
- A GitHub account with **GitHub Copilot** assigned 
- Copilot coding agent & code review agent enabled (these should be enabled automatically, but if not, contact your administrator)

---

### Step 1 — Create a new repo & prompt Copilot at creation

1. Go to [github.com](https://github.com) → **New repository**
2. Give it a name (e.g., `calculator-pages`)
3. At repo creation, locate the **"Start coding with Copilot"** prompt and enter:

   > *Create a simple calculator app that can be deployed via GitHub Pages. Create a README describing the app and giving me the steps necessary to deploy to GitHub Pages.*

4. Click **Create repository** — Copilot's coding agent will begin working.

---

### Step 2 — Explore the Agents tab

5. Navigate to the **Agents** tab in your repository (or watch the agent's activity in the Issues view)
6. Observe in real time:
   - What files Copilot is creating
   - What decisions and tool calls it's making
   - The agent's progress log

---

### Step 3 — Review the Pull Request Copilot Opens

7. When the agent finishes, it opens a **Pull Request** with all generated code
8. Review the diff — examine the files

---

### Step 4 — Add Copilot Code Review

9. Inside the PR, click **"Request a review"** and select **Copilot** as the reviewer
10. Copilot will analyze the code and post inline comments with suggestions
11. Review its feedback, address any issues, then **Merge the PR**

---

### Step 5 — Start a new Copilot coding agent session for a tweak

12. Open the **Agents** tab (or create a new Issue and assign Copilot) and start a new coding agent session
13. Give Copilot a follow-up prompt, for example:

    > *Add a dark mode toggle to the calculator app.*

14. Watch Copilot create a new branch and open a new PR with the changes
15. Repeat the review and merge cycle

---

> 💡 **Tip:** You may need to edit the GitHub Pages settings to see your deployment go live. Copilot should include these instructions in the repo README.md if included in the prompt. You can access these settings by going to repo settings > Pages to access. If Copilot did not originally include the deployment instructions / settings changes, you can kick off another agent session to include these. 

---

*Happy adventuring! 🚀*
