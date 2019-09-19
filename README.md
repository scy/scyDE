# scyDE – erweitertes deutsches Tastaturlayout

**Note for English speakers:** This project provides an extended version of the normal German keyboard (as used in Germany), geared towards programmers and typophiles. As its intended audience is German, this document is currently provided in German only. If you think that’s a mistake, feel free to translate this document and submit a pull request.

## Status

Ich habe scyDE für einige Zeit im täglichen Einsatz verwendet und war zufrieden.
Inzwischen bin ich jedoch, um ein möglichst einheitliches Tastaturlayout auf allen Geräten zu haben (insbesondere auch meinem Smartphone, das kein Selbstbau-Tastaturlayout ermöglicht), auf das US-Tastaturlayout umgestiegen und ergänze es auf Windows mit [WinCompose](http://wincompose.info/).
**scyDE wird daher aktuell von mir nicht aktiv weiterentwickelt.**

Wenn Interesse besteht, kann ich Pull Requests aufnehmen; alternativ kann auch gern jemand mich als Maintainer ablösen.

## Zielgruppe

Dieses Projekt stellt ein erweitertes deutsches Tastaturlayout zur Verfügung und richtet sich vorrangig an Softwareentwickler*innen und Typophile, also Leute, denen korrekte Typographie in ihren maschinengeschriebenen Texten wichtig ist.

## Systemvoraussetzungen

* Microsoft Windows (getestet unter Windows 10)

Eine Portierung auf andere Betriebssysteme werde ich vornehmen, wenn ich sie aktiv nutze. Gerade bei Linux dürfte das demnächst der Fall sein. Pull Requests werden gern genommen.

## Vorteile

* scyDE *erweitert* das bestehende deutsche Tastaturlayout. Alle Zeichen bleiben an ihren bekannten Positionen, es kommen nur neue hinzu.
  * Das [NEO](https://www.neo-layout.org/)-Projekt pflegt beispielsweise ein komplett umgebautes deutsches Tastaturlayout, dessen Fokus vor allem auch auf Ergonomie liegt. NEO bietet weit mehr Zeichen als scyDE, aber hat dafür eine signifikante Lernkurve: Alle Zeichen (auch die Buchstaben) befinden sich an komplett anderen Positionen.
* Im Gegensatz zu [WinCompose](https://github.com/samhocevar/wincompose), das ebenfalls einen größeren Zeichenumfang bietet, werden (fast) alle Zeichen in scyDE ganz „normal“ über <kbd>Alt Gr</kbd> in Kombination mit einer Buchstaben- oder Ziffertaste aufgerufen und nicht mit mehreren aufeinanderfolgenden Tastendrücken.
* Einige Zeichen sind zusätzlich zu ihren normalen Positionen auch an „bequemeren“ Orten erreichbar. So finden sich beispielsweise die zum Programmieren wichtigen `[]{}` auch auf <kbd>Alt Gr</kbd>+`asdf`.
* Die auf deutschen Tastaturen üblicherweise als [Tottasten](https://de.wikipedia.org/wiki/Tottaste) ausgeführten Zeichen ^, ` und ´ gibt es in scyDE zusätzlich in einer untoten(?) Variante. Die meist nicht tote Tilde (~) gibt es zusätzlich in tot.
* Das Dezimaltrennzeichen auf dem Ziffernblock ist der Punkt, nicht das Komma.
* Bei aktiviertem Caps-Lock (wer auch immer das benutzt) erscheint bei einem Druck auf eine Ziffer trotzdem die Ziffer, nicht Interpunktion. Leider lässt sich das Layout nicht so konfigurieren, dass ein kleines ß mit Caps Lock zu einem großen wird.

## Zeichenvorrat

scyDE bietet folgende zusätzliche Zeichen:

* Auslassungspunkte (…)
* Versal-Eszett (ẞ) und langes s (ſ)
* das geschützte Leerzeichen in der üblichen und einer schmalen Form (wie beispielsweise zwischen „z. B.“ empfohlen)
* typographisch korrekte Anführungszeichen in „doppelt“ und ‚einfach‘ sowie auch in der “englischen” ‘Fassung’
* Chevrons in »doppelt« und ›einfach‹ (und zwar im Gegensatz zu Mac-Tastaturen in der richtigen Reihenfolge)
* Halb- und Geviertstrich (–, —)
* den bedingten Trenn- und den geschützten Bindestrich sowie den Bindehemmer
* mathematische Zeichen für Laien, nämlich `×`, `÷`, `Σ`, `⌀`, `‰`, `‌±`, `≤`, `≥` und `≠`, sowie `≈`, `≃` und `≅` über die tote Tilde
* 1, 2 und 3 in hoch- und tiefgestellter Variante
* das Aufzählungszeichen (Bullet, •) sowie Kreuz (†) und Zweibalkenkreuz (‡)
* die wichtigsten Pfeile für Fließtext: ← ↔ → und ⇐ ⇔ ⇒
* ã, ñ, õ, Ã, Ñ und Õ (über die tote Tilde)
* das Zeichen ␣ als sichtbares Leerzeichen
* ♯ und ♭
* der unterbrochene senkrechte Balken (¦)

Hier das Layout in grafischer Form:

![Tastaturlayout](doc/scyDE.png)

* Die Tasten sind links mit der Belegung ohne, rechts mit <kbd>Alt Gr</kbd> beschriftet. Oben befindet sich die Beschriftung für mit, unten für ohne <kbd>Shift</kbd>.
* Tottasten sind rot markiert.
* Einige nichtdruckbare Zeichen sind mit Abkürzungen aufgeführt:
  * NBSP: geschütztes Leerzeichen *(non-breaking space)*
  * NNBSP: schmales geschütztes Leerzeichen *(narrow non-breaking space)*
  * SHY: bedingter Trennstrich *(soft hyphen)*
  * NBHY: geschützter Bindestrich *(non-breaking hyphen)*
  * ZWNJ: Bindehemmer *(zero-width non-joiner)*
* Die Zeichen auf <kbd>Z</kbd> und <kbd>M</kbd> sind auf der Grafik nicht so einfach zu unterscheiden. Auf <kbd>Z</kbd> liegen Halbgeviert- und (mit <kbd>Shift</kbd>) Geviertstrich, auf <kbd>M</kbd> wie üblich das µ für Mikro und (mit <kbd>Shift</kbd>) das Minuszeichen.
* Die Akzente links von Backspace sind in der nicht-toten Variante (mit <kbd>Alt Gr</kbd>) vertauscht. Das ist Absicht: Der sonst nur in Kombination mit <kbd>Shift</kbd> erreichbare Gravis wird beim Programmieren weit häufiger benutzt als der Akut.
* Die Grafik wurde mit `keyboard-layout-editor.com` erstellt, Informationen zur Anpassung findest du (auf Englisch) in [doc/chart.md](https://github.com/scy/scyDE/blob/master/doc/chart.md).

## Installation

Du findest ein ZIP-File mit einem Installationsprogramm im [Releases-Bereich bei GitHub](https://github.com/scy/scyDE/releases). Pack das File aus und starte die `setup.exe` darin.

## Build-Prozess

Wenn du Binaries von Fremden nicht vertraust (gut so!), kannst du das Layout auch aus der Quelldatei selbst bauen. Momentan ist der Build-Prozess für Windows manuell, aber auch sehr simpel.

**Wichtig:** Unbequemerweise lässt sich dieser Prozess nicht starten, wenn scyDE aktuell auf deinem Computer installiert ist. Du musst es also vorher über den in Windows üblichen Weg deinstallieren. Damit du das kannst, musst du das Layout evtl. in den Spracheinstellungen vorher ebenfalls entfernen.

- Installiere den [Microsoft Keyboard Layout Creator](https://msdn.microsoft.com/en-us/globalization/keyboardlayouts.aspx).
- Öffne die Datei `src/scyDE.klc` aus diesem Repository mit ihm (über *File* → *Load Source File…*).
- Wähle *Project* → *Build DLL and Setup Package*. Ein Log mit Warnungen sowie das Installationspaket werden erstellt.
  * Die Warnung zu `is not in the default system code page (1252)` kann ignoriert werden; viele der verwendeten Zeichen kommen nur in Unicode vor und können daher in Windows-1252 nicht gefunden werden.
  * Auch `is already defined more than once` ist vernachlässigbar, da wir ja absichtlich Zeichen doppelt definieren.
  * `This key may not be present on all keyboards` bezieht sich auf Tasten, die nur auf einer (physisch) deutschen Tastatur an dieser Stelle sind. Eine solche hast du aber hoffentlich.
- Im erstellten Ordner findest du `.msi`-Files und DLLs für verschiedene Prozessorarchitekturen, von denen die jeweils richtige bei der Installation ausgewählt wird. Ein Doppelklick auf `setup.exe` sollte den Installationsprozess starten.

## Begründungen

Die Zeichen wurden nicht einfach zufällig auf der Tastatur verteilt.

* Die Klammern bei `ASDF` orientieren sich an NEO. Sie liegen an dieser wertvollen Stelle, weil sie beim Programmieren ständig benutzt werden. Mit Mittel- und Zeigefinger Klammern öffnen und schließen zu können ist wichtiger, als das `7890`-Layout zu übernehmen.
* Die runden Klammern auf `8` und `9` sind eigentlich recht einfach zu erreichen, erfordern aber trotzdem ein stärkeres Verschieben der rechten Hand als eine Bewegung der linken, wenn sie auf `R` und `T` liegen.
* Ähnliches gilt für den Slash auf dem `W`, der dort insbesondere in Unix-Shells sehr hilfreich ist. Auf eine Kopie des Backslashes wurde dagegen verzichtet, weil der sich in meinen Augen recht einfach auf seiner normalen Position greifen lässt.
* Beim Schreiben bequem viele bedingte Trennstriche setzen zu können ist manchmal wichtig, daher liegt er einprägsam auf der Taste für das Bindestrich-Minus. Der geschützte Bindestrich liegt der Merkbarkeit halber auf derselben Taste. Der ebenfalls häufig genutzte Halbgeviertstrich sollte auf `Z` mit der linken Hand noch gut genug erreichbar sein, der weniger häufig genutzte Geviertstrich liegt wieder passend bei ihm.
* Die Anführungszeichen brauchen gleich drei nebeneinander liegende Tasten, jeweils mit und ohne Shift. Da C und V für Zwischenablagen-Shortcuts (vor allem IntelliJ’s <kbd>Strg</kbd>+<kbd>Alt</kbd>+<kbd>Shift</kbd>-Kombinationen) frei bleiben sollen, die Tasten aber auch im Fließtext gut erreichbar sein müssen, wurde `GH` bzw. `HJ` gewählt, was mit der linken Hand noch machbar sein sollte.
* Die Pfeile brauchen genau so viel Platz, müssen aber nicht so gut erreichbar sein.
* Um den Apostroph bei einem Genitiv-s nicht so kompliziert mit <kbd>Alt Gr</kbd> und <kbd>Shift</kbd> greifen zu müssen, gibt es ihn auch auf der Rautetaste, wo sich ja auch das ASCII-Singlequote, das dafür häufig benutzt wird, befindet.
* Die Chevrons lassen sich im Fließtext mit der linken Hand ebenfalls gut greifen.
* Das Multiplikationszeichen lässt sich mit „n-mal“ einigermaßen gut merken, das Divisionszeichen liegt auf derselben Taste. M für Minuszeichen ist auch eine gute Eselsbrücke, genau wie das ♭, das eben auf `b` liegt.
* `U` steht für „Umme“ und „Urchschnitt“. Das lange s sieht fast aus wie ein I, und da es ein s ist, passt auch das Zeichen für Space dazu? Okay, langsam wird’s wild. Ich hör schon auf.

## Autor und Lizenz

Dieses Tastaturlayout wurde erstellt von Tim Weber (@scy). Die Projektseite findet sich unter <https://github.com/scy/scyDE>.

Das Projekt ist gemeinfrei (public domain).
