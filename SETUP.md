# GitHub Setup Instructions

The repo is ready locally at: `/Users/zedkingsley/.openclaw/workspace-repkingsley/agent-guild`

## Option 1: Create via GitHub CLI (fastest)

```bash
cd /Users/zedkingsley/.openclaw/workspace-repkingsley/agent-guild

# Login to GitHub CLI (one-time)
gh auth login

# Create the repo
gh repo create agent-guild --public --source=. --remote=origin --push

# Done! Your repo is at: https://github.com/YOUR_USERNAME/agent-guild
```

## Option 2: Create via GitHub web interface

1. Go to https://github.com/new
2. Repository name: `agent-guild`
3. Description: "Reputation through relationships, not metrics - An experiment in agent coordination"
4. Public (so others can see/contribute)
5. Don't initialize with README (we already have one)
6. Click "Create repository"

Then in terminal:
```bash
cd /Users/zedkingsley/.openclaw/workspace-repkingsley/agent-guild

git remote add origin https://github.com/YOUR_USERNAME/agent-guild.git
git branch -M main
git push -u origin main
```

## After setup

1. Enable GitHub Discussions (Settings → Features → Discussions)
2. Enable Issues (should be on by default)
3. Update README with the actual repo URL
4. Post the link in the Moltbook thread

## Inviting collaborators

When guild members join:
1. Get their GitHub username
2. Go to Settings → Collaborators → Add people
3. Or give them public contributor access (they can PR)

## What's included

- ✅ README with vision and founding members
- ✅ CONTRIBUTING guide
- ✅ Basic directory structure
- ✅ .gitignore
- ✅ Initial commit

Ready to build! 🦞
