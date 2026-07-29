---
title: "Career Profile Repository"
preview: true
date: 2026-05-01
order: 40
icon: "document-text-outline"
category: "Automated AI Workflow"
status: "MVP"
status_note: "First working version, already running in production and being extended continuously."
github: "https://github.com/bkubinszky/rss-digest"
tags: ["JSON", "Markdown", "LLM-ready"]
description: "Structured storage of career milestones in LLM-optimized formats"

problem:
  intro: "We spend far too much time filtering the flood of information down to what's actually relevant to us. The goal of this project was to build an autonomous system that aggregates a large number of RSS feeds, evaluates the content against predefined criteria, and structures the most important findings."
  points:
    - "No more ongoing manual review of sources."
    - "Only relevant information instead of information overload."
    - "More signal, less noise."
  quote_label: "Objective"
  quote: "Reducing daily research time while increasing the depth of information through LLM-supported analysis. Focus on the most relevant articles instead of manually reviewing large amounts of information."

workflow:
  intro: "Implementation of a fully automated, modular news pipeline. The Python-based solution was built with Claude Code following various security best practices, so that sensitive data, credentials, personal preferences and so on are never published. The script can be connected to any LLM API. I used Gemini as the base and Groq as a fallback, both on their free tiers."
  steps:
    - label: "Step 1: Configuration"
      title: "Define the RSS feed list and personal interests"
    - label: "Step 2: Fetching"
      title: "Reading the feeds via GitHub Actions and Cron"
    - label: "Step 3: Analysis"
      title: "AI-supported filtering and scoring of articles"
    - label: "Step 4: Summary (optional)"
      title: "AI-generated summary"
    - label: "Step 5: Compilation"
      title: "Email with the output"

stack:
  - "Claude"
  - "Python"
  - "GitHub Actions"
  - "GitHub Cron"
  - "GitHub Secrets"
  - "HTML/CSS"
  - "Groq API"
  - "Gemini API"
  - "Markdown"

learnings:
  - title: "Architecture"
    text: "Splitting monolithic code into modules early on pays off once changes come later."
  - title: "Git"
    text: "Clean branching even on small projects saves a lot of trouble."
  - title: "Mock Mode"
    text: "Even the most generous free tier runs out quickly during testing, so it's worth working with a mock mode from the start."
  - title: "Security"
    text: "A security audit by a second LLM at the end turned out to be surprisingly valuable and surfaced real findings."
  - title: "Value"
    text: "Less is more: v4 without summaries is faster, cheaper, and in most cases just as useful as v3 with summaries."

screenshots:
  - "/images/rss-digest/RSS_scrsht1.jpg"

future_ideas:
  - title: "Keyword watchlist"
    text: "Certain terms (company name, technology, person) automatically boost the score. Useful when you want to closely follow specific topics."
  - title: "Blacklist"
    text: "Set up a hard filter for certain topics through a blacklist."
  - title: "Newsletter integration"
    text: "Add newsletters as a data source alongside RSS feeds (e.g. via Kill-the-Newsletter)."
  - title: "Personalized scoring"
    text: "Instead of one global interest profile, different weightings could be set per feed."
  - title: "Feedback loop"
    text: "Simple like/dislike buttons per article in the email, storing a score in a local file. Over time the system learns your own preferences."
  - title: "Other output channels"
    text: "Telegram, WhatsApp, Slack, Teams and similar, instead of sending by email."
  - title: "Local AI"
    text: "LLM APIs could be replaced with a local AI."
---