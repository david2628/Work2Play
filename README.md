# Work2Play
Work2Play will be a fun task managing tool  
https://work2playtogether.wordpress.com/




TBD-ASAP:
-korrekte implementierung für Tasks und rewards
-Gruppierung von Tasks in Projekte/Tabs
-Accountsystem
-Gruppentasks (Erstellen v. gemeinsamemprojekt, sync auf verschiedene Nutzer)
-Habittracker(Verlauf und sich wiederholende Tasks)
-Verlauf? (evt Diagramm, evt nur abgespeckt(nur coins pro task o.ä.))(Extra datenbank/Tabelle für abgeschlossene Tasks)
-Design(Farben, Coin PixelArt ..., Animationen, verschiedene größe Confettiregen nach Task Größe)
-Toast/Smiley/Motivationssprüche etc

TBD-optional:
-Zuweisung von Geteilten Tasks
-Notification
-Syncronisierung mit mehreren Geräten
-Backup(automatisiert/manuell)


-definition für rewards:
  Anzeige in Liste:
    -Titel
    -Kosten(Coins)
    lang halten: extramenu(dropDown):
      -Löschen(Datensatz entfernen)
      -Einlösen(Coins von Konto abziehen)(Mehrfache rewards: behalten & einfache Löschen)
    kurz klicken:
      -direkt in Bearbeitungsmodus
      -im Bearbeitungsmodus auch Abschließen und löschen möglich

-klare definition von Taskansicht, verschiedene Fälle: in der Liste, nach klicken auf Task, nach halten auf Task
  Anzeige in Liste:
    -Titel
    -Lohn(Coins)
    (evt Tasks mit naher Deadline einfärben)
    sortierung nach Deadline??? ohne Deadline nach ganz unten
  lang halten: extramenu(dropDown):
    -Löschen(datensatz entfernen)
    -Abschließen(datensatz reduzieren auf Titel und Coins)
  kurz klicken:
    -direkt in Bearbeitungsmodus
    -im Bearbeitungsmodus auch Abschließen und löschen möglich
  beim löschen popup und nachfragen
  nach Abschließen nicht mehr anzeigen löschung nach begrenztem Zeitraum oder maximaler anzahl an datensätzen (evt 30tage)
  wiederholende Tasks tauchen wieder auf nach Abschließen (nicht die Beschreibung löschen)


  Task
    .Titel: ajklsdglaksdng
    .Beschreibung: kjabsdfklajsdbgkjbadsg
    .Coins: 202
    .DeadlineDatum(optional)
    .WiederholenderTask: boolean
    .WiederholungsFrequenz: (Wöchentlich,Täglich,Monatlich, alle..Tage,...)
    .Projekt

rewards
  .Titel
  .Kosten
  .mehrfach einlösbar

Projekt
  .Titel
  .Geteilten
  .Mitglieder
