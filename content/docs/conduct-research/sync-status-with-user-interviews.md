---
title: "Integrating Perspective AI with User Interviews"
description: "Automatically sync participant statuses between Perspective AI and User Interviews using link parameters to eliminate manual tracking work."
date: "2025-11-04"
tags: ["integrations", "user-interviews", "automation", "participant-management"]
nav_order: 4
nav_display: true
---

# Integrating Perspective AI with User Interviews

If you're using User Interviews to recruit participants for Perspective AI research projects, link parameters enable automatic status updates from "invited" to "complete"—eliminating manual tracking and saving significant time. This integration carries User Interviews invite IDs through the entire interview experience and automatically updates participant status when they finish.

<div style="padding:62.21% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/1130372851?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media; web-share" referrerpolicy="strict-origin-when-cross-origin" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Run Market Research With Perspective AI and User Interviews"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

## How It Works

Link parameters flow through three stages:

1. **Participant receives invitation** – User Interviews sends the invite with a tracked link to Perspective AI
2. **Interview is conducted** – The invite ID travels invisibly through the conversation
3. **Participant clicks completion button** – The redirect sends them back to User Interviews and automatically marks them complete

No manual status updates, no spreadsheets, no tracking headaches.

## Prerequisites

Before setting up the integration, ensure you have:
- A User Interviews account with an active research project
- A completed research outline in Perspective AI
- Admin access to both platforms

## Setting Up the Integration

### Step 1: Prepare your Perspective research outline

1. Create and finalize your research outline in Perspective AI
2. Click **Invite Participants**
3. Copy the invite link

![Copying the invite link from Perspective](/images/invite-link.png "screenshot")
*Copy your Perspective invite link before heading to User Interviews.*

### Step 2: Configure User Interviews

1. Navigate to User Interviews and open your research project
2. Go to the **Research Activity** section
3. Click **Edit the Task Platform**
4. Select **Tracked Custom Link** as the platform type
5. Paste your Perspective invite link into the URL field
6. Copy the **User Interviews redirect URL** that appears

![User Interviews tracked custom link setup](/images/user-interviews-tracked-link.gif "screenshot")
*Configure the tracked custom link in User Interviews and copy the redirect URL.*

### Step 3: Add the redirect URL to Perspective

1. Return to Perspective AI
2. Open your research outline's **Settings**
3. Expand the **Wrap Up** section
4. In the call-to-action button field, add button text (e.g., "Claim Your Reward")
5. Paste the User Interviews redirect URL you copied
6. Save your changes

![Perspective wrap-up settings with CTA button](/images/user-interviews-tracked-cta-link.gif "animated")
*Add a call-to-action button with the User Interviews redirect URL in your outline settings.*

That's it—your integration is configured and ready to use.

## Testing the Integration

Before inviting participants, verify the integration is working correctly:

1. In User Interviews, click **Preview and Confirm Setup**
2. The Perspective interview will launch
3. To skip through quickly, tell Perspective "skip to the end"
4. When asked if there's anything else to share, respond "no"
5. Click the call-to-action button (e.g., "Claim Your Reward")
6. You should see a User Interviews confirmation page

![Successful redirect confirmation page](/images/user-interviews-reditect-successful.png "screenshot")
*A successful integration redirects participants to this User Interviews confirmation page.*

If you see the confirmation page, the integration is working correctly. Participants will now automatically move to "completed" status after finishing interviews.

## What Participants Experience

From the participant's perspective, the experience is seamless:

1. They receive an invitation from User Interviews
2. They click the link and complete the Perspective AI interview
3. At the end, they see a button (e.g., "Claim Your Reward")
4. Clicking the button takes them back to User Interviews
5. Their status automatically updates to complete
6. They can proceed with any next steps (incentive claims, etc.)

## Best Practices

**Test before launching.** Always run through the preview flow yourself before sending invitations to real participants.

**Use clear CTA button text.** Choose text that motivates action, like "Claim Your Reward," "Get Your Incentive," or "Complete Your Session."

**Communicate the full flow.** In your User Interviews invitation, let participants know they'll be redirected to complete the interview and then brought back to claim rewards.

**Monitor both platforms initially.** For your first few participants, check both systems to ensure statuses are updating correctly.

**Keep URLs current.** If you update your Perspective research outline and get a new invite link, remember to update the URL in User Interviews as well.

## Common Pitfalls & Fixes

**Participants not marked complete** → Verify the redirect URL is correctly pasted in Perspective's wrap-up settings. A missing or incorrect URL will break the status update.

**Integration breaks after outline changes** → If you significantly modify your research outline, test the integration again to ensure the redirect still works properly.

**Preview doesn't work** → Clear your browser cache and try again. Some tracking parameters can be cached incorrectly during testing.

## Availability

Link parameter integration with User Interviews is available now for all Perspective AI customers. Give it a try and streamline your participant management workflow.
