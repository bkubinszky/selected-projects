---
title: "Uptime Monitor"
preview: false
date: 2026-07-27
order: 11
icon: "telescope-outline"
category: "Website Uptime Monitoring"
status: "WPT"
status_note: "Working Prototype: das erste funktionstüchtige Modell eines Produkts."
github: "https://github.com/bkubinszky/uptime-monitoring"
tags: ["GitHub Actions", "GitHub Secrets", "Python", "SMTP", "HTML", "CSS"]
description: "Ein kleines Python-Projekt zur Überwachung der Verfügbarkeit von Websites über GitHub Actions und zum Versenden von E-Mail-Benachrichtigungen, falls eine Website ausfällt."

problem:
  intro: "Websites und Services können jederzeit ausfallen, oft unbemerkt, bis Nutzer selbst darauf stoßen. Ohne eigene Serverinfrastruktur oder kostenpflichtige Monitoring-Dienste bleibt ein Ausfall häufig längere Zeit unentdeckt. Der Uptime Monitor löst dieses Problem durch eine serverlose, kostenfreie Lösung, die ausschließlich auf bestehender GitHub-Infrastruktur läuft und automatisiert per E-Mail informiert, sobald ein überwachter Dienst nicht mehr erreichbar ist."
  points:
  
  quote_label: "Zielsetzung"
  quote: "Entwicklung eines kostenlosen, wartungsarmen Systems zur automatisierten Überwachung mehrerer Websites mit Benachrichtigung bei Ausfällen. Obwohl es viele Online Dienste gibt, die ein uptime monitoring anbieten (auch mit free tier bis zu einer begrenzten Größenordnung), z.B. https://uptimerobot.com, war es mein Ziel, die Problemstellung ohne ein 3rd-party Tool zu lösen."

workflow:
  intro: Entwicklung eines schlanken, serverlosen Monitoring-Tools auf Basis von Python und GitHub Actions. Die Lösung prüft in konfigurierbaren Intervallen den Status mehrerer Websites und versendet bei einem erkannten Ausfall automatisch eine übersichtliche HTML-E-Mail mit Statusübersicht. Sämtliche Konfiguration, von der zu überwachenden Website-Liste bis zu den E-Mail-Zugangsdaten, wird sicher über GitHub Secrets verwaltet, ohne dass sensible Daten im Code oder Repository sichtbar sind. Besonderes Augenmerk lag auf einer robusten Fehlerbehandlung, sicherer Konfigurationsverwaltung und einer klar strukturierten, gut lesbaren Benachrichtigungs-E-Mail.
  steps:
    - label: "Schritt 1: Konfiguration"
      title: "Hinterlegen der zu überwachenden Websites sowie der E-Mail-Zugangsdaten als GitHub Secrets"
    - label: "Schritt 2: Zeitgesteuerte Ausführung"
      title: "Automatischer Start des Prüflaufs über einen Cron-Zeitplan in GitHub Actions"
    - label: "Schritt 3: Statusprüfung"
      title: "Abfrage jeder hinterlegten Website und Auswertung des HTTP-Statuscodes"
    - label: "Schritt 4: Aufbereitung"
      title: "Zusammenstellung der Ergebnisse in einer übersichtlichen HTML-Tabelle mit Statusanzeige je Website"
    - label: "Schritt 5: Benachrichtigung"
      title: "Versand einer E-Mail ausschließlich bei erkanntem Ausfall, inklusive Zeitstempel und Link zum Repository"

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
  - title: "Konfiguration ohne Code"
    text: "Die konsequente Trennung von Code und Konfiguration über GitHub Secrets ermöglicht Anpassungen (Website-Liste, Intervall, Empfänger) ohne jeden Eingriff in den Quellcode."
  - title: "Iterative Fehlerbehebung"
    text: "Fehler wie eingebettete Zeilenumbrüche in Secrets oder E-Mail-Header-Probleme zeigten, wie wichtig defensives Parsing und Bereinigung von Eingabedaten ist, auch bei scheinbar einfachen Skripten."
  - title: "Sicherheitsbewusstsein"
    text: "Ein externes Security-Audit deckte auf, dass auch kleine Tools von grundlegenden Sicherheitsprinzipien profitieren, etwa korrektes URL-Parsing, HTML-Escaping und explizite TLS-Zertifikatsprüfung."
  - title: "Serverlose Architektur"
    text: "GitHub Actions eignet sich auch für wiederkehrende Hintergrundaufgaben abseits von CI/CD, wodurch für private Projekte dieser Größenordnung keine eigene Serverinfrastruktur nötig ist."

screenshots:
  - "/images/uptime-monitor/uptime_mail.jpg"

future_ideas:
  - title: "Statuswechsel-Logik"
    text: "Benachrichtigung nur bei Statusänderung (up→down, down→up) statt bei jedem Prüflauf während eines andauernden Ausfalls."
  - title: "Alternative Benachrichtigungskanäle"
    text: "Integration von Slack- oder Discord-Webhooks als Alternative oder Ergänzung zur E-Mail-Benachrichtigung."
  - title: "Erweiterte Statuslogik"
    text: "Berücksichtigung von Antwortzeiten und historischer Verfügbarkeit, nicht nur des reinen Erreichbarkeitsstatus."
  - title: "SSL-Zertifikatsprüfung"
    text: "Warnung, wenn das SSL-Zertifikat einer überwachten Website in Kürze abläuft, ein häufiger, leicht vermeidbarer Ausfallgrund."
  - title: "Verlaufsprotokoll"
    text: "Einfaches Logging der Prüfergebnisse in eine Datei oder ein GitHub-Issue, um über Zeit nachvollziehen zu können, wie oft und wann eine Website ausgefallen war."
  - title: "Individuelle Prüfintervalle pro Website"
    text: "Manche Seiten sind kritischer als andere, dafür könnten unterschiedliche Prüffrequenzen sinnvoll sein statt eines globalen Intervalls für alle."
---