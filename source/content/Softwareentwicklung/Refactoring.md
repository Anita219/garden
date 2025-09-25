Refactoring kommt aus dem Englischen bedeutet übersetzt **Überarbeitung**. Wenn wir von Softwareentwicklung reden, sprechen wir auch im Deutschen üblicherweise von **refactoring**, seltener von **Refaktorierung**. 

> [!INFO] Inhaltlich bedeutet Refactoring, dass man den Code verändert, ohne sein Verhalten zu verändern. 

Aber warum will man das tun? Kommt es bei Code nicht darauf an was er tut, egal wie er aussieht? **Nein.** Die einzige Situation in der es egal ist, ist wenn du ein Skript schreibst, was du nur ein paar mal kurz ausführst um etwas zu erledigen und dann weg schmeißt. Also beispielsweise für eine einmalige Auswertung von irgendwelchen Daten. Oder um *einmalig* deine Ordnerstruktur aufzuräumen und alles von A nach B zu schieben. Dann ist es egal, Hauptsache der Job ist erledigt.

Sobald du den Code länger benötigst oder jemand anderes auch mit ihm arbeiten soll (das kannst auch du selbst in 1 Jahr sein), lohnt es sich den Code möglichst sauber zu hinterlassen. Stell es dir wie deinen Schreibtisch zuhause vor. Du willst ihn aufrüsten - ein neuer, größerer Schreibtisch soll her. Prima. Du suchst dir einen aus, er wird geliefert und jetzt geht es ans Zusammenbauen und Aufstellen. Geht das so einfach, wenn dein Schreibtisch komplett voll mit Papierkram, Stiften und leeren Colaflaschen liegt? Oder ist es vielleicht einfacher, wenn das Zimmer indem der Schreibtisch steht aufgeräumt ist und du nur schnell den PC abbauen, Schreibtisch aufbauen und dann den PC wieder aufbauen musst? Na? Richtig, letzteres ist viel leichter. Sonst sieht es schnell so aus:

<iframe src="https://giphy.com/embed/RJVyvWomrVuVRXThoM" width="480" height="271" style="" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

Genauso verhält es sich mit Software. Du fängst ein Stück an anzupassen, weil es ein neues Feature geben soll, beispielsweise einfach nur ein neues Textfeld für den Kunden in einem Formular. Doch dann musst du auch das Layout anpassen, damit das Feld auch auf die Seite passt und einen Endpunkt schreiben. Und weil der Endpunkt bisher aber nicht nur für dieses Formular gilt sondern auch für andere, musst du auch andere Formulare anpassen, die gar nichts mit dem ursprünglichen Formular zu tun haben. Und so weiter. Das nennt man **Technische Schuld**. Ein ganz toller Begriff, den Product Owner und Project Manager am liebsten hören :)

Wir überarbeiten also den Code ohne seine Funktionalität zu verändern. Damit wir das können, brauchen wir Tests. Und zwar gute Tests, die uns eine hohe Abdeckung bieten. Dazu später mehr ;)

Wenn wir das haben, können wir Stück für Stück den Code verbessern bis wir ihn für gut genug halten. Hier brauchen wir keine 100% Lösung, die 80% Lösung reicht. Hier gilt die gut alte [[Pfadfinderregel - Hinterlasse es besser, als du es vorgefunden hast]]. Nun kann man das ganze intuitiv machen - oder man richtet sich nach schlauen Menschen wie Martin Fowler und macht das ganze strukturiert. 

Es gibt Regeln, **wann** man refactored und auch **wie** man refactored. Hier findest du eine (unvollständige) Liste, die ich stetig ergänzen werde :)

___
#softwareentwicklung #programmieren #methodik #aufräumen
