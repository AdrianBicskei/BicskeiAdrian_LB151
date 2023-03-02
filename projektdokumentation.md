# Projekt-Dokumentation

Bicskei

| Datum | Version | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
| 26.01 | 0.0.1   | Ich habe das GitHub Repository erstellt und mich zum Python Flask mit Datenbanken verbunden informiert.   |
| 02.02 | 0.0.2   | Ich habe die 4 Tiers beschrieben und die User Storys angefangen.           |       
| 09.02 | 0.0.3   | Ich habe die User Storys fertiggestellt und die Testfälle angefangen.     |
| 16.02 | 0.0.4   | Ich habe mit dem erstellen der Applikation begonnen.                                                             |
| 23.02 | 0.0.6   |                                                              |
|       | 1.0.0   |                                                              |

# 0 Ihr Projekt

Bei diesem Projekt handelt es sich um eine abgewandte abgewandelte Version der Fernsehquiz Glücksrad als eine Webapplikation, welcher mit einer Datenbank verbunden ist. 

# 1 Analyse

* Tier 1 (Presentation): Die User Interface, also die Anzeige der Inhalte des Spiels und die Entgegennahme der Benutzereinträge. Eventuell noch prüfen auf Leereingaben. 
* Tier 2 (Webserver): Die Steuerung des Programmablaufs. Eventuell Überprüfung der Benutzereingaben. 
* Tier 3 (Application Server): Die Geschäftslogik, also die Funktionen und Operation, die zum Spiel gehören. 
* Tier 4 (Dataserver): Die Persistenz, also die Speicherung der zum Spiel gehörenden Daten in der Datenbank. 

# 2 Technologie

✍️ Beschreiben Sie für dieselben Tiers, welche Programmiersprache bzw. Technologie Sie verwenden möchten.

* Tier 1 (Presentation): Für den User Interface verwende ich HTML-Templates im Rahmen einer Python Flask Projekt. 
* Tier 2 (Webserver): Für die Steuerung in der Webapplikation verwende ich die Python Flask. 
* Tier 3 (Application Server): Für die Geschäftslogik der Applikation verwende ich Python Flask. 
* Tier 4 (Dataserver): Die Persistenz der Daten stelle ich durch eine MySQL-Datenbank sicher, welcher mithilfe der SQLAlchemy Erweiterung mit meiner Applikation verbunden ist. 


# 3 Datenbank

Die Ansteuerung der Datenbank erfolgt durch zwei vom Spiel separaten Seiten mit Formularfeldern, welche nur dem Administrator durch Authentifizierung zugänglich sind. Mit einer dieser Formularseiten ist es dem Administrator möglich, einen bestimmten Spieler aus der Highscoreliste zu entfernen und mit dem anderen kann der Admin Wörter und Kategorien für das Spiel anlegen. 

# 4.1 User Stories

✍️ Formulieren Sie klare Anforderungen in der Form von User Stories (*„als … möchte ich … damit …“*) und zu jeder Anforderung mindestens einen dazugehörigen Testfall (in Kapitel 4.2). 

✍️ Formulieren Sie weitere, eigene Anforderungen und Testfälle, wie Sie Ihre Applikation erweitern möchten. Geben Sie diesen statt einer Nummer einen Buchstaben (`A`, `B`, etc.)

| US-№ | Verbindlichkeit | Typ  | Beschreibung                       |
| ---- | --------------- | ---- | ---------------------------------- |
| 1    |        Muss         |   Funktional   | Als Administrator möchte ich mich durch Benutzername und Passwort authentifizieren können, damit der Datenbank nur von mir bearbeitet werden kann. |
| 2  |Wichtig|    Funktional  | Als Administrator möchte ich Phrasen und Rätselwörter in der Datenbank anlegen können, damit die gefragten Phrasen und Rätselwörter im Spiel abwechslungsreich sind.                                  |
| 3  |          Muss       |   Funktional   | Als Administrator möchte ich in der Datenbank Kategorien anlegen und jedes Wort bzw. jede Frage einer Kategorie zuordnen können, damit man im Spiel mit Wörtern verschiedener Kategorien spielen kann. |
| 4  |        Muss         |  Funktional    |    Als Administrator möchte ich in der Datenbank einzelne Einträge der Highscore-Liste löschen können, um Kontrolle über die Highscore-Liste zu haben.                                |
| 5  |         Muss        |   Funktional   |  Als Kandidat möchte ich einen Namen eingeben können, damit dieser auf der Highscore-Liste erscheint.                                  |
| 6  |         Muss        |   Rahmenbedingung   | Als Kandidat möchte ich zu jeder Zeit die Lebenspunkte sehen, damit man über die Anzahl Lebenspunkte bewusst ist.                                   |
| 7 |        Muss         |   Rahmenbedingung   |      Als Kandidat möchte ich die in der Highscore Liste aufgeführten aktuellen Daten (Rang, Name des Spielers, Zeitpunkt des Spiels und Geldbetrag, Anzahl Spielrunden) zu jeder Zeit sehen, damit ich über den Fakt, ob eine Antwort richtig oder falsch war, informiert werde.                          |
| 8  |        Muss         |   Funktional   | Als Kandidat möchte ich, dass die Highscore-Liste nach Rang, der durch die Höhe des Geldbetrags bestimmt wird, aufsteigend sortiert wird, damit ich über die Rangliste informiert werde.  |
| 9  |         Unwichtig        |    Funktional  |   Als Kandidat möchte ich, dass mir kein Rätselwort und keine Phrase mehr als einmal gestellt werden, damit die Fragen im Spiel abwechslungsreich sind. |
| 10  |        Muss         |   Funktional   |      Als Kandidat möchte ich zu jederzeit entweder spielen oder aufhören können und meinen Gewinn in die Highscore-Liste übernehmen, damit ich das Spiel entweder weiterspielen oder aufhören kann. |
| 11  |         Kann        |   Qualität   |    Als Kandidat möchte ich, dass das Spiel (der Datenbank) mit einer spielbaren Anzahl Wörtern und Fragen gefüllt ist, damit ich spielen kann.      |
| 12  |        Muss         |   Funktional   |    Als Kandidat möchte ich, dass die Anzahl der Spielrunden gezählt wird, um darüber informiert zu werden.                          |
| 13  |         Muss        |   Funktional   |    Als Kandidat möchte ich, dass ich beim Erdrehen der Feld "Bankrott" mein Guthaben verliere und ein neues Spiel beginnen muss, damit das Spiel zufällig ist.                          |
| 14  |        Kann         |  Funktional    |    Als Kandidat möchte ich, dass das Erdrehen der Feld "Bankrott" eine Wahrscheinlichkeit von 1 zu 20 hat, damit die Wahrscheinlichkeit des Bankrotts optimal ist.                          |
| 15  |        Muss         |   Funktional   |    Als Kandidat möchte ich, dass mir beim Erdrehen der Feld "Geldbetrag X" eine kategorisierte Frage aus einem Wort mit ein paar abgedeckten Buchstaben gestellt wird, damit ich die Frage beantworten kann.               |
| 16  |        Muss         |   Funktional   |    Als Kandidat möchte ich, dass mir bei einer falschen Antwort jeweils ein Lebenspunkt abgezogen wird, damit man im Spiel verlieren kann.               |
| 17  |        Muss         |   Funktional   |    Als Kandidat möchte ich, dass ich beim Aufbrachen meiner Lebenspunkte ein neues Spiel beginnen muss, damit man im Spiel verlieren kann.               |
| 18  |         Muss        |   Funktional   |    Als Kandidat möchte ich, dass mir beim richtigen Antwort auf eine Frage ein entsprechender Geldbetrag in der Highscore-Liste gutgeschrieben wird, damit man in der Highscore-Liste aufsteigen kann.              |
| A  |          Kann       |  Qualität    |    Als Benutzer möchte ich, dass ich beim Starten der Webapplikation durch Bildern aus Spiel und Adminlogin auswählen kann, damit die Navigation in der Applikation schnell und einfach ist.             |
| B  |       Kann          |   Qualität   |    Als Administrator möchte ich, dass ich nach der Authentifizierung durch Bildern auswählen kann, welche Tabelle ich in der Datenbank besteuern möchte, damit die Besteuerung der Datenbank schnell und einfach erfolgen kann.              |
| C  |         Kann        |   Qualität   |    Als Kandidat möchte ich, dass ich durch das Anklicken eines zum Spiel passenden Bildes das Rad drehen kann, damit der Spielablauf schnell und einfach erfolgen kann.              |
| D  |         Kann        |   Funktional   |    Als Administrator möchte ich, dass ich beim Besteuern der Datenbank die Tabelleninhalte auf der Webseite aufgelistet habe, damit ich über den Inhalt der Tabellen bewusst bin.              |
| E |         Kann        |   Funktional   |    Als Kandidat möchte ich, dass mir zufällige Buchstaben der gestellten Frage mit Sternen abgedeckt werden, damit ich es schwierig habe das Wort zu erraten.              |



✍️ Jede User Story hat eine ganzzahlige Nummer (1, 2, 3 etc. oder Zahl), eine Verbindlichkeit (Muss oder Kann?), und einen Typ (Funktional, Qualität, Rand). 

# 4.2 Testfälle

| TC-№ | Vorbereitung | Eingabe | Erwartete Ausgabe |
| ---- | ------------ | ------- | ----------------- |
| A.1  |       Webapplikation starten      |     Admin Bild klicken        |        Admin Login Page           |
| 1.1  |       Admin Bild wählen       |    Benutzername: adrian, Passwort: passwort      |        Admin Page           |
| 2.1, 3.1, B.1, D.1  |       Als Admin eingeloggt, Bild für Wörter anlegen ausgewählt       |     Wort: Skoda, Kategorie: Automarke    |        Neue Liste mit Skoda enthalten           |
| 4.1, B.2, D.2  |       Als Admin eingeloggt, Bild für Spieler löschen ausgewählt       |     id: 39   |        Neue Liste ohne Spieler ID 39          |
| 5.1, 8.1, A.2 |      Spiel Bild ausgewählt       |     Name: Adrian  |        Highscore-Liste mit Spieler Adrian enthalten nach Geldbetrag aufsteigend sortiert, Page zum Rad drehen         |
| 7.1, 8.2, C.1  |     Name eingegeben/Rad gedreht       |     Name: Adrian/Rad drehen  |        Highscore-Liste mit Spieler Adrian enthalten nach Geldbetrag aufsteigend sortiert       |
| 11.1, D3 |     Als Admin eingeloggt, Bild für Wörter anlegen      |     -  |        Mindestens 15 Wörter angelegt      |
| 13.1, 14.1, C.2, 7.2, 8.2 |    evtl. "random_bool" manuell auf False stellen, beim aktuellen Spieler manuell durch SQL-Befhel den Guthaben von 1500 setzen     |    Rad drehen |        Bankrott Page, Guthaben in der Highscore-Liste auf 0      |
| 15.1, E.1, C.3,  7.3, 8.3  |    Bild Spiel gewählt     |    Rad drehen |        Guess Page, Kategorie: Automarke, Frage: Mercedes, mit zufälligen Buchstaben abgedeckt, Highscore-Liste    |

✍️ Die Nummer hat das Format `N.m`, wobei `N` die Nummer der User Story ist, die der Testfall abdeckt, und `m` von `1` an nach oben gezählt. Beispiel: Der dritte Testfall, der die zweite User Story abdeckt, hat also die Nummer `2.3`.

# 5 Prototyp

✍️ Erstellen Sie Prototypen für das GUI (Admin-Interface und Quiz-Seite).

# 6 Implementation

✍️ Halten Sie fest, wann Sie welche User Story bearbeitet haben

| User Story | Datum | Beschreibung |
| ---------- | ----- | ------------ |
| ...        |       |              |

# 7 Projektdokumentation

| US-№ | Erledigt? | Entsprechende Code-Dateien oder Erklärung |
| ---- | --------- | ----------------------------------------- |
| 1    | ja / nein |                                           |
| ...  |           |                                           |

# 8 Testprotokoll

✍️ Fügen Sie hier den Link zu dem Video ein, welches den Testdurchlauf dokumentiert.

| TC-№ | Datum | Resultat | Tester |
| ---- | ----- | -------- | ------ |
| 1.1  |       |          |        |
| ...  |       |          |        |

✍️ Vergessen Sie nicht, ein Fazit hinzuzufügen, welches das Test-Ergebnis einordnet.

# 9 `README.md`

✍️ Beschreiben Sie ausführlich in einer README.md, wie Ihre Applikation gestartet und ausgeführt wird. Legen Sie eine geeignete Möglichkeit (Skript, Export, …) bei, Ihre Datenbank wiederherzustellen.

# 10 Allgemeines

- [ ] Ich habe die Rechtschreibung überprüft
- [ ] Ich habe überprüft, dass die Nummerierung von Testfällen und User Stories übereinstimmen
- [ ] Ich habe alle mit ✍️ markierten Teile ersetzt