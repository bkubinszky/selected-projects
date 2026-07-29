---
title: "Uptime Monitor"
preview: false
date: 2026-07-27
order: 11
icon: "telescope-outline"
category: "Website Uptime Monitoring"
status: "WPT"
status_note: "Working Prototype: the first functional model of a product."
github: "https://github.com/bkubinszky/uptime-monitoring"
tags: ["GitHub Actions", "GitHub Secrets", "Python", "SMTP", "HTML", "CSS"]
description: "A Python project for free, serverless monitoring of website availability"

problem:
  intro: "Websites and services can go offline at any time, often without anyone noticing until users encounter the issue themselves. Without dedicated server infrastructure or paid monitoring services, an outage can remain undetected for an extended period. The Uptime Monitor solves this problem with a free, serverless solution that runs entirely on existing GitHub infrastructure and automatically sends an email as soon as a monitored service becomes unavailable."
  points:
  
  quote_label: "Objective"
  quote: "Development of a free, low-maintenance system for automatically monitoring multiple websites and sending notifications when outages occur. Although many online services offer uptime monitoring, including free tiers for a limited number of websites, such as https://uptimerobot.com, my goal was to solve the problem without relying on a third-party tool."

workflow:
  intro: Development of a lightweight, serverless monitoring tool based on Python and GitHub Actions. The solution checks the status of multiple websites at configurable intervals and automatically sends a clear HTML email with a status overview when an outage is detected. All configuration, from the list of monitored websites to the email credentials, is managed securely through GitHub Secrets, so sensitive data is never visible in the code or repository. Particular attention was given to robust error handling, secure configuration management and a clearly structured, easy-to-read notification email.
  steps:
    - label: "Step 1: Configuration"
      title: "Store the websites to be monitored and the email credentials as GitHub Secrets"
    - label: "Step 2: Scheduled execution"
      title: "Automatically start each check through a cron schedule in GitHub Actions"
    - label: "Step 3: Status check"
      title: "Request each configured website and evaluate its HTTP status code"
    - label: "Step 4: Formatting"
      title: "Compile the results in a clear HTML table showing the status of each website"
    - label: "Step 5: Notification"
      title: "Send an email only when an outage is detected, including a timestamp and a link to the repository"

stack:
  - "Claude"
  - "Vibe (Mistral)"
  - "Python"
  - "GitHub Actions"
  - "GitHub Secrets"
  - "SMTP"
  - "HTML"
  - "CSS"
  - "Cron"
  - "Git"

learnings:
  - title: "Configuration Without Code"
    text: "Keeping code and configuration strictly separate through GitHub Secrets makes it possible to change the website list, interval or recipients without modifying the source code."
  - title: "Iterative Troubleshooting"
    text: "Issues such as embedded line breaks in secrets or email header errors showed how important defensive parsing and input sanitisation are, even in seemingly simple scripts."
  - title: "Security Awareness"
    text: "An external security audit showed that even small tools benefit from basic security principles, including correct URL parsing, HTML escaping and explicit TLS certificate verification."
  - title: "Serverless Architecture"
    text: "GitHub Actions is also suitable for recurring background tasks beyond CI/CD, which removes the need for dedicated server infrastructure for private projects of this scale."

screenshots:
  - "/images/uptime-monitor/uptime_mail.jpg"

future_ideas:
  - title: "Status Change Logic"
    text: "Send notifications only when the status changes (up→down, down→up), rather than after every check during an ongoing outage."
  - title: "Alternative Notification Channels"
    text: "Integrate Slack or Discord webhooks as an alternative or addition to email notifications."
  - title: "Extended Status Logic"
    text: "Include response times and historical availability rather than only checking whether a website is reachable."
  - title: "SSL Certificate Check"
    text: "Send a warning when the SSL certificate of a monitored website is about to expire, a common and easily preventable cause of outages."
  - title: "History Log"
    text: "Log check results in a file or GitHub issue to track how often and when a website has been unavailable over time."
  - title: "Individual Check Intervals per Website"
    text: "Some websites are more critical than others, so different check frequencies may be more useful than one global interval for all websites."
---