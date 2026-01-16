# Quick Setup Guide

## Prerequisites

Before starting the assessment, ensure you have:

- [ ] **VS Code** installed on your machine
- [ ] **Git** installed and configured
- [ ] **Node.js** (v20 or higher) and npm installed
- [ ] **GitLab account** with access to fork repositories
- [ ] **Basic Solidity knowledge**

---

## Step 1: Fork the Repository

1. Click the **Fork** button in the top right 
2. Select your namespace to fork the project

---

## Step 2: Clone to Your Local Machine

```bash
# Clone your forked repository
git clone https://gitlab.wethinkco.de/YOUR_USERNAME/blockchain_dev_entry_test.git

# Navigate into the directory
cd blockchain_dev_entry_test
```

---

## Step 3: Open in VS Code

```bash
# Open VS Code in the current directory
code .
```

---

## Step 4: Install Solidity Extension (Optional but Recommended)

1. Open VS Code Extensions (Ctrl+Shift+X)
2. Search for "Solidity" by Juan Blanco
3. Click **Install**

---

## Step 5: Initialise Hardhat (Optional)

If you want to compile and test your contracts locally:

```bash
# Install Hardhat
npm install --save-dev hardhat @nomicfoundation/hardhat-toolbox

# Initialise Hardhat project
npx hardhat

# Select: Create a basic sample project
# Accept defaults
```

---

## Step 6: Verify Git Configuration

```bash
# Check your Git identity
git config user.name
git config user.email

# If not set, configure them
git config user.name "Your Name"
git config user.email "your.email@example.com"
```

---

## Step 7: Test Push Access

```bash
# Create a test commit
git commit --allow-empty -m "Test: Verify push access"

# Push to verify access
git push origin main

# If successful, you're ready!
```

---

## During the Assessment

### Commit Regularly (Every 15 Minutes)

```bash
git add .
git commit -m "Progress: [describe what you did]"
git push origin main
```

### File Structure You'll Work With

```
blockchain_dev_entry_test/
├── README.md                     # This file
├── PartA_MCQ_Answers.md          # Fill in your MCQ answers here
├── PartB_Design.md               # Document your design decisions
├── PartB_Tests.md                # Describe your test scenarios
├── contracts/
│   ├── SkillsMarketplace.sol     # VERSION 1 (choose one)
│   └── SecureLottery.sol         # VERSION 2 (choose one)
└── test/
│   ├── YourContractName.test.js  # Create this file for test implementation
└── docs/
    ├── GIT-WORKFLOW.md           # Git help
    └── SOLIDITY-PATTERNS.md      # Security patterns
```

**Test Implementation Requirements**:
1. Create a `test` directory if it doesn't exist
2. Name your test file as `YourContractName.test.js` (e.g. `SkillsMarketplace.test.js`)
3. Use Hardhat's testing framework (already set up if you initialized Hardhat)
4. Your tests should:
   - Be written in JavaScript/TypeScript
   - Cover all scenarios described in PartB_Tests.md
   - Be executable with `npx hardhat test`

---

## Troubleshooting

### Can't Push to GitLab

```bash
# Make sure you're on the right branch
git branch

# Make sure you forked (not cloned the original)
git remote -v

# Should show YOUR_USERNAME, not performanceteam
```

### VS Code Not Opening

```bash
# Try full path
"C:\Program Files\Microsoft VS Code\Code.exe" .

# Or add VS Code to PATH and restart terminal
```

### Solidity Syntax Not Highlighting

- Install Solidity extension from VS Code Marketplace
- Restart VS Code
- Check file extension is `.sol`

---

## Quick Reference

| Command | Purpose |
|---------|--------|
| `git status` | Check what files changed |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Save changes locally |
| `git push origin main` | Upload to GitLab |
| `git log --oneline` | View commit history |

---

## Need Help During Assessment?

- Refer to `docs/GIT-WORKFLOW.md` for Git commands
- Check `docs/SOLIDITY-PATTERNS.md` for security patterns
- Review `docs/RESOURCES.md` for learning materials

---

**All the best!**