I need you to pay attention carefully to the rules provided here and I need you to read all the java files in detail and understand them completley and run them to look at the results. I need you to try to fix this Code Base and make it run using small amounts of changes and additions but do them where necessary. The output has to be correct it is the most important thing, which is why you have to test it until it is right according to what the following text wants from you. We are currently working on Aufgabe 2 which builds on the basis of Aufgabe 1 but changes some of its stuff.

# Aufgabe 1 & 2 — Programmierparadigmen (TU Wien)

## Aufgabe 1

1.  Programmieraufgabe Programmierparadigmen LVA-Nr. 194.023 2025/2026 W
    TU Wien Kontext Bienen
    leisteneinenentscheidendenBeitragzurVermehrungvonBlüten- pﬂanzen und
    sind für die Nahrungsmittelproduktion unverzichtbar. Im- Themen: ker
    streichen gerne heraus, dass ihre Honigbienen zu den
    allerwichtigsten Aufbau der Zusammen- Nutztieren zählen und die
    Nahrungsmittelproduktion ohne sie drastisch arbeit in der Gruppe,
    zurückgehen würde. Ergebnisse aktueller Untersuchungen schüren
    jedoch Einrichten einer Arbeitsumgebung, Zweifel an solchen
    Darstellungen. Für einen Überblick siehe: Modularisierung, nominale
    Abstraktion
    https://www.fibl.org/fileadmin/documents/shop/1633-wildbienen.pdf
    Etwa 78% aller Blütenpﬂanzenarten der gemäßigten Breiten sind für
    ihre Bestäubung auf Insekten wie Bienen, Wespen, Fliegen und Käfer
    ange- Ausgabe: wiesen, unter den wichtigsten Kulturpﬂanzen 80%.
    Dafür am wichtigsten 13.10.2025 sind Bienen, die in Mitteleuropa mit
    etwa 750 Arten vertreten sind. Den Großteil der Bestäubungsleistung
    übernehmen Wildbienen (dazu zählen solitäre Bienen und Hummeln)
    sowie zu einem kleinen Teil Schwebﬂie- gen. Honigbienen erbringen
    höchstens ein Drittel der Bestäubungslei- Abgabe (Deadline): stung.
    Wildbienen erhöhen den Fruchtansatz landwirtschaftlicher Kul-
    20.10.2025, 13:00 Uhr turen sogar dort, wo Honigbienen häuﬁg sind.
    Honigbienen können die Bestäubungsleistung durch Wildbienen
    ergänzen, aber nicht ersetzen. Ei- nige Kulturpﬂanzen wie Rotklee,
    Luzerne oder Tomate sind auf speziali- Abgabeverzeichnis: sierte
    Wildbienenarten angewiesen, da Honigbienen sie meiden. Aufgabe1-3
    Wildbienensindgefährdet(25%bis68%derArten)undmüssendurch Hochladen
    ins Git- gezielte Maßnahmen gefördert werden. Die Erhaltung blüten-
    und klein- Repository mittels push strukturreicher Lebensräume hat
    höchste Priorität. Vor allem eine enge auch eingebundene
    NachbarschaftvonNahrungs-undNistressourcen(z.B.besonntesTotholz
    Pakete hochladen oder vegetationsarme Bodenstellen) und ein
    kontinuierliches Blütenange- (außer Standard-Pakete) bot sind von
    entscheidender Bedeutung. Aufgabe: Programmaufruf: Simulation von
    Blütenpﬂanzen- und Wildbienenpopulationen java Test Zur Förderung
    von Wildbienen wird ein Teil einer landwirtschaftlichen
    FlächefürdenBewuchsmitverschiedenenBlütenpﬂanzenreserviert.Über
    Grundlage: Simulationen soll geklärt werden, welche
    Zusammensetzungen der Pﬂan- Kapitel 1 des Skriptums zenarten
    erfolgversprechend sind. Ausgehend von einer Wildbienenpopu-
    lationundPopulationenverschiedenerBlütenpﬂanzenwirdsimuliert,wie
    sich diese Populationen über einen langen Zeitraum entwickeln, wobei
    die Entwicklungen von vorgegebenen Eigenschaften der Blütenpﬂanzen
    und zufällig generierten Witterungsverläufen abhängen.
    EineSimulationkanndieimmenseKomplexitättatsächlicherVorgän-
    geinderNaturnichtmitvertretbaremAufwandnachahmen.Wirmüssen daher mit
    einem grob vereinfachten Modell arbeiten: Jahresverlauf:
    ZusimulierensindjährlicheVegetationsperioden von240 Tagen (März bis
    Oktober). In dieser Zeit wird täglich eine Neube- wertung
    vorgenommen. Das restliche Jahr bildet eine Ruhephase. Die Bewertung
    der Ruhephase erfolgt in einem einzigen Schritt. 1

Witterung: Die Witterung wird während der Vegetationsperiode täg-
lichdurchdieSonnenscheindauer dundÄnderungderBodenfeuchte
(Niederschlagbzw.Austrocknen)andiesemTagsimuliert.Vereinfa- chend
solldeine Zufallszahlzwischen 0 und12 sein (Tageslänge im-
mergleich).AbBeginnderVegetationsperiodeaufsummierteWerte der
Sonnenscheindauer ergeben die Sonnenstunden h. Die Boden- feuchte f mit
0 ≤ f ≤ 1 wird am Beginn der Vegetationsperiode zufällig gewählt und
täglich zufällig um bis zu 10% verändert. Wildbienenpopulation: Diese
wird abstrakt durch eine (nicht unbe- dingt ganze) Zahl x mit x ≥ 0
dargestellt. Näherungsweise kann man sie als Anzahl gesunder Individuen
beliebiger Wildbienenarten betrachten. Während der Vegetationsperiode
wird x täglich ange- passt: Sei n das Nahrungsangebot durch blühende
Pﬂanzen (siehe unten). Ist n ≥ x, wird x um 3% erhöht. Andernfalls (n \<
x) wird x um ((6·n/x)−3)% erhöht bzw. verringert. Zu Beginn der Simu-
lationisteinAnfangswertfürxgegeben.WährendeinerRuhephase wird x mit
einer Zufallszahl zwischen 0.1 und 0.3 multipliziert, um zu simulieren,
dass viele Wildbienen den Winter nicht überstehen.
Blütenpﬂanzenpopulationen: Jede Art von Blütenpﬂanzen bildet je- weils
eine eigene Population. Jede Population wird abstrakt durch drei Zahlen
y , b und s beschrieben, wobei i über die Arten läuft: i i i • y mit y ≥
0 bezeichnet die Wuchskraft, das ist die näherungs- i i weise Zahl der
Wildbienen, die während der Vollblüte durch die Pﬂanzenpopulation
täglich Nahrung ﬁnden. • b mit 0 ≤ b ≤ 1 ist der Anteil, der in Blüte
steht. i i • s mit 0 ≤ s ≤ 1 ist die Qualität der Samenentwicklung. i i
Das oben verwendete Nahrungsangebot n entspricht P (y ·b ), also i i i
der Summe von y multipliziert mit b für alle Arten i. Zu Beginn i i der
Vegetationsperioden sind b und s gleich 0. Anfangswerte für i i y sind
zu Beginn der Simulation gegeben. In Ruhephasen wird y i i mit s und
einer Zufallszahl zwischen c− und c+ multipliziert, um i i i die
Vermehrung zu simulieren. Dabei sind c− und c+ für die Pﬂan- i i zenart
i typische Konstanten. Tägliche Anpassungen von y , b und i i s während
Vegetationsperioden beruhen ebenso auf Konstanten: i • Die
Feuchtegrenzen f− und f+ mit 0 \< f− \< f+ \< 1 deﬁ- i i i i nieren den
günstigen Bereich der Bodenfeuchte. Im Fall von f−/2 \< f \< f− oder f+
\< f \< 2·f+ (ungünstiger Bereich), i i i i wird y um 1% reduziert. Gilt
sogar f ≤ f−/2 oder 2·f+ ≤ f i i i (sehr ungünstiger Bereich), wird y um
3% reduziert. i • Die Blühgrenzen h− und h+ mit 0 \< h− \< h+ stehen für
die i i i i Sonnenstunden, ab denen die Blüte einsetzt bzw. endet. Die
Blühintensität q mit 0 \< q \< 1/15 ist ein Faktor, der angibt, i i wie
rasch die Blüte einsetzt bzw. endet. Gilt h− ≤ h \< h+ i i (Blüte setzt
ein), wird b pro Tag um q ·(d+3) erhöht, bis b i i i das Maximum von 1
erreicht, wobei d die Sonnenscheindauer an diesem Tag ist. Gilt h+ ≤ h
(Blüte endet), wird b täglich i i um q ·(d+3) verringert, bis b das
Minimum von 0 erreicht. i i 2

• Die Bestäubungswahrscheinlichkeit p (0 \< p \< 1/(h+−h−)) i i i i ist
die Wahrscheinlichkeit, mit der eine Blüte bei ausreichend vielen
Bienenbesuchen innerhalb einer Sonnenstunde (und zu einem kleinen Teil
auch ohne Sonne) einen Samen ausbildet. Ausreichend viele Bienenbesuche
gibt es bei x ≥ n (Bienenpo- pulation x mindestens so groß wie
Nahrungsangebot n); dann erhöht sich s pro Tag um p ·b ·(d+1).
Andernfalls erhöht i i i sich s pro Tag um p ·b ·(d+1)·x/n. i i i Für
jeden Simulationslauf sind also folgende Parameter festzulegen: • Anzahl
der zu simulierenden Jahre, • Anfangswert der Wildbienenpopulation x, •
für jede Blütenpﬂanzenart (Index i läuft über die Arten): -- Anfangswert
der Wuchskraft y , i -- für die Art typische Vermehrungsgrenzen c− und
c+, i i -- für die Art günstige Feuchtegrenzen f− und f+, i i -- für die
Art typische Blühgrenzen h− und h+, i i -- für die Art typische
Blühintensität q , i -- für die Art typische
Bestäubungswahrscheinlichkeit p . i Ergebnisse jedes Simulationslaufs
enthalten den Wert der Wildbienenpo- pulation x und für jede
Blütenpﬂanzenart i die Wuchskraft y jeweils am i Ende der Ruhephase nach
der letzten simulierten Vegetationsperiode. Das Ziel besteht darin, eine
stabile Menge an Blütenpﬂanzenarten zu ﬁnden, die am Ende von
Simulationsläufen über viele Jahre zu einer großen Wildbienenpopulation
führt. „Stabil" bedeutet dabei, dass die y i zwar von Jahr zu Jahr (auch
stark) schwanken können, aber keine Art (beinahe) ausstirbt oder
(beinahe) ständig nur wächst. Im Idealfall liegt y für alle i am Ende
der Simulation in derselben Größenordnung wie die i Anfangswerte. Die
Parameter der einzelnen Pﬂanzenarten sollen mög- lichst unterschiedlich
sein, um eine gewisse Robustheit gegenüber zufällig weniger günstiger
Witterung zu erreichen. Welche Aufgabe zu lösen ist Programm. Entwickeln
Sie ein Java-Programm, das Simulationsläufe wie oben beschrieben
durchführt. Konkret sollen drei Gruppen von Simu- lationsparametern
(also vor allem unterschiedliche Gruppen von Blüten- pﬂanzenarten)
festgelegt werden, die möglichst stabil sind. Jede Gruppe soll zwischen
10 und 25 Blütenpﬂanzenarten umfassen. Für jede Grup- pe sollen 10
Simulationsläufe mit unterschiedlicher Witterung (also mit
unterschiedlichen Zufallswerten) über Zeiträume von jeweils 25 Jahren
durchgeführt werden. Die Parameter und Simulationsergebnisse sind in
möglichst übersichtlicher Weise in Textform auszugeben. Danach, deut-
lich von den Ergebnissen der eigentlichen Simulationsläufe abgesetzt,
sol- len zur Überprüfung der korrekten Vorgehensweise für einen
Simulations- lauf jährliche Zwischenergebnisse und für ein Jahr tägliche
Zwischener- gebnisse mit allen Zahlen, die Zustände beschreiben,
ausgegeben werden. 3

Testen. Testen Sie Ihr Programm sorgfältig, auch bezüglich der Plau-
Programmname „Test" sibilität von Simulationsergebnissen. Sorgen Sie
dafür, dass nach dem aus gutem Grund gewählt Programmstart keine
Benutzerinteraktion (das heißt, keine Eingabe über die Tastatur oder
Maus) nötig ist, sondern einfach nur die nötigen Aus- gaben gemacht
werden. Das Programm soll (nach neuerlicher Überset- im richtigen
Verzeichnis zungallervorhandenen.java-Dateien)mittelsjava
TestvomVerzeich- ausführbar? nis Aufgabe1-3 aus aufrufbar sein. Sie
können natürlich davon ausgehen,
dass.class-DateienanpassendenStellenangelegtwerden,aberSiemüs- sen vor
allem bei Verwendung von Paketen für die Ausführbarkeit durch den
vorgegebenen Aufruf im vorgegebenen Verzeichnis sorgen. Kommentare.
BetrachtenSiejedeDeﬁnitionundDeklarationeinerMe- thode als nominale
Abstraktion. Beschreiben Sie diese Abstraktionen durch kurze, aber
informative Kommentare. Versehen Sie auch jede Klas- Abstraktionen und
se und jedes Interface mit entsprechenden Kommentaren. Eine Java-
Modularisierungseinheiten Klasse kann Elemente unterschiedlicher
Modularisierungseinheiten ent- kurz beschreiben halten (Modul, Klasse,
Objekt). Beschreiben Sie in den Kommentaren (siehe Skriptum) deutlich,
welche Elemente zu welchen Modularisierungseinheiten gehören und welche
Abstraktionen hinter den Modularisierungseinheiten stecken. Sorgen Sie
für eine gute Programmstruktur mit mehreren Klassen. Neben Programmtext
soll die Datei Test.java als Kommentar am Dateianfang eine kurze, aber
verständliche Beschreibung der Aufteilung der Arbeiten auf die einzelnen
Gruppenmitglieder enthalten -- wer hat Arbeitsaufteilung kurz, was
gemacht. Beschreibungen wie die folgende reichen nicht: „Alle haben
verständlich beschreiben mitgearbeitet." Die Arbeitsaufteilung auf die
einzelnen Gruppenmitglie- der wird in jeder Aufgabe beschrieben werden
müssen. Bitte machen Sie das sorgfältig (keinesfalls jemand vergessen),
weil sich eine stark unter- schiedliche Belastung einzelner
Gruppenmitglieder über mehrere Aufga- ben hinweg auf die Beurteilung
auswirken kann.1 Wie die Aufgabe zu lösen ist Der Programmtext Ihrer
Lösung soll möglichst einfach sein und keine un- einfach halten nötige
Funktionalität haben. Er soll wiederverwendbar sein, da die näch- ste
Aufgabe auf Teilen davon aufbaut. Vermeiden Sie jedoch Vorgriﬀe, das
heißt, schreiben Sie keine Programmteile aufgrund der Vermutung, dass
diese Teile in der nächsten Aufgabe verlangt sein könnten. Zufallszahlen
spielen eine große Rolle, aber auch fest vorgegebene An- nahmen. Es
kommt auf ein ausgewogenes Verhältnis zwischen algorith- experimentieren
mischen Vorgaben, festgelegten Werten und Zufallswerten an. Um gute
Einstellungen zu ﬁnden, wird es notwendig sein, mit verschiedenen Wer-
ten und Vorgehensweisen zu experimentieren. Bei Simulationen geht es
häuﬁg, nicht nur in dieser Aufgabe darum, passende Parametrisierungen
1DurchKrankheitodersonstigeVorkommnisseistesimmermöglich,dasseinePer-
sonnichtbeijederAufgabegleichintensivmitarbeitenkann.Daherhateineungleich-
mäßige Arbeitsaufteilung bei einer einzelnen Aufgabe noch keine direkte
Konsequenz.
EskannaberauchindiesemFallsein,dassIhr_eTutor_inoderdieLVA-Leitungnach
einerUrsachedafürfragt.WennsichübermehrereAufgabenhinwegzeigt,dassimmer
wieder eine Person deutlich mehr oder weniger macht als die anderen
Gruppenmit-
glieder,wirddieBeurteilungfüreinzelneGruppenmitgliederunterschiedlichausfallen.
Dabei werden aber auch die von Ihnen genannten Gründe eine Rolle
spielen. 4

zu ﬁnden, sodass Simulationsergebnisse das möglichst gut wiedergeben,
was wir in der Realität vorﬁnden. Diese Aufgabe hilft Ihren Tutor_innen,
Ihre Kenntnisse sowie die Zu- sammenarbeit in der Gruppe einzuschätzen.
Bitte sorgen Sie in Ihrem ei- alle arbeiten mit
genenInteressedafür,dassjedesGruppenmitgliedetwaingleichemMaße
mitarbeitet. Sonst könnten Sie bei einer Fehleinschätzung wertvolle Zeit
verlieren. Scheuen Sie sich bitte nicht, Tutor_innen um Hilfe zu bitten,
falls Sie bei der Lösung der Aufgabe Probleme haben oder keine brauch-
bare Zusammenarbeit in der Gruppe zustande kommt. Warum die Aufgabe
diese Form hat Umfang und Schwierigkeitsgrad der Aufgabe wurden so
gewählt, dass die eigentliche Programmierung bei guter Organisation und
entsprechendem Vorwissen nicht zu viel Zeit in Anspruch nimmt, aber eine
Einarbeitung in neue Themen nötig ist und Diskussionsbedarf entsteht.
Nutzen Sie die Gelegenheit, um die Aufgabenverteilung und interne
Abläufe innerhalb der Gruppe zu organisieren. Details der Aufgabe
bleiben bewusst oﬀen: • Sie sollen in der Gruppe diskutieren, wie Sie
die Aufgabe verstehen und welche Lösungswege geeignet erscheinen. •
Siesollensichdarangewöhnen,dassAufgabennichtvollständigspe- ziﬁziert
sind, aber trotzdem Vorgaben eingehalten werden müssen. • Sie sollen
sich eine eigene brauchbare Faktorisierung überlegen und sich dabei
vorerst einmal nur von Abstraktionen leiten lassen. • Sie sollen auch
die Verantwortung für die Korrektheit Ihrer Lösung (so wie Sie sie
selbst verstehen) übernehmen, indem Sie entspre- chende Tests
durchführen. Allgemeine Informationen zur Übung Folgende Informationen
betreﬀen diese und auch alle weiteren Aufgaben. Was bei der Lösung der
Aufgabe zu beachten ist Unter der Überschrift „Wie die Aufgabe zu lösen
ist" ﬁnden Sie Hin- weise darauf, wie Sie die Lösung der Aufgabe
vereinfachen können und Schwerpunkte beachten welche Fallen Sie umgehen
sollen, erfahren aber auch, welche Aspekte bei der Beurteilung als
wichtig betrachtet werden. In der ersten Aufgabe
kommtesbeispielsweiseaufdieEinfachheitderLösungan,aberauchdar- auf, wie
gut die gewählten Algorithmen und angenommenen Werte bzw. Zufallswerte
zusammenpassen. Das heißt, in späteren Aufgaben können Ihnen bei solchen
Hinweisen etwa auch für unnötig komplizierte oder um- fangreiche
Lösungen Punkte abgezogen werden, weil Sie sich nicht an die Vorgaben
gehalten haben. Außerdem gilt natürlich alles, was in der Aufgabe
beschrieben ist. Beispielsweise müssen Kommentare die gewähl- ten
Abstraktionen verdeutlichen und beschreiben, welche Inhalte als Teil
welcher Modularisierungseinheiten anzusehen sind. Unterschiedliche Auf-
gaben haben unterschiedliche Schwerpunkte. Die nächste Aufgabe wird 5

nicht nach dem gleichen Schema beurteilt wie die vorige. Richten Sie
sich daher nach der jeweiligen Aufgabenstellung. Ein häuﬁger Fehler
besteht darin, eine Aufgabe nach Gefühl zu lösen ohne zu verstehen,
worauf es ankommt. Meist bezieht sich die Aufgabe auf ein Thema, das
zuvor theoretisch behandelt wurde. Versuchen Sie, strukturiert vorgehen
eine Beziehung zwischen der Aufgabenstellung und dem davor behandel-
tenStoﬀherzustellen.AchtenSiedarauf,Fachbegriﬀenichtnurumgangs-
sprachlichzuinterpretieren,sondernsowieimSkriptumbeschrieben.Die ersten
Aufgaben sind vielleicht auch ohne Skriptum lösbar, bei späteren
Aufgaben würde ein Ignorieren des Skriptums wahrscheinlich zu Fehlern
führen. Als Hilfestellung sind in jeder Aufgabenstellung Teile des
Skrip- tums genannt, in denen die relevantesten Themen behandelt werden,
bei komplizierten Themen oft nur wenige Seiten. Versuchen Sie nicht,
Teile der Aufgabenstellung durch Tricks oder Spitzﬁndigkeiten zu
umgehen. Beispielsweise gibt es immer wieder Lö- sungsversuche, in denen
die Test-Klasse nur „Test erfolgreich" ausgibt, statt sinnvolle Tests
durchzuführen. Solche Versuche werden durch hän- dische Beurteilungen
mit hoher Wahrscheinlichkeit erkannt. Spätere Auf- keine
Spitzﬁndigkeiten gaben enthalten oft Schwierigkeiten, die mit
Allgemeinwissen alleine oder über aufgabenbezogene Web-Recherchen bzw.
mit Hilfe von KI kaum zu lösen sind. Gerade in solchen Fällen ist davon
abzuraten, die Schwierig- keiten durch Tricks zu umgehen. Hinweise zur
richtigen Lösung lassen sich im Skriptum und auf den Vorlesungsfolien
ﬁnden. Ihre Lösung, bestehend aus .java-Dateien, muss am Tag der Abgabe
um 13:00 Uhr pünktlich im Git-Repository Ihrer Gruppe stehen. Über-
setzte .class-Dateien sollen nicht ins Repository gestellt werden, da
sie die Zusammenarbeit in der Gruppe erschweren und vor der Beurteilung
ohnehin neu generiert werden. Zugangsinformationen zum Repository er-
halten Sie in Kürze. Informationen zum Umgang mit dem Repository ﬁnden
Sie in TUWEL. Es wird empfohlen, rechtzeitig vor der Deadline
ausprobieren die Lösung auf dem Übungsrechner auszuprobieren und die
Daten da- bei durch pull aus dem Repository zu laden. So können Sie
typische Fehler bei der Abgabe (z.B. auf push vergessen, Lösung im
falschen Ver- zeichnis, falsche package- und include-Anweisungen,
Klassen aus Nicht- Standard-Paketen verwendet und nicht mit abgegeben)
sowie Inkompati-
bilitätenaufgrundunterschiedlicherVersionenundBetriebssystemeinstel-
lungen (z.B. Dateinamen mit Umlauten sowie neueste Sprach-Features nicht
unterstützt) erkennen und beseitigen. Was Ihr_e Tutor_in von Ihnen
wissen möchte Ihr_e Tutor_in wird Ihnen in Kürze eine Mail schreiben, um
sich vor- zustellen und um Informationen über Sie zu bitten. Geben Sie
diese In- formationen möglichst bald, damit die für Sie am besten
geeignete Form der Betreuung gewählt werden kann. Unabhängig von der
Form der Be- treuung kann natürlich jedes Gruppenmitglied jederzeit
konkrete Fragen an Tutor_innen richten. Scheuen Sie sich bitte nicht,
sich auch mit or- ganisatorischen oder gruppeninternen Problemen, die
Sie möglicherweise nicht selbst lösen können, an Tutor_innen zu wenden.
Früh im Semester sind Probleme einfacher lösbar als im weit
fortgeschrittenen Semester. 6

---

## Aufgabe 2

2.  Programmieraufgabe Programmierparadigmen LVA-Nr. 194.023 2025/2026 W
    TU Wien Kontext Die Simulation aus der ersten Programmieraufgabe ist
    viel zu oberﬂäch- lich. Hauptsächlich geht es darum, Simulationen
    besser an die Realität Themen: in der Natur anzupassen und
    zuverlässigere Ergebnisse zu erzielen, ohne Aufwandsabschätzung, den
    Aufwand unnötig in die Höhe zu treiben. Verbesserungen sollen vor
    Programmiereﬃzienz, allem in folgende Richtungen gehen: Überblick
    über prozedurale und • Das Umfeld genauer betrachten und alle als
    wesentlich erachteten objektorientierte Programmierung Faktoren in
    die Simulation einbeziehen (Modell vervollständigen). • Beziehungen
    zwischen den Elementen des Modells genauer analy- sieren und
    darstellen (Modell verfeinern). Ausgabe: 20.10.2025 •
    Simulationsergebnisse mit in der Natur ermittelten Werten in Ein-
    klang bringen (Rückkopplung und Justierung von Parametern). Abgabe
    (Deadline): Welche Aufgabe zu lösen ist 27.10.2025, 13:00 Uhr
    Simulation verbessern. Die Lösung der 1. Aufgabe ist deutlich zu
    ver- bessern. In jede der drei unter „Kontext" genannten Richtungen
    sind Verbesserungen nötig. Es ist nicht vorgegeben, wie diese
    Verbesserungen Abgabeverzeichnis: genau ausschauen sollen. Die
    folgenden drei Absätze weisen auf Verbes- Aufgabe1-3
    serungspotentiale hin, schreiben aber nicht vor, was genau zu tun
    ist. Modell vervollständigen.
    DasModellkönntesovervollständigtwerden: Programmaufruf: • Es gibt
    sehr viele Arten von Wildbienen, teilweise auf ganz be- java Test
    stimmte Blütenpﬂanzen spezialisiert, mit unterschiedlichen Anfor-
    derungen an Nistplätze und in unterschiedlichen Zeiträumen aktiv.
    Das Modell soll zwischen diesen Arten unterscheiden und auf ihre
    Grundlage: Lebensbedingungen Rücksicht nehmen. Skriptum, Abschnitt
    2.1 und 2.2 • Wildbienen reagieren empﬁndlich auf Entfernungen
    zwischen Nist- und Nahrungsressourcen. Es reicht also nicht,
    irgendeinen Teil ei- ner großen landwirtschaftlichen Fläche für
    Blütenpﬂanzen vorzuse- hen, sondern es müssen kleinräumige
    Strukturen gebildet werden, in denen Bereiche mit blühenden Pﬂanzen
    nicht weit entfernt sind. Entfernungen zwischen Nistplätzen und
    Nahrungsquellen sollen in die Simulation einbezogen werden. •
    Wildbienen reagieren empﬁndlich auf Störungen und Veränderun- gen
    der Umweltbedingungen. Es wird kaum möglich sein, Umwelt-
    bedingungen über so lange Zeiträume, die simuliert werden sollen,
    konstant zu halten. Daher sollen Veränderungen von Umweltbedin-
    gungen in die Simulation einbezogen werden. Das betriﬀt beispiels-
    weise auch Feldfruchtfolgen (zur Bodenschonung in aufeinander fol-
    genden Jahren unterschiedliche Kulturpﬂanzen), die als Störungen
    betrachtet werden können. 1

• Wildbienen sind nicht die einzigen Bestäuber von Blütenpﬂanzen. Die
Bestäubungsleistung kann teilweise von anderen Insekten, etwa
Honigbienen und Schwebﬂiegen übernommen werden, auch wenn diese
Bestäuber weniger eﬀektiv sind. Vereinfacht kann man die Anwesenheit
dieser Bestäuber als gegeben annehmen, aber auch ei- neSimulation
derLebensgewohnheitenandererInsektenkannsinn- voll sein. Die Anwesenheit
von Honigbienen kann gezielt beeinﬂusst werden, was auch in die
Simulation einﬂießen soll. • Andere Bestäuber sind nicht nur teilweiser
Ersatz für Wildbienen,
sondernauchNahrungskonkurrenten,diedieVerfügbarkeitvonBlü- tennektar
reduzieren. Das sollte simuliert werden. Wildbienen sind
durchihrenhohenSpezialisierungsgradsehreﬀektiveBestäuber,für die Pﬂanzen
bei gleicher Bestäubungsleistung weniger Nektar pro- duzieren müssen als
für andere Bestäuber. Es bringt einer Pﬂanze daher Vorteile, von einer
Wildbiene bestäubt zu werden, was zu einer etwas besseren Wuchskraft
führen kann. • Pﬂanzen entwickeln sich nicht nach einem ﬁxen Schema, wie
in der 1. Aufgabe angenommen. Unterschiedliche Pﬂanzen haben unter-
schiedliche Strategien. Zumindest die Temperatur ist ein Faktor, der
bezüglich Wachstum und Blühzeitpunkt berücksichtigt werden sollte.
Manche Pﬂanzen blühen mehrfach und können mehrmals im Jahr Früchte
entwickeln. Auch nahe beieinander wachsende Pﬂan- zen können ganz
unterschiedlich besonnt sein, wodurch die Sonnen- stunden kein besonders
gut geeignetes Mittel zur Synchronisation des Blühbeginns sind. Viele
Pﬂanzen können sich über chemische Substanzen koordinieren oder den
Blühbeginn von der Anwesen- heit von Insekten abhängig machen, genau so
wie Wildbienen ihre Aktivitäten vermutlich an das Vorhandensein von
Blüten anpassen. • In praktisch keinem Fall triﬀt die Annahme zu, dass
die Qualität und Menge von Samen von der Wachstumskraft am Ende der Ve-
getationsperiode abhängt. Samen bilden sich oft viel früher und Pﬂanzen
sterben danach ab oder gehen in einen anderen Modus
über,indemsiesichaufdieRuhephasevorbereiten.HinterderVer- mehrung und
Wuchskraft vergleichsweise langlebiger Blütenpﬂan- zen wie Kirsch- oder
Apfelbäumen stecken ganz andere Mechanis- men als hinter einjährigen
Pﬂanzen. In Bezug auf die Vermehrung sollen wesentlich ausgefeiltere
Mechanismen modelliert werden. Modell verfeinern. Im Modell aus der 1.
Aufgabe sind viele Zahlen ﬁx einkodiert, etwa die Änderung der
Wildbienenpopulation abhängig vom Nahrungsangebot. Derart ﬁxierte
Änderungen gibt es in der Natur nicht. Wir könnten das Modell
vervollständigen, indem wir etwa das Fortpﬂan- zungsverhalten
unterschiedlicher Wildbienenarten im Detail simulieren. Aber so genaue
Simulationen würden den Aufwand immens in die Höhe treiben. Es bleibt
uns nichts anderes übrig, als mit groben Annäherungen
andieRealitätzuarbeiten.Wirkönnenjedochdafürsorgen,dasskleinste
Änderungen der Daten keine großen Auswirkungen nach sich ziehen und
genauereAusformungenanStellen,andenensiesichalssinnvollerweisen,
ermöglicht werden. Das Modell könnte z.B. so verfeinert werden: 2

• StattmiteinfachengleichverteiltenZufallszahleningewissenWerte-
bereichen soll mit Wahrscheinlichkeitsverteilungen gearbeitet wer- den,
die der Natur abgeschaut sind. Wertebereiche werden damit meist größer,
aber die gewählten Werte sind realistischer. • Änderungen bestimmter
Werte sollen nicht linear mit einem ﬁxen Faktor oder Prozentsatz
erfolgen, sondern in Abhängigkeit von der
Größe,durchdiedieÄnderungveranlasstwurde.Beispielsweisesoll sich die
Wuchskraft einer Pﬂanze bei geringfügiger und kurzzeitiger
Überschreitung der Feuchtegrenzen nur geringfügig auswirken, bei starker
oder lang anhaltender Überschreitung dagegen stark, mit kontinuierlichen
Verläufen statt sprunghaften Änderungen. •
UnterschiedlicheWildbienenartenundBlütenpﬂanzenhabenunter- schiedliche
Lebensgewohnheiten. Es soll möglich sein, das Modell modular so zu
erweitern, dass Simulationen der Lebensgewohnhei- ten einzelner
Populationen hinzugefügt und auch wieder entfernt werden können, ohne
die Struktur des restlichen Modells anpas- sen zu müssen. Beispielsweise
können die Lebensgewohnheiten in Java-Klassen beschrieben sein, die ein
gemeinsames Interface im- plementieren; Instanzen dieses Interfaces
(also Objekte) können in die Simulation eingebunden werden. •
SowieLebensgewohnheitenvonPopulationenalsObjektezurSimu-
lationhinzugefügtwerdenkönnen,sollenauchEreignissealsObjek- te zur
Simulation hinzugefügt werden können. Beispielsweise könn- te es Klassen
und entsprechende Objekte geben, die die Auswir- kungen gelegentlicher
Naturereignisse (Gewitter, Sturm, Hangrut- schung, ...) oder sonstiger
Störungen (Mahd, Ernte, Fruchtwech-
sel,...)simulieren.AuchWahrscheinlichkeitsverteilungensollenauf diese
Weise ﬂexibel austauschbar sein. • Wenn wir schon dabei sind,
Schnittstellen zur Erweiterung des Mo- dells anzubieten, können wir das
gesamte Modell gleich modular
aufbauen,sodassallesimuliertenPopulationen,Ereignisse,etc.über Objekte
eingebunden werden. Entscheidend ist dabei, eine mög-
lichstﬂexibleFormderKommunikationzwischendeneinzelnenMo-
dularisierungseinheiten zu ermöglichen (also die „richtigen" Metho- den
in den Interfaces vorzusehen), sodass die Struktur des Modells der
Vervollständigung und Verfeinerung nicht im Weg steht. Modell justieren.
Ohne Bezug zur Realität wären Simulationen sinn- los. In einem gut
strukturierten Modell soll es möglich sein, Parameter so anzupassen,
dass Simulationsergebnisse gut zu Beobachtungen in der Realität passen.
Der Begriﬀ „Parameter" ist dabei in einem weiten Sinn zuverstehen,nicht
nurals Methodenparameter. Parameterkönnen inder
SimulationverwendeteelementareWerte,aberetwaauchWahrscheinlich-
keitsverteilungen sein. Wir können dafür sorgen, dass das Modell besser
justierbar wird und wir können reale Daten einbeziehen: • In einigen
Fällen kennen wir die Natur recht genau und können daher auch mit
genauen realen Daten arbeiten. Ein Beispiel ist die Tageslänge abhängig
von Standort und Jahreszeit. 3

• Wir können die Witterung nicht nur abstrakt simulieren, sondern reale
Wetterdaten vergangener Jahre als Grundlage verwenden. • Auch ohne
jahrelange Feldversuche können wir auf viele bekannte Daten
zurückgreifen. Beispielsweise sind typische Blütezeiten realer
Blütenpﬂanzen leicht zu eruieren und wir können überprüfen, ob diese
Pﬂanzen auch in der Simulation zur richtigen Zeit blühen und die
Simulation bei Bedarf anpassen. • Alle für uns interessanten
mathematischen Funktionen auf realen Zahlen können beliebig genau durch
Polynome angenähert werden. Praktisch reichen für unsere Zwecke Polynome
niedriger Potenzen.
JedesModelllässtsichsoparametrisieren,wiewiresinderRealität beobachten,
wenn wir jede Einﬂussgröße als Polynom betrachten,
dessenKoeﬃzientenfüralleniedrigenPotenzenwirbeliebigeinstel- len können.
Auf diese Weise können wir für Justierbarkeit sorgen. • Parameter sind
nicht nur reale Zahlen oder Funktionen auf realen Zahlen. Wenn wir
Objekte beliebiger Klassen (bzw. von Unterklas- sen bestimmter Typen)
als Parameter einsetzen können, haben wir weitere Möglichkeiten, die es
erlauben, Teile des Modells beliebig genau an die Realität anzunähern. •
Unabhängig von der eigentlichen Simulation können wir Parame- ter
(idealerweise als Polynome betrachtet) als Korrekturwerte der Ergebnisse
vorsehen. Damit lassen sich leicht alle gewünschten Er- gebnisse
einstellen. Allerdings bedeutet das auch, dass wir etwas simulieren, was
sich in der Realität sicher nicht so abspielt. •
VieleSystemeundModellezeigenchaotischesVerhalten,wobeiwin- zige
Änderungen große Auswirkungen haben. So lange sich die Si-
mulationähnlichchaotischverhältwiedieRealität,istanderSimu- lation
nichts falsch. Aber die Simulation sollte kein chaotisches Ver-
haltenzeigen,dasinderRealitätnichtbeobachtbarist.Wirkönnen die
Simulation dahingehend analysieren, wo chaotisches Verhalten auftritt
und die Simulationsgenauigkeit dort gezielt erhöhen. Funktionsumfang.
Bestimmen Sie selbst den Funktionsumfang Ihres Programms. Das Programm
soll möglichst viel der nötigen (vorgeschlage- Funktionsumfang nen oder
selbst gefundenen) Funktionalität abdecken und über Testfälle selbst
wählen überprüfen. Jedoch sollte zumindest je eine Maßnahme getroﬀen
werden, um das Modell zu vervollständigen, zu verfeinern und zu
justieren oder justierbar zu machen. Testen
DasProgrammsollwieinder1.Programmieraufgabenachneu- im richtigen
Verzeichnis erlicherÜbersetzungmittelsjava
TestvomVerzeichnisAufgabe1-3aus testen aufrufbar sein und die selbst
gewählte Funktionalität überprüfen. Tests sollen ohne
Benutzerinteraktion ablaufen, sodass Aufrufer keine Testfälle auswählen
oder Testdaten eintippen müssen. 4

Paradigmen und Kommentare Neben nominaler Abstraktion dürfen nominale
Abstraktion Sie auch Lambda-Abstraktion einsetzen. Jedoch soll jede
nominale Ab- nur mit Kommentaren straktion mit Kommentaren versehen
sein, die die Abstraktion erläutern. Setzen Sie Programmierstile des
objektorientierten und des prozedu- Paradigmen erläutern
ralenParadigmasgemischtein.BittestreuenSieinIhrProgrammanmin- (mind. 5
Stellen) destens 5 relevanten Stellen je einen Kommentar ein, der mit
„STYLE:" beginnt und eine Erklärung enthält, welchem Paradigma der an
dieser Stelle verwendete Programmierstil entspricht und woraus das
ersichtlich ist. Abstraktionen müssen zum Paradigma passen. Dort, wo ein
objekt- orientierter Stil verwendet wird, achten Sie bitte darauf, dass
der betref- Klassenzusammenh. hoch, fende Programmteil ausschließlich
durch Abstraktionen verständlich ist Objektkopplung schwach, sowie der
Klassenzusammenhalt hoch und die Objektkopplung schwach
Untertypbeziehungen ist. Sorgen Sie dafür, dass auch Untertypbeziehungen
vorkommen. An Grenzen, an denen Stile unterschiedlicher Paradigmen
aneinanderstoßen, machen Sie bitte klar, wie die Paradigmen
zusammenwirken. Neben Programmtext soll die Datei Test.java als
Kommentar am beschreiben: Struktur, Dateianfang die Grobstruktur und den
(geplanten) Funktionsumfang der Funktionsumfang, Lösung zusammenfassen
sowie eine kurze, aber verständliche Beschrei- Aufgabenaufteilung bung
der Aufteilung der Arbeiten auf die einzelnen Gruppenmitglieder
enthalten (wer tatsächlich was gemacht hat, nicht die geplante Auftei-
lung), nicht nur für die erste Aufgabe, sondern auch für diese. Wie die
Aufgabe zu lösen ist Die oben aufgezählten Vorschläge zur Verbesserung
der Simulation sind als Anhaltspunkte gedacht. Sie können Punkte
weglassen, abändern oder durch andere sinnvoll erscheinende
Verbesserungen ersetzen. Eine Schwierigkeit besteht in der richtigen
Abschätzung des Umfangs der Arbeiten. Planen Sie nach Ihren Fähigkeiten
möglichst viel ein, das Sie in der vorgesehenen Zeit zum Abschluss
bringen können -- das heißt, so viel Sie können, aber nicht mehr. Als
groben Anhaltspunkt sollten Sie (jedes Gruppenmitglied) etwa elf mit
intensiver Arbeit gefüllte Stunden investieren, keinesfalls mehr als
fünfzehn. Versuchen Sie, so eﬃzient wie möglich zu arbeiten und rasch zu
einer brauchbaren Lösung zu kommen.
IgnorierenSieDetails,dieIhnenunwichtigerscheinen.BedenkenSie,dass Sie
Ihre Lösung durch Testfälle überprüfen sollen und planen Sie Zeit für
die Entwicklung der Testfälle und die Fehlerbeseitigung ein. Erstellen
Sie zuerst ein Konzept Ihrer geplanten Arbeiten. Schicken Konzept an
Tutor_in Sie es frühzeitig an Ihre_n Tutor_in. Sie werden so bald wie
möglich erfahren, ob das Konzept ausreicht oder Änderungen nötig sind.
Eine Schwierigkeit ist der gleichzeitige Umgang mit mehreren Pa-
Paradigmen kombinieren radigmen. Sie müssen das prozedurale und
objektorientierte Paradigma verwenden und den Übergang zwischen den
Paradigmen in Kommenta- ren nachvollziehbar beschreiben. Lesen Sie
Unterscheidungskriterien im Skriptum nach. Es wird dazu geraten, die
Anzahl der Übergänge zwi- schen den Paradigmen klein zu halten. Im
objektorientierten Teil ist auf hohen Klassenzusammenhalt, schwache
Objektkopplung und die Verwen- dung von Untertypbeziehungen zu achten.
Für die ersten drei Aufgaben weisen Tutor_innen Sie einige Zeit nach
derAbgabebeiBedarfaufkonkreteFehlerhinundbittetumBeseitigung.
DieswirktsichnurdannaufIhreBeurteilungaus,wennSiederBittenicht 5

nachkommen. Sie sollten selbst (auch ohne Feedback) ein Gefühl für die
Qualität Ihrer Lösungen entwickeln. Wegen der großen Zahl erwarteter
Fehler können Tutor_innen nicht auf jede Kleinigkeit eingehen. Warum die
Aufgabe diese Form hat Bei allen anderen Aufgaben geht es darum, am Ende
eine vollständige und perfekte Lösung abzuliefern. In dieser Aufgabe
kann man ein solches Ziel zwar anstreben, aber nicht erreichen. Unter
Einhaltung der Bedin- gungen ist es unmöglich, eine perfekte Lösung zu
produzieren. Vielmehr geht es darum, dass Sie Ihre eigenen Fähigkeiten
und Grenzen beim Pro- grammieren unter Zeitdruck als Einzelperson und
Gruppe kennenlernen. Sie sollen selbst erkennen, wo Ihre Stärken liegen
und zu welchen Arten von Fehlern Sie eher neigen (auf allen Ebenen von
der Problemanalyse bis hin zum Testen ebenso wie hinsichtlich der
Zusammenarbeit in der Gruppe). Im Hinblick darauf gibt es keine
richtigen und falschen Lösun- gen. Es ist aber erkennbar, wie sehr Sie
sich darum bemüht haben, eine beinahe unlösbare Aufgabe so gut wie
möglich zu lösen. Das Feedback durch die Tutor_innen wird genau darauf
abzielen: Haben Sie sich ausreichend darum bemüht, in möglichst vielen
Bereichen etwas Machbares zu machen, oder sind in zu vielen Bereichen
keine An- sätze erkennbar? In letzterem Fall werden Tutor_innen
Nachbesserungen
verlangen,abernicht,wennausZeitdruckirgendwelchekleineFehlerpas- siert
sind, mit denen bei einer solchen Aufgabe immer zu rechnen ist. Sie
sollen möglichst große Freiheit bei der Lösung der Aufgabe haben und
selbst die Verantwortung für alles übernehmen. Niemand schreibt Ihnen
vor, wie die Aufgabenstellung genau zu verstehen ist. Diese Aufgabe
stellt hohe Anforderungen an jedes Gruppenmitglied und die
Zusammenarbeit in der Gruppe -- eine Nagelprobe für das Funk- tionieren
der Gruppe und zum Aufdecken möglicher Schwachstellen. Nebenbei bietet
es sich an, die Aufgabe zur Vertiefung eines über- blicksartigen
Verständnisses von Paradigmen einzusetzen. Der Schwer- punkt liegt auf
der objektorientierten Programmierung (bei einem intui- tiven Zugang) im
Unterschied zur prozeduralen Programmierung. 6
