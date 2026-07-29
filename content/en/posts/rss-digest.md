---
title: "RSS Digest & AI News Summary"
preview: false
date: 2026-03-15
order: 10
icon: "newspaper-outline"
category: "Automated AI Workflow"
status: "MVP"
status_note: "First functional version, already running in production and continuously being expanded."
github: "https://github.com/bkubinszky/rss-digest"
tags: ["Automation", "AI Workflow", "Python", "LLM", "API"]
description: "Fully automated workflow for collecting, filtering, analysing and creating AI-assisted summaries of relevant news from RSS sources"

problem:
  intro: "We spend far too much time filtering the news that matters to us from the constant flood of information. The aim of this project was to develop an autonomous system that aggregates a wide range of RSS feeds, evaluates their content based on predefined criteria and presents the most important insights in a structured format."
  points:
    - "No need for ongoing manual review of sources."
    - "Relevant information instead of information overload."
    - "More signal, less noise."
  quote_label: "Objective"
  quote: "Reduce daily research time while gaining deeper insights through LLM-assisted analysis. Focus on the most relevant articles instead of manually reviewing large volumes of information."

workflow:
  intro: "Implementation of a fully automated, modular news pipeline. The Python-based solution was built with Claude Code and follows various security best practices to ensure that sensitive data, credentials, personal preferences, etc. are not exposed. The script can be connected to any LLM API. I used Gemini as the primary model and Groq as a fallback, both on their free tiers."
  steps:
    - label: "Step 1: Configuration"
      title: "Define the RSS feed list & personal interests"
    - label: "Step 2: Fetching"
      title: "Scheduled feed retrieval using GitHub Actions & Cron"
    - label: "Step 3: Analysis"
      title: "AI-assisted filtering and scoring of articles"
    - label: "Step 4: Summary (optional)"
      title: "AI-assisted summarisation"
    - label: "Step 5: Compilation"
      title: "Email delivery of the results"

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
    text: "Breaking monolithic code into modules early pays off when changes are needed later."
  - title: "Git"
    text: "Clean branching saves a lot of effort, even in small projects."
  - title: "Mock Mode"
    text: "Even the most generous free tier is quickly exhausted during testing, so it is worth working with a mock mode from the start."
  - title: "Security"
    text: "A security audit by a second LLM at the end was surprisingly valuable and uncovered genuine issues."
  - title: "Value"
    text: "Less is more: v4 without summaries is faster, cheaper and, in most cases, just as useful as v3 with summaries."

screenshots:
  - "/images/rss-digest/RSS_scrsht1.jpg"

future_ideas:
  - title: "Keyword watchlist"
    text: "Specific terms such as a company, technology or person automatically boost the score. Useful when you want to follow particular topics closely."
  - title: "Blacklist"
    text: "Set up hard filters for specific topics using a blacklist."
  - title: "Newsletter Integration"
    text: "Expand the data sources beyond RSS feeds by adding newsletters, for example via Kill the Newsletter."
  - title: "Personalised Scoring"
    text: "Instead of using one global interest profile, different weightings could be defined for each feed."
  - title: "Feedback Loop"
    text: "Simple like and dislike buttons for each article in the email could store a score in a local file. Over time, the system would learn the user's preferences."
  - title: "Additional Output Channels"
    text: "Telegram, WhatsApp, Slack, Teams and similar platforms instead of email delivery."
  - title: "Local AI"
    text: "The LLM APIs could be replaced with a locally hosted AI model."
---
