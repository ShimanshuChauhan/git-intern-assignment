# Git and GitHub Intern Assignment

## Objective

This assignment teaches you how to:

- Clone a GitHub repository
- Create a Git branch
- Make and review changes
- Commit and push changes
- Create a pull request
- Respond to review feedback
- Resolve merge conflicts
- Merge a pull request

> **Important:** Never commit directly to the `main` branch.

## Assignment

Add your personal profile to the `interns.md` file using this format:

```markdown
## Your Name

- Role: Your internship role
- Location: Your city
- Favorite technology: Your favorite language or framework
- Learning goal: What you want to learn during this internship
- Fun fact: One appropriate fact about yourself
```

Do not edit or delete another intern’s profile.

## Step 1: Clone the repository

Copy the repository URL from GitHub and run:

```bash
git clone <repository-url>
cd git-intern-assignment
```

## Step 2: Create a branch

Create a branch using your name:

```bash
git switch -c intern/<your-name>
```

Example:

```bash
git switch -c intern/rahul-sharma
```

Check your current branch:

```bash
git branch
```

## Step 3: Make your change

Open `interns.md` and add your profile at the bottom of the file.

Save the file when finished.

## Step 4: Review your change

Check which files changed:

```bash
git status
```

Review the exact changes:

```bash
git diff
```

Make sure:

- You changed only `interns.md`.
- You added only your own profile.
- The Markdown formatting is correct.
- You did not add passwords, tokens, or private information.

## Step 5: Commit your change

Stage the file:

```bash
git add interns.md
```

Create a commit:

```bash
git commit -m "Add profile for Your Name"
```

Example:

```bash
git commit -m "Add profile for Rahul Sharma"
```

## Step 6: Push your branch

```bash
git push -u origin intern/<your-name>
```

Example:

```bash
git push -u origin intern/rahul-sharma
```

## Step 7: Create a pull request

1. Open the repository on GitHub.
2. Click **Compare & pull request**.
3. Confirm that the destination branch is `main`.
4. Confirm that the source branch is `intern/<your-name>`.
5. Use this PR title:

```text
Add profile for Your Name
```

6. Add this description:

```markdown
## Summary

- Added my profile to `interns.md`.
- Checked that no unrelated files were changed.

## Verification

- [x] Reviewed the changes using `git diff`.
- [x] Checked the Markdown formatting.
- [x] Did not include private information.

Closes #ISSUE_NUMBER
```

Replace `ISSUE_NUMBER` with your assigned GitHub issue number.

7. Request a review from your mentor.
8. Do not merge the pull request yourself until it is approved.

## Step 8: Address review feedback

If your reviewer requests a change:

1. Make the requested change in `interns.md`.
2. Run:

```bash
git add interns.md
git commit -m "Address review feedback"
git push
```

The existing pull request will update automatically. Do not create another pull request.

## Step 9: Update your local repository

After the pull request is merged:

```bash
git switch main
git pull origin main
git branch -d intern/<your-name>
```

## Merge conflict exercise

If Git reports a conflict, open the affected file. You may see:

```text
<<<<<<< HEAD
Your version
=======
The version from main
>>>>>>> origin/main
```

Keep the correct content and remove the conflict markers. Then run:

```bash
git add interns.md
git commit -m "Resolve profile merge conflict"
git push
```

Ask your mentor for help if you are unsure which content to keep.

## Completion checklist

- [ ] I created a separate branch.
- [ ] I added my profile to `interns.md`.
- [ ] I reviewed my changes.
- [ ] I created a clear commit.
- [ ] I pushed my branch.
- [ ] I opened a pull request.
- [ ] I linked my assigned issue.
- [ ] I responded to review feedback.
- [ ] My pull request was approved and merged.
- [ ] I updated my local `main` branch.

## Reflection questions

Answer these questions in your assigned GitHub issue:

1. What is the difference between Git and GitHub?
2. Why do we create branches?
3. What is the difference between a commit and a push?
4. What happens when you push another commit to an open pull request?
5. What causes a merge conflict?
6. Why should the `main` branch be protected?
