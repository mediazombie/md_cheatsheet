# Markdown Cheat Sheet
Markdown ist eine einfache Möglichkeit, Text mit Klartextsymbolen zu schreiben und zu formatieren. Es ist eine leichte Sprache, mit der man schön formatierten Text ohne die Verwendung von komplexer Codierung erstellen können. Die Idee ist, es den Menschen leicht zu machen, die Formatierung zu lesen und zu verstehen, auch wenn sie den Rohtext betrachten.

Dieses Cheat Sheet wird einige der Schlüsselkomponenten des Markdowns durchgehen, einschließlich Code-Syntaxen und Beispiele, die der Leser verwenden kann, um einen eigenen hochformatierten Textartikel zu erstellen.

## Inhalt:


## Überschriften
| Element | Markdown Syntax |
| :---: | :---: |
| H1 | # H1 Überschrift |
| H2 | ## H2 Überschrift |
| H3 | ### H3 Überschrift |
| H4 | #### H4 Überschrift |
| H5 | ##### H5 Überschrift |
| H6 | ###### H6 Überschrift |

## Text Formatierung
Markdown ermöglicht es uns, viele Stile, wie Fett, Kursiv, Blockquotes, Unterstreichung, Durchstreichung, etc., auf eine ausgewählte Textauswahl anzuwenden.

| Element | Markdown Syntax |
| :---: | :---: |
| Fett | \*\*Text** oder \_\_Text__ |
| Kursiv | \*Text* oder \_Text_ |
| Zitat | \> Zitierter Text |
| Unterstrichen | \<u>Text\<u> |
| Durchgestrichen | \~~Text~~ |
| Hochgestellt | \<sup>Text\</sup> |
| Tiefgestellt | \<sub>Text\</sub> |

## Syntax Hervorhebung (Code)
Mit der Syntax-Hervorhebung in Markdown kann man Code-Snippets für eine bessere Lesbarkeit formatieren und hervorheben. Es ist besonders nützlich, wenn Code in technischen Dokumentationen oder Online-Foren geteilt wird.

| Element | Markdown Syntax | Ausgabe |
| :---: | :---: | :---: |
| Inline Code | \`int z=19;\` | `int z=19` |
| Mehrzeiliger Code | \``` int y=4; cout<<y<<endln; \``` | ```int y=4; cout<<y<<endln; ``` |

Mehrzeiliger Code kann für spezifische Hervorhebung auch eine Sprachangabe enthalten (z.B. \```php ...\``` oder \```shell ...\``` usw.).

## Tabellen
Markdown-Tabellen sind eine Möglichkeit, Daten in einem strukturierten Format in einem Markdown-Dokument zu organisieren. Sie bestehen aus Zeilen und Spalten, wobei jede Zelle Daten enthält. Tabellen in Markdown werden mit einer Kombination aus vertikalen Balken (|) und Bindestrichen (-) erstellt, um die Spalten bzw. Zeilen zu definieren. Die erste Zeile enthält typischerweise die Spaltenüberschriften, während nachfolgende Zeilen die Daten enthalten. Zum Beispiel:

```
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Data 1   | Data 2   | Data 3   |
| Data 4   | Data 5   | Data 6   |
```

Dies führt zu folgender Ausgabe:

| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Data 1   | Data 2   | Data 3   |
| Data 4   | Data 5   | Data 6   |

In Markdown kann man die Werte der Spalten einer Tabelle nach links, rechts oder mittig mit den Symbolen :---, ---: bzw. :---: ausrichten. Dies geschieht, indem diese Symbole zwischen den vertikalen Balken (|) in der Kopfzeile der Tabelle platziert werden.

**Beispiel:**
```
| Left-aligned | Center-aligned | Right-aligned |
|:-------------|:--------------:|--------------:|
| Data 1       | Data 2         | Data 3        |
| Data 4       | Data 5         | Data 6        |
```

**Ausgabe:**

| Left-aligned | Center-aligned | Right-aligned |
|:---|:---:|---:|
| Data 1 | Data 2 | Data 3 |
| Data 4 | Data 5 | Data 6 |

Miitels dem HTML-tag `<br>` ist es auch möglich, in einer Tabellenzelle einen Zeilenumbruch zu erzeugen.

## Links
### Inline Links
Um "normale" Inline-Links zu erstellen, den Link-Text in eckige Klammern einschliessen (z.B. [Duck Duck Go]), gefolgt von der URL in runden Klammern (z.B. (https://duckduckgo.com)).
```
Meine bevorzugte Suchmaschine ist [Duck Duck Go](https://duckduckgo.com)
```
Dies führt zu folgender Ausgabe:
[Duck Duck Go](https://duckduckgo.com)

#### Beschreibung (Tooltipp) hinzufügen
Optional kann auch eine Beschreibung zum Link hinzugefügt werden. Diese erscheint dann beim hoovern über den Link als eine art Tooltipp. Um eine Beschreibung zu einem Link hinzuzufügen, den gewünschten Text in Anführungszeichen am Ende der URL anfügen.
```md
Meine bevorzugte Suchmaschine ist [Duck Duck Go](https://duckduckgo.com "Meine bevorzugte Suchmaschine!")
```
Dies führt dann zu folgender Ausgabe:  
[Duck Duck Go](https://duckduckgo.com "Meine bevorzugte Suchmaschine!")

### URLs und Email-Adressen
Meistens werden URLs automatisch als solche erkannt (je nach Editor oder verwendetem Tool). Möchte man diese explizit und rasch als solche Kennzeichnen können auch spitze Kalmmern verwendet werden.
```md
<https://duckduckgo.com>
<fake@beispiel.com>
```
Dies erzeugt folgende Ausgabe:  
<https://duckduckgo.com>  
<fake@beispiel.com>

### Links formatieren
Links können genau so wie [Text](#text-formatierung) formatiert werden (fett, kursiv, usw.).
```md
Ich mag **[EFF](https://eff.org)**.  
Das ist die Suchmaschine "Duck Duck Go": *[Duck Duck Go](https://duckduckgo.com)*
```
Das sieht dann so aus:  
Ich mag **[EFF](https://eff.org)**.  
Das ist die Suchmaschine "Duck Duck Go": *[Duck Duck Go](https://duckduckgo.com)*

### Fussnoten
Es können auch Fussnoten verwendet werden. Dies geschieht mit folgendem Syntax:
```
Das ist eine einfache Fussnote[^1].

[^1]: Das ist der referenzierte Text.
[^2]: Fügt man am Anfang jeder neuen Zeile 2 Leerzeichen ein,
  kann man Fussnoten über mehrere Zeilen schreiben.
[^notiz]: Benannte Fussnoten erscheinen zwar weiterhin als Nummern im Text, können es aber einfacher machen, Referenzen zu identifizieren und zu verlinken.
```
