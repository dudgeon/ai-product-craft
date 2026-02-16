---
title: "Farm-to-Table Software: How I Built a Thanksgiving Party Hub with Lovable & Hacked Recipes with ChatGPT"
created: 2026-02-15
updated: 2026-02-16
template: templates/source.md
template_version: 3
tags: [source, ai-pm, claude-added]
status: unread
source_type: podcast
source_url: "https://www.chatprd.ai/how-i-ai/thanksgiving-party-hub-with-lovable"
archive_url: ""
author: "Claire Vo"
host: ""
published: 2025-11-19
discovered: 2026-02-15
summary: "Claire Vo walks through two personal AI workflows: (1) vibe coding a custom Thanksgiving party hub using Lovable, Google Fonts, and Midjourney — going from generic AI-generated template to warm, personalized 'farm-to-table software' with custom dietary restriction tracking; (2) using ChatGPT to reformat cluttered online recipes into clean, step-by-step guides with inline measurements so you never scroll with messy hands."
domain: professional-development
project: ai-pm
# taxonomy_inference: software-methodology (vibe-coding, Lovable)
# provenance: bulk-added by Claude from podcast-episode-compilation.md (2026-02-15)
# rescrape_needed: false — full article scraped from ChatPRD 2026-02-16
---

# Farm-to-Table Software: How I Built a Thanksgiving Party Hub with Lovable & Hacked Recipes with ChatGPT

**By**: Claire Vo
**Source**: [How I AI (ChatPRD)](https://www.chatprd.ai/how-i-ai/thanksgiving-party-hub-with-lovable)
**Type**: podcast

## Summary

Claire Vo demonstrates two personal AI workflows in this pre-Thanksgiving episode. The first workflow covers vibe coding a custom Thanksgiving party hub using Lovable, transforming a generic AI-generated app into what she calls "farm-to-table software" — something warm, personal, and artisanally crafted. She uses Google Fonts (Homemade Apple + Railway) for cozy typography, Midjourney with style references for a custom header image, and iterative prompting to add personalized features like multi-select dietary restriction tracking that connects guests to dishes through allergen tags. The second workflow shows her kitchen hack: using a ChatGPT prompt to reformat any cluttered online recipe into a clean, numbered step-by-step guide with ingredients and measurements embedded directly in each instruction step — eliminating the need to scroll back to the ingredients list while cooking.

## Key Ideas Extracted

- **"Farm-to-table software"** concept: Don't accept the first AI output — iterate with your own design taste using fonts, custom images, and personal features to transform generic templates into something uniquely yours
- **Google Fonts integration in Lovable**: One of the fastest ways to uplevel vibe-coded apps; Lovable handles the API call, Tailwind config, and CSS automatically
- **Midjourney style references**: Browse X/Twitter for style codes from other creators, then adapt prompts to your theme for unique visuals that generic stock photos can't match
- **Specific UI vocabulary matters**: Using the term "multi-select" in the prompt told Lovable to use checkboxes instead of a text field — precise language drives better component choices
- **Custom data models from natural language**: Connecting dietary restrictions from guest profiles to dish tags created a relational data model in minutes that would take hours to code manually
- **Recipe reformatting prompt pattern**: The key instruction is telling ChatGPT to embed measurements directly into instruction steps so you never reference the ingredients list separately
- **Productized personal workflow**: Claire and her son turned the recipe hack into a website called Runaway Pancakes — example of how small AI workflows can become products

## Notes

Episode is a solo walkthrough (no guest interview). Two distinct workflows make this a good reference for both vibe coding methodology and practical ChatGPT prompt patterns. The "farm-to-table software" framing is a memorable way to describe the philosophy of personalizing AI-generated output.

## Raw Content

With Thanksgiving just around the corner, I wanted to do something a little different. Instead of interviewing a guest, I'm taking you into my own kitchen — and my own code editor — to show you how I use AI to solve real, everyday problems. Hosting a big holiday meal can be chaotic, from tracking who's coming and what they can eat, to coordinating dishes and trying to follow a recipe with flour-dusted hands. My solution was to build a personalized Thanksgiving party hub.

In this episode, I'm walking you through two of my favorite personal AI workflows. First, we'll build a complete party planning app from scratch using Lovable. I'll show you how to go from a generic, AI-generated starting point to what I like to call "farm-to-table software" — something that feels warm, personal, and artisanally crafted. We'll use Google Fonts to improve the typography and Midjourney to create beautiful, custom visuals that generic apps just can't match.

Then, for the second workflow, I'm sharing a kitchen hack I swear by. I'll show you my simple prompt for turning any cluttered online recipe into a perfectly formatted, step-by-step guide using ChatGPT. It's a trick I use all the time, especially when cooking with my kids, and it's a perfect example of how AI can bring a little more ease and joy into our daily lives.

### Workflow 1: Vibe Coding a 'Farm-to-Table' Thanksgiving Party Hub

**Goal**: Create a central place for Thanksgiving festivities — a hub for managing invites, coordinating potluck dishes, sharing recipes, and creating a photo gallery. Something more personal than a standard e-vite.

**Step 1: The Initial Prompt in Lovable**
Started with a simple, direct prompt outlining core features needed for a holiday gathering. The result was functional but bland — boring stock photo, clunky layout, no personality. Classic AI-generated slop.

**Step 2: Upleveling Typography with Google Fonts**
One of the fastest ways to improve any design. Used Canva's Font Combinations page for inspiration. Chose a cozy, handwritten feel:
- Headline Font: Homemade Apple
- Body Font: Railway

Simple instruction to Lovable to use Google Fonts with those choices. Instantly changed the feel — warmer, more personal, unique. Lovable adds the Google Fonts API call, configures fonts in Tailwind CSS, and updates default CSS.

**Step 3: Designing a Custom Header with Midjourney**
Replaced the generic header image. Used Midjourney style references — browsed X for cool style codes from other creators. Found a whimsical paper-cutout style from Michael Ramone. Adapted for Thanksgiving theme: "geometric paper, autumnal harvest tablescape."

Hit a common issue: initial image was square but needed a wide banner. Fix: removed hardcoded aspect ratio and used Midjourney settings for wide 2:1 ratio.

Returned to Lovable with multi-part prompt: update header image, change title, personalize all copy.

**Step 4: Adding Custom Features for Real-Life Needs**
Family has mix of vegans, gluten-free, and dairy-free folks. Standard invite apps don't handle this well. Prompted Lovable to add dietary preferences as a multi-select (key term — checkboxes instead of text field). Lovable pre-populated with common restrictions.

Then connected restrictions to dish-coordination section — dietary restriction tags on dishes so everyone knows what they can eat. Created a custom data model connecting guests to dishes through dietary needs — would have taken hours manually, done in minutes.

### Workflow 2: The Ultimate AI Recipe Hack with ChatGPT

**The Problem**: Online recipes list ingredients at top and instructions at bottom, forcing scrolling up and down with messy hands.

**Step 1**: Copy entire recipe text from website (used Polenta and Sausage Stuffing recipe).

**Step 2**: Paste into ChatGPT with specific reformatting instructions:
- Title, Description, Cook time, Ingredients, Servings, Instructions
- Instructions clearly in numbered steps
- Both ingredients and measurements inline in each step (the key instruction)

**Step 3**: ChatGPT returned perfectly clean, structured recipe. Each step numbered with exact measurements embedded. E.g., instead of "add water and salt," it says "Bring 6 cups of water and 2 tsp salt to a boil."

Claire and her son productized this into a website called Runaway Pancakes with kid-friendly recipes in this format.

### Bringing It All Together

Going from a generic template to a fully customized, beautifully designed party hub shows how to use AI as a creative partner. The process: don't accept the first output — iterate with your own design taste using Google Fonts, create unique art with Midjourney, and add deeply personal features that solve specific problems. The recipe hack exemplifies using language models to reorganize information for our own brains.
