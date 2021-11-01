---
description: Goobi viewer Digest für Oktober 2021
---

# Oktober

## **C**oming soon :rocket:

* Überarbeitung der **Kommentare**
* Änderungen am **Suchalgorithmus**

## Ankündigungen

Wir wollen uns in den kommenden Monaten der Überarbeitung der Suche widmen. In der Regel sind Änderungen in diesen Codebereichen schwer zu greifen, da sie oft keine visuellen Anpassungen beinhalten. Gleichzeitig sind sie komplex, da viel Logik nicht nur verstanden, sondern auch in Algorithmen umgesetzt werden muss. Mehrere Wochen Arbeit führen dann dazu, das ein Suchtreffer weiter oben oder weiter unten in der Liste erscheint. Neue Buttons oder Features gibt es aber gleichzeitig nicht.

Innerhalb der Community haben sich bereits verschiedene Partner bei uns gemeldet, die eine Änderung von Teilbereichen angefragt haben um die Finanzierung zu prüfen.

Es gibt aber noch weitere Punkte die in diesem Zusammenhang wünschenswert wären. Diese beinhalten auch visuelle Änderungen und beziehen sich zum Beispiel auf die Überarbeitung der Bedienbarkeit der einfachen und der erweiterten Suche. Aber auch weitere Entwicklungen wie eine dedizierte Auflistung von Personen- und Ortstreffern, die Integration der DNB Entity Facts, Suche in Inhalten von CMS-Seiten oder Export von Trefferlisten als IIIF Collection sind Wünsche, die in der Vergangenheit geäußert wurden.

Wenn Interesse an der Konzeption und Übernahme einzelner Posten besteht freuen wir uns über eine Kontaktaufnahme!

## Entwicklungen

### Archivansicht

Die Archivansicht wurde an vielen Stellen überarbeitet und erweitert. Was sicherlich als erstes ins Auge springt ist, dass sie nun Farben und Logos aus dem Corporate Design enthält. Dadurch wirkt sie nativer in den Rest des Goobi viewers integriert.

Die Icons im Archivplan sind jetzt konfigurierbar und Übernehmen in der Standardkonfiguration die Icons aus dem Archivmanagement Plugin von Goobi workflow. Ein Piktogramm zeigt an hinter welchen Knoten und Verzeichnungseinheiten Digitalisate vorliegen. Außerdem wird im Baum unterhalb einer Verzeichnungseinheit der Entstehungszeitraum angezeigt, so dass eine schnelle zeitliche Navigation möglich ist.

Komplett neu ist die Auswahl und der Wechsel zwischen verschiedenen Beständen. Diese Option wird automatisch eingeblendet sobald mehr als ein Bestand vorliegt.

Zusammen mit dieser Überarbeitung ist die alternative Tektonikansicht ersatzlos weggefallen. Alle Vorteile, die diese alternative Ansicht geboten hat, sind in die Archivansicht eingeflossen.

Auch die Konfigurationsdatei wurde in dem Bereich restrukturiert und folgt jetzt einer klareren Logik.

![Wenn mehrere Bestände vorliegen wird automatisch eine Auswahl angeboten](../.gitbook/assets/21.10\_DE\_archive\_select-collection.png)

![Die Archivansicht wurde visuell Überarbeitet](../.gitbook/assets/21.10\_DE\_archive\_visual-changes.png)

### Profil

Nachdem wir im letzten Monat die Benutzereinstellungen überarbeitet haben wird mit diesem Release eine Profilseite für Benutzer eingeführt. Dort sind zeitlich absteigend die letzten Aktivitäten aufgelistet, gefolgt von einer Übersicht der Merklisten, gespeicherten Suchen und Kommentare.

Weiter wurde mit diesem Release die Benennung der Einträge im Benutzermenü geprüft und überarbeitet. Dabei wurde sichergestellt, dass diese mit den Überschriften auf den verlinkten Seiten übereinstimmen. Auch die Breadcrumbs und teilweise die URLs wurden in dem Zuge für den Benutzerbereich geprüft. Teilweise wurde die Benennung in den Breadcrumbs angeglichen und  teilweise auch neue Ebenen eingefügt, damit diese mit der URL Struktur konsistent sind.

![Die neue Profilseite gibt angemeldeten Benutzern einen neuen Überblick](../.gitbook/assets/21.10\_DE\_dashboard.png)

### Anmeldedialog

Der Anmeldedialog wurde nicht inhaltlich, wohl aber visuell umgestaltet. Des öfteren haben wir in den letzten Jahren die Rückmeldung bekommen, dass Funktionalität, wie die um ein neues Konto zu registrieren oder auch die Passwort vergessen Funktionalität nicht gut zu finden sein.

Wir haben das Feedback gesammelt, gesucht und jetzt eine Möglichkeit gefunden die Elemente klarer anzuordnen. Hier eine Vergleichsansicht der beiden Dialoge nebeneinander:

![Links der frühere, rechts der neue Anmeldedialog](../.gitbook/assets/21.10\_DE\_login-compare.png)

### Barrierefreiheit

Die Barrierefreiheit wurde weiter verbessert und es erscheint nun bei der Navigation mit der Tastatur und Tabulator in der Webseite ein Fokusring. Wird eine Maus verwendet ist dieser jedoch nicht sichtbar. Diese Änderung ermöglicht eine schnellere, visuelle Navigation.

![Ein roter Fokusring zeigt den ausgewählten Link bei der Navigation mit der Tastatur an](../.gitbook/assets/21.10\_DE\_wcag-focus.png)

### CSS und Javascript Libraries

Die Verwaltung der CSS und Javascript Libraries erfolgt jetzt über die `package.json` und das Tool npm. Ähnlich wie bei den Java Abhängigkeiten mit maven, wurde eine zentrale Stelle eingeführt in der die Abhängigkeiten mit ihren Versionen aufgeführt sind. Im zusammenspiel mit dem Tool Grunt, können die Libraries jetzt einfacher verwaltet und aktuell gehalten werden. Diese Änderung mag in dem Digest nur am Ende stehen, kurz sein und unscheinbar aussehen, aber sie ist ein großer Meilenstein auf dem Weg zu stets gepflegten und aktuellen Versionen der eingesetzten Libraries.

![Verwaltung von CSS und Javascript Abhängigkeiten mit npm](../.gitbook/assets/21.10\_DE+EN\_npm-outdated.png)

## Versionsnummern

Die Versionen die in der `pom.xml` des Themes eingetragen werden müssen um die in diesem Digest beschriebenen Funktionen zu erhalten lauten:

```markup
<dependency>
    <groupId>io.goobi.viewer</groupId>
    <artifactId>viewer-core</artifactId>
    <version>21.10</version>
</dependency>
<dependency>
    <groupId>io.goobi.viewer</groupId>
    <artifactId>viewer-core-config</artifactId>
    <version>21.10</version>
</dependency>
<dependency>
    <groupId>io.goobi.viewer</groupId>
    <artifactId>viewer-connector</artifactId>
    <version>21.10</version>
</dependency>
```

Der **Goobi viewer Indexer** hat die Versionsnummer **21.10**

Das **Goobi viewer Crowdsourcing Modul** hat die Versionsnummer **21.10**
