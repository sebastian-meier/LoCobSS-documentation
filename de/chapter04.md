<div class="print-hide">
<a href="../HTML.html">Zurück zur Übersicht</a>
</div>

## Wissenschaftskommunikation
**Auf Benutzer\*innen zugeschnittenes, datengestütztes Storytelling im Web**

Klassische Wissenschaftskommunikation ist nach wie vor statisch, unidirektional und textlastig. Die strukturelle Nähe zu akademischen Publikationen macht diese nur schwer zugängig für viele interessierte Bürger\*innen. Alternativen zu diesen Kommunikationspraktien finden sich beispielsweise im Bereich des Daten-Journalismus oder der Daten- und Informationsvisualisierung. Dort werden Ansätze entwickelt und genutzt, welche den aktuellen Seh- und Nutzungsgewohnheiten der Leser\*innen entsprechen. In diesem Teilabschnitt des LoCobSS Vorhabens wurden zwei exemplarische Anwendungen entwickelt, welche aufzeigen sollen, wie man mit diesen Methoden des daten-gestützten Storytellings auch wissenschaftliche Inhalte bürgernah vermitteln kann. Darüber hinaus wurden Methoden der Personalisierung entwickelt, um es den Leser\*innen zu erleichtern Bezüge zwischen den wissenschaftlichen Ergebnissen und der eigenen Lebenswelt herzustellen.

### Daten-gestütztes Storytelling

Die zunehmende Verfügbarkeit von Daten, barrierearme Werkzeuge zur Erstellung von Visualisierungen und Bemühungen von Akteur\*innen wie Datenjournalist\*innen, haben in den letzten Jahren dazu beigetragen, dass Visualisierungen von Daten und Informationen nicht mehr nur in der Fachliteratur zu finden sind, sondern Einzug in die Massenmedien gehalten haben. Besonders hervorzuheben für ihre herausragende datenjournalistische Arbeit auf diesem Gebiet sind z.B. folgende Plattformen:

**Deutschland**
- [Zeit-Online](https://www.zeit.de/datenjournalismus)<sup class="print"></sup>
- [Spiegel Online](https://www.spiegel.de/thema/daten/)<sup class="print"></sup>
- [Tagesspiegel](https://interaktiv.tagesspiegel.de/)<sup class="print"></sup>
- [Morgenpost](https://www.morgenpost.de/interaktiv/)<sup class="print"></sup>

**Europa**
- [NZZ](https://www.nzz.ch/visuals)<sup class="print"></sup>
- [The Guardian](https://www.theguardian.com/interactive)<sup class="print"></sup>

<div class="page-break"></div>

**Weltweit**
- [New York Times](https://www.nytimes.com/interactive/2020/12/30/us/2020-year-in-graphics.html)<sup class="print"></sup>
- [Washington Post](https://www.washingtonpost.com/graphics/2017/ns/year-in-graphics/)<sup class="print"></sup>
- [The Pudding](https://pudding.cool/)<sup class="print"></sup>
- [Financial Times](https://www.ft.com/visual-and-data-journalism)<sup class="print"></sup>
- [FiveThirtyEight](https://projects.fivethirtyeight.com/)<sup class="print"></sup>

<figure>
<figcaption>New York Times: Verschiebungen bei den Wahlen 2020</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/newyorktimes.jpg" alt="" /></center>
</figure>

Wie in der beispielhaften Abbildung aus der New York Times oben zu sehen, gehen die Formen von Visualisierungen mittlerweile weit über einfache Balken- und Liniendiagramme hinaus und bieten komplexe Darstellungen und Analysemöglichkeiten. Diese komplexen Formen der Visualisierungen sollten aber mit Bedacht genutzt werden, da die Zunahme solcher Darstellung nicht zwingend Hand-in-Hand geht mit der Visual-Literacy in der breiten Leserschaft. Weshalb wir in den folgenden Prototypen versucht haben die visuelle und informationelle Komplexität möglichst gering zu halten.

Weiterführende Lektüre zum Thema Datenjournalismus:

- [Segel & Heer (2010) Narrative Visualization: Telling Stories with Data](http://idl.cs.washington.edu/papers/narrative/?s=03)<sup class="print"></sup>
- [Literaturübersicht im Bereich Datenvisualisierung](https://airtable.com/shrugbQMDGVNvArMT/tblSrU1fNAykSMyXU)<sup class="print"></sup>
- [Datajournalism Handbook](https://datajournalism.com)<sup class="print"></sup>
- [Anton Zhiyanov (2021) DataViz Guidelines](https://github.com/nalgeon/dataviz)<sup class="print"></sup>


### Personalisierung und Relevanz

Besonders wenn es um eher abstrakte wissenschaftliche Phänomene geht, ist es wichtig den Leser\*innen Bezüge zur eigenen Lebenswelt aufzuzeigen, um die Relevanz dieser Thematiken deutlich zu machen. Beim Beispiel der Klimawandelkommunikation, welche wir in unseren Prototypen thematisiert haben, wird dies besonders deutlich. Im Gegensatz zum lokalen Wetter, beschreibt der Klimawandel langfristige und großräumliche Veränderungen. Hierdurch kann es für Bürger\*innen schwierig sein Bezüge zum eigenen Leben und Handeln herzustellen. Die Herausforderung ist also diese Verbindungen herzustellen, umso persönlicher die Bezüge, umso einfacher die Verbindung zur Lebenswelt der Bürger\*innen. 

Den folgenden Prototypen liegt folgendes Modell zu Grunde (siehe Meier & Glinka 2017): 1) es gibt einen Datenraum, welcher für die Visualisierung genutzt wird (z.B. Klimazonen in Deutschland), 2) es gibt Leser\*innen die bestimmte Eigenschaften haben (Datenattribute, wie z.B. der Wohnort). Auf diesem Modell aufbauend, kann man die abstrahierte datengestützte Repräsentation einer Leser\*in mit dem Datenraum abgleichen und verschiedene Operationen durchführen:

Bei mehrdimensionen Datenräumen kann eine Dimensionsreduktion genutzt werden, um möglichst ähnliche Datenobjekte im Vergleich zur Leser\*in zu identifizieren, um so einen Einstieg in den größeren Datenraum zu erleichtern.

<div class="page-break"></div>

<figure>
<figcaption>Personalisierung: Dimensionsreduktion (blau Leser\*in)</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/personal_dr.png" alt="" /></center>
</figure>

Ähnliche Prinzipien zumn identifizieren ähnlicher Datenpunkte oder Gruppen ähnlicher Datenpunkte lassen sich auch mit anderen Verfahren durchführen, wie z.B. KNN oder KMC.
<figure>
<figcaption>Personalisierung: K-Nearest-Neighbour und K-Means-Clustering (blau Leser\*in)</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/personal_knn.png" alt="" /></center>
</figure>
<div class="page-break"></div>
Genauso können die Attribute der Leser\*in auch als Filter genutzt werden, um den Datenraum herunterzubrechen und zu verkleinern.
<figure>
<figcaption>Personalisierung: Filteransatz</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/personal_filter.png" alt="" /></center>
</figure>

In den beiden Prototypen wurde dieses abstrakte Modell anschaulich umgesetzt:

1. **Klimawandel und Mobilität**: In dem Artikel soll das Thema CO2-Fußabdruck vermittelt werden. Die Leser\*innen geben ihre Postleitzahl, ihr primäres Verkehrsmittel, sowie ihre tägliche Reisedistanz an. Dies ist das individuelle Datenobjekt. Dieses Datenobjekt wird nun genutzt, um CO2-Ziele im Rahmen der Klimawandelbekämpfung darzustellen. Statt allgemeiner Darstellungen, werden die Auswirkung von CO2-Reduktion direkt in der heimischen Postleitzahl der Leser\*innen dargestellt. Weitere Details siehe unten.
2. **Klimawandelrisiken**: In diesem Artikel sollen Klimawandelauswirkungen in Deutschland kommuniziert werden. Die Leser\*innen geben hierzu ihre Postleitzahl ein. Über die Postleitzahl werden die Auswirkungen herausgefiltert, welche für diese Region Deutschlands zutreffend sind (Filter). Diese werden dann für die angegebene Postleitzahl lokal visualisiert. Weitere Details siehe unten.

Weiterführende Literatur zur Personalisierung von Visualisierungen:

- Meier, S., Glinka, K. (2018) Data-driven Personal Cartographic Perspectives – An Overview Of Applied, Artistic, And Academic Visualization Projects For Egocentric Retrospective Analysis Of Personal Spatio-Temporal Behavior Cartograms, Kartographische Nachrichten, (13/8).<sup class="print"></sup>

<div class="page-break"></div>

- Meier, S., Glinka, K. (2017) The Individual in the Data, the Aspect of Personal Relevance in Designing Casual Data Visualisations. i-com Journal of Interactive Media. Special issue: Human-Computer Interaction in Geovisualization. De Gruyter.16(3).<sup class="print"></sup>


### Umsetzung

Bei der Umsetzung wurde die in <a class="local" href="chapter02.html">Kapitel 2</a> beschriebene client-side classifiction genutzt, in Kombination mit vorberechneten statischen Datenextrakten. Hierdurch konnte eine privatsphären-konforme Implementation der folgenden Prototypen sichergestellt werden. Während der Interaktion mit den Visualisierungen werden keine Daten über die Nutzer\*innen gespeichert.

Beide Prototypen nutzen das sogenannte Scrollytelling-Konzept. Die Benutzer\*innen müssen zur Interaktion einfach nur scrollen. Dadurch werden Animationen und Interaktionen ausgelöst. Diese niedrigschwellige Form der Interaktion ist sehr intuitiv und funktioniert sowohl auf Desktop als auch auf mobilen Endgeräten. Die Nutzer\*innen können durch das Scrolling, die Gewschwindigkeit der Erzählung selber beeinflussen und steuern.

Für weitere technische Details der Umsetzung, siehe <a class="local" href="chapter05.html">Kapitel 5</a>.

### Prototyp I - Klimawandel und Mobilität

Um den Klimawandel zu verlangsamen, muss der Ausstoß schädlicher Treibhausgase reduziert werden. CO2 ist unter den Treibhausgasen einer der wichtigsten Treiber des Klimawandels. 30% der CO2-Emissionen in Europa werden durch den Verkehr verursacht. PKWs sind für mehr als 13% der CO-Emissionen in Europa verantwortlich. Während wir als Bürger\*innen nur indirekten Einfluss auf viele Formen der CO2-Produktion haben, können wir sehr direkten Einfluss auf unsere tägliche Mobilität nehmen und damit einen Beitrag leisten. 

In diesem ersten Prototypen sollen verschiedene Szenarien geplanter CO2-Reduktion und deren Auswirkungen auf unsere Mobilität aufgezeigt werden.

<div class="page-break"></div>

<figure>
<figcaption>Protoyp Mobilität: Intro</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/mobilitaet/mobilitaet-1.png" alt="" /></center>
</figure>

Hierzu wird den Leser\*innen zuerst aufgezeigt, welche Bedeutung dem PKW in Bezug auf CO2-Emissionen zukommt. Hierzu werden animierte Graphen genutzt, welche mit kurzen Absätzen unterstützt werden. Die Informationen werden in kleine Einheiten aufgebrochen und in Kombination aus Text und Visualisierung vermittelt.

<figure>
<figcaption>Protoyp Mobilität: Allgemeine Einführung in die Thematik</figcaption>
<center>
<img style="width:50%; margin:0; padding:0; display:inline;" src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/mobilitaet/mobilitaet-2.png" alt="" /><img style="width:50%; margin:0; padding:0; display:inline;" src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/mobilitaet/mobilitaet-3.png" alt="" /></center>
</figure>

Dieser erste Abschnitt ist noch sehr allgemein gehalten. Als Einstieg in den personalisierten Bereich müssen die Leser\*innen ein paar Informationen über sich preisgeben. Diese werden anschließend genutzt, um die Erzählung anzupassen.

<figure>
<figcaption>Protoyp Mobilität: Interface zur Erfassung der persönlichen Angaben</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/mobilitaet/mobilitaet-4.png" alt="" /></center>
</figure>

Die personalisierte Erzählung beginnt dann mit einem Wechsel zur von der Nutzer\*in eingegebenen Postleitzahl. Dort wird durch einen Kreis die durchschnittliche tägliche Reisedistanz aufgezeigt, basierend auf dem gewählten Fortbewegungsmittel (basierend auf [Mobilität in Tabellen](https://mobilitaet-in-tabellen.dlr.de/)<sup class="print"></sup>, DLR).

<div class="page-break"></div>

<figure>
<figcaption>Protoyp Mobilität: Darstellung der ausgewählten Region mit der durchschnittlichen Reiseentfernung anderer Bürger*innen</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/mobilitaet/mobilitaet-5.png" alt="" /></center>
</figure>

Im nächsten Schritt wird der Durchschnitt mit der Angabe der Leser\*in kombiniert und erlaubt ein erstes Reflektieren der eigenen Mobilität mit dem Durchschnitt in der Region. Der Einbezug regionalisierter Durchschnitte ist durchaus relevant, da es regionale Unterschiede im Mobilitätsverhalten gibt, z.B. zwischen ländlichen und städtischen Regionen.

<div class="page-break"></div>

<figure>
<figcaption>Protoyp Mobilität: Vergleich der durchschnittlichen Reiseentfernung mit der eigenen Angabe</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/mobilitaet/mobilitaet-6.png" alt="" /></center>
</figure>

In den darauf folgenden Schritten wird der CO2-Fußabdruck der eigenen Mobilität in den Fokus genommen. Basierend auf Prognosen des Umweltbundesamts werden verschiedene Szenarien eröffnet, um wieviel man die eigene Mobilität einschränken müsste. Um Alternativen aufzuzeigen, werden anschließend unterschiedliche Mobilitätskombinationen aufgezeigt (z.B. ÖPNV+PKW oder ÖPNV+Rad), um so Mobilitätspotentiale aufzuzeigen. Die Art der Kombinationen und Szenarien hängt von der oben getroffenen Auswahl ab.

<figure>
<figcaption>Protoyp Mobilität: Darstellung von CO-2 Redukations Szenarien in Kombination mit verschiedenen Mobilitäts-Mix-Kombinationen</figcaption>
<center>
<img style="width:33%; margin:0; padding:0; display:inline;" src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/mobilitaet/mobilitaet-7.png" alt="" /><img style="width:33%; margin:0; padding:0; display:inline;" src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/mobilitaet/mobilitaet-8.png" alt="" /><img style="width:33%; margin:0; padding:0; display:inline;" src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/mobilitaet/mobilitaet-9.png" alt="" /></center>
</figure>

Da Flugreisen so viel CO2 produzieren, dass diese im ersten Teil nicht abgebildet werden konnten, haben wir ein abschließendes Modul entwickelt, welches den nächstgelegenen Flughafen zur angegebenen Postleizahl berechnet und dann CO2-Emissionen für Flugreisen mit anderen Mobilitätsformen für Reisen innerhalbs Europa aufzeigt (z.B. für den Ort Weissach im Tal ist der nächstgelegene Flughafen Suttgart, eine Reise von Stuttgart nach Melbourn entspräche 105 Zugreisen nach Madrid). 

<figure>
<figcaption>Protoyp Mobilität: Visualisierung des Fußabdrucks von Flugreisen</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/mobilitaet/mobilitaet-10.png" alt="" /></center>
</figure>


### Prototyp II - Klimawandelrisiken in Deutschland

Der zweite Prototyp setzt sich mit der Thematik der Klimawandelrisiken in Deutschland auseinander. Wenn man den aktuellen Nachrichten folgt, bekommt man häufig das Gefühl vermittelt, dass der Klimawandel zwar akut ist, aber bisher primär andere Länder betrifft, wie exotische Inseln die vom Meeresanstieg bedroht sind oder Waldbrände in Kalifornien und Buschfeuer in Australien. Studien des Umweltbundesamts zeigen aber auf, dass die Folgen des Klimawandels längst in Deutschland angekommen sind und in den nächsten Jahren weiter zunehmen werden.

In dieser Storytelling-Anwendungen werden Erkenntnisse des Umweltbundesamts zu Klimawandelrisiken auf den Wohnort der Leser\*in heruntergebrochen und lokal visualisiert.

<div class="page-break"></div>

<figure>
<figcaption>Protoyp Kliamwandel: Intro</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-2.png" alt="" /></center>
</figure>

Hierzu beginnt der personalisierte Teil der Anwendung, wie im ersten Prototypen, mit dem eingeben der eigenen Postleitzahl. Daraufhin werden die für diese Postleitzahl notwendigen Daten geladen und dargestellt.

<figure>
<figcaption>Protoyp Kliamwandel: Auswahl der Region</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-3.png" alt="" /></center>
</figure>

Der eigentliche Storytelling-Abschnitt beginnt mit einer Verortung der Erzählung in der angegebenen Postleitzahl auf einer Karte.

<figure>
<figcaption>Protoyp Kliamwandel: Darstellung der ausgewählten Region</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-4.png" alt="" /></center>
</figure>

Danach wird erklärt in welcher Klimazone sich dieses Gebiet befindet. In den nächsten Schritten wird die Bedeutung der Klimazone erklärt, zukünftige Entwicklungen und Bereich aus Umwelt, Gesellschaft und Wirtschaft die besonders von diesen Auswirkungen betroffen sind.

<figure>
<figcaption>Protoyp Kliamwandel: Details zur Klimaregion und zukünftigen Herausforderungen</figcaption>
<center>
<img style="width:33%; margin:0; padding:0; display:inline;" src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-5.png" alt="" /><img style="width:33%; margin:0; padding:0; display:inline;" src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-6.png" alt="" /><img style="width:33%; margin:0; padding:0; display:inline;" src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-7.png" alt="" /></center>
</figure>

Abhängig von der eingegebenen Postleitzahl werden weitere Risiken mit lokalem Bezug visualisiert. Diese speziellen Risiken erstrecken sich über Verdichtungsräume (siehe Abbildung), Gebiete an der Küste mit Sturmflutrisiken, bis hin zu Hochwassern in Flussgebieten (siehe nächster Abschnitt).

<figure>
<figcaption>Protoyp Kliamwandel: Verdichtungsräume</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-8.png" alt="" /></center>
</figure>

Für die Visualisierung der lokalen Hochwassergefahren, wurden Daten der [Bundesanstalt für Gewässerkunde](https://geoportal.bafg.de/inspire/download/NZ/servicefeed.xml)<sup class="print"></sup> genutzt. Hierzu werden den Leser\*innen verschiedene Szenarien (Wahrscheinlichkeiten) für Hochwasser aufgezeigt.

<figure>
<figcaption>Protoyp Kliamwandel: Prognosen für Hochwasser</figcaption>
<center>
<img style="width:33%; margin:0; padding:0; display:inline;" src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-9.png" alt="" /><img style="width:33%; margin:0; padding:0; display:inline;" src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-10.png" alt="" /><img style="width:33%; margin:0; padding:0; display:inline;" src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-11.png" alt="" /></center>
</figure>

Um die zeitliche Entwicklung deutlich zu machen, werden zum Abschluss des personalisierten Bereichs die Entwicklungen der lokalen Durchschnittstemperaturen mit den Entwicklungen der Temperaturen in ganz Deutschland verglichen. Hierbei werden der deutliche Anstieg der Temperaturen unabhängig von vllt. lokal abweichenden Phänomenen hervorgehoben. 

<div class="page-break"></div>

<figure>
<figcaption>Protoyp Kliamwandel: Vergleich Temperaturen in Deutschland und der ausgwählten Postleitzahl</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-13.png" alt="" /></center>
</figure>

Der Vergleich zwischen den lokalen und nationalen Temperaturtrends schafft den Bezug zwicher der lokalen und nationalen Ebene. Dies schließt der letzte Abschnitt der Anwendung ab, indem auf einer Deutschlandkarte die Entwicklung der Temperaturen der letzten 100 Jahre abgebildet werden.

<figure>
<figcaption>Protoyp Kliamwandel: Temperaturentwicklung für ganz Deutschland</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-14.png" alt="" /></center>
</figure>

Für Leser\*innen die sich weiter mit der Materie auseinandersetzen wollen, werden zum Abschluss der Anwendungen noch Leseempfehlungen gegeben. Diese Empfehlungen sind auch abhängig von den Angaben der Leser\*innen personalisiert, sodass Themen für die Region der Leser\*in besonders hervorgehoben werden.

<figure>
<figcaption>Protoyp Kliamwandel: Personalisierte Literaturempfehlungen</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/klima/klimawandel-15.png" alt="" /></center>
</figure>
