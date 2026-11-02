# Tests und Reproduzierbarkeit — Vagina / bisher vajayjay

## Voraussetzungen
CMake, C++17/MSVC und gepinnter vollständiger VST3-SDK-Checkout; siehe BUILD.md.

## Befehle
```text
ctest --test-dir <BUILD_DIRECTORY> -C Release --output-on-failure
```

Start/Build: Mit eigenem frischem Buildordner und -DVST3_SDK_ROOT konfigurieren; vollständiges VST3-Bundle in isoliertem Testhost laden. Keine Installation in DAW-Pluginordner ohne gezielten Auftrag.

## Tatsächlicher Befund vom 02.11.2026
Vagina 0.2.0 wurde neu unter Windows x64 kompiliert; 47 offizielle Validatorprüfungen und vier native Release-Suiten bestanden. Keine aktuelle DAW-Abnahme in dieser Runde. Frühere Linux-Belege sind versions-/umgebungsspezifisch.

Bei fehlenden Paketen/Hardware/Betriebssystemen ist das Ergebnis „nicht ausgeführt“, kein Pass. Plattformnachweise aus älteren Detailberichten gelten nur für die dort genannten Versionen. Android-Automatisierung ausschließlich mit expliziter emulator-Seriennummer und bestätigtem ro.kernel.qemu=1. Physische Geräte, persönliche Medien und Produktionskonten sind keine Testfixtures.

## Vor Merge
`git diff --check` ausführen; relevante Funktionstests wiederholen, wenn Codeänderungen ihren Befund entwerten. Speicherdaten/alte Versionen erhalten. Fehlende externe Abnahmen in HANDOFF.md benennen.
