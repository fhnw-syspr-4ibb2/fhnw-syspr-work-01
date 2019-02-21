# System-Programmierung
## Hands-on zu Lektion 1
Für Slides und Code Beispiele, siehe [Lektion 1](../../../fhnw-syspr/blob/master/01/README.md)

> *Achtung: Arbeiten Sie nicht direkt auf diesem Repository.*<br/>
> *[Erstellen Sie eine persönliche Kopie, mit diesem GitHub Classroom Link](https://classroom.github.com/a/-xV9LSkq).*

### a) int Wertebereich, 15'
* Hardware bzw. Compiler-abhängige Konstanten:<pre>
    #include <limits.h></pre>
* Schreiben Sie ein Programm *my_range.c*, das für die Typen char, int, long, short Wertebereiche so ausgibt:<pre>
    type: TYPE_SIZE byte, TYPE_MIN .. TYPE_MAX</pre>
* Erweitern Sie das Programm für unsigned Typen.
* Tipp: $ gcc FILE.c -M zeigt include Pfade an.

### b) Argumente lesen, 15'
* Command-Line Argumente als Parameter von main:<pre>
    int main(int argc, char *argv[]);</pre>
* Schreiben Sie ein Programm *my_args.c*, das alle Command-Line Argumente mit Index ausgibt:<pre>
    $ ./my_args hoi => 0: ./my_args, 1: hoi</pre>
* Erweitern Sie das Programm, dass es einen Fehler ausgibt, falls ein Argument nicht aus [a-z]* besteht.

### c) Bäume, 15'
* Erstellen Sie eine Datei *my_tree.c* mit einem Struct Typ Tree mit Zeigern auf *left*, *right* vom selben Typ, und einem String *label* von maximal 32 Byte Länge.
* Instanzieren Sie einen binären Baum mit 3 Blättern, verwenden Sie dazu die Funktionen malloc und free.
* Erweitern Sie den Node Typ für Bäume mit variabler Anzahl (N > 2) Ästen, wie [Darwin's Tree of Life](https://en.wikipedia.org/wiki/%20Tree_of_life_(biology)#/media/File:On_the_Origin_of_Species_diagram.PNG).

### d) BLE Pakete, 15'
* Erstellen Sie ein C Struct Typ für BLE Pakete gemäss: https://devzone.nordicsemi.com/f/nordic-q-a/12211/ble-packet-structure in einer neuen Datei *my_ble.c*

### e) Makefile, 15'
* Erstellen Sie ein *makefile* für Ihren Hands-on Code.
* Verwenden Sie die Compiler Flags aus dem Script.
* Korrigieren Sie allfällige neue Kompilationsfehler.
* Führen Sie *make clean* aus, vor dem *git commit*.

### Abgabe (optional)
* Lokale Änderungen [committen und pushen](#git).
* GitHub [Issue erstellen](../../issues/new) mit "Bitte um Review, @tamberg".
* Offene Fragen ausformulieren, was geht nicht, was haben Sie versucht.
* GitHub mailt mir (@tamberg) automatisch, ich versuche in weniger als 24h zu antworten :)

## Tools
### Git
Auf Ihrem Computer
* Zu Beginn jeder Lektion wird der Hands-on Repository Link freigeschaltet
* Nachdem Sie das "Assessment" annehmen, bekommen Sie per Email ein Repository
* Die REPO_URL enthält Ihren GitHub Account USER_NAME und Ihre Klasse 3ia oder 3ib, z.B.<br/>
            https://github.com/fhnw-syspr-3ia/fhnw-syspr-work-01-tamberg

Auf dem Raspberry Pi
* Repository klonen<pre>
    $ cd ~
    $ git clone REPO_URL</pre>
* Neue Datei kreieren<pre>
    $ git add FILE</pre>
* Änderungen committen<pre>
    $ git commit FILE -m "Fixed all bugs"</pre>
* Änderungen hochladen<pre>
    $ git push</pre>

### Nano
Auf dem Raspberry Pi
* Neue oder bestehende Datei öffnen mit $ nano FILE
* Editieren (Achtung, nano hat kein Undo)
* Speichern mit `CRTL-X` `Y` `RETURN`

### SSH
Auf Ihrem Computer
* Terminal öffnen (Mac) oder `WINDOWS` `R` cmd `RETURN` (Windows)
* SSH Session starten mit<pre>
    $ ssh pi@raspberrypi.local</pre>

## Support
- [FHNW Syspr Slack](https://fhnw-syspr.slack.com/)
