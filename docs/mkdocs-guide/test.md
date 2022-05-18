# MkDocs

## MkDocs benutzen

Um MkDocs zu benutzen, muss man einige Punkte beachten. Wichtig dabei ist, das man im Richtigen Ordner die Dateien verändert, sowie in der Richtigen Reihenfolge die Befehle benutzt.

## Die Ordnerstruktur

Die Ordnerstruktur sieht so aus:

    mkdocs/mkdocs.yml    # The configuration file.
    mkdocs/docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

Wichtig dabei ist das man die Doku *nur* im ../docs Ordner bearbeitet. Niemals unter ../pages.

### Doku bearbeiten

Ist man nun im Verzeichnis **mkdocs/docs/** angekommen, kann man dort Seiten erstellen oder die Vorhandenen bearbeiten. 
Die **index.md** ist die Startseite der Doku. In dieser müssen die neuen Seiten aufgeschrieben werden.

### Doku pushen

Das hochladen ist etwas komplizierter. 

Als erstes muss man alle neu erstellten Dateien oder veränderten Dateien im Git hinzufügen.

** git add .**

Im Anschluss müssen die änderungen noch commited werden.

** git commit -m "Änderung beschreiben"**

Nachdem alles gespeichert wurde, kann nun die Seite angepasst werden. Dazu muss nur der folgende Befehl ausgeführt werden:

** mkdocs build **

Zuletzt muss das noch deployed werden, damit die Seite es auch mitbekommt.

** mkdocs gh-deploy **

Hier mit den Git Daten einloggen, damit der deploy auch funktioniert.

### Fehler

Manchmal kommt ein Fehler das bereits etwas anderes was verändert hat und man sich erstmal die Änderung ziehen soll.
Das kann mit folgendem Befehl getan werden.

** git pull https://github.com/xchwihan/mkdocs --allow-unrelated-histories **
