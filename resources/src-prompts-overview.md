# Source Prompts Overview: Complete Workflow Guide

This document provides a comprehensive explanation of the source prompts folder structure and the complete logic flow of the prompt series used to generate Google Ads campaigns and landing pages for Zume Training's verse-based advertising system.

## What is the Source Prompts Folder?

The `resources/src-prompts/` folder contains the individual prompt files that make up the complete automated workflow for creating Google Ads campaigns. These prompts are designed to be executed sequentially by an AI assistant (like Cursor Agent) to transform a Bible verse reference into a fully functional advertising campaign with:

- **Google Ads keywords** - Search terms people might use
- **Ad group configuration** - Campaign structure files
- **Ad copy** - Headlines and descriptions for Google Ads
- **Landing pages** - HTML pages optimized for conversions

Each prompt file is a self-contained instruction set that builds upon the outputs of previous prompts, creating a cascading workflow where each step produces data needed for subsequent steps.

---

## Workflow Overview: The Seven-Step Process

The workflow is organized into **7 main steps**, each containing one or more prompts that work together to accomplish specific tasks:

1. **Initial Setup** (Prompts 1.1 - 1.7) - Configuration and context loading
2. **Keyword Generation** (Prompts 2.1 - 2.2) - Search term research and file creation
3. **Headline Generation** (Prompts 3.1 - 3.2) - Ad headline creation and quality control
4. **Description Generation** (Prompts 4.1 - 4.2) - Ad description creation and quality control
5. **Create Ads CSV** (Prompt 5.1) - Compile ad assets into Google Ads format
6. **Landing Page Development** (Prompts 6.1 - 6.3) - Content cross-referencing and page generation
7. **Quality Assurance** (Prompts 7.1 - 7.2) - Translation review and final improvements

---

## Step-by-Step Prompt Breakdown

### Step 1: Initial Setup (Prompts 1.1 - 1.7)

The initial setup phase establishes the foundation for the entire campaign by loading configuration variables, creating directory structures, and loading essential context about Zume Training's brand, concepts, and Google's advertising policies.

#### Prompt 1.1: Variable Setup

**Purpose**: Establishes the core file path variables and derived campaign variables needed throughout the workflow.

**What it does**:
- Defines directory paths for all output files (`HTML_PATH`, `ADS_PATH`, `AD_GROUP_PATH`, `KEYWORDS_PATH`, `PROMPTS_PATH`)
- Creates the `[AD_GROUP_NAME]` variable by combining `[CAMPAIGN_PREFIX]` and `[LANGUAGE_CODE]` (e.g., `matt2818-es`)
- Generates the `[TARGET_URL]` variable that points to where the landing page will be hosted
- Sets up the language variable format for display purposes

**Why it's important**: All subsequent prompts reference these variables, so establishing them first ensures consistent file naming and path structures across the entire workflow. Without this prompt, files would be created in wrong locations or with incorrect names.

**Output**: Variables stored in context for use by all subsequent prompts.

---

#### Prompt 1.2: Create Ad Group CSV

**Purpose**: Creates the foundational Google Ads ad group configuration file that will contain the campaign structure.

**What it does**:
- Creates the directory structure `[AD_GROUP_PATH]/[LANGUAGE_CODE]` if it doesn't exist
- Generates a CSV file named `[AD_GROUP_NAME]_new_ad_group.csv` with the proper Google Ads format
- Populates the CSV with default template values including:
  - Row type (Ad group)
  - Action (Add)
  - Ad group status (Enabled)
  - Campaign name (from variables)
  - Ad group name (from variables)
  - Ad group type (Standard)
  - Ad rotation settings (Optimize)
  - Various bidding and tracking fields (left empty for manual configuration)

**Why it's important**: Google Ads requires a specific CSV format for bulk uploads. This prompt creates the properly formatted file structure that can be directly imported into Google Ads, saving hours of manual data entry. The file serves as the container that will hold all the ad variations.

**Output**: A CSV file at `[AD_GROUP_PATH]/[LANGUAGE_CODE]/[AD_GROUP_NAME]_new_ad_group.csv` ready for Google Ads import.

---

#### Prompt 1.3: Load Zume Tone and Voice

**Purpose**: Loads Zume Training's brand voice and tone guidelines into the context so all generated content matches the organization's communication style.

**What it does**:
- Loads comprehensive brand voice documentation that defines Zume's communication style as:
  - **Knowledgeable**: Demonstrates expertise without being overly academic
  - **Motivational**: Encourages action and growth
  - **Approachable**: Friendly and accessible, not intimidating
  - **Action-oriented**: Focuses on practical application
- Provides examples of what the tone IS and IS NOT
- Establishes that the tone should build trust and position Zume as a valuable partner

**Why it's important**: Brand consistency is crucial for effective marketing. This prompt ensures that all ad copy, headlines, descriptions, and landing page content maintain a consistent voice that reflects Zume Training's values and approach. Without this, generated content might sound generic or inconsistent with the brand.

**Output**: Brand voice guidelines stored as `[ZUME_TONE_AND_VOICE]` variable for reference in content generation prompts.

---

#### Prompt 1.4: Load Zume Concepts

**Purpose**: Loads comprehensive information about Zume Training's 33 core concepts and training topics into context.

**What it does**:
- Loads a complete list of all 33 Zume Training concepts (from "God Uses Ordinary People" to "3-Circles Gospel Presentation")
- Provides detailed descriptions for each concept explaining:
  - What the concept teaches
  - Why it's important for disciple-making
  - How it's applied practically
  - How it fits into the overall training program
- Creates a knowledge base that connects biblical concepts to practical training applications

**Why it's important**: This prompt enables the AI to make intelligent connections between the Bible verse being advertised and Zume Training's actual curriculum. When generating landing page content (in Step 6), the AI can identify which Zume concepts naturally relate to the verse, creating more relevant and compelling landing pages that accurately represent what users will learn.

**Output**: Complete Zume Training curriculum information stored as `[ZUME_CONCEPTS]` variable for cross-referencing in later prompts.

---

#### Prompt 1.5: Load Google Policies

**Purpose**: Loads Google Ads policies specifically tailored for Christian discipleship training to ensure all generated content complies with Google's advertising guidelines.

**What it does**:
- Loads a comprehensive guide explaining Google's policy on religious advertising
- Clarifies the critical distinction: **ads can contain religious terms, but cannot target users based on religious identity**
- Provides DO's and DON'Ts with specific examples:
  - **DO**: Focus on user intent, needs, and program benefits
  - **DO**: Use terms like "faith-based" and "biblical" to describe the program
  - **DON'T**: Target users based on their religious identity
  - **DON'T**: Use phrases like "For Christians" or "As a Christian"
- Includes compliant and non-compliant headline and description examples

**Why it's important**: Google Ads has strict policies about personalized advertising and religious targeting. Violating these policies can result in ad rejection or account suspension. This prompt ensures all generated ad copy complies with Google's requirements while still effectively communicating the value of Zume Training. It's particularly crucial because religious content requires careful handling to avoid policy violations.

**Output**: Google Ads policy guidelines stored as `[GOOGLE_POLICIES]` variable for compliance checking in content generation.

---

#### Prompt 1.6: Load Effective Writing Guide

**Purpose**: Loads best practices for writing effective Google Search Ads, including structure, keyword usage, emotional triggers, and calls-to-action.

**What it does**:
- Loads comprehensive guidelines covering:
  - **Ad Structure & Limits**: Headlines (max 30 chars), Descriptions (max 90 chars), variety requirements
  - **Keyword Relevance**: How to naturally incorporate keywords
  - **Tone for Faith-Based Audience**: Warm, positive, inclusive language
  - **Emotional Triggers**: Words like hope, purpose, belonging, growth
  - **Calls to Action**: Examples of effective CTAs
  - **Editorial Guidelines**: Spelling, grammar, no gimmicks
  - **Value Proposition**: How to highlight unique benefits
- Provides sample headlines and descriptions as reference
- Includes Google-specific tips for responsive search ads

**Why it's important**: Writing effective ads requires understanding both Google's technical requirements and marketing best practices. This prompt ensures generated content is not only compliant but also optimized for performance. It helps the AI create ads that are compelling, relevant, and likely to achieve good click-through rates.

**Output**: Writing best practices stored as `[EFFECTIVE_WRITING]` variable for content quality optimization.

---

#### Prompt 1.7: (If exists)

**Note**: Prompt 1.7 may exist in some versions of the workflow. If present, it would typically handle additional setup tasks or configuration.

---

### Step 2: Keyword Generation (Prompts 2.1 - 2.2)

The keyword generation phase creates the search terms that will trigger the ads to appear in Google search results. This is foundational because keywords determine when ads are shown and must align with how people actually search.

#### Prompt 2.1: Generate Keywords

**Purpose**: Generates a comprehensive list of search keywords that people might use to find the target Bible verse.

**What it does**:
- Takes the perspective of "an average person with little Bible training" searching for the verse
- Generates **three categories of keywords**:
  1. **10 reference variations**: Different ways people might type the verse reference (e.g., "Matthew 28:18", "Matt 28 18", "Mt 28.18")
  2. **20 key phrase keywords**: Important phrases from the verse itself that people might search (e.g., for John 3:16, "For God so loved the world")
  3. **10 theological connections**: Related theological concepts or names for the passage (e.g., "Great Commission" for Matthew 28:18-20)
- Ensures all keywords are 5 words or less
- Removes non-standard characters that Google doesn't allow
- Outputs keywords in the target language

**Why it's important**: Keywords are the bridge between what people search for and your ads. This prompt creates a diverse keyword set that captures various search intents - from people who know the exact verse reference to those searching by theme or concept. The variety ensures ads appear for different types of searches, maximizing reach and relevance.

**Output**: A list of keywords stored as `[KEYWORDS]` variable, typically 40 keywords total.

---

#### Prompt 2.2: Create Keywords TXT

**Purpose**: Saves the generated keywords to a text file for easy import into Google Ads.

**What it does**:
- Creates the directory `[KEYWORDS_PATH]/[LANGUAGE_CODE]` if it doesn't exist
- Creates a text file named `[AD_GROUP_NAME]_keywords.txt`
- Writes each keyword from `[KEYWORDS]` on a separate line
- Formats the file for easy copy-paste into Google Ads keyword planner or bulk upload

**Why it's important**: Google Ads requires keywords to be uploaded in a specific format. This prompt creates a properly formatted file that can be directly imported into Google Ads, saving time and reducing errors from manual entry. The file also serves as documentation of which keywords were selected for the campaign.

**Output**: A text file at `[KEYWORDS_PATH]/[LANGUAGE_CODE]/[AD_GROUP_NAME]_keywords.txt` containing all keywords, one per line.

---

### Step 3: Headline Generation (Prompts 3.1 - 3.2)

The headline generation phase creates compelling ad headlines that will appear in Google search results. Headlines are critical because they're the first thing users see and determine whether they click on the ad.

#### Prompt 3.1: Generate Headlines

**Purpose**: Creates a large pool of potential ad headlines from multiple sources, ensuring variety and relevance.

**What it does**:
- Acts as a "Google Advertising copywriting expert"
- Generates headlines in **two batches**:
  1. **60 headlines from keywords**: Creates headlines incorporating the generated keywords naturally
  2. **60 headlines from scripture**: Creates headlines based on the verse content itself
- Ensures all headlines are under 29 characters (Google's limit is 30, but 29 provides safety margin)
- Applies both `[GOOGLE_POLICIES]` and `[EFFECTIVE_WRITING]` guidelines
- Outputs in the target language
- Creates a combined master list of up to 120 headlines

**Why it's important**: Google's responsive search ads work best with variety. The more headline options Google has, the better it can match headlines to specific searches. This prompt creates a large pool of options that will be refined in the next step. Generating from both keywords and scripture ensures headlines are both search-relevant and content-relevant.

**Output**: A master list of headlines stored as `[HEADLINES]` variable, typically 100-120 headlines.

---

#### Prompt 3.2: Quality Check Headlines

**Purpose**: Refines the headline pool through multiple quality filters to select the best 15 headlines for the final ad.

**What it does**:
- Performs **four sequential quality checks**:
  1. **Remove duplicates**: Eliminates identical or near-identical headlines
  2. **Remove over-length**: Removes any headlines longer than 29 characters
  3. **Remove irrelevant**: Filters out headlines not relevant to the scripture
  4. **Remove non-compliant**: Eliminates headlines that violate Google policies
- After each filter, ensures at least 15 headlines remain (generates more if needed)
- **Final selection**: If more than 15 headlines remain, evaluates and selects the top 15 based on `[EFFECTIVE_WRITING]` criteria:
  - Keyword relevance
  - Emotional appeal
  - Call-to-action effectiveness
  - Brand voice alignment
  - Conversion potential

**Why it's important**: Quality over quantity. While Google allows up to 15 headlines, using the best 15 is more effective than using all available options. This prompt ensures the final headlines are compliant, relevant, compelling, and optimized for performance. The multi-stage filtering process catches issues that could hurt ad performance or cause policy violations.

**Output**: A refined list of 15 high-quality headlines stored as `[FINAL_HEADLINES]` variable.

---

### Step 4: Description Generation (Prompts 4.1 - 4.2)

The description generation phase creates the ad descriptions that appear below headlines in Google search results. Descriptions provide additional context and encourage clicks.

#### Prompt 4.1: Generate Descriptions

**Purpose**: Creates a pool of potential ad descriptions that complement the headlines and provide more detail about the offering.

**What it does**:
- Acts as a "Google Advertising copywriting expert"
- Generates descriptions in **two batches**:
  1. **20 descriptions from keywords**: Creates descriptions incorporating keywords naturally
  2. **20 descriptions from scripture**: Creates descriptions based on the verse content
- Ensures all descriptions are under 89 characters (Google's limit is 90, but 89 provides safety margin)
- Applies both `[GOOGLE_POLICIES]` and `[EFFECTIVE_WRITING]` guidelines
- Outputs in the target language
- Creates a combined master list of up to 40 descriptions

**Why it's important**: Descriptions provide the "why" behind the headline. They give users more information to make a click decision and can include additional keywords for relevance. Like headlines, variety helps Google match descriptions to different search queries effectively.

**Output**: A master list of descriptions stored as `[DESCRIPTIONS]` variable, typically 30-40 descriptions.

---

#### Prompt 4.2: Quality Check Descriptions

**Purpose**: Refines the description pool through quality filters to select the best 4 descriptions for the final ad.

**What it does**:
- Performs **five sequential quality checks**:
  1. **Remove duplicates**: Eliminates identical descriptions
  2. **Remove over-length**: Removes descriptions longer than 89 characters
  3. **Remove irrelevant**: Filters out descriptions not relevant to the scripture
  4. **Remove non-compliant**: Eliminates descriptions that violate Google policies
  5. **Final selection**: If more than 4 descriptions remain, selects the top 4 based on `[EFFECTIVE_WRITING]` criteria
- Ensures at least 4 descriptions remain after filtering (generates more if needed)

**Why it's important**: Google allows up to 4 descriptions per responsive search ad. Selecting the best 4 ensures maximum relevance and performance. The quality checks ensure descriptions are compliant, relevant, and compelling while working together with headlines to create effective ad combinations.

**Output**: A refined list of 4 high-quality descriptions stored as `[FINAL_DESCRIPTIONS]` variable.

---

### Step 5: Create Ads CSV (Prompt 5.1)

The CSV creation phase compiles all generated ad assets into a format that can be directly imported into Google Ads.

#### Prompt 5.1: Create Ads CSV

**Purpose**: Assembles all ad components (headlines and descriptions) into a properly formatted Google Ads CSV file.

**What it does**:
- **Step 1**: Loads the default Google Ads CSV template structure with all required fields:
  - Row type (Ad)
  - Action (Add)
  - Ad status (Enabled)
  - Campaign and ad group information
  - 15 headline fields (Headline 1-15)
  - 4 description fields (Description 1-4)
  - URL fields (Final URL, Path 1, etc.)
  - Tracking and bidding fields
- **Step 2**: Merges the generated content:
  - Places the 15 headlines from `[FINAL_HEADLINES]` into Headline 1-15 columns
  - Places the 4 descriptions from `[FINAL_DESCRIPTIONS]` into Description 1-4 columns
  - Sets the Final URL to `[TARGET_URL]` (the landing page)
  - Sets Path 1 to `[AD_GROUP_PREFIX]` for URL display
- **Step 3**: Saves the completed CSV file to `[ADS_PATH]/[LANGUAGE_CODE]/[AD_GROUP_NAME]_ad.csv`
- Ensures all content is properly enclosed in double-quotes as required by Google

**Why it's important**: Google Ads requires a very specific CSV format for bulk uploads. This prompt creates a file that can be directly imported into Google Ads without manual formatting or data entry. It combines all the work from previous prompts into a single, ready-to-use file. The proper formatting prevents import errors and saves significant time.

**Output**: A complete Google Ads CSV file at `[ADS_PATH]/[LANGUAGE_CODE]/[AD_GROUP_NAME]_ad.csv` ready for import into Google Ads.

---

### Step 6: Landing Page Development (Prompts 6.1 - 6.3)

The landing page development phase creates the web pages that users land on after clicking ads. These pages must be optimized for conversions and accurately represent Zume Training.

#### Prompt 6.1: Cross-Reference Content

**Purpose**: Identifies natural connections between the ad content and Zume Training's curriculum to create relevant landing page content.

**What it does**:
- Analyzes three content sources:
  - `[ZUME_CONCEPTS]` - All 33 Zume Training topics
  - `[KEYWORDS]` - The search terms people are using
  - `[FINAL_HEADLINES]` and `[FINAL_DESCRIPTIONS]` - The ad copy
- Identifies natural connections and relationships between:
  - The Bible verse being advertised
  - Zume Training concepts that relate to that verse
  - The keywords and ad copy that brought users to the page
- Generates an enumerated list with:
  - Descriptive titles for each connection
  - Expansive paragraphs explaining how the verse connects to Zume Training
  - Why that connection matters for potential students

**Why it's important**: Landing pages need to fulfill the promise of the ad. If someone clicks an ad about a Bible verse, the landing page should explain how Zume Training helps them understand or apply that verse. This prompt creates the intellectual bridge between the ad and the training program, making the landing page relevant and compelling rather than generic.

**Output**: A cross-referenced content list stored as `[CROSS_REFERENCED_CONTENT]` variable, containing connections between the verse and Zume Training concepts.

---

#### Prompt 6.2: Generate Landing Page JSON

**Purpose**: Creates the data structure (JSON) that will populate the landing page template with verse-specific and language-specific content.

**What it does**:
- Loads the landing page template (`landing.html`) and existing JSON structure (`landing.json`)
- Rewrites the JSON content for the specific campaign by:
  - **Translating** all content into the target language (`[LANGUAGE]`)
  - **Updating quotes and references** to match the target `[SCRIPTURE]`
  - **Replacing URL placeholders** with actual URLs:
    - `[TARGET_URL]` - The landing page URL
    - `[PUBLIC_URL]` - The main Zume Training site URL
    - `[CTA_URL]` - The call-to-action form URL
  - **Enhancing content** using `[CROSS_REFERENCED_CONTENT]`:
    - Updates help card sections with relevant Zume concepts
    - Enhances FAQ content with verse-specific information
  - **Replacing identifiers**:
    - `[AD_GROUP_NAME]` with campaign ID
    - `[LANGUAGE_CODE]` with actual language code
- Outputs clean JSON ready for template population

**Why it's important**: Landing pages need to be personalized for each verse and language. This prompt transforms a generic template into verse-specific, language-specific content that feels relevant to the user. The JSON structure allows for easy template population while maintaining consistency across all landing pages.

**Output**: A complete JSON data structure stored as `[LANDING_JSON]` variable, containing all content for the landing page.

---

#### Prompt 6.3: Generate HTML Landing Page

**Purpose**: Merges the JSON data with the HTML template to create the final, complete landing page file.

**What it does**:
- **Creates the file**: Generates `[AD_GROUP_NAME].html` in `[HTML_PATH]/[LANGUAGE_CODE]/`
- **Processes the template**: 
  - Takes the `[LANDING_TEMPLATE]` (from `landing.html`)
  - Replaces all placeholder variables (like `[KEY_NAME]`) with corresponding values from `[LANDING_JSON]`
  - Ensures every placeholder is replaced with actual content
- **Validates output**:
  - Maintains original HTML structure and CSS classes
  - Preserves all styling and formatting
  - Ensures all links and URLs are properly formatted
  - Verifies no placeholder variables remain in the final file

**Why it's important**: This is the final step that creates the actual web page users will see. The landing page must be complete, properly formatted, and functional. This prompt ensures the page is ready to deploy without manual editing. A properly generated landing page improves user experience and conversion rates.

**Output**: A complete HTML landing page file at `[HTML_PATH]/[LANGUAGE_CODE]/[AD_GROUP_NAME].html` ready for deployment.

---

### Step 7: Quality Assurance (Prompts 7.1 - 7.2)

The quality assurance phase reviews and improves the generated content, particularly focusing on translation quality and cultural appropriateness.

#### Prompt 7.1: Translation Quality Assessment

**Purpose**: Evaluates the quality of translated content across three critical dimensions to ensure it's effective for the target audience.

**What it does**:
- Reviews the generated HTML landing page (`[AD_GROUP_NAME].html`) in the target language
- Assesses quality across **three dimensions**:
  1. **Purpose and Communication Alignment**:
     - Checks if phrases are technically correct but miss the mark for the page's purpose
     - Evaluates if calls-to-action, headlines, and messaging have clear persuasive power
     - Identifies subtle meaning shifts that could confuse users
  2. **Domain-Specific Terminology Accuracy**:
     - Verifies "Zúme" is not mistranslated (e.g., as "Zoom" or "Zoome")
     - Checks if specialized theological terms from the glossary are translated correctly
     - Ensures technical terms maintain precise meaning for the target audience
  3. **Natural Language and Local Dialect**:
     - Evaluates if text sounds natural to native speakers
     - Checks if sentence structures match local dialect
     - Assesses if tone and formality level are appropriate for cultural context
     - Identifies awkward phrasings suggesting literal translation
- For each issue found, provides:
  - The problematic text (quoted)
  - Which dimension(s) it affects
  - Explanation of why it's problematic
  - Suggested improved translation
  - Severity rating (Critical/Moderate/Minor)
- Uses a comprehensive glossary of Zume Training terms to ensure accurate translation

**Why it's important**: Machine translation can be technically correct but culturally inappropriate or ineffective. This prompt catches issues that could hurt user experience, reduce conversions, or misrepresent Zume Training. It ensures the landing page feels native to the target language and culture, not like a translation.

**Output**: A quality assessment report identifying issues and providing improvement suggestions.

---

#### Prompt 7.2: Apply Quality Improvements

**Purpose**: Implements all suggested improvements from the quality assessment to create the final, polished landing page.

**What it does**:
- Takes the quality assessment report from Prompt 7.1
- Applies all suggested improvements to the HTML file
- Updates problematic text with improved translations
- Ensures all critical and moderate issues are resolved
- Optionally addresses minor issues for polish
- Maintains HTML structure while improving content quality

**Why it's important**: Identifying issues is only half the job - they must be fixed. This prompt ensures the landing page is not just complete, but polished and effective. A well-translated, culturally appropriate landing page significantly improves conversion rates and user trust.

**Output**: An improved HTML landing page file with all quality issues resolved, ready for final deployment.

---

## Workflow Logic Flow

The prompts follow a **cascading dependency model** where each step builds upon previous outputs:

```
Initial Setup (1.1-1.7)
    ↓
    Creates: Variables, Directories, Context (Brand, Policies, Writing Guide)
    ↓
Keyword Generation (2.1-2.2)
    ↓
    Uses: Variables from 1.1
    Creates: [KEYWORDS] variable + Keywords file
    ↓
Headline Generation (3.1-3.2)
    ↓
    Uses: [KEYWORDS], [GOOGLE_POLICIES], [EFFECTIVE_WRITING]
    Creates: [FINAL_HEADLINES] variable
    ↓
Description Generation (4.1-4.2)
    ↓
    Uses: [KEYWORDS], [GOOGLE_POLICIES], [EFFECTIVE_WRITING]
    Creates: [FINAL_DESCRIPTIONS] variable
    ↓
Create Ads CSV (5.1)
    ↓
    Uses: [FINAL_HEADLINES], [FINAL_DESCRIPTIONS], Variables
    Creates: Google Ads CSV file
    ↓
Landing Page Development (6.1-6.3)
    ↓
    Uses: [KEYWORDS], [FINAL_HEADLINES], [FINAL_DESCRIPTIONS], [ZUME_CONCEPTS]
    Creates: [CROSS_REFERENCED_CONTENT], [LANDING_JSON], HTML file
    ↓
Quality Assurance (7.1-7.2)
    ↓
    Uses: Generated HTML file
    Creates: Improved HTML file
```

## Key Design Principles

### 1. **Separation of Concerns**
Each prompt has a single, well-defined purpose. This makes the workflow maintainable and allows for easy updates to individual steps without affecting others.

### 2. **Variable-Based Architecture**
Content flows through variables (`[KEYWORDS]`, `[HEADLINES]`, etc.) rather than being hardcoded. This allows for easy customization and reusability.

### 3. **Quality Gates**
Multiple prompts include quality checks (3.2, 4.2, 7.1) ensuring content meets standards before proceeding. This prevents low-quality content from propagating through the workflow.

### 4. **Compliance First**
Google policies and brand guidelines are loaded early (1.3, 1.5) and referenced throughout, ensuring all content is compliant and on-brand from the start.

### 5. **Iterative Refinement**
Content is generated in large pools (120 headlines, 40 descriptions) then refined down to the best options. This ensures quality through selection rather than generation.

### 6. **Context Awareness**
Later prompts (6.1, 6.2) use earlier outputs to create coherent, connected content. The landing page references the same concepts as the ads, creating a seamless user experience.

## File Structure

The `src-prompts/` folder contains:

- **`_first_prompt.md`**: Example initial prompt showing how to load variables and execute the workflow
- **`1.1.txt` through `1.7.txt`**: Initial setup prompts
- **`2.1.txt`, `2.2.txt`**: Keyword generation prompts
- **`3.1.txt`, `3.2.txt`**: Headline generation prompts
- **`4.1.txt`, `4.2.txt`**: Description generation prompts
- **`5.1.txt`**: Ads CSV creation prompt
- **`6.1.txt`, `6.2.txt`, `6.3.txt`**: Landing page development prompts
- **`7.1.txt`, `7.2.txt`**: Quality assurance prompts
- **`landing.html`**: HTML template for landing pages
- **`landing.json`**: JSON template structure for landing page data

## Usage

To execute the complete workflow:

1. **Load initial variables** (Scripture, Language, Campaign settings)
2. **Execute prompts sequentially** from 1.1 through 7.2
3. **Review generated files** in their respective directories
4. **Import to Google Ads** (CSV files) and **Deploy landing pages** (HTML files)

The prompts are designed to be executed by an AI assistant (like Cursor Agent) that can maintain context across multiple prompts and execute file operations.

---

## Summary

The source prompts folder contains a sophisticated, 7-step workflow that transforms a Bible verse reference into a complete Google Ads campaign with keywords, ad copy, and optimized landing pages. Each prompt serves a specific purpose in a carefully orchestrated sequence, with quality checks and compliance measures built in at key points. The workflow ensures brand consistency, Google Ads compliance, and high-quality, conversion-optimized content for each campaign.

