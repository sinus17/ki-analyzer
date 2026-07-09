# 🔍 KI-Text-Analyzer

Stylometrische Analyse deutschsprachiger wissenschaftlicher Arbeiten auf typische LLM-Muster — komplett lokal im Browser, ohne Server, ohne Datenupload.

**Live-Demo:** https://sinus17.github.io/ki-analyzer/

## ⚠️ Wichtiger Hinweis

Kein Verfahren kann KI-generierten Text zuverlässig nachweisen — auch dieses nicht. Die Ergebnisse sind **Indizien, keine Beweise**. Falsch-Positive sind häufig, besonders bei formellem wissenschaftlichem Stil und Nicht-Muttersprachlern. Der Bericht ist ausschließlich als Ausgangspunkt für ein Gespräch mit dem/der Studierenden gedacht, nie als alleinige Grundlage für Konsequenzen.

## Features

- **Datei-Import:** PDF, DOCX und TXT per Drag & Drop oder Dateiauswahl, alternativ Text einfügen
- **Absatzweise Markierung:** verdächtige Passagen farblich hervorgehoben (gelb / orange / rot) mit Begründung
- **Phrasen-Highlighting:** typische LLM-Formulierungen werden direkt im Text unterstrichen
- **Auffälligkeits-Index:** Gesamtscore 0–100 mit Metrik-Übersicht
- **Befunde-Liste:** sortiert nach Score, klickbar zum Springen an die Textstelle
- **100 % lokal:** die Analyse läuft vollständig im Browser, es werden keine Daten übertragen

## Analysierte Signale

| Signal | Beschreibung |
|---|---|
| LLM-Phrasen | Typische Formulierungen wie „zusammenfassend lässt sich sagen", „spielt eine entscheidende Rolle", „in der heutigen digitalen Welt" |
| Floskel-Dichte | Häufung von Übergangsfloskeln („darüber hinaus", „des Weiteren", „zudem") |
| Paar-Konstruktionen | „sowohl … als auch", „nicht nur … sondern auch" |
| Satzlängen-Uniformität | LLM-Texte haben oft auffällig gleichförmige Satzlängen (geringe Burstiness) |
| Satzanfänge | Mehrfach identisch beginnende Sätze |
| Lexikalische Diversität | Geringe Wortvielfalt innerhalb eines Absatzes |

## Nutzung

Einfach `index.html` im Browser öffnen — keine Installation, kein Build-Schritt nötig.

Die einzigen externen Abhängigkeiten ([pdf.js](https://mozilla.github.io/pdf.js/) und [mammoth.js](https://github.com/mwilliamson/mammoth.js) für PDF-/DOCX-Extraktion) werden per CDN geladen; für reine Text-Analyse funktioniert das Tool auch offline.

## GitHub Pages aktivieren

Repo → **Settings** → **Pages** → Source: `main`-Branch, Ordner `/ (root)` → Save. Das Tool ist danach unter `https://sinus17.github.io/ki-analyzer/` erreichbar.

## Lizenz

MIT — siehe [LICENSE](LICENSE).
