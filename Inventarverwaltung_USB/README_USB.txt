Inventarverwaltung LEV/KEV auf USB-Stick
========================================

Ordner verwenden
----------------
Kopiere den kompletten Ordner "Inventarverwaltung_USB" auf den USB-Stick.
Andere Ordner auf dem USB-Stick werden nicht benutzt und nicht veraendert.

Starten
-------
Windows: Doppelklick auf Start_Windows.bat
macOS:   Doppelklick auf Start_macOS.command
Linux:   Start_Linux.sh ausfuehren
iPhone:  Start_iPhone.html in der Dateien-App oder Safari oeffnen

Alternativ kann Start_Inventarverwaltung.html direkt im Browser geoeffnet
werden. Fuer den vollen Funktionsumfang (automatisches Speichern, Dateien
verwalten) wird Chrome oder Edge benoetigt.

Datenordner einmalig verbinden
------------------------------
1. Beim ersten Start im Bereich "Datenordner" auf "Datenordner auswaehlen"
   klicken und den Ordner "Inventarverwaltung_USB" (oder einen Unterordner
   davon) auswaehlen.
2. Ab jetzt merkt sich der Browser diesen Ordner. Beim naechsten Start der
   App wird automatisch der zuletzt gespeicherte Stand geladen - ein
   manuelles Laden der JSON-Datei ist nicht mehr noetig.
3. Falls der Browser den Zugriff erneut bestaetigen moechte, erscheint
   links unten der Knopf "Zugriff bestaetigen". Ein Klick genuegt.

Automatisches Speichern
------------------------
Bei jeder Eingabe (neuer oder bearbeiteter Datensatz, Import, Loeschen)
speichert die App automatisch. Dabei wird im Unterordner "daten" eine neue
Datei mit Datums- und Uhrzeitstempel angelegt, zum Beispiel
inventar_daten_2026-07-01_14-32-05.json. Alte Staende bleiben erhalten und
werden nicht ueberschrieben.

Beim naechsten Start laedt die App automatisch den neuesten Stand. Wer
einen aelteren Stand braucht, findet im Bereich "Datenordner" unter
"Gespeicherte Staende" eine Liste aller Sicherungen mit Datum und Uhrzeit
und kann dort gezielt einen aelteren Stand oeffnen.

Der Knopf "Automatisch speichern" im Bereich "Datenordner" kann bei Bedarf
deaktiviert werden; dann speichert nur noch der Knopf "Speichern" oben
rechts. Ueber "Alte Staende bereinigen" lassen sich sehr alte Sicherungen
loeschen (die neuesten 100 bleiben immer erhalten); dafuer ist immer eine
Bestaetigung noetig.

Wenn ungespeicherte Aenderungen vorhanden sind, warnt der Browser beim
Schliessen oder Neuladen der App.

Dateien verwalten (Uebergabeprotokolle, Kaufbelege, Fotos)
-----------------------------------------------------------
Im Bereich "Dokumente" koennen beliebige Dateien (PDF, Bilder, ...)
dauerhaft im Unterordner "dokumente" abgelegt werden - zum Beispiel ein
unterschriebenes Uebergabeprotokoll als PDF. Jede Datei kann mit einem
Inventarobjekt, einer Uebergabe und/oder einer Person verknuepft werden.

Die Datei kann entweder per Klick auf das gestrichelte Feld ausgewaehlt
oder direkt per Drag & Drop aus dem Dateimanager/Explorer/Finder in das
Feld gezogen werden.

Beim Erfassen einer Uebergabe kann direkt im Formular das zugehoerige
Uebergabeprotokoll als PDF hochgeladen werden. In der Uebergaben-Tabelle
erscheint dann ein "Oeffnen"-Knopf, ueber den die Datei jederzeit wieder
angezeigt werden kann. Dateien koennen im Bereich "Dokumente" auch geloescht
werden; dabei wird die Datei auch vom Datentraeger entfernt.

Die Dateiverwaltung benoetigt einen verbundenen Datenordner und Chrome oder
Edge. Im iPhone-Modus ist sie nicht verfuegbar (iOS erlaubt keinen
dauerhaften Ordnerzugriff); dort bitte Uebergabeprotokolle separat in der
Dateien-App oder iCloud ablegen.

Uebergabeprotokolle erstellen
------------------------------
Im Bereich "Uebergaben" kann ueber "Leeres Protokoll vorbereiten" ein
druckfertiges, einseitiges Uebergabeprotokoll mit zwei Unterschriftenfeldern
(abgebend/empfangend) erzeugt werden - zum Beispiel um es vorab auszudrucken
und bei einem Treffen von Hand auszufuellen. Bei einer bereits erfassten
Uebergabe erzeugt der Knopf "Protokoll" in der Tabelle stattdessen ein
Protokoll, das Datum, Beteiligte, Protokoll-Nr. und Zustand schon aus dem
Datensatz uebernimmt.

Als zweite Seite wird automatisch eine Anlage mit der aktuellen
Inventarliste (nur Inventar-Nr. und Bezeichnung) zum Ankreuzen angehaengt;
bei einem bereits erfassten Datensatz ist das betroffene Inventarobjekt
schon angekreuzt. Das Protokoll oeffnet sich in einem neuen Tab; dort im
Browser "Drucken" bzw. "Als PDF speichern" waehlen. Das fertig
unterschriebene Protokoll kann anschliessend als PDF im Bereich
"Dokumente" oder direkt am Uebergabe-Datensatz abgelegt werden (siehe
oben, "Dateien verwalten").

Daten korrigieren
-----------------
In den Tabellen fuer Inventar, Personen und Uebergaben gibt es je Datensatz
"Bearbeiten" und "Loeschen".

Bei neuem Inventar kann die Inventar-Nr. leer bleiben. Dann vergibt die App
automatisch eine Nummer aus Gremium, Jahr und laufender Nummer, zum Beispiel
LEV-2026-0001 oder KEV-SEGEBERG-2026-0001.

Wenn eine Person nur nicht mehr in einem Gremium vertreten ist, kann sie unter
"Personen" bearbeitet und das Gremium geleert oder geaendert werden. "Loeschen"
entfernt die Person aus der Datenliste und leert vorhandene Verweise auf diese
Person.

Personen importieren
--------------------
Im Ordner daten liegt die Vorlage personen_import_vorlage.csv (unter
"Personen" -> "CSV-Vorlage" auch jederzeit neu herunterladbar). Sie kann mit
Excel oder LibreOffice Calc gefuellt werden.

Spalten:
Vorname; Nachname; E-Mail; Telefon; Gremien; Funktion; Notiz

Mehrere Gremien werden in der Spalte Gremien mit | getrennt, zum Beispiel:
LEV|KEV Segeberg

Die App liest CSV-Dateien sowohl in UTF-8 als auch im aelteren
Windows-1252-Format (typisch fuer aeltere Excel-Exporte), sodass Umlaute in
jedem Fall korrekt angezeigt werden.

Beim Import sucht die App nach moeglichen Duplikaten anhand von E-Mail oder
gleichem Vor- und Nachnamen. Dann kann entschieden werden:
OK = zusammenfuehren, Abbrechen = als eigenen Datensatz anlegen.

Die aktuelle Personenliste kann jederzeit ueber "CSV exportieren" als
CSV-Datei oder ueber "PDF erstellen" als druckfertige Liste (Name,
Kontakt, Gremium, Funktion) exportiert werden.

Inventar importieren
--------------------
Im Ordner daten liegt die Vorlage inventar_import_vorlage.csv (unter
"Inventar" -> "CSV-Vorlage" auch jederzeit neu herunterladbar). Sie kann mit
Excel oder LibreOffice Calc gefuellt werden.

Spalten:
Inventar-Nr; Bezeichnung; Kategorie; Status; Gremium; Besitzer Vorname;
Besitzer Nachname; Besitzer E-Mail; Hersteller; Modell; Seriennummer;
Anschaffungsdatum; Preis; Garantie bis; Zustand; Enthaelt Daten; Notiz

Pflicht ist nur die Bezeichnung. Wenn Inventar-Nr leer bleibt, vergibt die App
automatisch eine passende Nummer nach Gremium und Jahr. Wenn Inventar-Nr
ausgefuellt ist, wird sie uebernommen. Ist diese Nummer schon vorhanden, fragt
die App, ob der vorhandene Datensatz aktualisiert oder die Zeile uebersprungen
werden soll.

Gremium, Kategorie und Status werden als Text erkannt, zum Beispiel:
LEV, KEV Segeberg, Laptop, Drucker, Buch, im Bestand, defekt. Das erkennt
sowohl "KEV Luebeck" als auch "KEV Lübeck".

Anschaffungsdatum und Garantie bis werden flexibel erkannt: als
JJJJ-MM-TT (zum Beispiel 2026-06-10), als deutsches Datum TT.MM.JJJJ
(zum Beispiel 10.06.2026) oder als von Excel erzeugte Seriennummer,
falls die Spalte in Excel nicht als Datum/Text formatiert war. Der
Preis wird sowohl mit Komma (899,00) als auch mit Punkt (899.00) und
mit Tausenderpunkt (1.234,56) als Dezimaltrennzeichen erkannt.

Besitzer werden anhand E-Mail oder Vor-/Nachname vorhandenen Personen
zugeordnet. Nicht gefundene Besitzer werden nicht automatisch neu angelegt; sie
werden nach dem Import in der Zusammenfassung gezaehlt.

Personen mit aktuellem Inventarbesitz koennen nur geloescht werden, wenn das
Inventar vorher uebergeben wurde oder der Gegenstand als defekt markiert ist.
Bei Buechern reicht Zustand oder Notiz "veraltet".

Berichte
--------
Unter "Berichte" koennen Inventarlisten und Mitgliederlisten erstellt werden.
Die Auswahl kann fuer alle Gremien, nur LEV, alle Kreiselternvertretungen oder
ein einzelnes Gremium erfolgen.

Unter "Spalten fuer diesen Bericht" kann jede einzelne Spalte per Haekchen
ein- oder ausgeblendet werden (zum Beispiel Besitz/Person, Hersteller,
Preis, Notiz ...). "Alle auswaehlen"/"Alle abwaehlen" setzen alle Haekchen
auf einmal. Die Auswahl gilt fuer Tabelle, CSV-Export und PDF gleichermassen
und kann beliebig oft und ohne Neuladen der Seite geaendert werden.

"CSV exportieren" erstellt eine CSV-Datei (mit UTF-8-Kennung, damit Excel
Umlaute korrekt anzeigt). "PDF erstellen" oeffnet eine Druckansicht in einem
neuen Tab; dort im Browser "Als PDF speichern" waehlen. Bei vielen
ausgewaehlten Spalten stellt die App automatisch auf Querformat und eine
kleinere Schrift um, damit die Tabelle immer sauber lesbar bleibt.

iPhone und iPad
---------------
Start_iPhone.html oeffnet die App im iPhone-Modus. In diesem Modus speichert
die App lokal im Browser-Speicher des iPhones. Da iOS keinen automatischen
Schreibzugriff auf USB-Ordner erlaubt, bitte regelmaessig eine Sicherungsdatei
herunterladen und in der Dateien-App auf dem USB-Stick oder in iCloud ablegen.

Ordner im Paket
---------------
daten       wird beim ersten Verbinden automatisch angelegt; enthaelt alle
            zeitgestempelten Sicherungen (siehe oben)
dokumente   wird automatisch angelegt; enthaelt hochgeladene Dateien wie
            Uebergabeprotokolle, Kaufbelege oder Fotos
exporte     Ablage fuer eigene CSV-/PDF-Exporte

Hinweis
-------
Die HTML-App laeuft vollstaendig offline im Browser, es werden keine Daten
irgendwohin uebertragen. Fuer automatisches Speichern, Sicherungen und die
Dateiverwaltung wird ein Browser mit Unterstuetzung fuer die File System
Access API benoetigt (aktuelle Versionen von Chrome oder Edge). In anderen
Browsern (zum Beispiel Firefox oder Safari am Mac) stehen weiterhin "Datei
importieren" und "Kopie speichern unter" zur Verfuegung.
