---
title: "Using URL Parameters to Customize Interviews"
description: "Pass contextual information through URL parameters to personalize interview experiences, enable branching logic, and eliminate repetitive questions."
date: "2025-11-04"
tags: ["url-parameters", "customization", "branching-logic", "advanced-features"]
nav_order: 5
nav_display: true
---

# Using URL Parameters to Customize Interviews

URL parameters enable you to pass contextual information about participants directly into Perspective AI interviews. By appending data to your invite links, you can personalize interview experiences, implement branching logic, track recruitment sources, and eliminate repetitive demographic questions—all without manual configuration for each participant.

## How URL Parameters Work

URL parameters are key-value pairs added to the end of your Perspective invite link:
```
https://perspective.ai/interview/abc123
  ?plan=enterprise&role=admin&source=email
```

In this example:
- `plan=enterprise` tells Perspective the participant is on an enterprise plan
- `role=admin` indicates their role
- `source=email` tracks that they came from an email campaign

Perspective AI automatically reads these parameters and incorporates them into the interview context, enabling the AI to reference this information naturally during conversations or use it for conditional logic.

## Use Cases

### Pass Demographic Information

Eliminate repetitive qualifying questions by passing known information through URL parameters:

**What you can pass:**
- Company size, industry, or revenue tier
- User role, department, or seniority level
- Plan type, subscription tier, or account age
- Product usage metrics or feature adoption status
- Geographic location or time zone

**Example parameter string:**
```
company_size=500-1000&industry=fintech&role=product_manager
```

Instead of asking "What's your role?" Perspective already knows and can skip directly to substantive questions or reference this information naturally: "As a product manager at a mid-sized fintech company, how do you approach..."

### Enable Branching Logic

Use parameters to dynamically adjust interview flow, questions, or incentive structures based on participant attributes:

**Example use cases:**
- Show different incentive offers based on recruitment channel
- Adjust interview depth based on user expertise level
- Route power users to advanced feature discussions while guiding new users through basics
- Present different pricing research questions to free vs. paid users
- Customize onboarding interviews based on signup source

**Example parameter string:**
```
channel=referral&user_type=power_user&tenure=12months
```

Perspective can use this information to determine which topics to prioritize, how much context to provide, or which follow-up questions to ask.

### Track Recruitment Sources

Identify which channels drive the highest quality feedback by passing source information:

**Example sources:**
- Marketing campaigns (email, social, paid ads)
- Product touchpoints (in-app prompts, post-checkout surveys)
- Partner referrals or integrations
- Community channels or user groups

**Example parameter string:**
```
utm_source=newsletter&utm_campaign=q4-research&utm_medium=email
```

Analyze interview quality and completion rates across sources to optimize your recruitment strategy.

### Personalize Interview Experience

Create tailored experiences for different participant segments:

**Example personalizations:**
- Adjust technical depth based on user expertise
- Reference specific features the participant has used
- Acknowledge their relationship with your company (customer vs. prospect)
- Customize tone based on user segment (B2B vs. B2C, enterprise vs. startup)

**Example parameter string:**
```
segment=beta_tester&features_used=ai_assistant_analytics&customer_since=2023
```

### Pre-Qualify Participants

Pass screening criteria results to ensure Perspective focuses on research objectives rather than qualification:

**Example parameter string:**
```
screened=true&meets_criteria=yes&screening_date=2025-11-04
```

### A/B Test Interview Approaches

Experiment with different interview styles or question sequences:

**Example parameter string:**
```
variant=direct_questions&experiment_id=nov2025_test
```

Compare engagement, completion rates, and insight quality across variants.

## Setting Up URL Parameters

### Step 1: Define your parameters

Decide what information you want to pass and create a naming convention. Use clear, consistent parameter names:

**Good examples:**
- `plan_tier`, `user_role`, `company_size`
- `source`, `campaign`, `channel`

**Avoid:**
- Generic names like `type` or `data`
- Spaces or special characters
- Overly long parameter names

### Step 2: Construct your URLs

Append parameters to your base Perspective invite link using this format:
```
[base_url]?parameter1=value1&parameter2=value2&parameter3=value3
```

**Real example:**

Base URL: `https://perspective.ai/share/abc123`

With parameters: `https://perspective.ai/share/abc123?plan=pro&role=designer&source=linkedin&campaign=fall2025`

### Step 3: Distribute customized links

Send different URLs to different segments:

- Email campaigns: Merge parameter values from your email platform
- In-app invites: Dynamically generate URLs based on user data
- Partner integrations: Include partner-specific identifiers
- Marketing channels: Use unique parameters for each channel

### Step 4: Configure interview behavior (optional)

In your research outline settings, you can instruct Perspective how to use specific parameters:

**Example instructions:**

"If the plan parameter is 'enterprise', focus questions on team collaboration and admin features. If it's 'individual', focus on personal productivity."

![Outline settings with URL parameter instructions](/images/url-parameter-instructions.gif)
*Configure how Perspective should interpret and use URL parameters in your research outline settings.*

## Examples by Scenario

### Scenario 1: Customer Feedback by Plan Tier

**Goal:** Interview customers across different plan tiers without asking their plan type

**Parameter strings:**
- Free tier: `plan=free&user_id=12345`
- Pro tier: `plan=pro&user_id=67890`
- Enterprise tier: `plan=enterprise&user_id=11223`

**Outcome:** Perspective naturally adjusts questions based on plan tier, focusing on upgrade motivations for free users and advanced features for enterprise users.

### Scenario 2: Multi-Channel Recruitment Campaign

**Goal:** Track which channels produce the best research participants

**Parameter strings:**
- Email: `source=email&campaign=nov2025&list=engaged_users`
- LinkedIn: `source=linkedin&campaign=nov2025&ad_set=pmm_targeting`
- In-app: `source=product&campaign=nov2025&trigger=feature_launch`
- Community: `source=community&campaign=nov2025&platform=slack`

**Outcome:** Analyze completion rates and response quality by source to optimize future recruitment.

### Scenario 3: Onboarding Interview with Context

**Goal:** Interview new users without asking questions you already know answers to

**Parameter string:**
```
signup_date=2025-11-01&referral_source=friend&use_case=project_management&team_size=5
```

**Outcome:** Perspective skips basic qualifying questions and immediately explores how the user plans to use your product for project management with their small team.

### Scenario 4: Beta Testing with Different Incentives

**Goal:** Offer different incentive structures based on user segment

**Parameter strings:**
- Power users: `segment=power_user&incentive_tier=premium`
- Regular users: `segment=regular&incentive_tier=standard`
- New users: `segment=new&incentive_tier=entry`

**Outcome:** Present appropriate incentive messaging at interview completion based on the parameter value.

## Best Practices

**Keep parameter names consistent.** Use the same naming convention across all your research projects to avoid confusion.

**Document your parameters.** Maintain a reference sheet of what each parameter means and which values are valid.

**Don't overload URLs.** Include only parameters that improve the interview experience. Too many parameters make URLs difficult to manage.

**Use URL encoding for special characters.** Spaces, ampersands, and special characters should be properly encoded.

**Test parameter variations.** Before launching, test URLs with different parameter combinations to ensure they behave as expected.

**Respect privacy.** Don't pass sensitive personal information through URL parameters unless necessary. They're visible in browser history and server logs.

**Combine with form fields.** Use parameters for information you already have and form fields for information you need to collect.

**Monitor parameter usage.** Track which parameters actually improve your research and eliminate ones that don't add value.

## Common Pitfalls & Fixes

**Parameters not recognized** → Ensure parameter names don't contain spaces or special characters. Use underscores or camelCase instead.

**Inconsistent parameter values** → Standardize values across your systems. "Enterprise," "enterprise," and "ENTERPRISE" are treated as different values.

**Overly complex URLs** → Limit to 5-7 meaningful parameters. More than that becomes difficult to manage and debug.

**Missing parameters break logic** → Always test what happens when expected parameters are missing. Build fallback behavior.

**Hardcoding assumptions** → Don't assume parameter values are always present or accurate. Validate on the backend when using parameters for critical branching.

**Not testing edge cases** → Test with unusual parameter values, missing parameters, and malformed URLs before launching.

**Privacy concerns** → Avoid passing PII (personally identifiable information) in URLs. Use anonymous identifiers and look up details server-side if needed.

## Technical Considerations

**Parameter encoding:** Special characters must be URL-encoded:
- Space → `%20` or `+`
- Ampersand → `%26`
- Equals → `%3D`

**Parameter order:** Order doesn't matter, but consistency helps with tracking and debugging.

**Character limits:** Most browsers support URLs up to 2,000 characters, but keep yours much shorter for reliability.

**Case sensitivity:** Parameters are typically case-sensitive. Be consistent with capitalization.

## Availability

URL parameter support is available for all Perspective AI customers. Start passing contextual information to create more efficient, personalized research experiences.
