#naming #process

Namensgebung als Prozess würde ich das  Konzept von Arlo Belshee nennen, dass er im Englischen "naming as a process" nennt. [Arlo Belshee](https://arlobelshee.com/tag/naming-is-a-process/)

Es gibt noch sein früheres Konzept, in dem er von 7 Schritten spricht, diese hat er in der aktuellsten Version auf 4 ähnliche reduziert, wie man im unteren Bild sehen kann. Die Artikel über den einzelnen Punkten stehen dabei für die Artikel, die ich auch oben verlinkt habe, die die einzelnen Schritt jeweils genauer beschreiben.

![[naming_as_a_proceess.png]]

Dabei gibt es 4 Schritte, die man durchführen kann. 

## Schritt 1: Schreib offensichtlichen Schwachsinn hin. 
Namen, die offensichtlich nichts über den Inhalt aussagen, können tatsächlich eine Verbesserung sein. Und zwar gegenüber fehlenden Namen und gegenüber irreführenden Namen. 

Wenn ich ein Konzept im Code habe, das irgendetwas tut, ich dem Ding aber keinen Namen gegeben habe, dann kann ich es auch nicht referenzieren. Höchstens mit "ja Dings halt". So kann man das nicht überarbeiten oder wieder verwenden. 

Schlimmer sind nur noch irreführende Namen `savesToDatebase()` und dann passiert das überhaupt nicht. Ja komisch, wo kommt denn der Bug nur her? 

In beiden Situationen kann es helfen, die entsprechenden Methoden, Variablen oder Klassen mit offensichtlichen Quatschnamen zu benennen. Wenn ich meine Methode "Holger" nenne, kann ich sie wenigstens verwenden und weiß, dass an der, der und der Stelle "Holger" gemacht wird - was auch immer das dann heißt. 

Natürlich ist das dann wieder verbesserungswürdig. Aber es kann ein Zwischenschritt sein und ist besser als ein Kommentar `#careful: does not actually save to database` über der Methode `savesToDatabase()` , den man im Zweifel überliest.

## Schritt 2: Finde raus, was es wirklich tut
Jetzt wird es Zeit ehrlich zu sein und auch mal Schwäche zu zeigen. Wenn du weißt, dass die Methode `holger()` irgendwie etwas aus einer Datei liest und in einem Objekt speichert, dann gehört in den Methodennamen nicht nur, das was du weißt, sondern auch das, was du nicht weißt. So etwas wie `initializeFromFile_AndMore()` enthält die Info, dass ein Objekt aus einer Datei initialisiert wird. Und dass da noch irgendwas anderes passiert, was man gerade noch gar nicht so genau weiß. Aber damit kann man ja jetzt erstmal besser weiter arbeiten und bei der nächsten Refactoring Runde oder wenn der nächste dran vorbei kommt und mit dieser Methode arbeiten muss, findet er vielleicht mehr raus und kann den Methodennamen entsprechend anpassen zu `initializeFromFile_AndDeletesFile` oder was auch immer die Methode wirklich tut.

## Schritt 3: Kleinschneiden


## Schritt 4: Kontext aufzeigen

