# Ad Campaign Project

A comprehensive workflow system for creating verse-based Google Ads campaigns and landing pages for Zume Training.

## Overview

This project provides a structured, step-by-step workflow for generating:
- Google Ads keywords, ad groups, and ad copy
- Policy-compliant responsive search ads
- Custom landing pages optimized for conversion
- Multi-language support with translation quality assessment

## Project Structure

```
.
├── landing.html          # HTML template for landing pages
├── landing.json          # JSON template for landing page content
├── prompt.md            # Complete workflow instructions and prompts
├── website/             # Generated landing pages
│   └── [LANGUAGE_CODE]/ # Language-specific landing pages
├── ads/                 # Generated ad CSV files
│   └── [LANGUAGE_CODE]/ # Language-specific ad files
├── ad-groups/           # Generated ad group CSV files
│   └── [LANGUAGE_CODE]/ # Language-specific ad group files
├── keywords/            # Generated keyword text files
│   └── [LANGUAGE_CODE]/ # Language-specific keyword files
└── README.md            # This file
```

## Key Features

- **Policy-Compliant Ads**: Ad copy follows Google's personalized advertising policies, focusing on user intent rather than religious identity
- **SEO Optimized**: Landing pages include structured data, meta tags, and canonical URLs
- **Multi-Language Support**: Complete workflow supports translation and localization with quality assessment
- **Conversion Focused**: Landing pages designed with clear CTAs and user journey optimization
- **Brand Aligned**: Content follows Zume Training's tone and voice guidelines
- **Quality Assurance**: Built-in translation quality assessment and content review process

## Workflow Overview

The project follows a comprehensive 7-step workflow documented in `prompt.md`:

### Step 1: Initial Setup (Prompts 1.1 - 1.6)
1. **Variable Setup (1.1)**: Configure campaign variables and file paths
2. **Create Ad Group CSV (1.2)**: Generate ad group structure with default template
3. **Load Zume Tone and Voice (1.3)**: Load brand voice guidelines
4. **Load Zume Concepts (1.4)**: Load complete topic list and descriptions (33 concepts)
5. **Load Google Policies (1.5)**: Load advertising policy guidelines
6. **Load Effective Writing Guide (1.6)**: Load copywriting best practices

### Step 2: Keyword Generation (Prompts 2.1 - 2.2)
1. **Generate Keywords (2.1)**: Create 40 keywords from scripture reference:
   - 10 variation keywords (e.g., "Mt 28 18", "Matt 28.18")
   - 20 phrase keywords (key phrases from the verse)
   - 10 theologically connected keywords
2. **Create Keywords CSV (2.2)**: Save keywords to text file

### Step 3: Headline Generation (Prompts 3.1 - 3.2)
1. **Generate Headlines (3.1)**: Create 120 headlines:
   - 60 from keywords
   - 60 from scripture
   - All under 29 characters, policy-compliant
2. **Quality Check Headlines (3.2)**: Filter to top 15 headlines:
   - Remove duplicates
   - Remove over-length headlines
   - Remove irrelevant content
   - Remove policy violations
   - Select best based on effective writing guidelines

### Step 4: Description Generation (Prompts 4.1 - 4.2)
1. **Generate Descriptions (4.1)**: Create 40 descriptions:
   - 20 from keywords
   - 20 from scripture
   - All under 89 characters, policy-compliant
2. **Quality Check Descriptions (4.2)**: Filter to top 4 descriptions using same quality criteria

### Step 5: Create Ads CSV (Prompt 5.1)
- Merge 15 headlines and 4 descriptions into responsive search ad CSV
- Use default template structure with all required Google Ads fields
- Save to language-specific directory

### Step 6: Landing Page Development (Prompts 6.1 - 6.3)
1. **Cross-Reference Content (6.1)**: Identify connections between ad content and Zume Training concepts
2. **Generate Landing Page JSON (6.2)**: Translate and customize landing page content:
   - Translate to target language
   - Update scripture references
   - Integrate cross-referenced content
   - Customize help cards and FAQ sections
3. **Generate HTML Landing Page (6.3)**: Merge JSON data with HTML template to create final landing page

### Step 7: Quality Assurance (Prompts 7.1 - 7.2)
1. **Translation Quality Assessment (7.1)**: Evaluate translation across three dimensions:
   - Purpose and communication alignment
   - Domain-specific terminology accuracy (including Zúme brand name)
   - Natural language and local dialect
2. **Apply Quality Improvements (7.2)**: Implement suggested improvements to HTML file

## Configuration

### Campaign Variables

Load these variables into your context at the start of each campaign:

**Core Campaign Variables:**
- **[CAMPAIGN_NAME]**: Google Ads campaign name (e.g., `Verses-English`)
- **[SCRIPTURE]**: Bible verse reference (e.g., `Timothy 2:2`)
- **[CAMPAIGN_PREFIX]**: Short identifier for files/URLs (e.g., `tim22`)
- **[LANGUAGE_CODE]**: ISO 639-1 language code (e.g., `en`, `hr`, `es`)
- **[LANGUAGE]**: Full language name (e.g., `English`, `Croatian`)
- **[BASE_URL]**: Base URL for landing pages (e.g., `https://pages.zume.training/verse`)
- **[PUBLIC_URL]**: Public site URL (e.g., `https://zume.training/[LANGUAGE_CODE]`)
- **[CTA_URL]**: Call-to-action URL (e.g., `[PUBLIC_URL]/form.html`)

**File Path Variables:**
- **[HTML_PATH]**: Landing page directory (default: `./website`)
- **[ADS_PATH]**: Ad CSV directory (default: `./ads`)
- **[AD_GROUP_PATH]**: Ad group CSV directory (default: `./ad-groups`)
- **[KEYWORDS_PATH]**: Keywords directory (default: `./keywords`)
- **[PROMPTS_PATH]**: Prompts directory (default: `./verse-prompts`)

**Derived Variables:**
- **[AD_GROUP_NAME]**: `[CAMPAIGN_PREFIX]-[LANGUAGE_CODE]`
- **[TARGET_URL]**: `[BASE_URL]/[LANGUAGE_CODE]/[AD_GROUP_NAME].html`

### Example Configurations

**English Campaign:**
```
[CAMPAIGN_NAME] = Verses-English
[SCRIPTURE] = Timothy 2:2
[CAMPAIGN_PREFIX] = tim22
[LANGUAGE_CODE] = en
[LANGUAGE] = English
[BASE_URL] = https://pages.zume.training/verse
```

**Croatian Campaign:**
```
[CAMPAIGN_NAME] = Verses-Croatian
[SCRIPTURE] = Acts 2:41-47
[CAMPAIGN_PREFIX] = acts-2-41-47
[LANGUAGE_CODE] = hr
[LANGUAGE] = Croatian
[BASE_URL] = https://pages.zume.training/verse
```

## Content Blocks

The workflow references several content blocks that are loaded during setup:

- **[ZUME_TONE_AND_VOICE]**: Brand voice guidelines (knowledgeable, motivational, approachable)
- **[ZUME_CONCEPTS]**: Complete list of 33 Zume Training topics with detailed descriptions
- **[GOOGLE_POLICIES]**: Guide to writing compliant ads focusing on user intent vs. religious identity
- **[EFFECTIVE_WRITING]**: Copywriting guide for Google Search Ads (structure, tone, CTAs, etc.)
- **[GLOSSARY]**: Theological and metaphorical terms for translation quality assessment

## Key Concepts

### Google Ads Policy Compliance

The workflow emphasizes compliance with Google's personalized advertising policies:
- **DO**: Focus on user intent, needs, and program benefits
- **DON'T**: Target users based on religious identity or belief systems
- Ads can contain religious terms but cannot target by religious identity
- Content must appeal to interests (e.g., "community service") rather than identity

### Zume Training Concepts

The workflow integrates 33 core concepts including:
- Spiritual Breathing (hearing and obeying God)
- S.O.A.P.S. Bible Study method
- Accountability Groups
- Consumer vs Producer Lifestyle
- 3/3 Group Meeting Pattern
- Training Cycle (Model, Assist, Watch, Leave)
- And 27 more concepts covering discipleship and church multiplication

### Translation Quality Assessment

The quality assessment evaluates:
1. **Purpose and Communication Alignment**: Are CTAs and messaging clear and persuasive?
2. **Domain-Specific Terminology**: Is "Zúme" correctly preserved (not translated to Zoom/Zoome)?
3. **Natural Language**: Does the text sound natural to native speakers?

## Usage

1. **Start a New Campaign**: Load campaign variables (Step 1.1)
2. **Follow Prompts Sequentially**: Execute prompts 1.1 through 7.2 in order
3. **Review Outputs**: Check generated files in respective directories
4. **Quality Check**: Review translation assessment and apply improvements
5. **Upload to Google Ads**: Import CSV files for ad groups and ads
6. **Deploy Landing Pages**: Upload HTML files to web server

## Requirements

- Google Ads account
- Basic knowledge of HTML/CSS/JSON
- Understanding of Google Ads policies
- Translation resources (for multi-language campaigns)
- Access to Zume Training brand guidelines and content

## File Naming Conventions

- **Ad Groups**: `[AD_GROUP_NAME]_new_ad_group.csv`
- **Keywords**: `[AD_GROUP_NAME]_keywords.txt`
- **Ads**: `[AD_GROUP_NAME]_ad.csv`
- **Landing Pages**: `[AD_GROUP_NAME].html`

Where `[AD_GROUP_NAME]` = `[CAMPAIGN_PREFIX]-[LANGUAGE_CODE]`

## Notes

- All ad content must comply with Google's personalized advertising policies
- Landing pages use the template structure defined in `landing.html` and `landing.json`
- Campaigns are designed to promote Zume Training's free discipleship program
- The brand name "Zúme" must never be translated (it's a Greek word meaning "yeast")
- The workflow supports any language with proper translation resources
- Quality assessment includes a comprehensive glossary of theological terms

## Additional Resources

For detailed step-by-step instructions, refer to `prompt.md` which contains:
- Complete prompt templates for each workflow step
- Content blocks for brand voice, concepts, and policies
- Translation quality assessment criteria
- Comprehensive glossary of Zume Training terminology
