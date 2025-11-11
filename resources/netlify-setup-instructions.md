# Netlify Setup Instructions

This guide provides step-by-step instructions for setting up Netlify to automatically deploy your landing pages from your GitHub repository. Netlify will host your website and automatically update it whenever you push changes to GitHub.

## What is Netlify?

Netlify is a web hosting and deployment platform that makes it easy to deploy static websites. For this project, Netlify is essential for:
- Hosting your landing pages on the internet
- Automatically deploying updates when you push to GitHub
- Providing a public URL for your landing pages (e.g., `https://your-site.netlify.app`)
- Managing your website without manual file uploads

## Prerequisites

Before starting, ensure you have:
- **Internet connection** for accessing Netlify
- **A GitHub account** with your repository already created (see GitHub Setup Instructions)
- **Your GitHub repository** set up and ready (you should have completed the GitHub setup steps)
- **A web browser** (Chrome, Firefox, Safari, or Edge)

## Step-by-Step Instructions

### Step 1: Create or Sign In to Your Netlify Account

1. **Navigate to Netlify**
   - Open your web browser
   - Go to [https://www.netlify.com](https://www.netlify.com)

2. **Sign up or sign in**
   
   **Option A: Sign up with GitHub (Recommended)**
   - Click **"Sign up"** in the top right corner
   - Click **"Sign up with GitHub"** button
   - You'll be redirected to GitHub to authorize Netlify
   - Click **"Authorize Netlify"** to grant permissions
   - This automatically connects your GitHub account to Netlify (makes setup easier!)

   **Option B: Sign up with Email**
   - Click **"Sign up"** in the top right corner
   - Enter your email address
   - Create a password (at least 8 characters)
   - Click **"Sign up"**
   - Check your email for a verification link and click it
   - You'll need to connect GitHub later in the process

   **Option C: Sign in (if you already have an account)**
   - Click **"Log in"** in the top right corner
   - Enter your email and password, or click **"Log in with GitHub"** if you previously connected accounts

3. **Complete your profile (if prompted)**
   - You may be asked to provide your name or company name
   - This is optional and can be skipped or updated later

### Step 2: Access the Netlify Dashboard

1. **After signing in, you'll be taken to your Netlify dashboard**
   - The dashboard shows all your sites (initially empty if this is your first time)
   - You should see a button or link to **"Add new site"** or **"New site"**

2. **Verify you're logged in**
   - Look for your profile picture/avatar in the top right corner
   - You should see your account name or email

### Step 3: Create a New Site from GitHub

1. **Start the site creation process**
   - Click the **"Add new site"** button (usually a prominent button on the dashboard)
   - Or click **"Sites"** in the top navigation, then **"Add new site"**
   - Select **"Import an existing project"** from the options

2. **Choose GitHub as your Git provider**
   - You'll see options for different Git providers: GitHub, GitLab, Bitbucket
   - Click **"Deploy with GitHub"** or the GitHub logo/button
   - If you signed up with email, you'll need to authorize Netlify to access GitHub

3. **Authorize Netlify to access GitHub (if needed)**
   - If you haven't connected GitHub yet, you'll be redirected to GitHub
   - GitHub will ask you to authorize Netlify
   - You can choose to authorize:
     - **All repositories** (recommended for simplicity)
     - **Only select repositories** (more secure, but you'll need to select your repo)
   - Click **"Authorize Netlify"** or **"Install & Authorize"**
   - You'll be redirected back to Netlify

4. **Select your repository**
   - Netlify will show a list of your GitHub repositories
   - Search for your repository name (the one you created from the template)
   - Click on your repository name to select it
   - If you have many repositories, use the search box to filter

### Step 4: Configure Build Settings

This is a crucial step! You need to tell Netlify where your website files are located.

1. **Review the build settings page**
   - After selecting your repository, you'll see a configuration page
   - This page has several fields that need to be configured

2. **Set the Branch to Deploy**
   - **Branch**: Select **"main"** (or "master" if your repo uses that)
   - This tells Netlify which branch to deploy from

3. **Configure Build Command**
   - **Build command**: **Leave this EMPTY** or delete any default text
   - This project doesn't require a build step (it's just HTML files)
   - If there's any text in this field, clear it completely

4. **Configure Publish Directory (IMPORTANT!)**
   - **Publish directory**: Enter **`website`** (exactly as shown, lowercase, no quotes)
   - This tells Netlify to look in the `website` folder for your HTML files
   - **Do NOT** use `./website` or `/website` or `website/` - just `website`
   - This is critical! If this is wrong, your site won't deploy correctly

5. **Review Advanced Settings (Optional)**
   - Click **"Show advanced"** if you want to configure additional settings
   - For this project, you typically don't need to change anything here
   - You can leave these settings as default

6. **Deploy the site**
   - Click the **"Deploy site"** button (usually green, at the bottom of the page)
   - Netlify will start the deployment process

### Step 5: Monitor the Deployment

1. **Watch the deployment progress**
   - After clicking "Deploy site", you'll see a deployment log
   - Netlify will:
     - Clone your repository
     - Check for files in the `website` directory
     - Deploy those files to their CDN
   - This usually takes 30-60 seconds

2. **Check for deployment success**
   - Look for a green checkmark ✅ or "Published" message
   - If you see errors, see the Troubleshooting section below

3. **Get your site URL**
   - Once deployed, Netlify will generate a URL for your site
   - It will look like: `https://random-name-12345.netlify.app`
   - You can change this name later if desired
   - Click on the URL to open your site in a new tab

### Step 6: Verify Your Site is Working

1. **Visit your site URL**
   - Click the site URL provided by Netlify
   - Or copy the URL and paste it into your browser
   - You should see your landing page (initially, it will show the default `index.html`)

2. **Check the site settings**
   - Go back to your Netlify dashboard
   - Click on your site name to view site details
   - Verify the settings show:
     - **Publish directory**: `website`
     - **Build command**: (empty)
     - **Branch**: `main` (or `master`)

3. **Test automatic deployments**
   - Make a small change to a file in your `website` folder
   - Commit and push the change to GitHub
   - Watch your Netlify dashboard - you should see a new deployment start automatically
   - This confirms that Netlify is connected and watching your repository

### Step 7: Customize Your Site Name (Optional)

1. **Change the site name**
   - In your site's settings, click **"Site settings"** or **"Change site name"**
   - Enter a custom name (e.g., `my-zume-campaigns`)
   - Click **"Save"**
   - Your new URL will be: `https://your-custom-name.netlify.app`
   - Note: Site names must be unique across all Netlify sites

2. **Set up a custom domain (Optional - Advanced)**
   - If you have your own domain, you can configure it in Netlify
   - Go to **"Domain settings"** → **"Add custom domain"**
   - Follow Netlify's instructions for DNS configuration
   - This is optional and not required for basic setup

## Visual Guide

### Netlify Dashboard Overview

```
┌─────────────────────────────────────────┐
│  Netlify                    [Profile]   │
├─────────────────────────────────────────┤
│                                         │
│  Welcome to Netlify!                    │
│                                         │
│  [Add new site]  ← Click here          │
│                                         │
└─────────────────────────────────────────┘
```

### Site Creation Flow

**Step 1: Add new site**
```
[Add new site] → [Import an existing project]
```

**Step 2: Choose Git provider**
```
[Deploy with GitHub]  [Deploy with GitLab]  [Deploy with Bitbucket]
         ↑
    Click here
```

**Step 3: Select repository**
```
Search repositories: [your-repo-name        ]
─────────────────────────────────────────────
✓ your-repo-name
  your-other-repo
  another-repo
```

**Step 4: Configure settings**
```
Branch to deploy:        [main ▼]

Build command:           [                    ]  ← Leave empty

Publish directory:       [website            ]  ← Enter "website"

[Show advanced]  [Deploy site]  ← Click Deploy site
```

### Deployment Success Screen

```
┌─────────────────────────────────────────┐
│  Site deployed successfully! ✅         │
│                                         │
│  Your site is live at:                  │
│  https://your-site-name.netlify.app     │
│                                         │
│  [Open site]  [Site settings]          │
└─────────────────────────────────────────┘
```

## Troubleshooting

### Problem: Can't sign in to Netlify

**Possible causes and solutions:**

1. **Wrong email/password**
   - **Solution**: Use the "Forgot password" link to reset your password
   - Check that you're using the correct email address

2. **Account doesn't exist**
   - **Solution**: Make sure you've completed the sign-up process
   - Check your email for a verification link if you signed up with email

3. **GitHub authorization issues**
   - **Solution**: Try signing in with email instead, then connect GitHub later
   - Or revoke Netlify's access in GitHub settings and try again

### Problem: Can't find "Deploy with GitHub" option

**Possible causes and solutions:**

1. **GitHub not connected**
   - **Solution**: 
     - Go to your Netlify account settings
     - Look for "Connected accounts" or "Git providers"
     - Click "Connect to GitHub" and authorize access

2. **Using wrong Git provider**
   - **Solution**: Make sure you're clicking "Deploy with GitHub" not GitLab or Bitbucket
   - The button should have the GitHub logo/icon

### Problem: Repository not showing in the list

**Possible causes and solutions:**

1. **Repository is private and not authorized**
   - **Solution**: 
     - When authorizing Netlify on GitHub, make sure you selected "All repositories" or specifically selected your repository
     - Go to GitHub → Settings → Applications → Authorized OAuth Apps → Netlify
     - Click "Configure" and ensure your repository is selected

2. **Wrong GitHub account**
   - **Solution**: Make sure you're logged into the correct GitHub account
   - Check that the repository exists and you have access to it

3. **Repository name search**
   - **Solution**: Use the search box to filter repositories
   - Type part of your repository name to find it quickly

### Problem: Site not deploying / Build failed

**Possible causes and solutions:**

1. **Wrong publish directory**
   - **Solution**: 
     - Go to Site settings → Build & deploy → Build settings
     - Verify "Publish directory" is set to `website` (not `./website` or `/website`)
     - Click "Save" and trigger a new deployment

2. **Build command has content**
   - **Solution**: 
     - Go to Site settings → Build & deploy → Build settings
     - Clear the "Build command" field completely
     - Leave it empty
     - Click "Save"

3. **No files in website directory**
   - **Solution**: 
     - Make sure you have files in your `website` folder
     - At minimum, you should have `index.html`
     - Commit and push files to GitHub, then redeploy

4. **Wrong branch selected**
   - **Solution**: 
     - Go to Site settings → Build & deploy → Continuous Deployment
     - Verify the branch is set to `main` (or `master` if that's what your repo uses)
     - Make sure your files are committed to that branch

### Problem: Site deploys but shows "Page not found" or blank page

**Possible causes and solutions:**

1. **Publish directory incorrect**
   - **Solution**: 
     - Double-check that "Publish directory" is exactly `website` (lowercase, no quotes)
     - The folder name in your repository must match exactly

2. **Files in wrong location**
   - **Solution**: 
     - Verify your HTML files are in the `website` folder (not `website/[LANGUAGE_CODE]/` for the initial setup)
     - Check your repository structure on GitHub

3. **Index file missing**
   - **Solution**: 
     - Make sure there's an `index.html` file in your `website` folder
     - This is the default file Netlify looks for

### Problem: Changes not deploying automatically

**Possible causes and solutions:**

1. **Not pushing to correct branch**
   - **Solution**: 
     - Make sure you're pushing to the `main` branch (or `master`)
     - Check Netlify settings to see which branch is configured

2. **Netlify not watching repository**
   - **Solution**: 
     - Go to Site settings → Build & deploy → Continuous Deployment
     - Verify the repository is connected
     - Check that "Deploy notifications" are enabled

3. **Files not committed**
   - **Solution**: 
     - Make sure you're committing and pushing files to GitHub
     - Netlify only deploys when changes are pushed to GitHub

### Problem: Can't change site name

**Possible causes and solutions:**

1. **Name already taken**
   - **Solution**: Choose a different, more unique name
   - Site names must be unique across all Netlify sites globally

2. **Invalid characters**
   - **Solution**: Use only lowercase letters, numbers, and hyphens
   - No spaces or special characters allowed

## Verifying Your Setup

After completing the Netlify setup, verify everything is working:

1. ✅ **Site is accessible**
   - Visit your Netlify URL in a browser
   - You should see your landing page

2. ✅ **Settings are correct**
   - Publish directory: `website`
   - Build command: (empty)
   - Branch: `main` or `master`

3. ✅ **Automatic deployments work**
   - Make a small change to a file
   - Commit and push to GitHub
   - Check Netlify dashboard for new deployment

4. ✅ **Repository is connected**
   - Go to Site settings → Build & deploy
   - Verify your GitHub repository is listed

## Next Steps

After successfully setting up Netlify:

1. **Test your deployment**
   - Make changes to files in your `website` folder
   - Commit and push to GitHub
   - Watch Netlify automatically deploy the changes

2. **Generate your first campaign**
   - Follow the workflow instructions in README.md
   - Generate landing pages using the prompts
   - Files will be created in `website/[LANGUAGE_CODE]/`
   - Push to GitHub and Netlify will deploy them automatically

3. **Access your landing pages**
   - Your landing pages will be accessible at:
   - `https://your-site.netlify.app/[LANGUAGE_CODE]/[AD_GROUP_NAME].html`
   - Example: `https://your-site.netlify.app/es/matt2818.html`

4. **Monitor deployments**
   - Check your Netlify dashboard regularly
   - Review deployment logs if something goes wrong
   - Each deployment shows what changed

## Additional Resources

- **Netlify Documentation**: [https://docs.netlify.com](https://docs.netlify.com)
- **Netlify Getting Started Guide**: [Netlify Docs](https://docs.netlify.com/get-started/)
- **GitHub Integration**: [Netlify GitHub Docs](https://docs.netlify.com/integrations/github/)
- **Netlify Support**: [https://www.netlify.com/support](https://www.netlify.com/support)

## Summary

✅ **Completed Steps:**
1. Created/signed into Netlify account
2. Connected GitHub account to Netlify
3. Created a new site from your GitHub repository
4. Configured build settings (empty build command)
5. Set publish directory to `website`
6. Successfully deployed your site
7. Verified the site is accessible

🎉 **Your site is now live!** Every time you push changes to GitHub, Netlify will automatically deploy them.

---

For the complete setup process, refer to the main [README.md](../README.md) file.
For GitHub setup instructions, see [github-setup-instructions.md](github-setup-instructions.md).

