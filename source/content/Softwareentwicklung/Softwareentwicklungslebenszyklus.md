Der Softwareentwicklungs-Lebenszyklus (SDLC) beschreibt mehrere Aufgaben, die zum Erstellen einer Softwareanwendung notwendig sind. Der Entwicklungsprozess durchläuft mehrere Phasen, während Entwickler neue Funktionen hinzufügen und Störungen in der Software beheben, wobei die Phasen und deren Aufgaben je nach Modell unterschiedlich logisch und zeitlich zusammen hängen. Dadurch erfordert jedes Modell unterschiedliche Herangehensweisen ans Testen. 
### Sequenzielles Modell - Sequential Model
Im **sequenziellen** Softwareentwicklungs-Lebenszyklus wird eine Phase und eine Aufgabe nach der anderen abgearbeitet. Die nächste Phase soll erst beginnen, wenn die vorherige abgeschlossen ist. In der Theorie gibt es dabei keine Überlappung dieser Phasen. In der Praxis ist es jedoch von Vorteil, früher Feedback aus der folgenden Phase zu bekommen und einzubeziehen. 

Generell kann hier zwischen Entwurfs-, Implementierungs- und Testphasen unterschieden werden. Zunächst werden Entwürfe gemacht, diese werden implementiert und dann getestet. 
Zwischen den Phasen wird bei gegen die vorherige Phase **verifiziert**, das man noch "auf dem richtigen Weg ist", indem überprüft wird, dass Dokumente, Designs, der Code etc. in sich stimmig sind und die notwendigen Kriterien erfüllen. 
In der oder den Testphasen wird dann **validiert**, dass die Software das tut, was erwartet wird. Hier wird das tatsächliche Produkt getestet. 

Es gibt zwei sehr bekannte Modelle für dieses sequenzielle Vorgehen, das Wasserfall-Modell und das V-Modell. 
#### Wasserfallmodell
![[Wasserfallmodell.excalidraw]]
#### V-Modell nach Boehm
Das V-Modell nach [Boehm](https://de.wikipedia.org/wiki/Barry_W._Boehm) ist weiterhin weit verbreitet. Das angepasste V-Modell XT ist sogar der Standard für IT-Entwicklungsprojekte der Bundesrepublik Deutschland. Dabei kommt das V im Namen durch die Gegenüberstellung der Entwicklungsphasen gegenüber der Qualitätssicherung, wodurch ein V aufgebaut wird. 

![[VModell.excalidraw]]

In der Umsetzung kann man sich das so vorstellen:

Das Design einer neuen Shop-Software besteht aus
* einer **Anforderungsspezifikation** durch die Business Experten
* einer **funktionalen Spezifikation** durch Requirement Engineers gemeinsam mit Business Experten
* einem **technischen Design** durch System Architekten 
* der **Komponentenspezifikation** durch Senior Softwareentwickler.
Wobei jede Spezifikation auf die vorherige aufbaut und ihre Entscheidungen weiter spezifiziert. Zur **Verifikation** wird jeder Entwurf auf Sicherheits- und Zuverlässigkeitskriterien untersucht und kontrolliert, ob die neue Spezifikation mit der aus der vorherigen übereinstimmt. 

Dann erfolgt die **Implementierung** der Spezifikation.

Dann kommen die Testphasen, wobei
* die **Komponententests** durch verschiedene Entwickler geschrieben werden,
* die **Integrationstests** und **Systemtests** von einem seperaten Testteam durchgeführt werden,
* die **Akzeptanztests** durch die Business Experten erfolgen.

Wie man schon beim Lesen merkt, ist das ganze ein linearer Prozess. Und dabei merkt man eigentlich auch schon wo die Nachteile an sequenziellen Modellen liegt: Man bekommt nur sehr spät Feedback. Wenn ich als Entwicklerin in der Implementierung feststelle (oder beim Lesen der Komponentenspezifikation weiß), dass etwas nicht so umzusetzen ist, wie ich es gewünscht ist, dann haben diese Erkenntnisse keinen Einfluss auf die Anforderungen - es ist dann an den Softwareentwicklern einen Weg zu finden, diese Anforderungen "einfach" doch zu erfüllen. Auch wenn die ausführlichen Testphasen gegenüber dem Wasserfall Modell ein Fortschritt sind, sind sie immer noch sehr spät an der Reihe. Die Akzeptanztests kommen als aller letztes. Und das Feedback daraus kann eigentlich nur sein, dass das Projekt erfolgreich war, weil es alle Akzeptanzkriterien erfüllt oder dass es nicht erfolgreich war, weil nicht alle Anforderungen erfüllt wurden. Für mich ist es super riskant, das Feedback zu "ist das, was ich hier mache, so richtig?" so spät erst zu holen. Stellt euch vor, ihr wollt ein Haus bauen. Und dann redet ihr am Anfang einmal mit dem Bauleiter und dem Architekten und dann hört ihr nichts mehr davon, bis euch das Haus nach einem Jahr vor die Nase gesetzt wird, inklusive der Anordnungen der Steckdosen. Was ist, wenn es ein Missverständnis gab? Was ist, wenn ihr einfach euren Geschmack oder eure Anforderungen geändert habt? Dann ist das Haus zwar erfolgreich - ihr seid aber trotzdem unzufrieden. 

Das klappt allenfalls für ganz kleine Projekte, die schnell gehen, sehr deutliche Anforderungen haben und von null auf gebaut werden. Spätestens wenn Legacy Code ins Spiel kommt, klappt das einfach nicht mehr.

Diese Erfahrung habe nicht nur ich gemacht, sondern hunderte und tausende andere. Deshalb ist eine weitere Art der Modelle entstanden: Die Iterativ-Inkrementellen Modelle. 