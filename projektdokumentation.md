# Projekt-Dokumentation

Bicskei

| Datum | Version | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
| 26.01 | 0.0.1   | Ich habe das GitHub Repository erstellt und mich zum Python Flask mit Datenbanken verbunden informiert.   |
| 02.02 | 0.0.2   | Ich habe die 4 Tiers beschrieben und die User Storys angefangen.           |       
| 09.02 | 0.0.3   | Ich habe die User Storys fertiggestellt und die Testfälle angefangen.     |
| 23.02 | 0.0.4   |                                                              |
|       | 0.0.6   |                                                              |
|       | 1.0.0   |                                                              |

# 0 Ihr Projekt

Bei diesem Projekt handelt es sich um eine abgewandte abgewandelte Version der Fernsehquiz Glücksrad als eine Webapplikation, welcher mit einer Datenbank verbunden ist. 

# 1 Analyse

✍️ Beschreiben Sie, auf welchem Tier Sie die dynamischen Elemente der Anwendung unterbringen möchten:

* Tier 1 (Presentation): User Interfache
* Tier 2 (Webserver): Steuerung
* Tier 3 (Application Server): Geschäftslogik
* Tier 4 (Dataserver): Peristenz

# 2 Technologie

✍️ Beschreiben Sie für dieselben Tiers, welche Programmiersprache bzw. Technologie Sie verwenden möchten.

# 3 Datenbank

Für die Ansteuerung der Datenbank gibt es eine vom Spiel separate Seite mit Formularfeldern, welche nur dem Administrator durch Authentifizierung zugänglich ist. 

# 4.1 User Stories

✍️ Formulieren Sie klare Anforderungen in der Form von User Stories (*„als … möchte ich … damit …“*) und zu jeder Anforderung mindestens einen dazugehörigen Testfall (in Kapitel 4.2). 

✍️ Formulieren Sie weitere, eigene Anforderungen und Testfälle, wie Sie Ihre Applikation erweitern möchten. Geben Sie diesen statt einer Nummer einen Buchstaben (`A`, `B`, etc.)

| US-№ | Verbindlichkeit | Typ  | Beschreibung                       |
| ---- | --------------- | ---- | ---------------------------------- |
| 1    |                 |      | Als Administrator möchte ich mich mit durch Benutzername und Passwort Authentifizieren können, damit der Datenbank nur von mir bearbeitet werden kann. |
| ...  |                 |      | Als Administrator möchte ich Phrasen und Rätselwörter in der Datenbank anlegen, ändern und löschen können, damit die gefragten Phrasen und Rätselwörter im Spiel abwechslungsreich sein können.                                  |
| ...  |                 |      | Als Administrator möchte ich in der Datenbank Kategorien anlegen und jedes Wort bzw. jede Frage
einer Kategorie zuordnen können, damit man im Spiel mit Wörtern verschiedener Kategorien spielen kann. 
                                   |
| ...  |                 |      |    Als Administrator möchte ich in der Datenbank einzelne Einträge der Highscore-Liste löschen können, um Kontrolle über die Highscore-Liste zu haben.                                |
| ...  |                 |      |  Als Kandidat möchte ich einen Namen eingeben können, damit dieser auf der Highscore-Liste erscheint.                                  |
| ...  |                 |      | Als Kandidat möchte ich zu jeder Zeit den Kontostand sehen, damit man über den Kontostand bewusst ist.                                   |
| ...  |                 |      | Als Kandidat möchte ich zu jeder Zeit die Lebenspunkte sehen, damit man über die Anzahl Lebenspunkte bewusst ist.                                   |
| ...  |                 |      |      Als Kandidat möchte ich die in der Highscore Liste aufgeführten aktuellen Daten (Rang, Name des Spielers, Zeitpunkt des Spiels und Geldbetrag, Anzahl Spielrunden) zu jeder Zeit sehen, damit ich über den Fakt, ob eine Antwort richtig oder falsch war, informiert werde.                              |
| ...  |                 |      | Als Kandidat möchte ich, dass die Highscore-Liste nach Rang, der durch die Höhe des Geldbetrags
bestimmt wird, aufsteigend sortiert wird, damit ich über die Rangliste informiert werde. 
                                   |
| ...  |                 |      |   Als Kandidat möchte ich, dass mir kein Rätselwort und keine Phrase mehr als einmal gestellt
Werden, damit die Fragen im Spiel abwechslungsreich sind. 
                                 |
| ...  |                 |      |      Als Kandidat möchte ich zu jederzeit entweder spielen oder aufhören können und meinen Gewinn
in die Highscore-Liste übernehmen, damit ich das Spiel entweder weiterspielen oder aufhören kann.
                              |
| ...  |                 |      |    Als Kandidat möchte ich, dass das Spiel mit einer spielbaren Anzahl Wörtern und Fragen gefüllt ist, damit ich spielen kann.                                 |
| ...  |                 |      |    Als Kandidat möchte ich, dass die Anzahl der Spielrunden gezählt wird, um darüber informiert zu werden.                                 |

✍️ Jede User Story hat eine ganzzahlige Nummer (1, 2, 3 etc. oder Zahl), eine Verbindlichkeit (Muss oder Kann?), und einen Typ (Funktional, Qualität, Rand). 

# 4.2 Testfälle

| TC-№ | Vorbereitung | Eingabe | Erwartete Ausgabe |
| ---- | ------------ | ------- | ----------------- |
| 1.1  |              |         |                   |
| ...  |              |         |                   |

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
