# Agentenleitfaden — Vagina / bisher vajayjay

## Einstieg
VST3-Visualizer mit unverändertem Audio-Passthrough. Auf diesem Feature-Branch ist Vagina 0.2.0 für Windows neu gebaut und validiert; bisherige öffentliche Releases heißen weiterhin vajayjay.

Lies README.md, TESTING.md und HANDOFF.md. Anforderungen und vorhandene Funktionen unterscheiden. Technische Grundlagen: BUILD.md. Die bestehenden Detaildokumente bleiben maßgeblich; keine leeren SPEC-/ARCHITECTURE-/TODO-Kopien erzeugen. Offene Arbeit und Verlauf: PROGRESS.md; konkrete Einnahmegrenzen: MONETIZATION.md, soweit vorhanden.

## Umgebung und Start
CMake, C++17/MSVC und gepinnter vollständiger VST3-SDK-Checkout; siehe BUILD.md.

Mit eigenem frischem Buildordner und -DVST3_SDK_ROOT konfigurieren; vollständiges VST3-Bundle in isoliertem Testhost laden. Keine Installation in DAW-Pluginordner ohne gezielten Auftrag.

Tests: `ctest --test-dir <BUILD_DIRECTORY> -C Release --output-on-failure`. Bei mehreren Befehlen einzeln ausführen und jeden Exitcode prüfen. Vorhandene Installationen verwenden; fehlende Voraussetzungen melden statt automatisch globale Pakete oder Modelle zu installieren.

## Grenzen
- Größere Änderungen auf einem eigenen Branch; zuerst git status und fremde Änderungen prüfen. Keine parallelen widersprüchlichen Arbeiten am selben Branch.
- Keine Dateien/Repos löschen oder verschieben, keine Historien umschreiben, kein Force-Push. Keine Lizenzänderungen ohne konkrete Freigabe.
- Keine Secrets, privaten Daten, echten Nutzerinhalte oder großen generierten Dateien committen. Keine Sichtbarkeitsänderungen oder zusätzlichen Veröffentlichungen ohne Freigabe.
- Keine bezahlten Dienste, Werbenetzwerke, Zahlungsanbieter oder externe Nachrichten aktivieren.
- Source/Ids.h, Parameter-IDs, Zustand, vorhandene Lizenzen und Drittanbieterhinweise erhalten. SDK-/JSONchecker-Distributionsgrenzen prüfen.
- Projektwerkzeuge ändern keine anderen Projektquellen. Build-/Testartefakte in isolierten, ignorierten Arbeitsordnern halten. Vorhandene Ausgaben nicht unbesehen überschreiben.

## Nächste sichere Etappe
Umbenennung zu Vagina ist auf dem Feature-Branch umgesetzt: 47 Validatorprüfungen und vier native Windows-Suiten bestanden. Nächste Abnahme: neue Binary in einer isolierten DAW prüfen. AU/CLAP sind nicht implementiert.

## Übergabe
HANDOFF.md aktualisieren: Ausgangscommit/Branch, konkrete Änderungsliste, ausgeführte Befehle, Ergebnis, ausgelassene Tests samt Grund, Risiken und nächste Etappe. Nur tatsächlich ausgeführte Tests als bestanden ausweisen. Vor Merge Diff und Tests prüfen; externe Freigaben bleiben offen.
