# Download
Gehe zur [aktuellsten Version](https://github.com/lorenzdannerer/JKU-SVP-Vorlage/releases/latest) und lade unter "Assets" die .zip Datei herunter.
 
Diese ZIP kann dann in z.B. Overleaf importiert und benutzt werden.

# Updates
Die Vorlage wird laufend erweitert. Die Versionsnummer gibt dabei Auskunft über die Größe des Updates im Sinne der geänderten Dateien und Strukturen.
+ **1**.0.0 | Ändert sich die vorderste Ziffer der Version, wird eine Neuistallation der gesamten Vorlage empfohlen, weil sich Dateistrukturen und Inhalte geändert haben.
+ 1.**1**.0 | Ändert sich die zweite Ziffer von links, genügt ein Update der `JKU_SVP.sty` und `Einstellungen.tex`.
+ 1.1.**1** | Ändert sich nur die dritte Ziffer, genügt ein Update der `JKU_SVP.sty`.

# Allgemeine Hinweise
+ Die Ordner und Dateien namens "Protokoll+\<Nr\>" dürfen beliebig umbenannt werden, alle weiteren Dateien/Ordner sollten ihren orignalen Namen behalten.
+ Das gesamte Protokoll kann auch direkt im Hauptdokument geschrieben werden. Dann wird der Ordner "Kapitel" nicht benötigt und kann gelöscht werden.


# Funktionen
## Bilder einfügen


```TeX
\bild[
      caption=,
      label={},
      width=,
]{<Dateiname>}
```

`caption` Gibt den Text in der Bildbeschriftung hinter "Abbildung x: ..." an. Werden Komma verwendet, ist der gesamte Text in geschwungene Klammern {} zu setzen.

`label` Darf frei gewählt werden und dient zum späteren Referenzieren des Bildes mit \ref{<label>}

`width` Gibt die Breite des Bildes an (Einheit dazuschreiben, z.b. `width=3cm`, `width=0.5\textwidth` [50% der Textbreite], ...) Standardmäßig auf `0.7\textwidth` gesetzt, muss also nicht jedes Mal angegeben werden.

`options` hier lassen sich in geschwungenen Klammern die normalen `\includegraphics` Optionen einfügen. z.B. `options={angle=-90}` um das Bild um 90° zu drehen.

`<Dateiname>` gib den Dateinamen inkl. Endung zu der Datei im Grafikordner an. Der Pfad muss standardmäßig nicht angegeben werden. Es werden diverse Bildformate sowie .pdf unterstützt.

## Galerie
Mit der Galerie lassen sich schnell Bilder nebenander einfügen. Dabei kann man zwischen einer gesamten Bildbeschriftung oder für jedes Bild eine seperate Beschriftung wählen. Zudem können die Bilder mit einer kleinen weißen Box in der oberen linken Ecke versehen werden, welche automatisch alphabetisch/numerisch durchzählt.

```TeX
\begin{galerie}[
      cols=2,
      caption=,
      autolabel=A,
      label={}
]
      \bild[]{DATEI}
      \bild[]{DATEI}
      \bild[]{DATEI}
\end{galerie}
```
Der Bild-Befehl ist dabei gleich wie oben beschrieben zu verwenden, wobei es keinen Sinn macht, für die Bilder eine caption anzugeben, wenn die Galerie eine caption hat (Beschriftung aller Bilder gemeinsam).
Andersrum macht es keinen Sinn, in der Galerie eine caption anzugeben, wenn jedes Bild eine eigene Beschriftung haben soll.


`cols` gibt die Anzahl der horizontal zu plazierenden Bilder wieder. Wenn die Anzahl an eingefügten Bilder größer als `cols` ist, wird in die nächste Zeile umgebrochen und weitere Bilder platziert.

`caption` und `label` sind analog zum `\bild` Befehl zu verwenden.

`autolabel` wenn angegeben werden kleine weiße Boxen oben links in jedem Bild erstellt, welche durchnummeriert sind. Mögliche Werte: 
+ `A` für die Nummerierung A, B, C, …
+ `a` für die Nummerierung a, b, c, …
+ `1` für die Nummerierung 1, 2, 3, …

Es könne beliebig viele `\bild` Bilder hinzugefügt werden. Diese werden automatisch entsprechend den angegebenen Reihen ausgerichtet.

`cols=1` führt dazu, dass alle Bilder ubtereinander ausgerichtet werden.

--- tbc ---

