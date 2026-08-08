---
title: "Product Idea Stress Tester"
preview: false
date: 2026-08-01
order: 1
icon: "git-branch-outline"
category: "Synchronous Agentic AI Workflow"
status: "MVP"
status_note: "First functional version that already runs reliably and is continuously being expanded."
github: "https://github.com/bkubinszky/product-idea-stress-tester"
tags: ["Python", "CrewAI", "Ollama", "Local LLM", "Multi-Agent AI", "Agentic Workflow", "Synchronous AI"]
description: "A local synchronous agentic AI workflow that critically evaluates product ideas with specialized agents, identifies key assumptions and risks, and recommends targeted validation experiments."

problem:
  intro: "With new product or business ideas, there is often an immediate impulse to start thinking about features and technical implementation. At the same time, key assumptions about the problem, target users, value, or actual demand often remain untested. The goal of this project was to build a local AI system that analyzes ideas in a structured way, challenges them critically, and derives concrete next steps for validation."
  points:
    - "Critical assumptions are made explicitly visible."
    - "Weaknesses and unnecessary product complexity are challenged early."
    - "Validate before investing time in development."
  quote_label: "Objective"
  quote: "Rather than having a single AI simply evaluate a product idea, the goal is to let several specialized perspectives build on each other to reveal risks, assumptions, and meaningful validation steps early."

workflow:
  intro: "The application is based on a sequential CrewAI workflow with three clearly separated roles. A Product Strategist first structures the idea and its most important assumptions. A Skeptic then deliberately challenges this analysis before an Experiment Designer derives the simplest and most cost-effective validation experiments possible. All agents run fully locally via Ollama and use the outputs of previous steps as context. The results are validated and then presented as a compact CLI report."
  steps:
    - label: "Step 1: Input"
      title: "Describe the product or business idea"
    - label: "Step 2: Strategy"
      title: "Structure the problem, target users, value, and key assumptions"
    - label: "Step 3: Challenge"
      title: "Critically challenge assumptions, risks, and unnecessary complexity"
    - label: "Step 4: Validation"
      title: "Design fast and cost-effective validation experiments"
    - label: "Step 5: Report"
      title: "Combine the results into a structured overall assessment"

stack:
  - "Python"
  - "CrewAI"
  - "Ollama"
  - "Qwen3"
  - "Local LLM"
  - "uv"
  - "Git"
  - "GitHub"
  - "Markdown"

learnings:
  - title: "Agent Roles"
    text: "Multiple agents only provide real value when their responsibilities are clearly separated and they deliberately build on the results of previous steps."
  - title: "Critical Perspective"
    text: "The Skeptic is particularly valuable because it does not simply produce a second analysis, but specifically challenges the assumptions made by the Product Strategist."
  - title: "Structured Outputs"
    text: "Structured and validated outputs make the workflow significantly more reliable and enable consistent processing of the agents' results."
  - title: "Local Models"
    text: "Even a small local model can produce useful results for clearly defined agent tasks when prompts, roles, and output formats are sufficiently precise."
  - title: "Scope"
    text: "For the MVP, a well-designed CLI report is entirely sufficient. An additional user interface would initially have added little value to the core functionality."

screenshots:
  - "/images/product-idea-stress-tester/product-idea-stress-tester-cli.png"
  - "/images/product-idea-stress-tester/product-idea-stress-tester-cli-2.png"

future_ideas:
  - title: "Streamlit Interface"
    text: "A simple graphical interface for entering ideas and displaying the analysis if the CLI workflow should later become more accessible."
  - title: "Comparison Mode"
    text: "Analyze multiple product ideas using the same criteria and compare their key assumptions, risks, and validation effort."
  - title: "Evaluation Profiles"
    text: "Define different analysis focuses for digital products, services, internal tools, or new business models."
  - title: "Model Configuration"
    text: "Make local models interchangeable to compare the quality, speed, and resource requirements of different open-weight models."
  - title: "Iterative Analysis"
    text: "Run an existing analysis again after initial validation results and update assumptions, risks, and MVP recommendations accordingly."
---