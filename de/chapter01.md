<div class="print-hide">
<a href="../HTML.html">Zurück zur Übersicht</a>
</div>

## Zusammenfassung

Das Forschungsvorhaben LoCobSS wurde im Rahmen "[Ideenwettbewerb(s) für innovative analoge und digitale Partizipationsformate und -technologien](https://www.bmbf.de/foerderungen/bekanntmachung-2767.html)"<sup class="print"></sup> gefördert (Förderkennzeichen: [16IP103](https://foerderportal.bund.de/foekat/jsp/SucheAction.do?actionMode=view&fkz=16IP103)<sup class="print"></sup>).

Im **Wissenschaftsjahr 2022** soll ein großangelegtes Partizipationsverfahren durch das BMBF durchgeführt werden, um die Perspektive der Bürger\*innen auf Wissenschaft und Forschung in Deutschland zu erfassen. Ein [ähnliches Projekt](https://www.vraagvoordewetenschap.be/)<sup class="print"></sup> gab es bereits 2018 in Belgien. Der Ideenwettbewerb soll innovative Konzepte für die Umsetzung des Prozesses in Deutschland generieren. Dabei sollen sich die Ideen auf drei Phasen fokussieren:
1. Aktivierung & Befragung der Bürger\*innen
2. Analyse, Strukturierung und Auswertung der Fragen
3. Beantwortung und Nachnutzung der Fragen

Das Vorhaben LoCobSS konzentriert sich auf digitale Aspekte des Prozesses und legt einen Fokus auf **privatsphären-konforme Customization der User-Exprience**, sowohl für die **Bürger\*innen** als auch die **Redakteur\*innen** des Ministeriums. Um die entwickelten Methoden und Konzepte anschaulich zu demonstrieren, wurden eine Reihe an Prototypen entwickelt, welche in den folgenden Kapiteln vorgestellt werden.

### Executive Summary

Im Rahmen von LoCobSS wurden eine Reihe von Methoden entwickelt und in Bezug auf ihren Mehrwert für das Partizipationsverfahren evaluiert. Die dabei entstandenen Softwarekomponenten können als prototypische Grundlagen für eine anschließende finale Implementation dienen (siehe technische Dokumentation in <a class="local" href="chapter05.html">Kapitel 5</a>). Die aus dem Vorhaben LoCobSS gewonnenen Erkenntnisse sollen zukünftige Ausschreibungen und weitere Entwicklungen zum Partizipationsverfahren leiten und unterstützen:

#### 1.1.1 Privatsphäre sollte höchste Priorität haben

Nicht zuletzt die Entwicklung der Corona-Warn-App haben gezeigt, dass der Anspruch an und das Bewusstsein für das Thema Privatsphäre in der Bevölkerung weiter zunimmt. Für öffentliche Institutionen und Ministerien sollte diesem Thema folglich höchste Priorität zuteil werden.

Der Schutz der Privatsphäre steht einer Erhebung statistischer Daten nicht im Wege. Es sollten dabei einige Grundsätze beachtet werden:
- Es werden nur Daten erhoben, die tatsächlich *notwendig* sind (Datensparsamkeit & Datenvermeidung).
- Wenn Daten nicht in personenbezogender Form benötigt werden, müssen User-Daten und statistische Daten (unumkehrbar) getrennt bleiben.
- Dark-Design Patterns müssen vermieden werden (z.B. opt-in statt opt-out).

Weitere Hilfestellungen finden Sie in <a class="local" href="chapter02.html">Kapitel 2</a>.

#### 1.1.2 Barrierearm und nutzerfreundlich

Um eine möglichst breite Gruppe der Bevölkerung am Verfahren zu beteiligen, sollten Barrieren niedrig gehalten werden:

- Einfache Sprache wählen
- Möglichst wenig Pflichtfelder vorgeben
- Möglichst wenig Eingabebeschränkungen/-pflichten
- Keinen Registrierungszwang
- Mehrsprachigkeit unterstützen
- Den Nutzungsgewohnheiten und -ansprüchen entsprechen (z.B. Mobil-optimiert)

Weitere Hilfestellung hierzu ist im Prototypen zur Erfassung von Fragen in <a class="local" href="chapter02.html">Kapitel 2</a> aufgeführt.

**Kommentar**: Das Vorhaben LoCobSS hat sich auf digitale Komponenten des Partizipationsverfahren konzentriert. Für eine tatsächlich inklusive Gestaltung des Verfahrens sollten diese digitalen Komponenten nur einen Teil einer breit aufgestellten Aktivierungsstrategie darstellen und mit analogen Komponenten und einer breit aufgestellten Outreach-Kampagne kombiniert werden.

#### 1.1.3 Auch an die Redakteur\*innen denken

Während der Fokus des Partizipationsverfahrens klar auf der Aktivierung und Beteiligung von Bürger\*innen liegt, sollte nicht vergessen werden, dass ein gut ausgestattetes Team für die Redaktion der Inhalte unabdingbar ist. Das vergleichbare Projekt und Partizipationsverfahren in Belgien hat über 10.000 Fragen generiert. Entsprechend ist (bei vergleichbarer Durchführung) damit zu rechnen, dass in Deutschland über 50.000 Fragen zu erwarten sind. Die von Bürger\*innen eingereichten Fragen müssen validiert (Relevanz-Check, Schimpfwörter entfernen, missbräuchliche Einreichungen löschen oder nicht freigeben, etc.) und schließlich kategorisiert werden. LoCobSS hat die Möglichkeiten der Automatisierung bzw. automatisierten Unterstützung dieser Schritte auf Basis der Daten des belgischen Verfahrens evaluiert und zieht daraus folgende Schlüsse:

- Algorithmische Verfahren zur automatisierten Erkennung von Beschimpfungen, Hate-Speech, etc. sind bisher nur teilweise dazu in der Lage, unangebrachte Beiträge zuverlässig zu identifizieren. Entsprechende Verfahren können daher lediglich unterstützend angewendet werden und müssen weiterhin manuell ergänzt bzw. korrigiert werden.
- Sentimentanalysen (algorithmische Analysen) von Texten zur Erfassung von persönlichen Einstellungen, Stimmungen oder Haltungen zu bestimmten Themen haben ebenso nur eine bedingte Genauigkeit und sollten daher nicht für kritische Entscheidungen eingesetzt werden.
- Eine Unterstützung bei der Kategorisierung von Beiträgen kann allerdings durch algorithmische Verfahren der Inhaltsanalyse (z.B. word2vec oder ähnliche Verfahren) essenziell unterstützt werden. Hierzu haben wir einen funktionsfähigen Prototypen entwickelt.

Insgesamt lässt sich zu algorithmischen Verfahren für die Textanalyse zusammenfassend festhalten, dass diese häufig auf die englische Sprache hin optimiert sind. Durch eine vorgeschaltete Übersetzung der Inhalte kann diese Einschränkung jedoch in vielen Bereich umgangen werden. Bei sprachspezifischen Problemen, wie z.B. Beleidigungen, stoßen gängige Verfahren zur automatisierten Textanalyse ohne weitere Anpassungen (z.B. Optimierung durch erweiterte Trainingsdaten bei Machine Learning Prozessen) aber an ihre Grenzen.

Details zum Prototypen für die Kategorisierung von Beiträgen in <a class="local" href="chapter03.html">Kapitel 3</a>.

#### 1.1.4 Customization: Content-Recommendation

Durch Customization-Methoden kann die User-Experience personalisiert werden und so zu einer intensiveren Auseinandersetzung mit der Plattform führen. Um das explorieren der Inhalte auf der Plattform zu erleichtern und Serendipität zu fördern, sollten neben einer klassischen Suche auch Recommender-Funktionalitäten integriert werden. Hierbei unterscheidet man zwischen Content-based Recommendation und Collaborative Recommendation. Für letzteren Ansatz müssten allerdings die Interaktionen der Nutzer\*innen erfasst werden. Zum Schutz der Privatsphäre der Nutzer\*innen sollte dieser Ansatz nur mit bedacht durchgeführt werden. Im Rahmen dieses Vorhabens haben wir daher einen prototypischen Content-based Recommender entwickelt, der keinerlei Nutzer\*innendaten speichert und auf denselben Prinzipien des Redaktionswerkzeugs für die Kategorisierung aufbaut. 

Mehr zum Content-based Recommender in <a class="local" href="chapter03.html">Kapitel 3</a>.

#### 1.1.5 Customization: Wissenschaftsvermittlung

Klassische Wissenschaftsvermittlung ist häufig statisch, unidirektional und textlastig. Im Rahmen von LoCobSS haben wir in Abgrenzung dazu mit modernen Methoden des Datenjournalism und das data-driven Storytellings neue Formate zur Vermittlung wissenschaftlicher Erkenntnisse in Form von zwei interaktiven Prototypen entwickelt, die sich individuell personalisieren lassen. So wird die Lebenswelt der Nutzer\*innen in die Kommunikation mit einbezogen und erlaubt ihnen, direkte Bezüge zwischen ihrer Lebenswelt und den vermittelten Inhalten herzustellen. Durch interaktive Elemente wird die Aufmerksamkeit der Nutzer\*innen gebunden. Explorative Elemente laden zu einer tiefergehenden Auseinandersetzung mit der Materie ein. Auch bei den Ansätzen zur Personalisierung bleibt die Privatsphäre der Nutzer\*innen gewahrt.

Eine detaillierte Erklärung der beiden Prototypen folgt in <a class="local" href="chapter04.html">Kapitel 4</a>.

**Kommentar**: Falls auf diesen Prototypen aufbauende ähnliche Formate zur Vermittlung wissenschaftlicher Erkenntnisse und Themen häufiger implementiert und angepasst werden sollen, würde es Sinn machen, diese Konzepte zu standardisieren und entsprechende Frameworks zur Verfügung zu stellen. Dies würde es ermöglichen, neue Themen einfach und nachhaltig durch Nutzung des Frameworks zu erschließen und zu kommunizieren.

### Projekterfolgskontrolle

#### 1.2.1 Forschungsfragen

**Wie lassen sich Konzepte lebensweltlicher Taxonomien (z.B. Lebenslagen) mit Taxonomien wissenschaftlicher Wissensrepräsentation verbinden?**

**Wie lassen sich die Fragen der Bürger\*innen von den Wissenschaftler\*innen praxisnah und forschungsrelevant auswerten?**

Es ist mit einer extrem großen Zahl an Inhalten zu rechnen, die von den Redakteur\*innen bearbeitet werden müssen. Mit dem Ziel, Teile der Verwaltung dieser Inhalte technisch unterstützen oder automatisieren zu können, wurden verschiedene verfahren des Maschinellen Lernens (ML) exploriert. Die erfolgreichsten Ergebnisse wurden im Bereich der Kategorisierung (Taxonomien) erzielt. Hierzu wurde ein kooperatives ML-System entwickelt, welches die Redakteur\*innen bei ihrer Arbeit unterstütz und gleichzeitig den Bürger\*innen erlaubt die Inhalte einfach zu durchsuchen. Siehe hierzu <a class="local" href="chapter03.html">Kapitel 3</a>.

-----

**Wie lässt sich eine solche Erhebung mit dem Schutz der Privatsphäre der teilnehmenden Personen vereinen?**

Diese Dokumentation enthält Empfehlungen (siehe <a class="local" href="chapter02.html">Kapitel 2</a>) zur Konzeption und Umsetzung von Umfragen mit Fokus auf Wahrung der Privatsphäre der Teilnehmer\*innen. Für die Erhebung von daraus abgeleiteten Attributen wurde ein client-side classification Ansatz entwickelt. Die Empfehlungen und client-side classification wurden beispielhaft in einem Survey Prototypen (siehe <a class="local" href="chapter05.html">Kapitel 5</a>) implementiert.

-----

**Wie kann die Relevanz wissenschaftlicher Inhalte für die Bürger\*innen erhöht werden?**

**Welche Potentiale ergeben sich durch die Erhebung des räumlichen Kontextes in Hinblick auf die individuelle Relevanz der Inhalte?**

In Fortführung der Personalisierungsmethoden wurden zwei exemplarische Wissenschaftskommunikations-Anwendungen entwickelt, welche den räumlichen Kontext der Leser\*innen nutzen, um das interaktive Storytelling zu personalisieren. Mehr in <a class="local" href="chapter04.html">Kapitel 4</a>.

<div class="page-break"></div>

#### 1.2.2 Arbeitspakete

1. **Konzeption**: Die inhaltliche Konzeption ist in diese Dokumentation eingeflossen. Die technische Dokumentation befindet sich in <a class="local" href="chapter05.html">Kapitel 5</a>.
2. **Anwendungsbasis**: Um die einzelnen Komponenten möglichst realistisch demonstrieren und testen zu können, wurde eine webbasierte Anwendung entwickelt, welche in rudimentären Zügen die spätere Beteiligungsanwendung abbildet (Fragen eingeben, Fragen & Teilnehmer\*innen administrieren, Fragen kategorisieren), siehe <a class="local" href="chapter05.html">Kapitel 5</a>.
3. **Kontextualisierung**: Um die algorithmischen Verfahren zu automatischen Verarbeitung des Inputs der Bürger\*innen evaluieren zu können, wurden die Daten des belgischen Verfahrens als Basis genutzt. Die resultierenden Komponenten wurden modular als Microservices aufgesetzt, um eine spätere Nachnutzung möglichst einfach zu gestalten.
4. **Data-driven Storytelling**: Es wurden zwei interaktive Prototypen zur Vermittlung wissenschaftlicher Erkenntnisse entwickelt. Ein Prototyp zum Thema Klimawandel und Mobilität und ein Prototyp zum Thema Klimawandelrisiken in Deutschland. Die Anwendungen basieren auf Daten und Informationen des Umweltbundesamts.
5. **Evaluation**: Die Evaluation hat sich während der Corona-Pandemie als sehr schwierig gestaltet. Besonders der Kontakt zu Expert\*innen innerhalb der Ministerien war kaum möglich (was in diesen Zeiten durchaus verständlich ist). Wir haben die Konzepte und Prototypen deshalb mit Expert\*innen aus unserem privaten Netzwerk über virtuelle Formate evaluiert und das Feedback im iterativen Entwicklungsprozess eingearbeitet.
6. **Dokumentation**: Die Dokumentation wurde als Web- und PDF-Version umgesetzt. Alle entwickelten Softwarekomponenten wurden als frei lizensierter Quellcode unter einer MIT-Lizenz veröffentlicht und zur Nachnutzung gestellt. Für Links zu den einzelnen Repositorien, siehe <a class="local" href="chapter05.html">Kapitel 5</a>.
