## Initial Setup

Load these variables into the context:

- [SCRIPTURE] = Matthew 28:18-20
- [CAMPAIGN_PREFIX] = matt2818
- [LANGUAGE_CODE] = es
- [LANGUAGE] = Spanish
- [CAMPAIGN_NAME] = Verses-[LANGUAGE]
  
- [BASE_URL] = https://pages.zume.training/verse
- [PUBLIC_URL] = https://zume.training/[LANGUAGE_CODE]
- [CTA_URL] = [PUBLIC_URL]/form.html

---

## Prompt 1.1: Variable Setup

Load these variables into the context:

- [HTML_PATH] = ./website
- [ADS_PATH] = ./ads
- [AD_GROUP_PATH] = ./ad-groups
- [KEYWORDS_PATH] = ./keywords
- [PROMPTS_PATH] = ./verse-prompts
- [AD_GROUP_NAME] = [CAMPAIGN_PREFIX]-[LANGUAGE_CODE]
- [TARGET_URL] = [BASE_URL]/[LANGUAGE_CODE]/[AD_GROUP_NAME].html

---

## Prompt 1.2: Create Ad Group CSV

Create the folder [AD_GROUP_PATH]/[LANGUAGE_CODE] if not already created.

Create a csv file inside [AD_GROUP_PATH]/[LANGUAGE_CODE] and call the file [AD_GROUP_NAME]_new_ad_group.csv. Enclose all contents within double-quotes (").

Use the default template structure below for the header and default fields.
Include a header row in the csv file.

Default Template Structure:
- Row Type: Ad group
- Action: Add
- Ad group status: Enabled
- Campaign ID: 
- Campaign: [CAMPAIGN_NAME]
- Ad group ID: 
- Ad group: [AD_GROUP_NAME]
- Ad group type: Standard
- Ad rotation: Optimize
- Default max. CPC: 
- CPC%: 
- Max. CPM: 
- Max. CPV: 
- Target CPA: 
- Target CPM: 
- Target CPV: 
- Label: 
- Tracking template: 
- Final URL suffix: 
- Custom parameter: 
- Target ROAS: 

---

## Prompt 1.3: Load Zume Tone and Voice

Load the following content into the context and it will be referenced as [ZUME_TONE_AND_VOICE].

[ZUME_TONE_AND_VOICE] =
## Brand Voice and Tone

The brand voice of Zume Training is **knowledgeable**, **motivational**, and **approachable**. It aims to be an authoritative guide while maintaining a supportive and engaging tone. It is not overly formal, academic, or corporate.

Here are some specific examples:

**Adjectives that define the tone:**

* **Knowledgeable:** The content is rich with industry-specific terms and concepts, demonstrating deep expertise in project management and professional development.
* **Motivational:** The language often encourages the user to take action, improve their skills, and achieve their goals. Phrases like "propel your career" and "unlock your potential" are used frequently.
* **Approachable:** Despite the serious topics, the tone is friendly and easy to understand. It avoids being intimidating or exclusive, making the content accessible to a wide audience.
* **Action-oriented:** The website focuses on practical application and tangible outcomes, using direct and active verbs.

**Examples of what the tone is:**

* **"Propel your career with personalized learning paths."** (Motivational, action-oriented)
* **"A comprehensive approach to project management."** (Knowledgeable, authoritative)
* **"Ready to take the next step?"** (Approachable, motivational)

**Examples of what the tone is NOT:**

* **Not overly casual:** It doesn't use slang or overly informal language.
* **Not dry or academic:** It avoids complex jargon and a purely theoretical style, focusing instead on practical application.
* **Not overly aggressive or "salesy":** While it is motivational, it doesn't use pushy or high-pressure sales tactics. It's more about guidance and empowerment.

The overall tone is designed to build trust and position Zume Training as a valuable partner in the user's spiritual journey.

---

## Prompt 1.4: Load Zume Concepts

Load the following content into the context and it will be referenced as [ZUME_CONCEPTS].

[ZUME_CONCEPTS] =

Zúme Training is an online disciple-making movement designed for small groups of Jesus followers. We offer a free, self-paced training program that equips individuals to become disciples and make disciples. Our program includes 32 concepts and skills, 20 hours of training, and a variety of resources to help you grow in your faith and learn how to share it with others. We believe that anyone can be a disciple maker, and we provide the tools and support you need to make a difference in your community and the world.

# Complete Topic List

1. **God Uses Ordinary People** - Understanding how God works through ordinary people doing simple things
2. **Simple Definition of Disciple and Church** - Core concepts of discipleship and church
3. **Spiritual Breathing is Hearing and Obeying God** - The foundation of discipleship
4. **S.O.A.P.S. Bible Study** - Daily Bible study methodology
5. **Accountability Groups** - Weekly encouragement and correction groups
6. **Consumer vs Producer Lifestyle** - Four ways God transforms followers
7. **How to Spend an Hour in Prayer** - Extended prayer practice
8. **Relational Stewardship – List of 100** - Relationship management tool
9. **Spiritual Economy** - God's investment principles
10. **The Gospel and How to Share It** - Evangelism from creation to end times
11. **Baptism and How To Do It** - Practical baptism implementation
12. **Prepare Your 3-Minute Testimony** - Personal story sharing
13. **Vision Casting the Greatest Blessing** - Spiritual family multiplication
14. **Duckling Discipleship – Leading Immediately** - Early leadership development
15. **Eyes to See Where the Kingdom Isn't** - Kingdom awareness
16. **The Lord's Supper and How To Lead It** - Communion celebration
17. **Prayer Walking and How To Do It** - Prayer while walking
18. **A Person of Peace and How To Find One** - Evangelism strategy
19. **Faithfulness is Better Than Knowledge** - Action over information
20. **The BLESS Prayer Pattern** - Prayer mnemonic
21. **3/3 Group Meeting Pattern** - Simple church structure
22. **Training Cycle for Maturing Disciples** - Discipleship development process
23. **Leadership Cells** - Leadership development through service
24. **Expect Non-Sequential Growth** - Non-linear discipleship patterns
25. **Pace of Multiplication Matters** - Speed of growth importance
26. **Always Part of Two Churches** - Going and staying strategy
27. **Three-Month Plan** - Implementation planning
28. **Coaching Checklist** - Self-assessment tool
29. **Leadership in Networks** - Church network connections
30. **Peer Mentoring Groups** - Leader development groups
31. **Four Fields Tool** - Kingdom activity assessment
32. **Generational Mapping** - Growth visualization tool
33. **3-Circles Gospel Presentation** - Simple gospel illustration

---

# Detailed Descriptions

A comprehensive guide to all 33 topics in the Zume training curriculum, with detailed explanations of each concept and tool for disciple-making and church multiplication.

## Complete Topic Descriptions

### 1. God Uses Ordinary People
God intentionally chooses ordinary, everyday people to accomplish His extraordinary purposes in the world. This foundational truth liberates believers from feeling inadequate or unqualified for ministry work. The training emphasizes that God's power is made perfect in human weakness, and that simple obedience to God's leading is more valuable than impressive credentials or natural abilities.

### 2. Simple Definition of Disciple and Church
A disciple is someone who hears God's voice and obeys it, while a church is simply two or more believers gathered in Jesus' name. This simplified understanding removes the complexity and institutional barriers that often prevent people from engaging in disciple-making. The training challenges traditional notions of what constitutes "real" ministry and encourages believers to start where they are with what they have.

### 3. Spiritual Breathing is Hearing and Obeying God
Spiritual breathing represents the continuous cycle of receiving from God (hearing) and responding to Him (obeying). This metaphor helps believers understand that spiritual life requires ongoing communication with God, not just occasional religious activities. The practice involves daily listening for God's voice through Scripture, prayer, and circumstances, then immediately acting on what He reveals.

### 4. S.O.A.P.S. Bible Study
S.O.A.P.S. is a simple, reproducible Bible study method that anyone can use daily: Scripture (read a passage), Observation (what you notice), Application (how it applies to your life), Prayer (talk to God about it), and Sharing (tell someone else what you learned). This method transforms Bible reading from passive consumption to active engagement and creates natural opportunities for discipleship conversations.

### 5. Accountability Groups
Accountability groups are weekly gatherings of 2-4 believers who encourage one another, share struggles, and hold each other responsible for spiritual growth goals. These groups provide the relational support and gentle correction needed for sustained spiritual development. The training teaches how to form these groups, what questions to ask, and how to create a safe environment for vulnerability and growth.

### 6. Consumer vs Producer Lifestyle
This topic contrasts four different ways God transforms followers: from consumer to producer, from producer to consumer, from consumer to consumer, and from producer to producer. The training helps believers identify their current spiritual posture and move toward becoming producers who multiply disciples rather than just consuming religious content. It emphasizes that spiritual maturity is measured by fruitfulness, not just knowledge.

### 7. How to Spend an Hour in Prayer
This practical guide breaks down how to structure an extended prayer time using the Lord's Prayer as a framework. The training teaches participants to divide their hour into specific segments for adoration, confession, thanksgiving, and supplication. It includes practical tips for maintaining focus and creating a sustainable prayer rhythm that can transform one's spiritual life.

### 8. Relational Stewardship – List of 100
The List of 100 is a strategic tool for managing relationships by identifying 100 people in your life who need Jesus or spiritual growth. This tool helps believers be intentional about their relational investments and provides a framework for prayer and evangelism. The training teaches how to categorize relationships, pray strategically, and look for opportunities to share the gospel or disciple others.

### 9. Spiritual Economy
Spiritual economy explains how God invests in people and expects a return on His investment through multiplication. This concept helps believers understand that God has given them spiritual gifts, resources, and opportunities that He expects them to steward well. The training emphasizes that spiritual wealth increases through giving away what God has given, not hoarding it for personal benefit.

### 10. The Gospel and How to Share It
This comprehensive overview covers the gospel story from creation to the end times, providing believers with a complete narrative to share with others. The training teaches how to present the gospel in a way that connects with people's felt needs and life experiences. It includes practical tips for starting spiritual conversations and responding to common questions about faith.

### 11. Baptism and How To Do It
This practical training covers the biblical meaning of baptism, when someone is ready for baptism, and how to perform a baptism ceremony. It emphasizes that baptism is a public declaration of faith and the beginning of a disciple's journey, not the end goal. The training includes step-by-step instructions for planning and conducting baptism services in various settings.

### 12. Prepare Your 3-Minute Testimony
A 3-minute testimony is a concise, compelling story of how God has worked in your life that can be shared in any conversation. This training teaches believers how to craft their personal story with a clear beginning, middle, and end that points to Jesus. It includes practice exercises and tips for adapting the testimony to different audiences and situations.

### 13. Vision Casting the Greatest Blessing
The greatest blessing is having spiritual children and grandchildren through disciple-making, which brings more joy than any earthly achievement. This topic helps believers understand that their legacy will be measured by the people they've helped follow Jesus, not by their personal accomplishments. The training teaches how to communicate this vision to others and inspire them to join in the disciple-making mission.

### 14. Duckling Discipleship – Leading Immediately
Duckling discipleship encourages new believers to begin leading others immediately, even while they're still learning themselves. This approach recognizes that leadership is learned through practice, not just study, and that God can use even immature believers to help others grow. The training provides practical ways for new disciples to start serving and leading from day one.

### 15. Eyes to See Where the Kingdom Isn't
This topic develops spiritual awareness to recognize where God's kingdom is not yet present or active in the world around us. It teaches believers to look for spiritual needs, broken relationships, and areas of darkness that need God's light. The training helps participants develop a missional mindset that sees every situation as a potential opportunity for kingdom impact.

### 16. The Lord's Supper and How To Lead It
This practical training covers the biblical meaning of communion, when and how often to celebrate it, and how to lead a meaningful Lord's Supper service. It emphasizes that communion is a celebration of Jesus' sacrifice and a reminder of our unity as believers. The training includes sample prayers, readings, and practical considerations for celebrating communion in various settings.

### 17. Prayer Walking and How To Do It
Prayer walking involves praying while walking through neighborhoods, workplaces, or other areas where you want to see God's kingdom come. This practice combines physical activity with spiritual intercession, helping believers connect with their communities on a deeper level. The training teaches how to organize prayer walks, what to pray for, and how to recognize and respond to divine appointments.

### 18. A Person of Peace and How To Find One
A person of peace is someone who is open to the gospel and can help introduce you to their network of relationships. This topic teaches how to identify these key people who can open doors for evangelism and discipleship. The training includes practical strategies for finding people of peace and building relationships with them that lead to spiritual conversations.

### 19. Faithfulness is Better Than Knowledge
This principle emphasizes that consistent obedience to what we already know is more valuable than accumulating more biblical knowledge without application. The training challenges believers to focus on implementing what they've learned rather than constantly seeking new information. It includes practical ways to measure faithfulness and develop habits of consistent spiritual practice.

### 20. The BLESS Prayer Pattern
BLESS is a prayer mnemonic that helps believers pray for their neighbors and coworkers: Body (physical needs), Labor (work and career), Emotional (emotional and mental health), Social (relationships), and Spiritual (spiritual needs). This tool provides a structured way to pray comprehensively for people and often reveals opportunities to serve and share the gospel. The training teaches how to use this pattern effectively and integrate it into daily prayer routines.

### 21. 3/3 Group Meeting Pattern
The 3/3 pattern is a simple, reproducible structure for small group meetings that can be led by anyone: first third (looking back at last week), second third (looking up to God through Bible study), and third third (looking ahead to next week). This format ensures groups stay focused on spiritual growth and accountability while remaining simple enough for new leaders to implement. The training provides detailed guidance for each section and tips for facilitating effective discussions.

### 22. Training Cycle for Maturing Disciples
This training cycle provides a systematic approach to developing mature disciples through four phases: I do, you watch; I do, you help; You do, I help; You do, I watch. This method ensures that discipleship is both caught and taught, with practical experience building alongside theoretical knowledge. The training includes specific activities and milestones for each phase of development.

### 23. Leadership Cells
Leadership cells are small groups focused specifically on developing leadership skills and character in emerging leaders. These groups provide intensive training in areas like vision casting, team building, and problem solving while maintaining accountability and support. The training teaches how to identify potential leaders, structure leadership development content, and create opportunities for practical leadership experience.

### 24. Expect Non-Sequential Growth
Non-sequential growth recognizes that spiritual development doesn't always follow a predictable, linear pattern. This topic helps leaders understand that setbacks, plateaus, and unexpected breakthroughs are normal parts of the discipleship journey. The training provides strategies for supporting people through various growth phases and maintaining momentum even when progress seems slow.

### 25. Pace of Multiplication Matters
The speed at which disciples and churches multiply significantly impacts the overall growth of God's kingdom. This topic emphasizes that while quality is important, the pace of multiplication should be intentionally accelerated through systematic disciple-making processes. The training teaches how to balance rapid multiplication with healthy development and avoid common obstacles that slow down growth.

### 26. Always Part of Two Churches
This strategy encourages believers to be part of two churches: one where they receive spiritual care and one where they serve and minister to others. This approach ensures that everyone is both being discipled and making disciples, creating a sustainable multiplication cycle. The training provides practical guidance for balancing involvement in both churches and managing the time commitments effectively.

### 27. Three-Month Plan
A three-month plan provides a structured approach to implementing disciple-making strategies with specific goals, timelines, and accountability measures. This planning tool helps believers move from good intentions to concrete action steps that lead to measurable results. The training teaches how to create realistic plans, track progress, and adjust strategies based on outcomes and feedback.

### 28. Coaching Checklist
The coaching checklist is a self-assessment tool that helps leaders evaluate their effectiveness in key areas of disciple-making and church multiplication. This tool provides objective criteria for measuring progress and identifying areas that need improvement or additional training. The training includes how to use the checklist effectively and develop action plans based on assessment results.

### 29. Leadership in Networks
This topic explores how to develop and maintain connections between churches and leaders in a network that supports multiplication and resource sharing. It emphasizes that isolated churches and leaders are less effective than those connected in supportive relationships. The training teaches practical strategies for building networks, facilitating collaboration, and creating systems for ongoing support and accountability.

### 30. Peer Mentoring Groups
Peer mentoring groups bring together leaders at similar stages of development to learn from each other, share challenges, and provide mutual support. These groups create a collaborative learning environment where leaders can grow together rather than in isolation. The training covers how to form effective peer groups, facilitate meaningful discussions, and ensure that all participants benefit from the shared experience.

### 31. Four Fields Tool
The Four Fields tool helps believers assess kingdom activity in their area by examining four key areas: the harvest field (people ready to receive the gospel), the seed sowers (believers sharing the gospel), the soil (hearts and minds of people), and the seasons (timing and circumstances). This assessment tool provides a comprehensive view of evangelism opportunities and helps prioritize ministry efforts. The training teaches how to conduct four fields assessments and develop strategies based on the findings.

### 32. Generational Mapping
Generational mapping is a visual tool that tracks how disciples and churches multiply over time, showing the growth pattern and identifying where multiplication is happening or needs to happen. This tool helps leaders see the big picture of their disciple-making efforts and identify areas that need attention or resources. The training includes how to create and maintain generational maps, interpret the data, and use insights to improve multiplication strategies.

### 33. 3-Circles Gospel Presentation
The 3-Circles gospel presentation uses three overlapping circles to illustrate God's design, brokenness in the world, and the gospel as the solution. This simple visual tool makes the gospel easy to understand and share in any conversation or setting. The training teaches how to draw the circles, explain each section, and transition naturally into gospel conversations with people from various backgrounds and beliefs.

---

## Prompt 1.5: Load Google Policies

Load the following content into the context and it will be referenced as [GOOGLE_POLICIES].

[GOOGLE_POLICIES] =

# Guide to Writing Compliant Ads for Christian Discipleship Training

The most important principle to understand from Google's policy is the distinction between ad content and ad targeting. Your ads can contain religious terms, but they cannot be used to target users based on their religious identity. The following guide is designed to help you create ad copy that focuses on user needs and search intent rather than a user's personal identity, thereby aligning with Google's policies.

DO: Focus on User Intent, Needs, and Program Benefits

The goal is to frame your discipleship program as a solution to a user's search for personal growth, community, or leadership skills. This approach appeals to a user's interests rather than their perceived religious identity.

- Focus on Action and Growth: Use verbs that describe what the user will learn or achieve.
- Highlight Universal Values: Emphasize benefits like leadership, community service, and personal development.
- Describe the Program's Content: You are permitted to use terms like "Christian," "biblical," and "faith-based" to describe your program, as long as the targeting is compliant.
- Target Broad, Interest-Based Audiences: When setting up your campaigns, target users interested in topics like "community service" or "charitable activities" rather than trying to target users by religion.

Compliant Headline Examples

- Develop Your Leadership Skills: This focuses on a non-sensitive user need (skill development) which is a compliant advertising strategy.
- Faith-Based Community Leadership: The use of "Faith-Based" is permissible in the ad's content. The headline describes the program's topic, not the user's identity.
- Biblical Studies & Mentorship: This headline describes the service offered ("religious guidance," "religious education") without targeting users based on that identity.
- Find Purpose in Community Service: This appeals to a user's interest in "volunteering events" or "community service," which are compliant targeting criteria.
- A Journey of Personal Growth: The language is centered on a universal user need, which aligns with Google's principle of focusing on user interest, not identity.

Compliant Description Examples

- Our discipleship program builds strong leaders for community outreach. Learn practical skills based on biblical principles. This describes the program's content and its benefits without making assumptions about the user's beliefs. It connects to the compliant interest of "community service".
- Seeking personal development? Our courses offer guidance on faith, purpose, and leading a fulfilling life. All are welcome. This description focuses on a user's search for "guidance" and "personal development," which is a compliant intent-based approach.
- Explore faith-based teachings in a supportive community. We offer mentorship and training for local service projects. This uses the acceptable term "faith-based" and highlights the compliant activity of "community service".

---

DON'T: Focus on the User's Religious Identity

The core violation of this policy is targeting users based on their "fundamental or intrinsic self-identity or their belief systems". Your ad copy should never assume, single out, or call out a user's religious affiliation.

- Directly Address a Religious Group: Avoid headlines like "For Christians in Colorado" or "Calling All Believers".
- Assume the User's Identity: Do not use phrases like "Is your faith important to you?" or "As a Christian, you know...".
- Promote Exclusivity Based on Religion: Avoid language that suggests the program is only for people of a specific faith.
- Build Targeting Lists from Religious Affiliation: Never use an advertiser-curated audience list of email addresses from a church directory or a remarketing list of visitors to religious education pages on your site.

Non-Compliant Headline Examples

- Discipleship for Devout Christians: This explicitly targets users based on their "Personal religious beliefs," which is a direct violation of the personalized advertising policy.
- Are You a Christian Leader?: This headline attempts to single out users based on their religious identity, which is prohibited.
- Training for Your Church Members: This implies targeting based on affiliation with "places of worship" and suggests the use of a prohibited advertiser-curated audience list.
- Find Christian Fellowship Here: This could be interpreted by automated systems as targeting users based on their religious identity or belief system.
- Colorado's Best Christian Training: While it may seem like a location-based ad, combining it with "Christian" can be interpreted by automated systems as an attempt to target a specific religious identity within a geographic area.

Non-Compliant Description Examples

- Join other Christians in our exclusive discipleship program. This course is designed for believers looking to deepen their faith. This description explicitly targets users based on their religious belief system, which is not allowed in personalized advertising.
- If you're a Christian, you'll love our training program. We help followers of Christ become strong leaders. The copy makes a direct assumption about the user's identity ("If you're a Christian"), a clear violation of the policy against targeting based on belief systems.
- We've trained thousands of churchgoers. Our list of members from local churches can attest to our success. This description is an egregious violation, as it implies the use of advertiser-curated lists (e.g., church directories), which are subject to the strictest rules.

---

## Prompt 1.6: Load Effective Writing Guide

Load the following content into the context and it will be referenced as [EFFECTIVE_WRITING].

[EFFECTIVE_WRITING] =

# GUIDE: Writing Effective Google Search Ads for Disciple-Making Training
⸻

1. Ad Structure & Limits
- Headlines: up to 15 (max 30 characters each)
- Descriptions: up to 4 (max 90 characters each)
- Google mixes and matches to find best combinations
- Use variety, don't repeat the same phrase

⸻

2. Keyword Relevance
- Include keywords like: discipleship training, faith course, Christian leadership, spiritual growth
- Place them in headlines and descriptions
- Keep wording natural and not forced

⸻

3. Tone for Faith-Based Audience
- Warm, positive, inclusive
- Emphasize: community, purpose, hope, belonging, guidance
- Use "you" and "we" for connection (ex: "We'll guide you," "Find your calling")

⸻

4. Emotional Triggers
- Highlight transformation and growth
- Use words like: hope, purpose, belonging, growth, empower, uplifting
- Be genuine, not gimmicky

⸻

5. Calls to Action (CTA)
- Always include an action step
- Examples: "Join us today," "Learn more," "Sign up for training," "Start your journey"
- Test different CTAs to see which performs best

⸻

6. Editorial & Policy Guidelines
- Clear spelling and grammar
- No all caps or gimmicks (ex: "FREE!!!")
- Avoid repetition and symbols
- Match ad message with your landing page content
- Don't target by religion directly (just use relevant keywords)

⸻

7. Value Proposition
- Show what makes your training unique (mentor-led, small groups, online, etc.)
- State truthful benefits (not vague promises)

⸻

Sample Headlines (≤30 characters):
- Start Discipleship Training
- Join Our Journey of Faith
- Learn to Make Disciples
- Find Purpose in Faith
- Guided Christian Training
- Grow in Your Faith

Sample Descriptions (≤90 characters):
- Discover discipleship training. Mentor others in faith. Sign up today.
- Looking for spiritual growth? Join our online course and find purpose.
- Learn disciple-making skills from mentors. Start your journey today.
- Join a faith community. Guided training that transforms lives. Learn more.
- Grow deeper in faith with hands-on training. Enroll now.

⸻

Google Tips
- Use responsive search ads (more flexibility)
- Add as many unique headlines/descriptions as possible
- Watch "Ad Strength" feedback in Google Ads
- Keep important keywords in some headlines


---

## Prompt 2.1: Generate Keywords

You are an average person with little Bible training searching on Google for [SCRIPTURE]. Produce lists of possible search phrases that you might use to find [SCRIPTURE]. Do the following tasks step by step.

Create 10 keywords that are variations of the reference, for example Matthew 28:18 could be Mt 28 18 or Matt 28.18. Keywords cannot contain non-standard characters like: ! @ % , *

Create 20 keywords that pull key phrases out of the verse that might be used in search, for example John 3:16 might be searched for as "For God so loved the world"

Create 10 keywords that are theologically connected to [SCRIPTURE], for example Matt 28:18 is the "Great Commission".

List only the phrases, no numbering, no annotations, do not use ( ), one item per line. All keyword ideas must be 5 words or less.

Output in [LANGUAGE].

This result will be referenced as [KEYWORDS]

---

## Prompt 2.2: Create Keywords TXT

Create a txt file inside [KEYWORDS_PATH]/[LANGUAGE_CODE] and call the file [AD_GROUP_NAME]_keywords.txt.

Instructions:
- Populate the [AD_GROUP_NAME]_keywords.txt file with the [KEYWORDS].
- Make a new line for each keyword.

---

## Prompt 3.1: Generate Headlines

You are a Google Advertising copywriting expert.

Let's process the following instructions step by step. The outputs of each of these steps will be combined into a master list of headlines. This list of headlines will be referenced as [HEADLINES]. Write all content in [LANGUAGE].

Step 1: Create 60 headlines from the [KEYWORDS]. Each headline must be under 29 characters. Each headline must follow [GOOGLE_POLICIES] AND [EFFECTIVE_WRITING]. List only the phrases, no numbering, no annotations, do not use ( ).

Step 2: Create 60 headlines from the [SCRIPTURE]. Each headline must be under 29 characters. Each headline must follow [GOOGLE_POLICIES] AND [EFFECTIVE_WRITING]. List only the phrases, no numbering, no annotations, do not use ( ).

This combined list of headlines will be referenced as [HEADLINES].

---

## Prompt 3.2: Quality Check Headlines

Let's quality check the [HEADLINES] step by step:

First, remove duplicate headlines from [HEADLINES]. Remaining number of headlines must be greater than 15.

Second, remove headlines longer than 29 characters from [HEADLINES]. Remaining number of headlines must be greater than 15, if not generate more.

Third, remove headlines that are irrelevant to [SCRIPTURE] from [HEADLINES]. Remaining number of headlines must be greater than 15, if not generate more.

Fourth, remove the headlines that fail to comply with [GOOGLE_POLICIES] from [HEADLINES]. Remaining number of headlines must be greater than 15, if not generate more.

If more than 15 headlines remain, evaluate and choose the top 15 according to [EFFECTIVE_WRITING].

Output only the phrases, no numbering, no annotations, do not use ( ).

This final list will be referenced as [FINAL_HEADLINES].

---

## Prompt 4.1: Generate Descriptions

You are a Google Advertising copywriting expert.

Let's process the following instructions step by step. The outputs of each of these steps will be combined into a master list of descriptions. This list of descriptions will be referenced as [DESCRIPTIONS]. Write all content in [LANGUAGE].

Step 1: Create 20 descriptions from the [KEYWORDS]. Each description must be under 89 characters. Each description must follow [GOOGLE_POLICIES] AND [EFFECTIVE_WRITING]. List only the sentences, no numbering, no annotations, do not use ( ).

Step 2: Create 20 descriptions from the [SCRIPTURE]. Each headline must be under 89 characters. Each headline must follow [GOOGLE_POLICIES] AND [EFFECTIVE_WRITING]. List only the sentences, no numbering, no annotations, do not use ( ).

This combined list of descriptions will be referenced as [DESCRIPTIONS].

---

## Prompt 4.2: Quality Check Descriptions

Let's quality check the [DESCRIPTIONS] step by step:

First, remove duplicate descriptions from [DESCRIPTIONS]. Remaining number of descriptions must be greater than 4.

Second, remove descriptions longer than 89 characters. 

Third, remove descriptions that are irrelevant to [SCRIPTURE] from [DESCRIPTIONS]. Remaining number of descriptions must be greater than 4.

Forth, remove the descriptions that fail to comply with [GOOGLE_POLICIES] from [DESCRIPTIONS]. Remaining number of descriptions must be greater than 4.

Fifth, if more than 4 descriptions remain, evaluate and choose the top 4 according to [EFFECTIVE_WRITING].

Output only the phrases, no numbering, no annotations.

This final list will be referenced as [FINAL_DESCRIPTIONS].

---

## Prompt 5.1: Create Ads CSV

Build a csv file in 3 steps. Enclose all contents within double-quotes (").

Step 1: Load default template structure below for the header and default fields.

Default Template Structure:
Row Type = Ad
Action = Add
Ad status = Enabled
Campaign ID =
Campaign = [CAMPAIGN_NAME]
Ad group ID =
Ad group = [AD_GROUP_NAME]
Ad ID =
Ad type = Responsive search ad
Label =
Headline 1 =
Headline 2 =
Headline 3 =
Headline 4 =
Headline 5 =
Headline 6 =
Headline 7 =
Headline 8 =
Headline 9 =
Headline 10 =
Headline 11 =
Headline 12 =
Headline 13 =
Headline 14 =
Headline 15 =
Description 1 =
Description 2 =
Description 3 =
Description 4 =
Headline 1 position =
Headline 2 position =
Headline 3 position =
Headline 4 position =
Headline 5 position =
Headline 6 position =
Headline 7 position =
Headline 8 position =
Headline 9 position =
Headline 10 position =
Headline 11 position =
Headline 12 position =
Headline 13 position =
Headline 14 position =
Headline 15 position =
Description 1 position =
Description 2 position =
Description 3 position =
Description 4 position =
Path 1 = [AD_GROUP_PREFIX]
Path 2 =
Final URL = [TARGET_URL]
Mobile final URL =
Tracking template =
Final URL suffix =
Custom parameter =

Step 2: Merge the 15 headlines from the [FINAL_HEADLINES] in the 15 "Headline #" columns, and place the 4 descriptions from the [FINAL_DESCRIPTIONS] in the 4 "Description #" column.

Step 3:  Save the merged content into a csv file inside [ADS_PATH]/[LANGUAGE_CODE] with the file name [AD_GROUP_NAME]_ad.csv.

---

## Prompt 6.1: Cross-Reference Content

Cross-reference [ZUME_CONCEPTS] with [KEYWORDS], [FINAL_HEADLINES], AND [FINAL_DESCRIPTIONS].

Generate a list that identifies natural connections between the ad and zume training. Enumerate the list and give a descriptive title and an expansive paragraph for each connection.

This cross-referenced list will be referenced as [CROSS_REFERENCED_CONTENT].

---

## Prompt 6.2: Generate Landing Page JSON

Load the following HTML file found at ./landing.html into the context and it will be referenced as [LANDING_TEMPLATE].

Load the following JSON file found at ./landing.json into the context and it will be referenced as [LANDING_JSON].

Rewrite content of LANDING_JSON for use in a high conversion landing page that will receive the traffic from an advertisement for [SCRIPTURE] to promote Zume Training. 

Do the following steps:
- Translate the current content of the JSON into [LANGUAGE]. 
- Change all quotes and references to match the [SCRIPTURE].
- Update all placeholders with URLS ([TARGET_URL],[PUBLIC_URL],[CTA_URL]).Ad
- Use the [CROSS_REFERENCED_CONTENT] as informational background to help you rewrite the help card section and the FAQ content section.
- Replace [AD_GROUP_NAME] with the CAMPAIGN_ID, and the [LANGUAGE_CODE] with the LANGUAGE_CODE.

Output only JSON with new content and allow it to be referenced as [LANDING_JSON].

---

## Prompt 6.3: Generate HTML Landing Page

## Task: Generate HTML Landing Page

**Objective:** Create a complete HTML landing page file by merging template content with dynamic data.

**Steps:**
1. **File Creation:** Create a new HTML file named `[AD_GROUP_NAME].html` in the directory `[HTML_PATH]/[LANGUAGE_CODE]/`

2. **Content Replacement:** Use the data from `[LANDING_JSON]` to replace all placeholder variables in `[LANDING_TEMPLATE]`

3. **Template Processing:** 
   - Each key in `[LANDING_JSON]` corresponds to a placeholder in `[LANDING_TEMPLATE]`
   - Replace all instances of `[KEY_NAME]` with the corresponding value from the JSON
   - Ensure all placeholders are replaced with actual content

4. **Output:** Save the final HTML file with all placeholders replaced with the JSON data

**Requirements:**
- Maintain the original HTML structure and formatting
- Preserve all CSS classes and styling
- Ensure all links and URLs are properly formatted
- Validate that no placeholder variables remain in the final output

---

## Prompt 7.1: Translation Quality Assessment

## Translation Quality Assessment Prompt

**Context**: You are evaluating the translation quality of the [HTML_PATH]/[LANGUAGE_CODE]/[AD_GROUP_NAME].html written in [TARGET_LANGUAGE]. Please assess the communication quality across three critical dimensions:

### 1. Purpose and Communication Alignment
- Are there any phrases that are technically correct but miss the mark for the page's specific purpose?
- Do calls-to-action, headlines, and key messaging have clear persuasive/instructional power?
- Are there subtle meaning shifts that could confuse or mislead users?

### 2. Domain-Specific Terminology Accuracy
- Confirm Zúme has not been translated as Zoom or Zoome. Zúme is the brand name.
- Are the specialized terms in the [GLOSSARY] translated correctly, if they have been used?
- Do technical terms maintain their precise meaning for this specific audience?

### 3. Natural Language and Local Dialect
- Does the text sound natural to native speakers of [TARGET_LANGUAGE]?
- Are sentence structures and expressions appropriate for the local dialect?
- Is the tone and formality level suitable for the target audience and cultural context?
- Are there awkward phrasings that suggest literal translation rather than natural expression?

**Instructions**: For each issue identified, please:
1. Quote the problematic text
2. Specify which dimension(s) it affects
3. Explain why it's problematic
4. Suggest an improved translation
5. Rate the severity (Critical/Moderate/Minor)


[GLOSSARY] =
Below are theological and metaphorical terms used in the training that may need further definition:

- **Zúme**: A Greek term meaning "yeast", used metaphorically to describe how small, transformative actions can permeate and transform an entire community.
- **Spiritual Breathing**: Refers to the process of hearing from God (symbolically, "inhaling") and acting on His guidance ("exhaling"), much like the natural act of breathing that sustains life.
- **S.O.A.P.S. Bible Reading**: An acronym for a Bible study method that involves Scripture, Observation, Application, Prayer, and Sharing.
- **Accountability Groups**: Small groups that meet regularly to discuss spiritual progress and challenges, fostering mutual accountability and support.
- **Producer vs. Consumer**: A metaphor contrasting active participation in spiritual growth (producing disciples) versus passively absorbing teachings (consuming information).
- **Prayer Cycle**: A structured, multi-step approach to prayer that includes phases such as praise, waiting, confession, scripture reading, asking, intercession, thanking, singing, meditating, listening, and concluding with praise.
- **List of 100**: A tool encouraging individuals to identify 100 people within their network as a starting point for relational outreach and discipleship.
- **Three‑Minute Testimony**: A concise format for sharing one's personal faith journey in a clear and impactful manner.
- **The Lord's Supper**: Also known as Holy Communion, this sacramental practice commemorates the final meal of Jesus with His disciples.
- **Duckling Discipleship**: A metaphor drawn from observing ducklings that both follow and lead, symbolizing the dual role of a disciple as both learner and emerging leader.
- **3/3 Group Meeting**: A meeting format that divides time into three parts – Looking Back, Looking Up, and Looking Forward – to encourage reflection, learning, and application.
- **Training Cycle (Model, Assist, Watch, Leave)**: A structured discipleship method outlining stages of teaching and mentoring, from demonstrating an action to gradually stepping back as the learner gains competence.
- **Leadership Cells**: Small, focused groups aimed at rapidly training and equipping individuals for leadership roles within the community.
- **Non‑Sequential Growth**: An approach to discipleship that emphasizes overlapping and simultaneous processes rather than a strict, linear progression.
- **Pace**: The speed at which discipleship and multiplication occur; it underscores the importance of rapid spiritual growth and outreach.
- **Always Part of Two Churches**: A concept urging believers to remain active in both their established local church and in new congregations they help launch.
- **Coaching Checklist**: A tool used by mentors to evaluate and support the development of spiritual leaders, focusing on areas like obedience, sharing, and training.
- **Four Fields**: A strategic planning tool that categorizes areas of spiritual outreach and growth into phases such as Empty, Seeding, Growing, Harvesting, and Multiplying.
- **Generational Mapping**: A visual or conceptual tool for tracking the progress and multiplication of disciples across different generations of spiritual growth.
- **Leadership in Networks**: The concept of connecting multiple simple churches or spiritual groups into a larger, interconnected network that supports sustained growth and mutual support.
- **Peer Mentoring Groups**: Small groups where leaders support, evaluate, and mentor one another using structured formats to foster mutual growth.
- **Three‑Month Plan**: A planning tool designed to set short-term, actionable goals for discipleship and multiplication efforts within the community.

- **Simple Church**: A basic, grassroots gathering of believers, often without formal structure, emphasizing community and relational discipleship.
- **Disciple**: A learner and follower of Jesus who actively commits to studying, living, and spreading His teachings.
- **Follower of Jesus**: An individual who trusts in Jesus Christ and seeks to emulate His life and teachings, embracing the call to live out the Gospel.
- **Obedience**: The act of following God's commandments and teachings, demonstrating trust and submission to His will.
- **Ordinary Believer**: A typical member of the Christian community who, while not in a leadership role, reflects genuine faith and commitment to living out the principles of the Gospel.
- **Disciple Making**: The process of guiding and teaching individuals to follow Jesus, replicating the journey of faith so that they can in turn become disciples who make disciples.
- **Disciple Maker**: An individual who actively engages in disciple making by mentoring, teaching, and modeling the way of Jesus to help others become His followers.

- **Model**: The act of demonstrating a skill or behavior by example, allowing others to learn through observation.
- **Assist**: The process of providing support and guidance to someone as they begin to practice a new skill, ensuring they understand and can apply the demonstrated behavior.
- **Watch**: The phase of closely observing the learner as they attempt to perform the skill on their own, offering feedback and ensuring safe and correct execution without overt intervention.
- **Leave**: The step of gradually stepping back once the learner has achieved competence, entrusting them with the responsibility to perform independently while remaining available for occasional support.
- **MAWL**: An acronym representing the combined process of Model, Assist, Watch, and Leave; it encapsulates a structured approach to discipleship and training where a leader demonstrates a skill, supports the learner, observes their progress, and then releases control as they become self-sufficient.

---

## Prompt 7.2: Apply Quality Improvements

Add all suggested improvements to the html file.
