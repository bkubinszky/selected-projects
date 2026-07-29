---
title: "Wien Ticker"
preview: false
date: 2025-11-15
order: 20
icon: "bus-outline"
category: "Real-Time Open Data Application"
status: "WPT"
status_note: "Working Prototype: das erste funktionstüchtige Modell eines Produkts."
github: "https://github.com/bkubinszky/wien-ticker"
tags: ["Open Data", "Python", "Https", "LLM", "API"]
description: "Desktop-Widget zur Echtzeit-Überwachung des Wiener Nahverkehrs"

problem:
  intro: "Viele nutzen regelmäßig dieselben Haltestellen und müssen für die nächste Abfahrtszeit entweder eine App öffnen oder eine Website aufrufen. Wien-Ticker löst dieses Problem, indem die relevanten Echtzeit-Abfahrten der Wiener Linien dauerhaft in einem kompakten Desktop-Widget angezeigt werden und somit jederzeit auf einen Blick verfügbar sind."
  points:
  
  quote_label: "Zielsetzung"
  quote: "Bereitstellung einer einfachen Desktop-Anwendung zur kontinuierlichen Anzeige personalisierter Echtzeit-Abfahrtsinformationen der Wiener Linien."

workflow:
  intro: "Entwicklung einer schlanken Desktop-Anwendung zur Anzeige von Echtzeit-Abfahrtsinformationen der Wiener Linien. Die Python-basierte Lösung greift über die Open-Data-Schnittstelle der Wiener Linien auf aktuelle Verkehrsdaten zu und stellt diese in einem permanent verfügbaren Desktop-Widget dar. Nutzer:innen können individuelle Haltestellen und Linien konfigurieren, sodass nur die für sie relevanten Verbindungen angezeigt werden. Besonderes Augenmerk lag auf einer einfachen Bedienung, robuster Fehlerbehandlung und einer ressourcenschonenden Ausführung im Hintergrund.<br><br>Entstanden ist ein Working Prototyp mit Basisfunktionen und bewusst reduziertem UI/UX-Fokus. Details im Public GitHub Repository."
  steps:
    - label: "Schritt 1: Konfiguration"
      title: "Auswahl von Haltestellen und optionalen Linienfiltern über die Benutzeroberfläche"
    - label: "Schritt 2: Datenabfrage"
      title: "Abruf der Echtzeit-Abfahrtsdaten über die Wiener-Linien-Open-Data-API"
    - label: "Schritt 3: Verarbeitung"
      title: "Filterung, Aufbereitung und Priorisierung der relevanten Abfahrten"
    - label: "Schritt 4: Darstellung"
      title: "Anzeige der nächsten Abfahrten in einem kompakten Desktop-Widget"
    - label: "Schritt 5: Aktualisierung"
      title: "Regelmäßige automatische Aktualisierung der Daten im Hintergrund"

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
  - title: "Datenaufbereitung"
    text: "Öffentliche APIs liefern selten Daten in einer Form, die unmittelbar für Endanwender geeignet ist. Ein wesentlicher Teil der Arbeit bestand in der Aufbereitung, Filterung und nutzerfreundlichen Darstellung der Daten."
  - title: "Vibe-Coding"
    text: "Die Entwicklung mit KI-gestützten Coding-Tools (hier OpenAI) beschleunigt die Umsetzung erheblich, erfordert aber weiterhin menschliche Kontrolle bei Architekturentscheidungen, Debugging und Qualitätssicherung."
  - title: "Benutzerfreundlichkeit"
    text: "Benutzerfreundlichkeit entsteht oft durch viele kleine Details. Funktionen wie Stationssuche, Linienfilter, automatische Aktualisierung, System-Tray-Integration und UX/UI haben einen größeren Einfluss auf den praktischen Nutzen als die eigentliche Datenabfrage."
  - title: "Architektur"
    text: "Bereits einfache Prototypen profitieren von einer modularen Architektur, da Erweiterungen und Wartung dadurch deutlich erleichtert werden. Erst recht bei Vibe-Coding!"

screenshots:
  - "/images/wien-ticker/WT_scrsht1.png"
  - "/images/wien-ticker/WT_scrsht2.png.png"
  - "/images/wien-ticker/WT_scrsht3.jpg"

future_ideas:
  - title: "Caching"
    text: "Lokales Caching zur Reduktion von API-Anfragen."
  - title: "Installer"
    text: "Packaging und Installer für Windows."
  - title: "Notifications"
    text: "Individuelle Benachrichtigungen bei Verspätungen oder Betriebsstörungen."
  - title: "Weitere Verkehrsmittel"
    text: "Integration weiterer Verkehrsmittel (ÖBB, Badner Bahn, Sharing-Angebote, usw.)."
---