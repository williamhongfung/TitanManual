---
id: version-14.0-theatre-programming
title: Theatre Programming Quick Guide
sidebar_label: Theatre Programming
original_id: theatre-programming
---

Wenn Sie bereits mit anderen Theater-Lichtpulten gearbeitet haben, sind
Sie vermutlich eher an das Arbeiten mit Tasten, Nummern und Befehlen als
an Touchscreens wie bei Titan gewöhnt. Aber keine Angst: auch bei Titan
lässt sich eine Show mit Tasten, Nummern und Befehlen programmieren und
fahren.

-	'Richtige' Tasten mit Beschriftungen sind hier als graues Rechteck
	gezeigt, wie z.B. \<Enter\>. 
-	Die \<@\>-Taste ist die direkt bei den Zifferntasten.
-	Die \<Cue\>-Taste heißt auf manchen älteren Pulten noch \<Connect\> oder \<Connect\/Cue\>. 
-	Die \<Thru\>-Taste heißt auf manchen älteren Pulten noch \<Through\>.
- 	Die Tasten \<And\> und \<Thru\> gibt es auf manchen Pulten nicht als
	'richtige' Taste, sondern als Funktionstaste \[And\] bzw. \[Through\].

Dimmer und andere Geräte haben eine User Number (Benutzer-Nummer) (*entspricht  der Channel Number auf anderen Pulten*). Diese wird links oben
in der jeweiligen Schaltfläche angezeigt. In den hier aufgeführten
Befehlen wird die Nummer als **n** dargestellt. Die User Number lässt sich
über das Menü \[Set Legend\] ändern, siehe [Legende eingeben](../patching/changing-the-patch.md#legendenbezeichnungen-eingeben). Auch Gruppen
haben jeweils eine User Number.

![Fixtures Window showing user numbers](/docs/images/Fixtures-Window-showing-user-numbers.png)

## Dimmerwerte setzen

Tasten | Ergebnis
---- | ----
**n** \<@\> \<@\> | Dimmer/Gerät **n** auf 100%
**n** \<@\> **v** \<Enter\> | Dimmer/Gerät **n** auf **v%** *(v ist 2-stellig    einzugeben, also z.B. "50" für 50%)*
**n** \<Thru\> **m** \<@\> **v** \<Enter\> | Dimmer/Geräte **n** bis **m** auf **v%**
**n** \<And\> **m** \<And\> **p** \<@\> **v** \<Enter\> | Dimmer/Geräte **n**, **m**, **p** auf **v%**
\<Group\> **n** \<@\> **v** \<Enter\> | Dimmer/Geräte in Gruppe **n** auf **v%**
\<Clear\> | Sofortiges Release der editierten Kanäle auf den programmierten Status (*wie Cheat auf ETC-Pulten*)
**t** \<Clear\> | Release der editierten Kanäle in **t** Sekunden


## Andere Parameter bei Movinglights etc. einstellen

-   Die Geräte können mit den Tasten wie folgt angewählt werden:

    Tasten | Ergebnis
    ---- | ----
    **n** \<Enter\> | Gerät **n**
    **n** \<Thru\> **m** \<Enter\> | Geräte **n** bis **m**
    \<Group\> **n** \<Enter\> | Geräte der Gruppe **n**


-   Wählen Sie nun die  gewünschte Attributbank, z.B. \<Colour\>, \<Gobo\> etc.
    Die jeweilige Funktion der Wheels wird unten rechts im Bildschirm
    angezeigt. Gibt es mehrere Parameter pro Attributbank, z.B. Gobo1,
    Gobo2, jeweils mit Rotation etc., dann kann man mit wiederholtem
    Drücken der Attributbank-Taste durchschalten (hier also mehrfach auf
    \<Gobo\>).

-   Mit den Encoderrädern stellen Sie die gewünschten Werte ein. Alternativ drückt
    man die blaue \<@\>-Taste bei einem Wheel und kann den Wert mit den
    Zifferntasten eingeben.

## Programmieren von Cues

Titan kann mehrere Cuelisten parallel laufen lassen. Zum Programmieren
einer Cueliste drückt man auf \<Record\> und wählt im Menü \[Create Cue
List\]. Dann drückt man die **Auswahltaste** bei einem Fader, um dort die
Cueliste zu speichern.

Titan speichert normalerweise nur die Dimmer/Geräte, die seit dem
letzten Betätigen von \<Clear\> geändert wurden, und nur, wenn sich
gegenüber dem vorigen Cue Änderungen ergeben. Sind dagegen andere
Playbacks aktiv, werden diese nicht mit in den Cue gespeichert. Will man
doch alles, also alle Dimmer/Geräte, die gerade über 0% sind, speichern,
so wechselt man den Speichermodus \[Record Mode\] auf "Record by Stage" (siehe [Erstellen eines Cues](../cues/creating-a-cue.md#anlegen-eines-cues)).

Tasten | Ergebnis
-------|---------
\<Record\> {blaue Playbacktaste} {blaue Playbacktaste} | speichert den nächsten Cue an das Ende dieser Cueliste
\<Record\> \<Cue\> **n** \<Enter\> | Speichert Cue **n** (existiert bereits ein solcher Cue, erfolgt eine Rückfrage zum Mergen/Überschreiben)
\<Time\> **t** \<Enter\> | Setzen der Fadezeit im Programmer (wird in nachfolgend gespeicherte Cues übernommen; bereits angelegte Cues  bleiben unbeeinflusst)
\<Cue\> **n** \<Time\> **t** \<Enter\> | Setzt Fadezeit für Cue **n** auf **t** Sekunden
\<Delete\> \<Cue\> **n** \<Enter\> \<Enter\> | Löscht Cue **n** (2. \<Enter\> bestätigt)
\<Copy\> \<Cue\> **n** \<@\> \<Cue\> **m** \<Enter\> | Kopieren von Cue **n** in neuen Cue **m**
\<Copy\> \<Cue\> **n** \<@\> \<Enter\> | Kopieren von Cue **n** an das Ende der Cueliste
\<View/Open\> {blaue Playbacktaste} | Azeige der Cues der Liste in tabellarischer Form. Änderungen können direkt durch Anklicken erfolgen.

-	Mit \<Move\> (statt Copy) können Cues verschoben werden.\
	Verfügt das Pult über keine Move-Taste, drücken Sie \<Avo\> und \<Copy\>.

- 	Mehrere Cues auf einmal lassen sich mit den Tasten \<Thru\>, \<And\> 
	und \[Not\] auswählen. Um z.B. die Cues 3, 4 ,5 ,7, 10 zu kopieren und 
	ab Cue 20 einzufügen, drücken Sie \
	\<Copy\> {blaue Playbacktaste} **3** \<Thru\> **7** \[Not\] **6** \<And\> **10** \<@\> **20** \<Enter\>.

-	Zum Erstellen eines Block-Cues (Änderungen werden nicht getrackt) öffnet
	man die Cueliste wie beschrieben, klickt in der Spalte 'Tracking' auf
	die Zelle des entsprechenden Cues und wählt \[Block\] mit den
	Menütasten.

-	Um Cues [miteinander zu verlinken](cue-list-timing.md#schrittfolge-und-versatz), 	klickt man auf die entsprechende Zelle
	der Spalte ‚Link' (dort steht normalerweise ‚Wait For Go'). Dann kann
	man mit den Menütasten auf \[Link After Previous Cue\] oder \[Link With
	Previous Cue\]. Für 'Link After...' bestimmt dann der Wert für 'Delay
	Out', wie lange nach dem vorigen der neue Cue automatisch startet.

## Cues und Cuelisten abfahren

Schiebt man den Fader einer Cueliste hoch, so wird sie mit der Steuerung
verbunden *("connected")* und kann z.B. mit der \<Go\>-Taste gesteuert werden.

Weitere Möglichkeiten zur Steuerung (Auswahl):

Tasten | Ergebnis
-------|---------
\<Cue\> **{blaue Playbacktaste}** | Verbinden einer anderen Cueliste
\<Go\> | Nächster Cue wird mit den programmierten Zeiten eingeblendet
\<Cue\> **n** \<Go\> | Cue n wird mit den programmierten Zeiten eingeblendet
**t** \<Go\> | Nächster Cue wird in **t** Sekunden eingeblendet
**n** \<Cue\> **t** \<Go\> | Cue **n** wird in **t** Sekunden eingeblendet

-	Sollen Movinglights bereits im Off auf Position, in Gobo oder Farbe
	fahren, aktivieren Sie die Funktion [\[Move In Dark\]](cue-list-options.md#move-in-dark).

## Cues live editieren

Oft müssen Änderugnen an bereits programmierten Cues vorgenommen werden,
während diese gerade live sind. Es empfiehlt sich, \<Clear\> zu drücken,
um nicht versehentlich unerwünschte Werte mit zu speichern.

Tasten | Ergebnis
-------|---------
\<Record\> \<Cue\> \<Cue\> | Speichern der aktuell eingestellten Werte in den aktuellen Cue
\<Time\> **t** \<Enter\> \<Record\> \<Cue\> \<Cue\> | Speichern der Fadezeit **t** in den aktuellen Cue

- 	Eine andere Möglichkeit ist, die Cueliste mit \<View\> zu öffnen
    und dort die Änderungen vorzunehmen.


## Shapes und Effekte

You can't select Effects/Shapes from the keypad on Titan, but it's still
easy:

1.   Zu steuernde Geräte wählen

2.   Im Hauptmenü drückt man \[Shapes and Effects\], \[Shape Generator\],
    \[Create\]

3.   Den gewünschten Shape-Typ wählen, z.B. \[Dimmer\], \[Pan/Tilt\] etc.

4.   Den gewünschten Shape wählen (Menütasten oder Shapes-Fenster)

5.   Speed, Size, Spread mit den Wheels einstellen

Shapes können ganz normal in Cues gespeichert werden und tracken in
folgende Cues. Das Shape-Tracking lässt sich In der Playbacks-Ansicht sowie
in den Playback-Optionen getrennt deaktivieren.