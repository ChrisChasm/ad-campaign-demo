# GitHub Setup Instructions

This guide provides step-by-step instructions for setting up your own private GitHub repository using the ad-campaign-demo template. This is a crucial step that allows you to have your own copy of the project that you can modify and deploy.

## What is GitHub?

GitHub is a web-based platform for version control and collaboration. For this project, GitHub is essential for:
- Storing your campaign files and code
- Tracking changes to your project
- Automatically deploying your landing pages to Netlify
- Collaborating with others (if needed)

## Prerequisites

Before starting, ensure you have:
- **Internet connection** for accessing GitHub
- **A GitHub account** (free accounts work perfectly)
- **A web browser** (Chrome, Firefox, Safari, or Edge)

## Step-by-Step Instructions

### Step 1: Create or Sign In to Your GitHub Account

1. **Navigate to GitHub**
   - Open your web browser
   - Go to [https://github.com](https://github.com)

2. **Sign in or create an account**
   - If you already have a GitHub account:
     - Click **"Sign in"** in the top right corner
     - Enter your username/email and password
   - If you don't have a GitHub account:
     - Click **"Sign up"** in the top right corner
     - Enter your email address, create a password, and choose a username
     - Complete the verification steps (email verification, CAPTCHA, etc.)
     - Select the free plan when prompted

### Step 2: Find the Template Repository

1. **Navigate to the template repository**
   - In your browser, go to: [https://github.com/ChrisChasm/ad-campaign-demo](https://github.com/ChrisChasm/ad-campaign-demo)
   - You can also search for "ad-campaign-demo" in GitHub's search bar
   - Make sure you're viewing the repository owned by "ChrisChasm"

2. **Verify you're on the correct page**
   - You should see the repository name: **"ad-campaign-demo"**
   - The page should show files like `README.md`, `prompt.md`, and folders like `website/`, `resources/`
   - Look for a green button that says **"Use this template"** or **"Use template"** near the top of the page

### Step 3: Use the Template to Create Your Own Repository

1. **Click the "Use this template" button**
   - Look for the green button labeled **"Use this template"** or **"Use template"**
   - This button is typically located:
     - Near the top right of the repository page, next to the "Code" button
     - Or in a dropdown menu next to the "Code" button
   - If you don't see the button, make sure you're logged into GitHub

2. **Select "Create a new repository"**
   - After clicking "Use this template", you'll see options
   - Click **"Create a new repository"** (this is usually the default option)

3. **Configure your new repository**
   - **Owner**: Select your GitHub username from the dropdown
   - **Repository name**: 
     - Enter a name for your repository (e.g., `my-ad-campaigns`, `zume-campaigns`, `ad-campaign-demo`)
     - Use lowercase letters, numbers, and hyphens (no spaces)
     - Example: `my-zume-campaigns`
   - **Description** (optional): 
     - Add a brief description like "Ad campaign generator for Zume Training"
   - **Visibility**: 
     - ✅ **Select "Private"** to keep your repository private
     - This ensures only you (and people you invite) can see your repository
     - Private repositories are free on GitHub
   - **Include all branches** (optional):
     - Leave this unchecked unless you need multiple branches
   - **Include all tags** (optional):
     - Leave this unchecked unless you need version tags

4. **Create the repository**
   - Click the green **"Create repository from template"** button
   - GitHub will create your new repository (this takes a few seconds)

### Step 4: Verify Your New Repository

1. **You'll be redirected to your new repository**
   - GitHub will automatically take you to your new repository page
   - The URL will look like: `https://github.com/YOUR_USERNAME/YOUR_REPO_NAME`

2. **Verify the repository contents**
   - You should see all the files from the template:
     - `README.md`
     - `prompt.md`
     - `website/` folder
     - `resources/` folder
     - Other project files
   - The repository should show as **"Private"** (you'll see a lock icon 🔒)

3. **Note your repository URL**
   - Copy or remember your repository URL
   - You'll need this for cloning the repository later
   - Example: `https://github.com/yourusername/my-ad-campaigns.git`

### Step 5: Clone Your Repository (Next Step)

After creating your repository, you'll need to clone it to your local computer. This is covered in the main README.md file, but here's a quick overview:

1. **Get your repository URL**
   - On your repository page, click the green **"Code"** button
   - Copy the HTTPS URL (it will look like: `https://github.com/yourusername/repo-name.git`)

2. **Clone using Cursor or Git**
   - You can use Cursor IDE to clone the repository
   - Or use Git commands in your terminal
   - See the main README.md for detailed cloning instructions

## Visual Guide

### Finding the Template Button

The "Use this template" button appears in different locations depending on GitHub's interface:

**Option 1: Direct button**
```
[Code ▼] [Use this template ▼]
```

**Option 2: Inside Code dropdown**
```
[Code ▼]
  ↓
  - Clone
  - Open with GitHub Desktop
  - Download ZIP
  - Use this template  ← Click here
```

### Repository Creation Form

When you click "Use this template", you'll see a form like this:

```
Create a new repository from ad-campaign-demo

Owner: [YourUsername ▼]
Repository name: [my-ad-campaigns        ]
Description: [Ad campaign generator for Zume Training]

○ Public
  Anyone on the internet can see this repository.

● Private
  You choose who can see and commit to this repository.

[ ] Include all branches
[ ] Include all tags

[Create repository from template]
```

## Troubleshooting

### Problem: Can't find the "Use this template" button

**Possible causes and solutions:**

1. **Not logged into GitHub**
   - **Solution**: Make sure you're signed into your GitHub account
   - Check the top right corner for your profile picture/avatar

2. **Wrong repository page**
   - **Solution**: Verify you're on the correct repository URL
   - Make sure it's: `https://github.com/ChrisChasm/ad-campaign-demo`
   - Check that the repository name matches exactly

3. **Repository is not a template**
   - **Solution**: If the button doesn't appear, the repository owner may need to enable template mode
   - Contact the repository owner or use the "Fork" button as an alternative (though template is preferred)

4. **Button is in a dropdown menu**
   - **Solution**: Click the "Code" button and look for "Use this template" in the dropdown menu

### Problem: Can't create a private repository

**Possible causes and solutions:**

1. **Account limitations**
   - **Solution**: Free GitHub accounts can create unlimited private repositories
   - Make sure you're using a free account (not an organization account with restrictions)

2. **Organization account**
   - **Solution**: If you're using an organization account, check the organization's settings
   - You may need to upgrade or change account settings

### Problem: Repository creation fails

**Possible causes and solutions:**

1. **Repository name already exists**
   - **Solution**: Choose a different repository name
   - GitHub requires unique repository names per account

2. **Invalid repository name**
   - **Solution**: Use only lowercase letters, numbers, and hyphens
   - No spaces or special characters allowed
   - Must start with a letter or number

3. **Network issues**
   - **Solution**: Check your internet connection
   - Try refreshing the page and creating the repository again

### Problem: Can't see repository after creation

**Possible causes and solutions:**

1. **Wrong account**
   - **Solution**: Make sure you're logged into the correct GitHub account
   - Check the owner field matches your username

2. **Repository is private**
   - **Solution**: This is normal! Private repositories are only visible to you
   - Look in your repositories list: `https://github.com/YOUR_USERNAME?tab=repositories`

## Next Steps

After successfully creating your repository:

1. **Clone the repository** to your local computer (see README.md Step 2)
2. **Set up Netlify** to deploy your landing pages (see README.md Step 3)
3. **Configure your campaign variables** in `prompt.md`
4. **Run the workflow** to generate your first campaign

## Additional Resources

- **GitHub Documentation**: [https://docs.github.com](https://docs.github.com)
- **Creating a repository from a template**: [GitHub Help](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
- **GitHub Private Repositories**: [GitHub Help](https://docs.github.com/en/get-started/learning-about-github/types-of-github-accounts)

## Summary

✅ **Completed Steps:**
1. Created/signed into GitHub account
2. Found the template repository
3. Clicked "Use this template" button
4. Created a private repository with a custom name
5. Verified repository was created successfully

🎉 **You're ready for the next step!** Now you can clone your repository and start working on your ad campaigns.

---

For the complete setup process, refer to the main [README.md](../README.md) file.

