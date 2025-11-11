# Setup Instructions for Ad Campaign Demo

This guide will help you set up the development environment and infrastructure needed to create verse-based Google Ads campaigns and landing pages for Zume Training.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Step 1: Cursor Setup](#step-1-cursor-setup)
- [Step 2: GitHub Setup](#step-2-github-setup)
- [Step 3: Netlify Setup](#step-3-netlify-setup)
- [Step 4: Verify Git Requirement](#step-4-verify-git-requirement)
- [Step 5: Configure Campaign Variables](#step-5-configure-campaign-variables)
- [Step 6: Run the Workflow](#step-6-run-the-workflow)
- [Verification](#verification)
- [Troubleshooting](#troubleshooting)
- [Next Steps](#next-steps)

## Prerequisites

Before starting, ensure you have:

- **Internet connection** for accessing online services
- Google Account (recommended)

## Step 1: Cursor Setup

1. **Download and install Cursor IDE**
   - Go to [Cursor.com](https://cursor.com)
   - Download Cursor for your operating system (Mac/Windows/Linux)
   - Install the application following the on-screen instructions

2. **Open the project in Cursor**
   - Launch Cursor IDE
   - Click **File** → **Open Folder**
   - Navigate to and select your project folder
   - The project will open in Cursor

## Step 2: GitHub Setup

1. **Create or sign in to your GitHub account**
   - Go to [GitHub.com](https://github.com) and create a free account if needed

2. **Use the project template**
   - Navigate to the project repository: [https://github.com/ChrisChasm/ad-campaign-demo](https://github.com/ChrisChasm/ad-campaign-demo)
   - Click the **"Use this template"** button (green button near the top)
   - Give your new repository a name (e.g., `my-ad-campaigns`)
   - Choose whether to make it public or private
   - Click **"Create repository from template"**

3. **Clone the repository using Cursor**
   - On your new repository page, click the green **"Code"** button
   - Copy the repository URL
   - In Cursor IDE, open the chat interface (usually `Cmd+L` on Mac or `Ctrl+L` on Windows/Linux)
   - Ask Cursor: "Help me clone this GitHub repository: [YOUR_REPOSITORY_URL]"
   - Cursor will guide you through cloning the repository and opening it in Cursor

## Step 3: Netlify Setup

1. **Create or sign in to your Netlify account**
   - Go to [Netlify.com](https://www.netlify.com) and sign up for a free account
   - You can sign up with your GitHub account for easier integration

2. **Create a new site**
   - From your Netlify dashboard, click **"Add new site"** → **"Import an existing project"**
   - Choose **"Deploy with GitHub"** and authorize Netlify to access your GitHub account if prompted
   - Select the repository you created in Step 2

3. **Configure build settings**
   - **Build command**: Leave this empty (no build step needed)
   - **Publish directory**: Set to `website`
   - Click **"Deploy site"**

4. **Verify deployment**
   - Netlify will automatically deploy your site
   - You'll receive a URL like `https://your-site-name.netlify.app`
   - The site will automatically update whenever you push changes to your GitHub repository

## Step 4: Verify Git Requirement

If you don't have Git installed on your system, use Cursor's AI Assistant to help:

1. **Open Cursor IDE** (if not already open)
   - In the upper right of the screen, select the Agent icon
   - Make sure your project folder is open in Cursor

2. **Use Cursor's AI assistant to guide Git installation**
   - Open the Cursor chat interface (usually `Cmd+L` on Mac or `Ctrl+L` on Windows/Linux)
   - Ask Cursor: "Help me install Git on my system"
   - Cursor will provide step-by-step instructions based on your operating system

3. **Verify Git installation with Cursor**
   - After installation, ask Cursor: "Help me verify Git is installed and configured"
   - Cursor will guide you through verification and configuration steps
   - Cursor can also help configure your Git user name and email if needed

> **Note**: If you already have Git installed, you can skip this step. Git is required for cloning repositories and pushing changes to GitHub. Cursor can help verify and configure Git settings if needed.

## Step 5: Configure Campaign Variables

Before running the workflow, you need to configure your campaign variables. These are defined in `prompt.md` at the top of the file.

1. **Open `prompt.md` in your editor**

2. **Update the Initial Setup variables** (found at the top of the file):
   ```markdown
   - [SCRIPTURE] = Matthew 28:18-20
   - [CAMPAIGN_PREFIX] = matt2818
   - [LANGUAGE_CODE] = es
   - [LANGUAGE] = Spanish
   - [CAMPAIGN_NAME] = Verses-[LANGUAGE]
   - [BASE_URL] = https://pages.zume.training/verse
   - [PUBLIC_URL] = https://zume.training/[LANGUAGE_CODE]
   - [CTA_URL] = [PUBLIC_URL]/form.html
   ```

3. **Customize for your campaign**:
   - **`[SCRIPTURE]`**: The Bible verse reference you're creating a campaign for (e.g., `Timothy 2:2`, `Acts 2:41-47`)
   - **`[CAMPAIGN_PREFIX]`**: A short identifier for files/URLs (e.g., `tim22`, `acts-2-41-47`)
   - **`[LANGUAGE_CODE]`**: ISO 639-1 language code (e.g., `en` for English, `hr` for Croatian, `es` for Spanish)
   - **`[LANGUAGE]`**: Full language name (e.g., `English`, `Croatian`, `Spanish`)
   - **`[CAMPAIGN_NAME]`**: Your Google Ads campaign name (e.g., `Verses-English`, `Verses-Spanish`)
   - **`[BASE_URL]`**: Base URL for landing pages (typically `https://pages.zume.training/verse`)
   - **`[PUBLIC_URL]`**: Public site URL (e.g., `https://zume.training/en`)
   - **`[CTA_URL]`**: Call-to-action URL (e.g., `https://zume.training/en/form.html`)

4. **Save the file** after making your changes

> **Note**: For detailed information about all available variables, see the [Configuration section in README.md](README.md#configuration).

## Step 6: Run the Workflow

Once your variables are configured, you can run the complete workflow:

1. **In Cursor IDE or with Cursor Agent**, open a new chat or command interface

2. **Run the workflow prompt**:
   ```
   Run the following prompt step by step. @prompt.md
   ```

3. **The AI will execute the workflow**:
   - Step 1: Initial Setup (Prompts 1.1 - 1.6)
   - Step 2: Keyword Generation (Prompts 2.1 - 2.2)
   - Step 3: Headline Generation (Prompts 3.1 - 3.2)
   - Step 4: Description Generation (Prompts 4.1 - 4.2)
   - Step 5: Create Ads CSV (Prompt 5.1)
   - Step 6: Landing Page Development (Prompts 6.1 - 6.3)
   - Step 7: Quality Assurance (Prompts 7.1 - 7.2)

4. **Monitor the process**: The AI will create files in the following directories as it works:
   - `keywords/[LANGUAGE_CODE]/` - Keyword text files
   - `ad-groups/[LANGUAGE_CODE]/` - Ad group CSV files
   - `ads/[LANGUAGE_CODE]/` - Ad CSV files
   - `website/[LANGUAGE_CODE]/` - Landing page HTML files

## Verification

After completing the setup and running the workflow, verify everything is working:

1. **Check generated files**:
   Use your Finder or Explorer window to verify folders and assets were created

2. **Verify Netlify deployment**:
   - Tell Cursor-Agent to `save and push files to github`
   - Check your Netlify dashboard for successful deployments
   - Visit your Netlify URL to see if landing pages are accessible
   - Files should appear in the `website/[LANGUAGE_CODE]/` directory

3. **Review generated content**:
   - Open CSV files in `ads/[LANGUAGE_CODE]/` to verify ad content
   - Open HTML files in `website/[LANGUAGE_CODE]/` to preview landing pages
   - Check that all placeholders have been replaced with actual content

## Troubleshooting

### GitHub Issues

**Problem**: Can't find the "Use this template" button
- **Solution**: Make sure you're logged into GitHub and viewing the correct repository

**Problem**: Git clone fails
- **Solution**: Ask Cursor to help verify Git installation and troubleshoot the clone issue. Check your internet connection.

### Netlify Issues

**Problem**: Site not deploying
- **Solution**: 
  - Verify the publish directory is set to `website` (not `./website`)
  - Check that your GitHub repository is properly connected
  - Review the Netlify deployment logs for specific errors

**Problem**: Landing pages not showing up
- **Solution**: 
  - Ensure files are in `website/[LANGUAGE_CODE]/` directory
  - Check that files are committed and pushed to GitHub
  - Verify the file names match the expected format: `[AD_GROUP_NAME].html`

### Cursor Issues

**Problem**: Cursor IDE not working properly
- **Solution**: 
  - Make sure you have the latest version of Cursor IDE installed from [Cursor.com](https://cursor.com)
  - Restart Cursor IDE if needed
  - Check Cursor's documentation or ask Cursor's AI assistant for help

**Problem**: Cursor Agent permission denied
- **Solution**: 
  - On Mac: Go to System Preferences → Security & Privacy → Allow Cursor
  - On Windows: Check Windows security settings
  - Ask Cursor's AI assistant for help with permission issues

### Workflow Issues

**Problem**: Variables not being recognized
- **Solution**: 
  - Verify variables are set correctly in `prompt.md` at the top of the file
  - Check that variable names use square brackets: `[VARIABLE_NAME]`
  - Ensure no typos in variable names

**Problem**: Files not being created in correct directories
- **Solution**: 
  - Verify `[LANGUAGE_CODE]` is set correctly
  - Check that directory paths match the variables in Prompt 1.1
  - Ensure the AI has file creation permissions

## Next Steps

After completing the setup and running your first campaign:

1. **Review the generated content**:
   - Check ad copy in `ads/[LANGUAGE_CODE]/[AD_GROUP_NAME]_ad.csv`
   - Preview landing pages in `website/[LANGUAGE_CODE]/[AD_GROUP_NAME].html`
   - Review keyword lists in `keywords/[LANGUAGE_CODE]/[AD_GROUP_NAME]_keywords.txt`

2. **Upload to Google Ads**:
   - Import the ad group CSV from `ad-groups/[LANGUAGE_CODE]/`
   - Import the ads CSV from `ads/[LANGUAGE_CODE]/`
   - Upload keywords from `keywords/[LANGUAGE_CODE]/`

3. **Deploy landing pages**:
   - Landing pages are automatically deployed via Netlify when pushed to GitHub
   - Or manually upload HTML files to your web server

4. **Create additional campaigns**:
   - Update variables in `prompt.md` for new campaigns
   - Run the workflow again with different scripture references or languages

5. **Learn more**:
   - Read [README.md](README.md) for detailed workflow documentation
   - Review [prompt.md](prompt.md) for complete prompt templates
   - Check Google Ads documentation for campaign management best practices

## Additional Resources

- **GitHub**: [https://github.com](https://github.com)
- **Netlify**: [https://www.netlify.com](https://www.netlify.com)
- **Cursor**: [https://cursor.com](https://cursor.com)
- **Google Ads**: [https://ads.google.com](https://ads.google.com)

---

For detailed workflow instructions and prompt templates, see [prompt.md](prompt.md).  
For project overview and configuration details, see [README.md](README.md).
