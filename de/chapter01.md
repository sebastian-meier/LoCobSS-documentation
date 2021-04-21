# Teil 1

## 1.1 Einleitung
Das Forschungsvorhaben LoCobSS wurde im Rahmen "[Ideenwettbewerb(s) für innovative analoge und digitale Partizipationsformate und -technologien](https://www.bmbf.de/foerderungen/bekanntmachung-2767.html)" gefördert (Förderkennzeichen: [16IP103](https://foerderportal.bund.de/foekat/jsp/SucheAction.do?actionMode=view&fkz=16IP103)).

Im **Wissenschaftsjahr 2022** soll ein großangelegtes Partizipationsverfahren durch das BMBF durchgeführt werden, um die Perspektive der Bürger\*innen auf Wissenschaft und Forschung in Deutschland zu erfassen. Ein [ähnliches Projekt](https://www.vraagvoordewetenschap.be/) gab es bereits 2018 in Belgien. Der Ideenwettbewerb soll innovative Konzepte für die Umsetzung des Prozesses in Deutschland generieren. Dabei sollen sich die Ideen auf drei Phasen fokussieren:
- 1. Aktivierung & Befragung der Bürger\*innen
- 2. Analyse, Strukturierung und Auswertung der Fragen
- 3. Beantwortung und Nachnutzung der Fragen

Das Vorhaben LoCobSS konzentriert sich auf digitale Aspekte des Prozesses, mit einem spezifisch Fokus auf **privatsphären-konforme Customization der User-Exprience**, sowohl für die **Bürger\*innen** als auch die **Redakteur\*innen** des Ministeriums. Um die entwickelten Methoden und Konzepte zu demonstrieren wurden eine Reihe an Prototypen entwickelt, welche in den folgenden Kapiteln vorgestellt werden.

## 1.2 Executive Summary

Im Rahmen von LoCobSS wurden eine Reihe Methoden entwickelt und evaluiert in Bezug auf einen Mehrwert für das Partizipationsverfahren. Die dabei entstandenen Softwarekomponenten können als prototypische Grundlagen für eine finale Implementation dienen (siehe [technische Dokumentation](chapter04.md)). Doch noch viel wichtiger, sollen die folgenden Erkenntnisse Ausschreibungen und weitere Entwicklungen zum Partizipationsverfahren leiten und unterstützen:

### 1.2.1 Privatsphäre sollte höchste Priorität haben

Nicht zuletzt die Entwicklung der Corona-App haben gezeigt, dass das Bewusstsein in der Bevölkerung für das Thema Privatsphäre weiter zunimmt. Als öffentliche Institution sollte diesem Thema höchste Priorität gewidmet werden.

Der Schutz der Privatsphäre steht einer Erhebung statistischer Daten nicht im Wege. Es sollten dabei einige Grundsätze beachtet werden:
- Nur Daten erheben die tatsächlich *notwendig* sind (Datensparsamkeit & Datenvermeidung).
- Wenn Daten nicht in personenbezogender Form benötigt werden, User-Daten und statistische Daten (unumkehrbar) trennen.
- Vermeiden von Dark-Design Patterns (z.B. opt-in statt opt-out).

Weitere Hilfestellungen finden Sie in [Kapitel 2](chapter02.md).

### 1.2.2 Barrierearm und nutzerfreundlich

Um eine möglichst breite Gruppe der Bevölkerung am Verfahren zu beteiligen, sollten Barrieren niedrig gehalten werden:

- Einfache Sprache wählen
- Möglichst wenig Pflichtfelder
- Möglichst wenig Eingabebeschränken/-pflichten
- Keinen Registrierungszwang
- Mehrsprachigkeit unterstützen
- Den Nutzungsgewohnheiten und -ansprüchen entsprechen (z.B. Mobil-optimiert)

Weitere Hilfestellung hierzu im Prototypen zur Erfassung von Fragen in [Kapitel 2](chapter02.md).

**Kommentar**: Dieses Vorhaben hat sich auf digitale Komponenten des Partizipationsverfahren konzentriert. Für eine besonders inklusive Gestaltung des Verfahrens, sollten die digitalen Komponenten nur ein Teil der Aktivierungsstrategie darstellen und mit analogen Komponenten und einer breit aufgestellten Outreach-Kampagne kombiniert werden.

### 1.2.3 Auch an die Redakteur*innen denken

Während der Fokus klar auf die Bürger\*innen liegt, sollte nicht vergessen werden, dass es auch ein gut ausgestattets Team zur Redaktion der Inhalte benötigt. Das Verfahren in Belgien hat über 10.000 Fragen generiert. Entsprechend ist davon auszugehen, dass in Deutschland über 50.000 Fragen zu erwarten sind. Die eingehenden Fragen müssen validiert (Relevanz, Schimpfwörter, etc.) und kategorisiert werden. LoCobSS hat die Möglichkeiten der Automatisierung dieser Schritte auf Basis der Daten des belgischen Verfahrens evaluiert und zieht daraus folgende Schlüsse:

- Verfahren zur automatisierten Erkennung von Beschimpfungen, Hate-Speech, etc. erkennen diese bisher nur teilweise. Dies kann lediglich unterstützend angewandt werden und muss nachwievor manuell gemacht werden.
- Sentimentanalysen zur Erfassung von Einstellungen zu bestimmten Themen funktionieren auch nur bedingt und sollten nicht für kritische Entscheidungen eingesetzt werden.
- Eine Unterstützung der Kategorisierung kann durch Verfahren der Inhaltsanalyse (z.B. word2vec ähnliche Verfahren) essentiell unterstützt werden. Hierzu haben wir einen funktionsfähigen Prototypen entwickelt.

Insgesamt lässt sich zu automatisierten Verfahren sagen, dass viele auf die englische Sprache hin optimiert sind. Durch die Übersetzung der Inhalte kann dies in vielen Bereich umgangen werden. Bei sprachspezifischen Problemen, wie z.B. Beleidigungen stoßen diese Ansätze aber an ihre Grenzen.

Details zum Prototypen zur Kategorisierung in [Kapitel 3](chapter03.md).

### 1.2.4 Customization: Content-Recommendation

Durch Customization-Methoden kann die User-Experience personalisiert werden und so zu einer intensiveren Auseinandersetzung mit der Plattform führen. Um das explorieren der Inhalte auf der Plattform zu erleichtern und Serendipität zu fördern, sollte neben einer klassischen Suche auch Recommender-Funktionalitäten integriert werden. Hierbei unterscheidet man zwischen Content-based Recommendation und Collaborative Recommendation. Für letzteren Ansatz müssen die Interaktionen der Nutzer\*innen erfasst werden. Aus Privatsphärengründen sollte dies nur mit bedacht durchgeführt werden. Im Rahmen dieses Vorhabens, haben wir einen prototypischen Content-based Recommender entwickelt, welcher auf den selben Prinzipien des Redaktionswerkzeugs zur Kategoriesierung aufbaut. 

Mehr zum Recommender in [Kapitel 3](chapter03.md).

### 1.2.5 Customization: Wissenschaftsvermittlung

Klassische Wissenschaftsvermittlung ist traditionell statisch, unidirektional und textlastig. Im Rahmen von LoCobSS haben wir mit modernen Methoden des Daten-Journalism und das data-driven Storytellings, neue Formate zur Vermittlung wissenschaftlicher Formate entwickelt, welche sich individuell personalisieren lassen. So wird die Lebenswelt der Leser\*innen in die Kommunikation mit einbezogen und erlaubt den Leser\*innen so direkte Bezüge herzustellen. Durch interaktive Elemente wird die Aufmerksamkeit der Nutzer\*innen gebunden. Explorative Elemente laden zu einer tiefergehenden Auseinandersetzung mit der Materie ein. Die Personalisierung erfolgt ebenfalls mit Blick auf die Wahrung der Privatsphäre.

Eine detaillierte Erklärung der beiden Prototypen folgt in [Kapitel 4](chapter04.md).

**Kommentar**: Sollten solche Formate häufiger ausgerollt werden, würde es Sinn machen diese Konzepte zu standardisieren und entsprechende Frameworks zur Verfügung zu stellen, sodass neue Themen einfach und nachhaltig erschlossen werden können.

## 1.3 Projekterfolgskontrolle

### 1.3.1 Forschungsfragen

**Wie lassen sich Konzepte lebensweltlicher Taxonomien (z.B. Lebenslagen) mit Taxonomien wissenschaftlicher Wissensrepräsentation verbinden?**

**Wie lassen sich die Fragen der Bürger\*innen von den Wissenschaftler\*innen praxisnah und forschungsrelevant auswerten?**

Es ist mit einer extrem großen Zahl an Inhalten zu rechnen, die von den Redakteur*innen bearbeitet werden müssen. Mit dem Ziel Teile dieser Aufgaben zu unterstützen oder automatisieren zu können, wurden verschiedene verfahren des Maschinellen Lernens (ML) exploriert. Die erfolgreichsten Ergebnisse wurden im Bereich der Kategorisierung (Taxonomien) erzielt. Hierzu wurde ein kooperatives ML-System entwickelt, welches die Redakteur\*innen bei ihrer Arbeit unterstütz und gleichzeitig den Bürger\*innen erlaubt die Inhalte einfach zu durchsuchen. Siehe hierzu [Kapitel 3](chapter03.md).

-----

**Wie lässt sich eine solche Erhebung mit dem Schutz der Privatsphäre der teilnehmenden Personen vereinen?**

Diese Dokumentation enthält [Empfehlungen](chapter02.md) zur Konzeption und Umsetzung von Umfragen mit Fokus auf Wahrung der Privatsphäre der Teilnehmer*innen. Für die Erhebung von abgeleiteten Attributen, wurde ein client-side classification Ansatz entwickelt. Die Empfehlungen und client-side classification wurden beispielhaft in einem [Survey Prototypen](chapter05.md) implementiert.

-----

**Wie kann die Relevanz wissenschaftlicher Inhalte für die Bürger\*innen erhöht werden?**

**Welche Potentiale ergeben sich durch die Erhebung des räumlichen Kontextes in Hinblick auf die individuelle Relevanz der Inhalte?**

In Fortführung der Personalisierungsmethoden wurden zwei exemplarische Wissenschaftskommunikations-Anwendungen entwickelt, welche den räumlichen Kontext der Leser\*innen nutzen, um das interaktive Storytelling zu personalisieren. Mehr hierzu in [Kapitel 4](chapter04.md).

### 1.3.2 Arbeitspakete

1. **Konzeption**: Die inhaltliche Konzeption ist in diese Dokumentation eingeflossen. Die technische Dokumentation befindet sich in [Kapitel 5](chapter05.md).
2. **Anwendungsbasis**: Um die einzelnen Komponenten möglichst realistisch demonstrieren und testen zu können, wurde eine web-basierte Anwendung entwickelt, welche in rudimentären Zügen die spätere Beteiligungsanwendung abbildet (Fragen eingeben, Fragen & Teilnehmer administrieren, Fragen kategorisieren), siehe [Kapitel 5](chapter05.md).
3. **Kontextualisierung**: Um die algorithmischen Verfahren zu automatischen Verarbeitung des Inputs der Bürger\*innen evaluieren zu können, wurden die Daten des belgischen Verfahrens als Basis genutzt. Die resultierenden Komponenten wurden modular als Microservices aufgesetzt, um eine spätere Nachnutzung möglichst einfach zu gestalten.
4. **Data-driven Storytelling**: Es wurden zwei interaktive Anwendungen zur Vermittlung wissenschaftlicher Erkenntnisse entwickelt. Ein Prototyp zum Thema Klimawandel und Mobilität und ein Prototyp zum Thema Klimawandelrisiken in Deutschland. Die Anwendungen basieren auf Daten und Informationen des Umweltbundesamts.
5. **Evaluation**: Die Evaluation hat sich in Zeiten von Corona sehr schwierig gestaltet. Besonders der Kontakt zu Expert\*innen innerhalb der Ministerien (was in diesen Zeiten durchaus verständlich ist). Wir haben die Konzepte und Prototypen deshalb mit Expert\*innen aus unserem Netzwerk evaluiert und das Feedback eingearbeitet.
6. **Dokumentation**: Die Dokumentation wurde als Web- und PDF-Version umgesetzt. Alle entwickelten Software-Komponenten wurden alls quelloffener Source Code zur Verfügung gestellt. Für Links zu den individuellen Repositorien, siehe [Kapitel 5](chapter05.md).