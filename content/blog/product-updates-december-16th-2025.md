---
title: "Product Updates: December 16th, 2025"
date: "2025-12-16"
description: "This month brings our most powerful integrations yet—connect Perspective to your favorite AI assistants, deploy three specialized agent types, and automate post-interview routing with intelligent completion flows."
keywords: ["Perspective AI", "Perspective AI Product Updates", "Product Updates", "SaaS tools", "Customer Research", "AI in research", "AI-Powered Research", "AI-Driven Research", "MCP", "Model Context Protocol", "Agent Types", "Completion Flows", "Embed Interviews"]
author: "Perspective AI Team"
category: "Product News & Updates"
slug: "product-updates-december-16th-2025"
excerpt: "This month brings our most powerful integrations yet—connect Perspective to your favorite AI assistants, deploy three specialized agent types, and automate post-interview routing with intelligent completion flows."
image: "/images/blog/product-updates-december-2025.png"
tags: ["Product Management & Strategy", "Product News & Updates", "AI & Technology Trends"]
headings: ["Three Agent Types for Every Scenario", "Deploy Interviews Anywhere", "Connect Perspective to Your AI Workflow", "Intelligent Post-Interview Routing", "Looking Ahead"]
updated: "2025-12-16"
---

# Transform How You Conduct Research with Specialized Agents and Seamless Integrations

Welcome to December's update—our biggest leap forward in making research more integrated, intelligent, and adaptable to your specific needs.

This month, we're introducing capabilities that fundamentally change how you work with Perspective AI. We're launching three specialized agent types—each optimized for different research scenarios. We're giving you four flexible embed options to deploy interviews exactly where your users are. You can now connect your workspace directly to Claude Desktop, Claude Code, and Cursor through our MCP server. And we're adding intelligent completion flows that automatically route participants based on what they share.

Let's dive into what's new.

---

## Three Agent Types for Every Scenario

Not all research conversations should work the same way. This month, we're introducing three specialized agent types, each designed for specific use cases with distinct conversational approaches.

<img src="/images/agent-selection-gif.gif">

### Interviewer Agent: Deep Exploratory Research

The Interviewer agent conducts qualitative research using ethnographic techniques. Rather than following a rigid script, it lets themes emerge naturally by following the participant's narrative and asking adaptive follow-up questions.

<img src="/images/create-interviewer-agent-prompt.png">

**Use Interviewer agents when you need:**
- Emergent insights from exploratory conversations
- Participant-led exploration where they guide the conversation
- Rich, contextual understanding of behaviors and motivations
- Adaptive questioning that builds on what participants actually say

**Ideal for:** User research and discovery, customer experience mapping, feature exploration, understanding decision-making, churned customer conversations, early-stage market research.

### Concierge Agent: Intelligent Form Replacement

The Concierge agent replaces static forms with conversational experiences that infer what they can and only ask what they must. It uses an infer-and-validate approach—pre-filling obvious details and progressively narrowing questions based on responses.

<img src="/images/convert-existing-form-from-url.png">

**Use Concierge agents when you need:**
- Efficient structured data collection with known information requirements
- Context-aware questioning that skips redundant fields
- Progressive narrowing from broad to specific
- Adaptive field collection that adjusts based on what's already known

<img src="/images/extract-fields-from-form-url.gif">

**Ideal for:** Onboarding flows, lead qualification, support intake, application processes, converting web forms to conversations.

### Evaluator Agent: Surveys That Don't Suck

The Evaluator agent transforms surveys into engaging conversations. It applies structured assessment methodology to systematically gather feedback on specific criteria, presenting questions conversationally while maintaining consistency for quantitative analysis.

<img src="/images/create-evaluator-agent.png">

**Use Evaluator agents when you need:**
- Quantitative metrics presented conversationally
- Structured evaluation across consistent criteria
- Comparable data for statistical analysis
- Survey enhancement with better completion rates

**Ideal for:** Product satisfaction surveys (NPS, CSAT, CES), feature prioritization, usability testing, post-interaction feedback, market research.

### Choosing the Right Agent Type

- **Exploring the unknown?** → Interviewer
- **Collecting specific information efficiently?** → Concierge
- **Evaluating across defined criteria?** → Evaluator

Each agent type uses fundamentally different conversational approaches. Once you select a type, it's fixed for that outline—this ensures the methodology stays consistent with your research goals.

---

## Deploy Interviews Anywhere

### Four Flexible Embed Options

Your interviews can now live exactly where your users are. We've added four embed types, each optimized for different deployment scenarios:

<img src="/images/embed-interview-option.png">

**Full Page** – Displays the interview in a full-height iframe. Best for standalone experiences where the interview is the primary content.

**Inline Widget** – Drops the interview directly into your page content. Ideal for contextual placement within articles, product pages, or dashboards.

<img src="/images/embed-preview-inline.gif">

**Button** – Triggers the interview in three styles:
- **Popup**: Modal overlay centered on screen
- **Slider**: Side panel that slides in from the edge
- **Chat**: Chat-style interface anchored to the corner

<img src="/images/embed-preview-button.gif">

Choose Button for unobtrusive placement that doesn't interrupt page flow.

**Card** – Shows a clickable preview card that opens the interview in a new tab. Useful for resource centers or when you want users to opt into a full-screen experience.

<img src="/images/embed-options.gif">

**Preview before deploying:** Test Inline embeds and all three Button styles directly from the embed panel before adding code to your site.

For teams using AI-assisted development tools, you can integrate via the Perspective AI MCP server to add embed code directly from your IDE.

---

## Connect Perspective to Your AI Workflow

### MCP Server Integration

Your Perspective workspace now connects directly to AI assistants through the Model Context Protocol (MCP). This means you can create conversation agents, analyze interview data, and deploy embeds without switching contexts or leaving your IDE.

**What you can do with MCP:**

- **Create conversation agents** directly from Claude Desktop, Claude Code, or Cursor—no dashboard required
- **Analyze interviews from a single outline** by pulling responses and insights into your current workflow
- **Analyze across multiple outlines** to identify patterns and themes across research projects
- **Deploy embeds quickly** by generating and inserting embed code directly into your codebase

<img src="/images/generate-mcp-token.gif">

**Getting started is simple:**

1. Generate your MCP token from your profile menu
2. Configure your AI assistant with a single command or config snippet
3. Start using natural language to interact with Perspective: "Create a new interview outline for customer discovery" or "Pull all responses from the Q3 research outline and summarize key pain points"

<img src="/images/ai-ide-options.png">

For development teams already using AI-assisted coding tools, this integration means research becomes part of your natural workflow. No more context-switching between your IDE and browser tabs.

---

## Intelligent Post-Interview Routing

### Completion Flows

Completion Flows automatically route participants to different destinations at the end of interviews based on information gathered during the conversation. Instead of sending everyone to the same generic thank-you page, you create personalized next steps that match each participant's specific situation.

**Perfect for:**
- **Lead qualification** – Route high-value leads to sales while sending others to self-service resources
- **Support triage** – Direct urgent issues to support tickets and simple questions to documentation
- **Product recommendations** – Send participants to relevant product pages based on stated needs
- **Incentive distribution** – Provide different reward instructions based on eligibility criteria
- **Conversion optimization** – Guide qualified prospects to booking pages and others to nurture content

**How it works:**

1. Tell Perspective your routing conditions conversationally during outline creation
2. Perspective automatically adds a Completion Flow section to your outline
3. At the end of each interview, participants are redirected to the appropriate URL based on their responses
4. No manual routing required

<img src="/images/completion-flow-prompt.png">

**Example instruction:**

"Add a completion flow: if the participant's monthly budget is over $5,000 and company size is over 100 employees, redirect to example.com/book-enterprise-demo. Otherwise, redirect to example.com/self-service-plans."

<img src="/images/completion-flows-prompt-gif.gif">

Completion Flows evaluate conditions you define and automatically route participants—turning research insights into immediate action.

---

## Looking Ahead

This month's update represents a significant expansion in how Perspective integrates with your workflow and adapts to your specific research needs. The three agent types ensure you're using the right methodology for each scenario. Flexible embeds put interviews exactly where they need to be. The MCP server brings research into your development environment. And Completion Flows turn insights into immediate action.

We're continuing to invest in making research more intelligent, integrated, and effective. Stay tuned for more updates as we push the boundaries of what conversational AI can do for customer research.

As always, we'd love to hear what you think. Reach out through the in-app feedback or join our community to share your experience with these new features.

Happy researching!

— The Perspective AI Team
