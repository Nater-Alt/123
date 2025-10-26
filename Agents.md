2. Programmieraufgabe

Programmierparadigmen
LVA-Nr. 194.023
2025/2026 W
TU Wien

Kontext
Die Simulation aus der ersten Programmieraufgabe ist viel zu oberflächlich. Hauptsächlich geht es darum, Simulationen besser an die Realität
in der Natur anzupassen und zuverlässigere Ergebnisse zu erzielen, ohne
den Aufwand unnötig in die Höhe zu treiben. Verbesserungen sollen vor
allem in folgende Richtungen gehen:
• Das Umfeld genauer betrachten und alle als wesentlich erachteten
Faktoren in die Simulation einbeziehen (Modell vervollständigen).
• Beziehungen zwischen den Elementen des Modells genauer analysieren und darstellen (Modell verfeinern).
• Simulationsergebnisse mit in der Natur ermittelten Werten in Einklang bringen (Rückkopplung und Justierung von Parametern).

Themen:
Aufwandsabschätzung,
Programmiereffizienz,
Überblick über
prozedurale und
objektorientierte
Programmierung

Ausgabe:
20. 10. 2025

Abgabe (Deadline):

Welche Aufgabe zu lösen ist

27. 10. 2025, 13:00 Uhr

Simulation verbessern. Die Lösung der 1. Aufgabe ist deutlich zu verbessern. In jede der drei unter „Kontext“ genannten Richtungen sind
Verbesserungen nötig. Es ist nicht vorgegeben, wie diese Verbesserungen
genau ausschauen sollen. Die folgenden drei Absätze weisen auf Verbesserungspotentiale hin, schreiben aber nicht vor, was genau zu tun ist.

Abgabeverzeichnis:

Modell vervollständigen. Das Modell könnte so vervollständigt werden:

Programmaufruf:

• Es gibt sehr viele Arten von Wildbienen, teilweise auf ganz bestimmte Blütenpflanzen spezialisiert, mit unterschiedlichen Anforderungen an Nistplätze und in unterschiedlichen Zeiträumen aktiv.
Das Modell soll zwischen diesen Arten unterscheiden und auf ihre
Lebensbedingungen Rücksicht nehmen.
• Wildbienen reagieren empfindlich auf Entfernungen zwischen Nistund Nahrungsressourcen. Es reicht also nicht, irgendeinen Teil einer großen landwirtschaftlichen Fläche für Blütenpflanzen vorzusehen, sondern es müssen kleinräumige Strukturen gebildet werden,
in denen Bereiche mit blühenden Pflanzen nicht weit entfernt sind.
Entfernungen zwischen Nistplätzen und Nahrungsquellen sollen in
die Simulation einbezogen werden.
• Wildbienen reagieren empfindlich auf Störungen und Veränderungen der Umweltbedingungen. Es wird kaum möglich sein, Umweltbedingungen über so lange Zeiträume, die simuliert werden sollen,
konstant zu halten. Daher sollen Veränderungen von Umweltbedingungen in die Simulation einbezogen werden. Das betrifft beispielsweise auch Feldfruchtfolgen (zur Bodenschonung in aufeinander folgenden Jahren unterschiedliche Kulturpflanzen), die als Störungen
betrachtet werden können.
1

Aufgabe1-3

java Test

Grundlage:
Skriptum,
Abschnitt 2.1 und 2.2

• Wildbienen sind nicht die einzigen Bestäuber von Blütenpflanzen.
Die Bestäubungsleistung kann teilweise von anderen Insekten, etwa
Honigbienen und Schwebfliegen übernommen werden, auch wenn
diese Bestäuber weniger effektiv sind. Vereinfacht kann man die
Anwesenheit dieser Bestäuber als gegeben annehmen, aber auch eine Simulation der Lebensgewohnheiten anderer Insekten kann sinnvoll sein. Die Anwesenheit von Honigbienen kann gezielt beeinflusst
werden, was auch in die Simulation einfließen soll.
• Andere Bestäuber sind nicht nur teilweiser Ersatz für Wildbienen,
sondern auch Nahrungskonkurrenten, die die Verfügbarkeit von Blütennektar reduzieren. Das sollte simuliert werden. Wildbienen sind
durch ihren hohen Spezialisierungsgrad sehr effektive Bestäuber, für
die Pflanzen bei gleicher Bestäubungsleistung weniger Nektar produzieren müssen als für andere Bestäuber. Es bringt einer Pflanze
daher Vorteile, von einer Wildbiene bestäubt zu werden, was zu
einer etwas besseren Wuchskraft führen kann.
• Pflanzen entwickeln sich nicht nach einem fixen Schema, wie in der
1. Aufgabe angenommen. Unterschiedliche Pflanzen haben unterschiedliche Strategien. Zumindest die Temperatur ist ein Faktor,
der bezüglich Wachstum und Blühzeitpunkt berücksichtigt werden
sollte. Manche Pflanzen blühen mehrfach und können mehrmals im
Jahr Früchte entwickeln. Auch nahe beieinander wachsende Pflanzen können ganz unterschiedlich besonnt sein, wodurch die Sonnenstunden kein besonders gut geeignetes Mittel zur Synchronisation
des Blühbeginns sind. Viele Pflanzen können sich über chemische
Substanzen koordinieren oder den Blühbeginn von der Anwesenheit von Insekten abhängig machen, genau so wie Wildbienen ihre
Aktivitäten vermutlich an das Vorhandensein von Blüten anpassen.
• In praktisch keinem Fall trifft die Annahme zu, dass die Qualität
und Menge von Samen von der Wachstumskraft am Ende der Vegetationsperiode abhängt. Samen bilden sich oft viel früher und
Pflanzen sterben danach ab oder gehen in einen anderen Modus
über, in dem sie sich auf die Ruhephase vorbereiten. Hinter der Vermehrung und Wuchskraft vergleichsweise langlebiger Blütenpflanzen wie Kirsch- oder Apfelbäumen stecken ganz andere Mechanismen als hinter einjährigen Pflanzen. In Bezug auf die Vermehrung
sollen wesentlich ausgefeiltere Mechanismen modelliert werden.
Modell verfeinern. Im Modell aus der 1. Aufgabe sind viele Zahlen fix
einkodiert, etwa die Änderung der Wildbienenpopulation abhängig vom
Nahrungsangebot. Derart fixierte Änderungen gibt es in der Natur nicht.
Wir könnten das Modell vervollständigen, indem wir etwa das Fortpflanzungsverhalten unterschiedlicher Wildbienenarten im Detail simulieren.
Aber so genaue Simulationen würden den Aufwand immens in die Höhe
treiben. Es bleibt uns nichts anderes übrig, als mit groben Annäherungen
an die Realität zu arbeiten. Wir können jedoch dafür sorgen, dass kleinste
Änderungen der Daten keine großen Auswirkungen nach sich ziehen und
genauere Ausformungen an Stellen, an denen sie sich als sinnvoll erweisen,
ermöglicht werden. Das Modell könnte z. B. so verfeinert werden:
2

• Statt mit einfachen gleichverteilten Zufallszahlen in gewissen Wertebereichen soll mit Wahrscheinlichkeitsverteilungen gearbeitet werden, die der Natur abgeschaut sind. Wertebereiche werden damit
meist größer, aber die gewählten Werte sind realistischer.
• Änderungen bestimmter Werte sollen nicht linear mit einem fixen
Faktor oder Prozentsatz erfolgen, sondern in Abhängigkeit von der
Größe, durch die die Änderung veranlasst wurde. Beispielsweise soll
sich die Wuchskraft einer Pflanze bei geringfügiger und kurzzeitiger
Überschreitung der Feuchtegrenzen nur geringfügig auswirken, bei
starker oder lang anhaltender Überschreitung dagegen stark, mit
kontinuierlichen Verläufen statt sprunghaften Änderungen.
• Unterschiedliche Wildbienenarten und Blütenpflanzen haben unterschiedliche Lebensgewohnheiten. Es soll möglich sein, das Modell
modular so zu erweitern, dass Simulationen der Lebensgewohnheiten einzelner Populationen hinzugefügt und auch wieder entfernt
werden können, ohne die Struktur des restlichen Modells anpassen zu müssen. Beispielsweise können die Lebensgewohnheiten in
Java-Klassen beschrieben sein, die ein gemeinsames Interface implementieren; Instanzen dieses Interfaces (also Objekte) können in
die Simulation eingebunden werden.
• So wie Lebensgewohnheiten von Populationen als Objekte zur Simulation hinzugefügt werden können, sollen auch Ereignisse als Objekte zur Simulation hinzugefügt werden können. Beispielsweise könnte es Klassen und entsprechende Objekte geben, die die Auswirkungen gelegentlicher Naturereignisse (Gewitter, Sturm, Hangrutschung, . . . ) oder sonstiger Störungen (Mahd, Ernte, Fruchtwechsel, . . . ) simulieren. Auch Wahrscheinlichkeitsverteilungen sollen auf
diese Weise flexibel austauschbar sein.
• Wenn wir schon dabei sind, Schnittstellen zur Erweiterung des Modells anzubieten, können wir das gesamte Modell gleich modular
aufbauen, sodass alle simulierten Populationen, Ereignisse, etc. über
Objekte eingebunden werden. Entscheidend ist dabei, eine möglichst flexible Form der Kommunikation zwischen den einzelnen Modularisierungseinheiten zu ermöglichen (also die „richtigen“ Methoden in den Interfaces vorzusehen), sodass die Struktur des Modells
der Vervollständigung und Verfeinerung nicht im Weg steht.
Modell justieren. Ohne Bezug zur Realität wären Simulationen sinnlos. In einem gut strukturierten Modell soll es möglich sein, Parameter
so anzupassen, dass Simulationsergebnisse gut zu Beobachtungen in der
Realität passen. Der Begriff „Parameter“ ist dabei in einem weiten Sinn
zu verstehen, nicht nur als Methodenparameter. Parameter können in der
Simulation verwendete elementare Werte, aber etwa auch Wahrscheinlichkeitsverteilungen sein. Wir können dafür sorgen, dass das Modell besser
justierbar wird und wir können reale Daten einbeziehen:
• In einigen Fällen kennen wir die Natur recht genau und können
daher auch mit genauen realen Daten arbeiten. Ein Beispiel ist die
Tageslänge abhängig von Standort und Jahreszeit.
3

• Wir können die Witterung nicht nur abstrakt simulieren, sondern
reale Wetterdaten vergangener Jahre als Grundlage verwenden.
• Auch ohne jahrelange Feldversuche können wir auf viele bekannte
Daten zurückgreifen. Beispielsweise sind typische Blütezeiten realer
Blütenpflanzen leicht zu eruieren und wir können überprüfen, ob
diese Pflanzen auch in der Simulation zur richtigen Zeit blühen und
die Simulation bei Bedarf anpassen.
• Alle für uns interessanten mathematischen Funktionen auf realen
Zahlen können beliebig genau durch Polynome angenähert werden.
Praktisch reichen für unsere Zwecke Polynome niedriger Potenzen.
Jedes Modell lässt sich so parametrisieren, wie wir es in der Realität
beobachten, wenn wir jede Einflussgröße als Polynom betrachten,
dessen Koeffizienten für alle niedrigen Potenzen wir beliebig einstellen können. Auf diese Weise können wir für Justierbarkeit sorgen.
• Parameter sind nicht nur reale Zahlen oder Funktionen auf realen
Zahlen. Wenn wir Objekte beliebiger Klassen (bzw. von Unterklassen bestimmter Typen) als Parameter einsetzen können, haben wir
weitere Möglichkeiten, die es erlauben, Teile des Modells beliebig
genau an die Realität anzunähern.
• Unabhängig von der eigentlichen Simulation können wir Parameter (idealerweise als Polynome betrachtet) als Korrekturwerte der
Ergebnisse vorsehen. Damit lassen sich leicht alle gewünschten Ergebnisse einstellen. Allerdings bedeutet das auch, dass wir etwas
simulieren, was sich in der Realität sicher nicht so abspielt.
• Viele Systeme und Modelle zeigen chaotisches Verhalten, wobei winzige Änderungen große Auswirkungen haben. So lange sich die Simulation ähnlich chaotisch verhält wie die Realität, ist an der Simulation nichts falsch. Aber die Simulation sollte kein chaotisches Verhalten zeigen, das in der Realität nicht beobachtbar ist. Wir können
die Simulation dahingehend analysieren, wo chaotisches Verhalten
auftritt und die Simulationsgenauigkeit dort gezielt erhöhen.
Funktionsumfang. Bestimmen Sie selbst den Funktionsumfang Ihres
Programms. Das Programm soll möglichst viel der nötigen (vorgeschlagenen oder selbst gefundenen) Funktionalität abdecken und über Testfälle
überprüfen. Jedoch sollte zumindest je eine Maßnahme getroffen werden,
um das Modell zu vervollständigen, zu verfeinern und zu justieren oder
justierbar zu machen.
Testen Das Programm soll wie in der 1. Programmieraufgabe nach neuerlicher Übersetzung mittels java Test vom Verzeichnis Aufgabe1-3 aus
aufrufbar sein und die selbst gewählte Funktionalität überprüfen. Tests
sollen ohne Benutzerinteraktion ablaufen, sodass Aufrufer keine Testfälle
auswählen oder Testdaten eintippen müssen.

4

Funktionsumfang
selbst wählen

im richtigen Verzeichnis
testen

Paradigmen und Kommentare Neben nominaler Abstraktion dürfen
Sie auch Lambda-Abstraktion einsetzen. Jedoch soll jede nominale Abstraktion mit Kommentaren versehen sein, die die Abstraktion erläutern.
Setzen Sie Programmierstile des objektorientierten und des prozeduralen Paradigmas gemischt ein. Bitte streuen Sie in Ihr Programm an mindestens 5 relevanten Stellen je einen Kommentar ein, der mit „STYLE:“
beginnt und eine Erklärung enthält, welchem Paradigma der an dieser
Stelle verwendete Programmierstil entspricht und woraus das ersichtlich
ist. Abstraktionen müssen zum Paradigma passen. Dort, wo ein objektorientierter Stil verwendet wird, achten Sie bitte darauf, dass der betreffende Programmteil ausschließlich durch Abstraktionen verständlich ist
sowie der Klassenzusammenhalt hoch und die Objektkopplung schwach
ist. Sorgen Sie dafür, dass auch Untertypbeziehungen vorkommen. An
Grenzen, an denen Stile unterschiedlicher Paradigmen aneinanderstoßen,
machen Sie bitte klar, wie die Paradigmen zusammenwirken.
Neben Programmtext soll die Datei Test.java als Kommentar am
Dateianfang die Grobstruktur und den (geplanten) Funktionsumfang der
Lösung zusammenfassen sowie eine kurze, aber verständliche Beschreibung der Aufteilung der Arbeiten auf die einzelnen Gruppenmitglieder
enthalten (wer tatsächlich was gemacht hat, nicht die geplante Aufteilung), nicht nur für die erste Aufgabe, sondern auch für diese.

nominale Abstraktion
nur mit Kommentaren
Paradigmen erläutern
(mind. 5 Stellen)

Klassenzusammenh. hoch,
Objektkopplung schwach,
Untertypbeziehungen

beschreiben: Struktur,
Funktionsumfang,
Aufgabenaufteilung

Wie die Aufgabe zu lösen ist
Die oben aufgezählten Vorschläge zur Verbesserung der Simulation sind
als Anhaltspunkte gedacht. Sie können Punkte weglassen, abändern oder
durch andere sinnvoll erscheinende Verbesserungen ersetzen.
Eine Schwierigkeit besteht in der richtigen Abschätzung des Umfangs
der Arbeiten. Planen Sie nach Ihren Fähigkeiten möglichst viel ein, das
Sie in der vorgesehenen Zeit zum Abschluss bringen können – das heißt,
so viel Sie können, aber nicht mehr. Als groben Anhaltspunkt sollten Sie
(jedes Gruppenmitglied) etwa elf mit intensiver Arbeit gefüllte Stunden
investieren, keinesfalls mehr als fünfzehn. Versuchen Sie, so effizient wie
möglich zu arbeiten und rasch zu einer brauchbaren Lösung zu kommen.
Ignorieren Sie Details, die Ihnen unwichtig erscheinen. Bedenken Sie, dass
Sie Ihre Lösung durch Testfälle überprüfen sollen und planen Sie Zeit für
die Entwicklung der Testfälle und die Fehlerbeseitigung ein.
Erstellen Sie zuerst ein Konzept Ihrer geplanten Arbeiten. Schicken
Sie es frühzeitig an Ihre_n Tutor_in. Sie werden so bald wie möglich
erfahren, ob das Konzept ausreicht oder Änderungen nötig sind.
Eine Schwierigkeit ist der gleichzeitige Umgang mit mehreren Paradigmen. Sie müssen das prozedurale und objektorientierte Paradigma
verwenden und den Übergang zwischen den Paradigmen in Kommentaren nachvollziehbar beschreiben. Lesen Sie Unterscheidungskriterien im
Skriptum nach. Es wird dazu geraten, die Anzahl der Übergänge zwischen den Paradigmen klein zu halten. Im objektorientierten Teil ist auf
hohen Klassenzusammenhalt, schwache Objektkopplung und die Verwendung von Untertypbeziehungen zu achten.
Für die ersten drei Aufgaben weisen Tutor_innen Sie einige Zeit nach
der Abgabe bei Bedarf auf konkrete Fehler hin und bittet um Beseitigung.
Dies wirkt sich nur dann auf Ihre Beurteilung aus, wenn Sie der Bitte nicht
5

Konzept an Tutor_in

Paradigmen kombinieren

nachkommen. Sie sollten selbst (auch ohne Feedback) ein Gefühl für die
Qualität Ihrer Lösungen entwickeln. Wegen der großen Zahl erwarteter
Fehler können Tutor_innen nicht auf jede Kleinigkeit eingehen.

Warum die Aufgabe diese Form hat
Bei allen anderen Aufgaben geht es darum, am Ende eine vollständige
und perfekte Lösung abzuliefern. In dieser Aufgabe kann man ein solches
Ziel zwar anstreben, aber nicht erreichen. Unter Einhaltung der Bedingungen ist es unmöglich, eine perfekte Lösung zu produzieren. Vielmehr
geht es darum, dass Sie Ihre eigenen Fähigkeiten und Grenzen beim Programmieren unter Zeitdruck als Einzelperson und Gruppe kennenlernen.
Sie sollen selbst erkennen, wo Ihre Stärken liegen und zu welchen Arten
von Fehlern Sie eher neigen (auf allen Ebenen von der Problemanalyse
bis hin zum Testen ebenso wie hinsichtlich der Zusammenarbeit in der
Gruppe). Im Hinblick darauf gibt es keine richtigen und falschen Lösungen. Es ist aber erkennbar, wie sehr Sie sich darum bemüht haben, eine
beinahe unlösbare Aufgabe so gut wie möglich zu lösen.
Das Feedback durch die Tutor_innen wird genau darauf abzielen:
Haben Sie sich ausreichend darum bemüht, in möglichst vielen Bereichen
etwas Machbares zu machen, oder sind in zu vielen Bereichen keine Ansätze erkennbar? In letzterem Fall werden Tutor_innen Nachbesserungen
verlangen, aber nicht, wenn aus Zeitdruck irgendwelche kleine Fehler passiert sind, mit denen bei einer solchen Aufgabe immer zu rechnen ist.
Sie sollen möglichst große Freiheit bei der Lösung der Aufgabe haben
und selbst die Verantwortung für alles übernehmen. Niemand schreibt
Ihnen vor, wie die Aufgabenstellung genau zu verstehen ist.
Diese Aufgabe stellt hohe Anforderungen an jedes Gruppenmitglied
und die Zusammenarbeit in der Gruppe – eine Nagelprobe für das Funktionieren der Gruppe und zum Aufdecken möglicher Schwachstellen.
Nebenbei bietet es sich an, die Aufgabe zur Vertiefung eines überblicksartigen Verständnisses von Paradigmen einzusetzen. Der Schwerpunkt liegt auf der objektorientierten Programmierung (bei einem intuitiven Zugang) im Unterschied zur prozeduralen Programmierung.

1. Programmieraufgabe

Programmierparadigmen
LVA-Nr. 194.023
2025/2026 W
TU Wien

Kontext
Bienen leisten einen entscheidenden Beitrag zur Vermehrung von Blütenpflanzen und sind für die Nahrungsmittelproduktion unverzichtbar. Imker streichen gerne heraus, dass ihre Honigbienen zu den allerwichtigsten
Nutztieren zählen und die Nahrungsmittelproduktion ohne sie drastisch
zurückgehen würde. Ergebnisse aktueller Untersuchungen schüren jedoch
Zweifel an solchen Darstellungen. Für einen Überblick siehe:
https://www.fibl.org/fileadmin/documents/shop/1633-wildbienen.pdf

Etwa 78% aller Blütenpflanzenarten der gemäßigten Breiten sind für ihre
Bestäubung auf Insekten wie Bienen, Wespen, Fliegen und Käfer angewiesen, unter den wichtigsten Kulturpflanzen 80%. Dafür am wichtigsten
sind Bienen, die in Mitteleuropa mit etwa 750 Arten vertreten sind. Den
Großteil der Bestäubungsleistung übernehmen Wildbienen (dazu zählen
solitäre Bienen und Hummeln) sowie zu einem kleinen Teil Schwebfliegen. Honigbienen erbringen höchstens ein Drittel der Bestäubungsleistung. Wildbienen erhöhen den Fruchtansatz landwirtschaftlicher Kulturen sogar dort, wo Honigbienen häufig sind. Honigbienen können die
Bestäubungsleistung durch Wildbienen ergänzen, aber nicht ersetzen. Einige Kulturpflanzen wie Rotklee, Luzerne oder Tomate sind auf spezialisierte Wildbienenarten angewiesen, da Honigbienen sie meiden.
Wildbienen sind gefährdet (25% bis 68% der Arten) und müssen durch
gezielte Maßnahmen gefördert werden. Die Erhaltung blüten- und kleinstrukturreicher Lebensräume hat höchste Priorität. Vor allem eine enge
Nachbarschaft von Nahrungs- und Nistressourcen (z. B. besonntes Totholz
oder vegetationsarme Bodenstellen) und ein kontinuierliches Blütenangebot sind von entscheidender Bedeutung.

Aufgabe:
Simulation von Blütenpflanzen- und Wildbienenpopulationen
Zur Förderung von Wildbienen wird ein Teil einer landwirtschaftlichen
Fläche für den Bewuchs mit verschiedenen Blütenpflanzen reserviert. Über
Simulationen soll geklärt werden, welche Zusammensetzungen der Pflanzenarten erfolgversprechend sind. Ausgehend von einer Wildbienenpopulation und Populationen verschiedener Blütenpflanzen wird simuliert, wie
sich diese Populationen über einen langen Zeitraum entwickeln, wobei die
Entwicklungen von vorgegebenen Eigenschaften der Blütenpflanzen und
zufällig generierten Witterungsverläufen abhängen.
Eine Simulation kann die immense Komplexität tatsächlicher Vorgänge in der Natur nicht mit vertretbarem Aufwand nachahmen. Wir müssen
daher mit einem grob vereinfachten Modell arbeiten:
Jahresverlauf: Zu simulieren sind jährliche Vegetationsperioden von 240
Tagen (März bis Oktober). In dieser Zeit wird täglich eine Neubewertung vorgenommen. Das restliche Jahr bildet eine Ruhephase.
Die Bewertung der Ruhephase erfolgt in einem einzigen Schritt.
1

Themen:
Aufbau der Zusammenarbeit in der Gruppe,
Einrichten einer
Arbeitsumgebung,
Modularisierung,
nominale Abstraktion

Ausgabe:
13. 10. 2025

Abgabe (Deadline):
20. 10. 2025, 13:00 Uhr

Abgabeverzeichnis:
Aufgabe1-3
Hochladen ins GitRepository mittels push
auch eingebundene
Pakete hochladen
(außer Standard-Pakete)

Programmaufruf:
java Test

Grundlage:
Kapitel 1 des Skriptums

Witterung: Die Witterung wird während der Vegetationsperiode täglich durch die Sonnenscheindauer d und Änderung der Bodenfeuchte
(Niederschlag bzw. Austrocknen) an diesem Tag simuliert. Vereinfachend soll d eine Zufallszahl zwischen 0 und 12 sein (Tageslänge immer gleich). Ab Beginn der Vegetationsperiode aufsummierte Werte
der Sonnenscheindauer ergeben die Sonnenstunden h. Die Bodenfeuchte f mit 0 ≤ f ≤ 1 wird am Beginn der Vegetationsperiode
zufällig gewählt und täglich zufällig um bis zu 10% verändert.
Wildbienenpopulation: Diese wird abstrakt durch eine (nicht unbedingt ganze) Zahl x mit x ≥ 0 dargestellt. Näherungsweise kann
man sie als Anzahl gesunder Individuen beliebiger Wildbienenarten
betrachten. Während der Vegetationsperiode wird x täglich angepasst: Sei n das Nahrungsangebot durch blühende Pflanzen (siehe
unten). Ist n ≥ x, wird x um 3% erhöht. Andernfalls (n < x) wird
x um ((6 · n/x) − 3)% erhöht bzw. verringert. Zu Beginn der Simulation ist ein Anfangswert für x gegeben. Während einer Ruhephase
wird x mit einer Zufallszahl zwischen 0.1 und 0.3 multipliziert, um
zu simulieren, dass viele Wildbienen den Winter nicht überstehen.
Blütenpflanzenpopulationen: Jede Art von Blütenpflanzen bildet jeweils eine eigene Population. Jede Population wird abstrakt durch
drei Zahlen yi , bi und si beschrieben, wobei i über die Arten läuft:
• yi mit yi ≥ 0 bezeichnet die Wuchskraft, das ist die näherungsweise Zahl der Wildbienen, die während der Vollblüte durch
die Pflanzenpopulation täglich Nahrung finden.
• bi mit 0 ≤ bi ≤ 1 ist der Anteil, der in Blüte steht.
• si mit 0 ≤ si ≤ 1 ist die Qualität der Samenentwicklung.
Das oben verwendete Nahrungsangebot n entspricht i (yi · bi ), also
der Summe von yi multipliziert mit bi für alle Arten i. Zu Beginn
der Vegetationsperioden sind bi und si gleich 0. Anfangswerte für
yi sind zu Beginn der Simulation gegeben. In Ruhephasen wird yi
+
mit si und einer Zufallszahl zwischen c−
i und ci multipliziert, um
−
die Vermehrung zu simulieren. Dabei sind ci und c+
i für die Pflanzenart i typische Konstanten. Tägliche Anpassungen von yi , bi und
si während Vegetationsperioden beruhen ebenso auf Konstanten:
P

• Die Feuchtegrenzen fi− und fi+ mit 0 < fi− < fi+ < 1 definieren den günstigen Bereich der Bodenfeuchte. Im Fall von
fi− /2 < f < fi− oder fi+ < f < 2 · fi+ (ungünstiger Bereich),
wird yi um 1% reduziert. Gilt sogar f ≤ fi− /2 oder 2 · fi+ ≤ f
(sehr ungünstiger Bereich), wird yi um 3% reduziert.
−
+
+
• Die Blühgrenzen h−
i und hi mit 0 < hi < hi stehen für die
Sonnenstunden, ab denen die Blüte einsetzt bzw. endet. Die
Blühintensität qi mit 0 < qi < 1/15 ist ein Faktor, der angibt,
+
wie rasch die Blüte einsetzt bzw. endet. Gilt h−
i ≤ h < hi
(Blüte setzt ein), wird bi pro Tag um qi · (d + 3) erhöht, bis bi
das Maximum von 1 erreicht, wobei d die Sonnenscheindauer
an diesem Tag ist. Gilt h+
i ≤ h (Blüte endet), wird bi täglich
um qi · (d + 3) verringert, bis bi das Minimum von 0 erreicht.

2

−
• Die Bestäubungswahrscheinlichkeit pi (0 < pi < 1/(h+
i − hi ))
ist die Wahrscheinlichkeit, mit der eine Blüte bei ausreichend
vielen Bienenbesuchen innerhalb einer Sonnenstunde (und zu
einem kleinen Teil auch ohne Sonne) einen Samen ausbildet.
Ausreichend viele Bienenbesuche gibt es bei x ≥ n (Bienenpopulation x mindestens so groß wie Nahrungsangebot n); dann
erhöht sich si pro Tag um pi · bi · (d + 1). Andernfalls erhöht
sich si pro Tag um pi · bi · (d + 1) · x/n.

Für jeden Simulationslauf sind also folgende Parameter festzulegen:
• Anzahl der zu simulierenden Jahre,
• Anfangswert der Wildbienenpopulation x,
• für jede Blütenpflanzenart (Index i läuft über die Arten):
– Anfangswert der Wuchskraft yi ,
+
– für die Art typische Vermehrungsgrenzen c−
i und ci ,

– für die Art günstige Feuchtegrenzen fi− und fi+ ,
+
– für die Art typische Blühgrenzen h−
i und hi ,

– für die Art typische Blühintensität qi ,
– für die Art typische Bestäubungswahrscheinlichkeit pi .
Ergebnisse jedes Simulationslaufs enthalten den Wert der Wildbienenpopulation x und für jede Blütenpflanzenart i die Wuchskraft yi jeweils am
Ende der Ruhephase nach der letzten simulierten Vegetationsperiode.
Das Ziel besteht darin, eine stabile Menge an Blütenpflanzenarten
zu finden, die am Ende von Simulationsläufen über viele Jahre zu einer
großen Wildbienenpopulation führt. „Stabil“ bedeutet dabei, dass die yi
zwar von Jahr zu Jahr (auch stark) schwanken können, aber keine Art
(beinahe) ausstirbt oder (beinahe) ständig nur wächst. Im Idealfall liegt
yi für alle i am Ende der Simulation in derselben Größenordnung wie die
Anfangswerte. Die Parameter der einzelnen Pflanzenarten sollen möglichst unterschiedlich sein, um eine gewisse Robustheit gegenüber zufällig
weniger günstiger Witterung zu erreichen.

Welche Aufgabe zu lösen ist
Programm. Entwickeln Sie ein Java-Programm, das Simulationsläufe
wie oben beschrieben durchführt. Konkret sollen drei Gruppen von Simulationsparametern (also vor allem unterschiedliche Gruppen von Blütenpflanzenarten) festgelegt werden, die möglichst stabil sind. Jede Gruppe
soll zwischen 10 und 25 Blütenpflanzenarten umfassen. Für jede Gruppe sollen 10 Simulationsläufe mit unterschiedlicher Witterung (also mit
unterschiedlichen Zufallswerten) über Zeiträume von jeweils 25 Jahren
durchgeführt werden. Die Parameter und Simulationsergebnisse sind in
möglichst übersichtlicher Weise in Textform auszugeben. Danach, deutlich von den Ergebnissen der eigentlichen Simulationsläufe abgesetzt, sollen zur Überprüfung der korrekten Vorgehensweise für einen Simulationslauf jährliche Zwischenergebnisse und für ein Jahr tägliche Zwischenergebnisse mit allen Zahlen, die Zustände beschreiben, ausgegeben werden.
3

Testen. Testen Sie Ihr Programm sorgfältig, auch bezüglich der Plausibilität von Simulationsergebnissen. Sorgen Sie dafür, dass nach dem
Programmstart keine Benutzerinteraktion (das heißt, keine Eingabe über
die Tastatur oder Maus) nötig ist, sondern einfach nur die nötigen Ausgaben gemacht werden. Das Programm soll (nach neuerlicher Übersetzung aller vorhandenen .java-Dateien) mittels java Test vom Verzeichnis Aufgabe1-3 aus aufrufbar sein. Sie können natürlich davon ausgehen,
dass .class-Dateien an passenden Stellen angelegt werden, aber Sie müssen vor allem bei Verwendung von Paketen für die Ausführbarkeit durch
den vorgegebenen Aufruf im vorgegebenen Verzeichnis sorgen.
Kommentare. Betrachten Sie jede Definition und Deklaration einer Methode als nominale Abstraktion. Beschreiben Sie diese Abstraktionen
durch kurze, aber informative Kommentare. Versehen Sie auch jede Klasse und jedes Interface mit entsprechenden Kommentaren. Eine JavaKlasse kann Elemente unterschiedlicher Modularisierungseinheiten enthalten (Modul, Klasse, Objekt). Beschreiben Sie in den Kommentaren
deutlich, welche Elemente zu welchen Modularisierungseinheiten gehören
und welche Abstraktionen hinter den Modularisierungseinheiten stecken.
Sorgen Sie für eine gute Programmstruktur mit mehreren Klassen.
Neben Programmtext soll die Datei Test.java als Kommentar am
Dateianfang eine kurze, aber verständliche Beschreibung der Aufteilung
der Arbeiten auf die einzelnen Gruppenmitglieder enthalten – wer hat
was gemacht. Beschreibungen wie die folgende reichen nicht: „Alle haben
mitgearbeitet.“ Die Arbeitsaufteilung auf die einzelnen Gruppenmitglieder wird in jeder Aufgabe beschrieben werden müssen. Bitte machen Sie
das sorgfältig (keinesfalls jemand vergessen), weil sich eine stark unterschiedliche Belastung einzelner Gruppenmitglieder über mehrere Aufgaben hinweg auf die Beurteilung auswirken kann.1

Programmname „Test“
aus gutem Grund gewählt

im richtigen Verzeichnis
ausführbar?

Abstraktionen und
Modularisierungseinheiten
kurz beschreiben
(siehe Skriptum)

Arbeitsaufteilung kurz,
verständlich beschreiben

Wie die Aufgabe zu lösen ist
Der Programmtext Ihrer Lösung soll möglichst einfach sein und keine unnötige Funktionalität haben. Er soll wiederverwendbar sein, da die nächste Aufgabe auf Teilen davon aufbaut. Vermeiden Sie jedoch Vorgriffe,
das heißt, schreiben Sie keine Programmteile aufgrund der Vermutung,
dass diese Teile in der nächsten Aufgabe verlangt sein könnten.
Zufallszahlen spielen eine große Rolle, aber auch fest vorgegebene Annahmen. Es kommt auf ein ausgewogenes Verhältnis zwischen algorithmischen Vorgaben, festgelegten Werten und Zufallswerten an. Um gute
Einstellungen zu finden, wird es notwendig sein, mit verschiedenen Werten und Vorgehensweisen zu experimentieren. Bei Simulationen geht es
häufig, nicht nur in dieser Aufgabe darum, passende Parametrisierungen
1

Durch Krankheit oder sonstige Vorkommnisse ist es immer möglich, dass eine Person nicht bei jeder Aufgabe gleich intensiv mitarbeiten kann. Daher hat eine ungleichmäßige Arbeitsaufteilung bei einer einzelnen Aufgabe noch keine direkte Konsequenz.
Es kann aber auch in diesem Fall sein, dass Ihr_e Tutor_in oder die LVA-Leitung nach
einer Ursache dafür fragt. Wenn sich über mehrere Aufgaben hinweg zeigt, dass immer
wieder eine Person deutlich mehr oder weniger macht als die anderen Gruppenmitglieder, wird die Beurteilung für einzelne Gruppenmitglieder unterschiedlich ausfallen.
Dabei werden aber auch die von Ihnen genannten Gründe eine Rolle spielen.

4

einfach halten

experimentieren

zu finden, sodass Simulationsergebnisse das möglichst gut wiedergeben,
was wir in der Realität vorfinden.
Diese Aufgabe hilft Ihren Tutor_innen, Ihre Kenntnisse sowie die Zusammenarbeit in der Gruppe einzuschätzen. Bitte sorgen Sie in Ihrem eigenen Interesse dafür, dass jedes Gruppenmitglied etwa in gleichem Maße
mitarbeitet. Sonst könnten Sie bei einer Fehleinschätzung wertvolle Zeit
verlieren. Scheuen Sie sich bitte nicht, Tutor_innen um Hilfe zu bitten,
falls Sie bei der Lösung der Aufgabe Probleme haben oder keine brauchbare Zusammenarbeit in der Gruppe zustande kommt.

alle arbeiten mit

Warum die Aufgabe diese Form hat
Umfang und Schwierigkeitsgrad der Aufgabe wurden so gewählt, dass die
eigentliche Programmierung bei guter Organisation und entsprechendem
Vorwissen nicht zu viel Zeit in Anspruch nimmt, aber eine Einarbeitung
in neue Themen nötig ist und Diskussionsbedarf entsteht. Nutzen Sie die
Gelegenheit, um die Aufgabenverteilung und interne Abläufe innerhalb
der Gruppe zu organisieren. Details der Aufgabe bleiben bewusst offen:
• Sie sollen in der Gruppe diskutieren, wie Sie die Aufgabe verstehen
und welche Lösungswege geeignet erscheinen.
• Sie sollen sich daran gewöhnen, dass Aufgaben nicht vollständig spezifiziert sind, aber trotzdem Vorgaben eingehalten werden müssen.
• Sie sollen sich eine eigene brauchbare Faktorisierung überlegen und
sich dabei vorerst einmal nur von Abstraktionen leiten lassen.
• Sie sollen auch die Verantwortung für die Korrektheit Ihrer Lösung
(so wie Sie sie selbst verstehen) übernehmen, indem Sie entsprechende Tests durchführen.

Allgemeine Informationen zur Übung
Folgende Informationen betreffen diese und auch alle weiteren Aufgaben.

Was bei der Lösung der Aufgabe zu beachten ist
Unter der Überschrift „Wie die Aufgabe zu lösen ist“ finden Sie Hinweise darauf, wie Sie die Lösung der Aufgabe vereinfachen können und
welche Fallen Sie umgehen sollen, erfahren aber auch, welche Aspekte
bei der Beurteilung als wichtig betrachtet werden. In der ersten Aufgabe
kommt es beispielsweise auf die Einfachheit der Lösung an, aber auch darauf, wie gut die gewählten Algorithmen und angenommenen Werte bzw.
Zufallswerte zusammenpassen. Das heißt, in späteren Aufgaben können
Ihnen bei solchen Hinweisen etwa auch für unnötig komplizierte oder umfangreiche Lösungen Punkte abgezogen werden, weil Sie sich nicht an
die Vorgaben gehalten haben. Außerdem gilt natürlich alles, was in der
Aufgabe beschrieben ist. Beispielsweise müssen Kommentare die gewählten Abstraktionen verdeutlichen und beschreiben, welche Inhalte als Teil
welcher Modularisierungseinheiten anzusehen sind. Unterschiedliche Aufgaben haben unterschiedliche Schwerpunkte. Die nächste Aufgabe wird
5

Schwerpunkte beachten

nicht nach dem gleichen Schema beurteilt wie die vorige. Richten Sie sich
daher nach der jeweiligen Aufgabenstellung.
Ein häufiger Fehler besteht darin, eine Aufgabe nach Gefühl zu lösen
ohne zu verstehen, worauf es ankommt. Meist bezieht sich die Aufgabe
auf ein Thema, das zuvor theoretisch behandelt wurde. Versuchen Sie,
eine Beziehung zwischen der Aufgabenstellung und dem davor behandelten Stoff herzustellen. Achten Sie darauf, Fachbegriffe nicht nur umgangssprachlich zu interpretieren, sondern so wie im Skriptum beschrieben. Die
ersten Aufgaben sind vielleicht auch ohne Skriptum lösbar, bei späteren
Aufgaben würde ein Ignorieren des Skriptums wahrscheinlich zu Fehlern
führen. Als Hilfestellung sind in jeder Aufgabenstellung Teile des Skriptums genannt, in denen die relevantesten Themen behandelt werden, bei
komplizierten Themen oft nur wenige Seiten.
Versuchen Sie nicht, Teile der Aufgabenstellung durch Tricks oder
Spitzfindigkeiten zu umgehen. Beispielsweise gibt es immer wieder Lösungsversuche, in denen die Test-Klasse nur „Test erfolgreich“ ausgibt,
statt sinnvolle Tests durchzuführen. Solche Versuche werden durch händische Beurteilungen mit hoher Wahrscheinlichkeit erkannt. Spätere Aufgaben enthalten oft Schwierigkeiten, die mit Allgemeinwissen alleine oder
über aufgabenbezogene Web-Recherchen bzw. mit Hilfe von KI kaum zu
lösen sind. Gerade in solchen Fällen ist davon abzuraten, die Schwierigkeiten durch Tricks zu umgehen. Hinweise zur richtigen Lösung lassen
sich im Skriptum und auf den Vorlesungsfolien finden.
Ihre Lösung, bestehend aus .java-Dateien, muss am Tag der Abgabe
um 13:00 Uhr pünktlich im Git-Repository Ihrer Gruppe stehen. Übersetzte .class-Dateien sollen nicht ins Repository gestellt werden, da sie
die Zusammenarbeit in der Gruppe erschweren und vor der Beurteilung
ohnehin neu generiert werden. Zugangsinformationen zum Repository erhalten Sie in Kürze. Informationen zum Umgang mit dem Repository
finden Sie in TUWEL. Es wird empfohlen, rechtzeitig vor der Deadline
die Lösung auf dem Übungsrechner auszuprobieren und die Daten dabei durch pull aus dem Repository zu laden. So können Sie typische
Fehler bei der Abgabe (z.B. auf push vergessen, Lösung im falschen Verzeichnis, falsche package- und include-Anweisungen, Klassen aus NichtStandard-Paketen verwendet und nicht mit abgegeben) sowie Inkompatibilitäten aufgrund unterschiedlicher Versionen und Betriebssystemeinstellungen (z. B. Dateinamen mit Umlauten sowie neueste Sprach-Features
nicht unterstützt) erkennen und beseitigen.

Was Ihr_e Tutor_in von Ihnen wissen möchte
Ihr_e Tutor_in wird Ihnen in Kürze eine Mail schreiben, um sich vorzustellen und um Informationen über Sie zu bitten. Geben Sie diese Informationen möglichst bald, damit die für Sie am besten geeignete Form
der Betreuung gewählt werden kann. Unabhängig von der Form der Betreuung kann natürlich jedes Gruppenmitglied jederzeit konkrete Fragen
an Tutor_innen richten. Scheuen Sie sich bitte nicht, sich auch mit organisatorischen oder gruppeninternen Problemen, die Sie möglicherweise
nicht selbst lösen können, an Tutor_innen zu wenden. Früh im Semester
sind Probleme einfacher lösbar als im weit fortgeschrittenen Semester.

6

strukturiert vorgehen

keine Spitzfindigkeiten

ausprobieren




