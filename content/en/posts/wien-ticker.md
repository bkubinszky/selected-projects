---
title: "Wien Ticker"
preview: false
date: 2025-11-15
order: 20
icon: "bus-outline"
category: "Real-Time Open Data Application"
status: "WPT"
status_note: "Working Prototype: the first functional version of a product."
github: "https://github.com/bkubinszky/wien-ticker"
tags: ["Open Data", "Python", "Https", "LLM", "API"]
description: "Desktop widget for real-time monitoring of Vienna's public transport network"

problem:
  intro: "Many people use the same stops regularly and have to open an app or visit a website to check the next departure. Wien Ticker solves this by continuously displaying the relevant real-time Wiener Linien departures in a compact desktop widget, making them available at a glance at any time."
  points:
  
  quote_label: "Objective"
  quote: "Provision of a simple desktop application for continuously displaying personalised real-time departure information from Wiener Linien."

workflow:
  intro: "Development of a lightweight desktop application for displaying real-time departure information from Wiener Linien. The Python-based solution accesses current transport data through the Wiener Linien open data interface and displays it in a permanently available desktop widget. Users can configure individual stops and lines so that only the connections relevant to them are shown. Particular attention was paid to ease of use, robust error handling and resource-efficient background operation.<br><br>The result is a working prototype with basic functionality and a deliberately limited focus on UI/UX. Further details are available in the public GitHub repository."
  steps:
    - label: "Step 1: Configuration"
      title: "Selection of stops and optional line filters through the user interface"
    - label: "Step 2: Data Retrieval"
      title: "Retrieval of real-time departure data through the Wiener Linien Open Data API"
    - label: "Step 3: Processing"
      title: "Filtering, preparation and prioritisation of relevant departures"
    - label: "Step 4: Display"
      title: "Display of upcoming departures in a compact desktop widget"
    - label: "Step 5: Updates"
      title: "Regular automatic background updates of the data"

stack:
  - "OpenAI"
  - "Python"
  - "PyInstaller"
  - "WL Open Data API"
  - "JSON"
  - "CSV"
  - "HTTPS"
  - "Logging"
  - "Threading"

learnings:
  - title: "Data Processing"
    text: "Public APIs rarely provide data in a format that is immediately suitable for end users. A significant part of the work involved processing, filtering and presenting the data in a user-friendly way."
  - title: "Vibe Coding"
    text: "Development with AI-assisted coding tools, OpenAI in this case, speeds up implementation considerably but still requires human oversight for architectural decisions, debugging and quality assurance."
  - title: "Usability"
    text: "Usability often comes down to many small details. Features such as station search, line filters, automatic updates, system tray integration and UI/UX have a greater impact on practical value than the data retrieval itself."
  - title: "Architecture"
    text: "Even simple prototypes benefit from a modular architecture, as it makes extensions and maintenance considerably easier. This is especially true for vibe coding."

screenshots:
  - "/images/wien-ticker/WT_scrsht1.png"
  - "/images/wien-ticker/WT_scrsht2.png.png"
  - "/images/wien-ticker/WT_scrsht3.jpg"

future_ideas:
  - title: "Caching"
    text: "Local caching to reduce API requests."
  - title: "Installer"
    text: "Packaging and installer for Windows."
  - title: "Notifications"
    text: "Custom notifications for delays or service disruptions."
  - title: "Additional Transport Modes"
    text: "Integration of additional transport modes such as ÖBB, Badner Bahn, sharing services and others."
---