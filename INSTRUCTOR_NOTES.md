# Instructor Notes - Git Installation Assignment

## Assignment Overview

This repository serves as a starter template for a GitHub Classroom assignment focused on Git installation and verification. Students will install Git on their local machines and submit proof of installation.

---

## What Students Will Learn

1. How to download and install Git on their operating system
2. How to use Git Bash (Windows) or Terminal (macOS/Linux)
3. Basic command-line operations
4. How to verify software installation
5. How to take screenshots and submit work via Git

---

## Assignment Files

- **README.md** - Main instructions for students with detailed installation steps for all major operating systems
- **SUBMISSION.md** - Template file for students to fill out with their submission details
- **screenshots/** - Folder where students upload their screenshots

---

## Grading Guidelines

### Full Credit (100%)
- Git is successfully installed (verified by screenshot)
- Screenshot clearly shows Git Bash/Terminal with `whoami` command executed
- Screenshot is properly named and placed in correct folder
- SUBMISSION.md is completely filled out with accurate information
- All files are committed and pushed correctly

### Partial Credit (70-90%)
- Git is installed but screenshot quality is poor
- Missing some information in SUBMISSION.md
- File naming convention not followed
- Minor issues with commit messages

### Low Credit (50-69%)
- Installation appears incomplete or incorrect
- Screenshot doesn't show required command
- Multiple required fields missing from SUBMISSION.md

### No Credit (0%)
- No submission
- Screenshot is not of Git Bash/Terminal
- Clear evidence installation was not completed

---

## Common Student Issues

### Issue 1: Git command not found
**Solution:** Ensure students restart their computer after installation (especially on Windows)

### Issue 2: Using wrong terminal
**Solution:** Windows students must use Git Bash, not Command Prompt or PowerShell for the `whoami` command

### Issue 3: Screenshot doesn't show command
**Solution:** Screenshot must show both the command typed and the output

### Issue 4: Can't push to repository
**Solution:** Ensure students have properly cloned the repository and have the correct permissions

---

## GitHub Classroom Setup

1. **Create Assignment**
   - Use this repository as the starter code
   - Set deadline according to your schedule
   - Enable "Grant students admin access to their repository"

2. **Recommended Settings**
   - Individual assignment (not group)
   - Enable feedback pull request
   - Set max number of commits: Unlimited

3. **Auto-grading (Optional)**
   - You can set up auto-grading to check if:
     - Files exist (SUBMISSION.md, screenshot in screenshots folder)
     - SUBMISSION.md contains filled information (not just template)

---

## Reviewing Submissions

### Quick Review Checklist
For each student repository:

1. Check that screenshot exists in `screenshots/` folder
2. Open the screenshot - verify it shows:
   - Git Bash or Terminal window
   - The `whoami` command typed
   - The output (username)
3. Check SUBMISSION.md is filled out
4. Verify Git version is reasonable (2.x or higher)

### Batch Review Script

You can use this script to quickly check all repositories:

```bash
#!/bin/bash
# Save as check_submissions.sh

# List all screenshot files
echo "=== Screenshots Found ==="
find . -path "*/screenshots/*" -type f ! -name ".gitkeep"

# Check if SUBMISSION.md is modified
echo -e "\n=== SUBMISSION.md Status ==="
for repo in */; do
    if [ -f "$repo/SUBMISSION.md" ]; then
        if grep -q "\[Your Full Name\]" "$repo/SUBMISSION.md"; then
            echo "$repo: ❌ Not filled out"
        else
            echo "$repo: ✅ Filled out"
        fi
    fi
done
```

---

## Extending the Assignment

This assignment can be extended with:

1. **Part 2: Git Configuration**
   - Setting up user.name and user.email
   - Configuring default editor

2. **Part 3: First Repository**
   - Creating a local repository with `git init`
   - Making first commit

3. **Part 4: GitHub Connection**
   - Setting up SSH keys
   - Cloning a repository

---

## FAQ for Instructors

**Q: What if a student uses a different OS than expected?**
A: The instructions cover Windows, macOS, and Linux. Any standard OS should work.

**Q: What version of Git should students install?**
A: Any Git 2.x version is acceptable. As of 2024, 2.40+ is recommended.

**Q: Can students use GitHub Desktop instead?**
A: For this assignment, students should install command-line Git. GitHub Desktop can be introduced later.

**Q: What if a student already has Git installed?**
A: They should verify their installation using the same steps and submit the screenshot.

---

## Support Resources

Share these with students who need extra help:
- [Official Git Documentation](https://git-scm.com/doc)
- [Git Tutorial by GitHub](https://docs.github.com/en/get-started/quickstart/set-up-git)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)

---

## Feedback Welcome

If you have suggestions for improving this assignment template, please feel free to modify it for your needs or contribute back to the original repository.

**Good luck with your class! 📚**
