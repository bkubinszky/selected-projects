---
title: "Product Idea Stress Tester"
preview: false
date: 2026-08-01
order: 1
icon: "git-branch-outline"
category: "Synchronous Agentic AI Workflow"
status: "MVP"
status_note: "Erste funktionierende Version, die bereits produktiv läuft und laufend erweitert wird."
github: "https://github.com/bkubinszky/product-idea-stress-tester"
tags: ["Python", "CrewAI", "Ollama", "Local LLM", "Multi-Agent AI", "Agentic Workflow", "Synchronous AI"]
description: "Ein lokaler synchroner agentischer KI-Workflow, der Produktideen mit spezialisierten Agenten kritisch prüft, zentrale Annahmen und Risiken identifiziert und gezielte Validierungsexperimente empfiehlt."

problem:
  intro: "Bei neuen Produkt- oder Geschäftsideen entsteht schnell der Impuls, direkt über Features und technische Umsetzung nachzudenken. Dabei bleiben zentrale Annahmen zu Problem, Zielgruppe, Nutzen oder tatsächlichem Bedarf oft ungeprüft. Ziel dieses Projekts war ein lokales KI-System, das Ideen strukturiert analysiert, kritisch hinterfragt und daraus konkrete nächste Validierungsschritte ableitet."
  points:
    - "Kritische Annahmen werden explizit sichtbar gemacht."
    - "Schwachstellen und unnötige Produktkomplexität werden früh hinterfragt."
    - "Validieren, bevor Zeit in die Entwicklung investiert wird."
  quote_label: "Zielsetzung"
  quote: "Produktideen nicht einfach von einer KI bewerten lassen, sondern mehrere spezialisierte Perspektiven gezielt aufeinander aufbauen lassen, um Risiken, Annahmen und sinnvolle Validierungsschritte früh sichtbar zu machen."

workflow:
  intro: "Die Anwendung basiert auf einem sequenziellen CrewAI-Workflow mit drei klar getrennten Rollen. Ein Product Strategist strukturiert zunächst die Idee und ihre wichtigsten Annahmen. Anschließend hinterfragt ein Skeptic diese Analyse gezielt, bevor ein Experiment Designer daraus möglichst einfache und kostengünstige Validierungsexperimente ableitet. Alle Agenten laufen vollständig lokal über Ollama und verwenden die Ergebnisse der vorherigen Schritte als Kontext. Die Ergebnisse werden validiert und anschließend als kompakter CLI-Report ausgegeben."
  steps:
    - label: "Schritt 1: Input"
      title: "Produkt- oder Geschäftsidee beschreiben"
    - label: "Schritt 2: Strategy"
      title: "Problem, Zielgruppe, Nutzen und zentrale Annahmen strukturieren"
    - label: "Schritt 3: Challenge"
      title: "Annahmen, Risiken und unnötige Komplexität kritisch hinterfragen"
    - label: "Schritt 4: Validation"
      title: "Schnelle und kostengünstige Validierungsexperimente entwickeln"
    - label: "Schritt 5: Report"
      title: "Ergebnisse zu einer strukturierten Gesamtbewertung zusammenführen"

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
  - title: "Agentenrollen"
    text: "Mehrere Agenten bringen nur dann einen echten Mehrwert, wenn ihre Rollen klar getrennt sind und sie gezielt auf den Ergebnissen der vorherigen Schritte aufbauen."
  - title: "Kritische Perspektive"
    text: "Der Skeptic ist besonders wertvoll, weil er nicht einfach eine zweite Analyse erstellt, sondern die Annahmen des Product Strategist gezielt angreift."
  - title: "Structured Outputs"
    text: "Strukturierte und validierte Outputs machen den Workflow deutlich zuverlässiger und ermöglichen eine konsistente Weiterverarbeitung der Agentenergebnisse."
  - title: "Lokale Modelle"
    text: "Auch ein kleines lokales Modell kann für klar abgegrenzte Agentenaufgaben brauchbare Ergebnisse liefern, wenn Prompts, Rollen und Ausgabeformat ausreichend präzise definiert sind."
  - title: "Scope"
    text: "Für den MVP reicht ein gut aufbereiteter CLI-Report vollständig aus. Eine zusätzliche Benutzeroberfläche hätte den Kernnutzen zunächst kaum verbessert."

screenshots:
  - "/images/product-idea-stress-tester/product-idea-stress-tester-cli.png"
  - "/images/product-idea-stress-tester/product-idea-stress-tester-cli-2.png"

future_ideas:
  - title: "Streamlit Interface"
    text: "Eine einfache grafische Oberfläche für Eingabe und Darstellung der Analyse, falls der CLI-Workflow später leichter zugänglich gemacht werden soll."
  - title: "Vergleichsmodus"
    text: "Mehrere Produktideen anhand derselben Kriterien analysieren und ihre wichtigsten Annahmen, Risiken und Validierungsaufwände gegenüberstellen."
  - title: "Bewertungsprofile"
    text: "Unterschiedliche Analyse-Schwerpunkte für digitale Produkte, Services, interne Tools oder neue Geschäftsmodelle definieren."
  - title: "Modellkonfiguration"
    text: "Lokale Modelle austauschbar machen, um Qualität, Geschwindigkeit und Ressourcenbedarf verschiedener Open-Weight-Modelle vergleichen zu können."
  - title: "Iterative Analyse"
    text: "Nach ersten Validierungsergebnissen eine bestehende Analyse erneut durchlaufen lassen und Annahmen, Risiken sowie MVP-Empfehlung entsprechend aktualisieren."
---