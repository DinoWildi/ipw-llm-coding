# Beispielcode für das IPW-Kolloquium "LLM-gestütztes Kodieren von Zeitungsartikeln" vom 1. Juli 2026

## Dokumente
- IPW_Kolloquium.pdf: Slide Deck der Präsentation
- llm_beispiel_basics.ipynb: Jupyter-Notebook für Grundlagen mit Ollama
- llm_beispiel_strukturiert.ipynb: Jupyter-Notebook für strukturierte Outputs (also JSON)
- requirements.txt: Nötige Python-Pakete (siehe "Installation" unten)

## Voraussetzungen
- Ollama
- Python & pip
- Packages: numpy, pandas, ollama + dependencies; path, re für Laden und Speichern von Daten; pydantic, typing für strukturierte Outputs
- Für grössere Modelle (~20B aufwärts) ohne Cloud-Funktion: Zugriff auf eine GPU (z. B. via Google Colab or [bwHPC](https://wiki.bwhpc.de/e/Registration/bwUniCluster))

## Installation und Software-Nutzung

### Ollama
Auf der [Ollama-Website](https://ollama.com/) den gewünschten Client herunterladen und den Installationsanweisungen folgen. Wenn Ollama installiert ist, sollte das Python-Package automatisch die relevante Ollama-Installation finden.

Ollama ist eine Software-Lösung, die die lokale Nutzung verschiedener offener LLM-Modelle erlaubt. Lokale Anwendung von Modellen verlangt keinen Account; für die Nutzung von Cloud-Modellen ist eine Anmeldung notwendig. Ein Gratis-Account ist für die meisten kleineren Anwendungen ausreichend. Die verfügbaren Modelle können auf der Ollama-Website durchsucht werden. Zur Installation eines Modells muss lediglich im Python-Code der Befehl "ollama.pull(modellname) genutzt werden (siehe llm_beispiel_basics.ipynb).


### Python
Zur Installation von Python: Auf der [Python-Download-Seite](https://www.python.org/downloads/) die gewünschte Version herunterladen. Python sollte automatisch auch pip (nötig zum Installieren von Paketen) mitinstallieren. Zur idealen Nutzung von Python ist auch eine Entwicklungsumgebung (IDE) notwendig. 
Ich benutze hierfür [Visual Studio Code](https://code.visualstudio.com/), das man auch für viele andere Programmiersprachen nutzen kann und das mit Erweiterungen sehr stark personalisiert werden kann. Die Jupyter-Erweiterung und die Python-Erweiterung sollten vorinstalliert sein; falls nicht, müssen sie zur Nutzung des Codes heruntergeladen werden. Ich empfehle, mindestens auch die Erweiterung "Data Wrangler" herunterzuladen. 

### Python-Pakete
Python-Pakete werden im Allgemeinen über die Kommandozeile ("Eingabeaufforderung") installiert. Ich nutze persönlich die Installation via pip mit dem Kommando "pip install [package]"; man kann aber Packages auch über das VSCode-Interface installieren. Für den Beispielcode empfehle ich, die "requirements.txt"-Datei herunterzuladen. In der Kommandozeile kann man dann mit dem Kommando "pip install -r requirements.txt" alle nötigen Packages auf einmal installieren. 
Es empfiehlt sich, für jedes Projekt ein "virtual environment" zu erstellen. Dies kann man in der CMD mit dem Befehl "python -m venv /dateipfad/und/name/des/environments machen. Pakete werden dann nur im spezifischen Environment installiert. Damit kann man Probleme mit verschiedenen Versionen erstellen, und neue Pakete in einem Projekt können nicht ein anderes Projekt stören. VSCode fragt normalerweise, welches der entdeckten Environments man nutzen will.
