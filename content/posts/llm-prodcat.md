---
title: "LLM-lesbarer Produktkatalog für agentischen Handel"
date: 2025-09-15
icon: "cart-outline"
category: "Agentic Commerce"
status: "WT"
status_note: "Working Theory: vorläufige Annahme, das als Ausgangspunkt für weitere Untersuchungen dient."
github: 
tags: ["Produktdaten", "Agentic Commerce", "PIM", "LLM", "AEO"]
description: "Optimierung komplexer Produktdaten für Agentic Commerce Architekturen"

problem:
  intro: "Viele Produktdaten sind primär für Menschen und klassische Webshops optimiert. KI-Anwendungen, LLMs und autonome Agenten benötigen jedoch strukturierte, semantisch angereicherte Informationen, um Produkte zuverlässig finden, vergleichen und empfehlen zu können."
  points:
  
  quote_label: "Zielsetzung"
  quote: "Entwicklung einer Applikation das bestehende Legacy-Produktkataloge maschinenlesbar macht, indem die Produktinformationen in eine für LLMs und KI-Agenten optimierte Struktur umwandelt, anreichert und bereitstellt."

workflow:
  intro: "Dieses Projekt ist derzeit in der Ideation Phase, wo ich ähnliche bestehende Lösungen recherchiere und kleinere Test bzgl. der Machbarkeit der Teilaufgaben durchführe. <br><br> <b>Working Theory:</b>Entwicklung eines prototypischen Produktkatalogs für ausgewählte Outdoor-Marken. Die Produktdaten werden aus unterschiedlichen Quellen aggregiert, normalisiert und um zusätzliche Metadaten ergänzt. Anschließend werden die Informationen in einer strukturierten JSON-Architektur gespeichert, die von LLMs, RAG-Systemen oder Agenten direkt verarbeitet werden kann."
  steps:
    - label: "Schritt 1: Normalisierung der Legacy-Datenbank"
      title: "Vereinheitlichung von Kategorien, Attributen und Datenstrukturen"
    - label: "Schritt 2: Datenerfassung"
      title: "Sammlung von Produktinformationen aus Hersteller-, Händler- und sonstigen Quellen"
    - label: "Schritt 3: Anreicherung"
      title: "Ergänzung semantischer Metadaten, Produktmerkmale und Klassifizierungen"
    - label: "Schritt 4: Strukturierung"
      title: "Speicherung der Daten in einem LLM-freundlichen JSON-Schema"
    - label: "Schritt 5: Nutzung"
      title: "Bereitstellung für KI-Anwendungen, Produktsuche, Empfehlungen oder agentische Workflows"

stack:
  - "OpenAI"
  - "Python"
  - "JSON"
  - "CSV"
  - "LLM"
  - "Markdown"
  - "..."

learnings:
  - title: "Ideation Phase"
    text: "Dieses Projekt ist derzeit in der Ideation Phase und es kommen laufend neue Learnings hinzu!"
  - title: "Datenqualität"
    text: "Strukturierte Daten sind eine zentrale Voraussetzung für zuverlässige KI-Anwendungen. Die Qualität von Produktempfehlungen hängt stark von der semantischen Modellierung der Daten ab."
  - title: "SEO + AEO"
    text: "Klassische E-Commerce-Daten sind häufig nicht für KI-Anwendungsfälle optimiert. Der bisherige Fokus lag an SEO um Kunden erreichen zu können. Mit dem wachsenden Anteil des agentischen Handels im e-Commerce ist das nicht mehr ausreichend, es braucht zusätzliche AEO-Maßnahmen."

screenshots:
 

future_ideas:
  - title: "Ideation Phase"
    text: "Dieses Projekt ist derzeit in der Ideation Phase und es kommen laufend neue potentielle Erweiterungsideen hinzu!"
  - title: "Produktdaten als API-Service"
    text: "Bereitstellung der strukturierten Produktdaten über standardisierte APIs oder MCP-Endpunkte, damit externe Anwendungen direkt darauf zugreifen können."
  - title: "Lokale Installation"
    text: "Anbindung an Shop-Systeme und PIM-Lösungen."
  - title: "Conversational Commerce"
    text: "Anbindung an Chatbots und KI-Assistenten, die Produkte nicht nur finden, sondern auch vergleichen, empfehlen und Kaufentscheidungen unterstützen können."
  - title: "Automatische Datenanreicherung"
    text: "Ergänzung von Produktdaten durch KI."
---