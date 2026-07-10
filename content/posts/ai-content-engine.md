---
title: "AI Content Engine"
preview: true
order: 40
icon: "color-wand-outline"
category: "Automated AI Workflow"
status: "MVP"
status_note: "Erste funktionierende Version, die bereits produktiv läuft und laufend erweitert wird."
github: "https://github.com/bkubinszky/rss-digest"
tags: ["Content", "MarTech", "LLM", "API"]
description: "Skalierbare Marketing-Automation durch Integration von PIM-Systemen und Generative AI"

problem:
  intro: "Wir verbringen viel zu viel Zeit damit, für uns relevante Nachrichten aus der Flut an Informationen herauszufiltern. Ziel dieses Projekts war die Entwicklung eines autonomen Systems zur Aggregation einer Vielzahl von RSS-Feeds, zur inhaltlichen Bewertung anhand vordefinierter Kriterien sowie zur strukturierten Aufbereitung der wichtigsten Erkenntnisse."
  points:
    - "Laufende manuelle Sichtung der Quellen entfällt vollständig."
    - "Nur relevante Informationen statt Informationsüberlastung."
    - "More signal, less noise."
  quote_label: "Zielsetzung"
  quote: "Reduzierung der täglichen Recherchezeit bei gleichzeitiger Erhöhung der Informationstiefe durch LLM-gestützte Analyse. Fokus auf die relevantesten Artikel statt auf die manuelle Sichtung großer Informationsmengen."

workflow:
  intro: "Implementierung einer vollautomatischen, modularen News-Pipeline. Die Python-basierte Lösung wurde mit Claude Code unter Einhaltung verschiedener Security Best Practices aufgesetzt, so dass sensible Daten, Zugangsdaten, persönliche Präferenzen usw. nicht veröffentlicht werden. Das Script kann an jede beliebige LLM API angebunden werden. Ich habe Gemini als Basis und Groq als Fallback verwendet, beide im Free-Tier-Bereich."
  steps:
    - label: "Schritt 1: Configuration"
      title: "RSS Feedlist & persönliche Interessen definieren"
    - label: "Schritt 2: Fetching"
      title: "GitHub Actions & Cron gesteuertes Auslesen der Feeds"
    - label: "Schritt 3: Analysis"
      title: "KI-gestütztes Filtern und Bewerten der Artikel"
    - label: "Schritt 4: Summary (optional)"
      title: "KI-gestützte Zusammenfassung"
    - label: "Schritt 5: Compilation"
      title: "E-Mail mit Output"

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
  - title: "Architektur"
    text: "Monolithischen Code früh in Module aufteilen zahlt sich bei späteren Änderungen aus."
  - title: "Git"
    text: "Sauberes Branching auch bei kleinen Projekten spart viel Mühe."
  - title: "Mock Mode"
    text: "Auch das großzügigste Free Tier ist beim Testen schnell aufgebraucht, deshalb von Anfang an mit Mock Mode arbeiten."
  - title: "Security"
    text: "Ein Security Audit durch ein zweites LLM am Ende war überraschend wertvoll und hat echte Findings gebracht."
  - title: "Nutzen"
    text: "Weniger ist mehr: v4 ohne Summaries ist schneller, günstiger, und in den meisten Fällen genauso nützlich wie v3 mit Summaries."

screenshots:
  - "/images/rss-digest/RSS_scrsht1.jpg"

future_ideas:
  - title: "Keyword watchlist"
    text: "Bestimmte Begriffe (Firmenname, Technologie, Person) boosten den Score automatisch. Praktisch wenn man spezifische Themen eng verfolgen will."
  - title: "Blacklist"
    text: "Hard-Filter für bestimmte Themen per Blacklist einstellen."
  - title: "Newsletter Integration"
    text: "Datenquellen neben RSS-Kanälen mit Newslettern ergänzen (z.B. via Kill-the-Newsletter)."
  - title: "Personalisiertes Scoring"
    text: "Statt einem globalen Interesse-Profil könnte man pro Feed unterschiedliche Gewichtungen setzen."
  - title: "Feedback Loop"
    text: "Einfache Like/Dislike Buttons pro Artikel in der Mail, der einen Score in einer lokalen Datei speichert. Über Zeit lernt das System die eigenen Präferenzen."
  - title: "Weitere Output Kanäle"
    text: "Telegram, Whatsapp, Slack, Teams u.ä. anstatt E-Mail Versand."
  - title: "Lokale KI"
    text: "LLM-APIs könnten durch eine lokale KI ersetzt werden."
---