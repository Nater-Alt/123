I need you to pay attention carefully to the rules provided here and I need you to read all the java files in detail and understand them completley and run them to look at the results. I need you to try to fix this Code Base and make it run using small amounts of changes and additions but do them where necessary. The output has to be correct it is the most important thing, which is why you have to test it until it is right according to what the following text wants from you. We are currently working on Aufgabe 2 which builds on the basis of Aufgabe 1 but changes some of its stuff.
# 2. Programmieraufgabe – Programmierparadigmen
**LVA-Nr.:** 194.023  
**Semester:** 2025/2026 W  
**TU Wien**

**Ausgabe:** 20.10.2025  
**Abgabe (Deadline):** 27.10.2025, 13:00 Uhr  
**Abgabeverzeichnis:** `Aufgabe1-3`  
**Programmaufruf:** `java Test`  
**Grundlage:** Skriptum, Abschnitte 2.1 und 2.2

---

## Kontext
Die Simulation aus der 1. Aufgabe war zu oberflächlich. Ziel ist es, sie näher an reale Bedingungen in der Natur anzupassen, ohne den Aufwand unnötig zu erhöhen. Verbesserungen sollen in drei Bereichen erfolgen:

1. **Modell vervollständigen:** Wichtige Umwelt- und Lebensbedingungen berücksichtigen.
2. **Modell verfeinern:** Beziehungen und Prozesse realistischer und flexibler gestalten.
3. **Modell justieren:** Simulationsergebnisse an reale Daten anpassen.

---

## Welche Aufgabe zu lösen ist
Die Lösung der 1. Aufgabe soll **in allen drei Bereichen** verbessert werden. Die im Folgenden genannten Punkte sind **Vorschläge** und keine starren Vorgaben.

---

## 1. Modell vervollständigen (Hinweise)
- Unterschiede zwischen **Wildbienenarten** berücksichtigen (Spezialisierung, Aktivitätszeiten, Nistbedingungen).
- **Entfernungen** zwischen Nist- und Futterressourcen berücksichtigen (kleinräumige Strukturen).
- **Änderungen der Umweltbedingungen** einbeziehen (Witterung, Fruchtfolgen).
- **Weitere Bestäuber** wie Honigbienen und Schwebfliegen berücksichtigen (Bestäubung + Nahrungskonkurrenz).
- Pflanzen **artenabhängig** modellieren (Temperaturabhängigkeit, mehrfaches Blühen, Einfluss von Standort/Schattierung).
- **Reproduktion realistischer** modellieren (Samenbildung nicht nur vom Zustand am Ende der Saison abhängig).

---

## 2. Modell verfeinern (Hinweise)
- Statt einfacher Zufallswerte **realistischere Wahrscheinlichkeitsverteilungen** verwenden.
- **Nichtlineare Effekte** berücksichtigen (Auswirkungen abhängig von Intensität/Dauer von Abweichungen).
- **Modularität:** Lebensgewohnheiten verschiedener Arten durch Klassen, die ein gemeinsames Interface implementieren.
- **Ereignisse als Objekte** modellieren (z. B. Unwetter, Mahd, Ernte, Fruchtwechsel).
- Flexible Schnittstellen bereitstellen, um das Modell **erweiterbar** zu halten.

---

## 3. Modell justieren (Hinweise)
- **Realdaten** verwenden (z. B. Tageslänge, historische Wetterverläufe).
- Simulierte **Blühzeiten** mit realen Blühzeiten vergleichen und Parameter anpassen.
- Einflussgrößen durch **Polynome niedriger Ordnung** beschreibbar machen (für flexible Parametrisierung).
- **Objekte als Parameter** zulassen, um Modellteile austauschbar zu machen.
- Chaotisches Verhalten untersuchen und Modell so anpassen, dass es **realistisch chaotisch**, aber nicht künstlich instabil wird.

---

## Funktionsumfang
- Sie bestimmen den Funktionsumfang selbst.
- Mindestens **eine Verbesserung pro Bereich** (Vervollständigen, Verfeinern, Justieren).
- Programm muss sich selbst testen (keine Benutzereingaben).

---

## Testen
- Ausführung wie in Aufgabe 1:  
