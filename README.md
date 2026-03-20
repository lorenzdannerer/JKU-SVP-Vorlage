# Download
Das gesamte Verzeichnis lässt sich bei Code -> Download ZIP herunterladen und in z.B. Overleaf importieren.

Die Ordner und Dateien namens "Protokoll+<Nr>" dürfen beliebig umbenannt werden, alle weiteren Dateien/Ordner sollten ihren orignalen Namen behalten.

# Updates
Die Vorlage wird laufend erweitert. Die Versionsnummer gibt dabei Auskunft über die Größe des Updates im sinne der geänderten Dateien.
Ändert sich die vorderste Ziffer der Version, wird eine Neuistallation der gesamten Vorlage empfohlen, weil sich Dateistrukturen und Inhalte geändert haben.
Ändert sich die zweite Ziffer von links, genügt ein Update der JKU_SVP.sty und Einstellungen.tex.
Ändert sich nur die dritte Ziffer, genügt eine Update der JKU_SVP.sty.

# Funktionen
## Bilder einfügen


```
\bild[
      caption=,
      label={},
      width=,
]{<Dateiname>}
```


caption... Gibt den Text in der Bildbeschriftung hinter "Abbildung x: ..." an. Werden Komma verwendet, ist der gesamte Text in geschwungene Klammern {} zu setzen.
label... Darf frei gewählt werden und dient zum späteren Referenzieren des Bildes mit \ref{<label>}
width... Gibt die Breite des Bildes an (Einheit dazuschreiben, z.b. width=3cm, width=0.5\textwidth [50% der Textbreite], ...) Standardmäßig auf 0.7\textwidth gesetzt, muss also nicht jedes Mal angegeben werden.
<Dateiname>... gib den Dateinamen zu der Datei im Grafikordner an. Der Pfad muss standardmäßig nicht angegeben werden. Es werden diverse Bildformate sowie .pdf unterstützt.

## Galerie
Mit der Galerie lassen sich schnell Bilder nebenander einfügen. Dabei kann man zwischen einer gesamten Bildbeschriftung oder für jedes Bild eine seperate Beschriftung wählen. Zudem können die Bilder mit einer kleinen weißen Box in der oberen linken Ecke versehen werden, welche automatisch alphabetisch/numerisch durchzählt.

... tbc ...
