<div class="print-hide">
<a href="../HTML.html">Zurück zur Übersicht</a>
</div>

## Prototyp: Technische Dokumentation

Die technische Dokumentation gliedert sich in zwei Abschnitte. Zum einen die Umfrage-Plattform und alle dazugehörigen Komponenten und zum anderen die beiden Prototypen zur daten-gestützten Wissenschaftsvermittlung. Die hier vorliegende Dokumentation gibt eine Übersicht der verschiedenen entwickelten Komponenten. Eine detaillierte stärker technische Dokumentation befindet sich in den einzelnen Code-Repositorien, welche hier verlinkt werden. Diese detaillierten Dokumentationen sind in englische Sprache verfasst, um eine möglichste breite Nachnutzbarkeit der einzelnen Komponenten sicherzustellen.

Obwohl sich viele der Komponenten kurz vor einem Release-State befinden, muss hier deutlich unterstrichen werden, dass es sich hierbei nicht um einen Release-Candidate handelt. Ziel des Vorhabens war es Ideen und Möglichkeiten aufzuzeigen, um dies möglichst realistisch zu tun und gleichzeitig erste Grundlagen für eine spätere Implementierung zu schaffen, wurden diverse Komponenten und Prototypen entwickelt. Um das ganze hin zu einem Release weiterzuentwickeln sollten vor allem folgenden Punkte bearbeitet werden:

- Test für alle Bereiche schreiben
- Continous-Deployment verfeinern und mit Tests kombinieren
- Weitere Mobil-Optimierungen
- Frontends auf allen Browsern testen
- Code und Implementation auf Skalierung hier optmieren
- Sicherheitsfeatures ergänzen und überprüfen
- Datenschutzbestimmung basierend auf den genutzten Komponenten erarbeiten

#### 5.1 Umfrage-Plattform

#### 5.1.1 Übersicht

In der aktuellen Version wurden die Services und Komponenten für die Google-Cloud-Infrastruktur optimiert. Die meisten Komponenten sind aber völlig plattform-unabhängig. Die einzigen Komponenten die sich nicht ganz so leicht anpassen lassen sind alle Komponenten rund um die Nutzerverwaltung. Da selbige nicht im Fokus der prototypischen Entwicklung, haben wir Googles Firebase Ökosystem genutzt, um möglichst unkompliziert eine Verwaltung von Nutzer\*innen implementieren zu können.

<figure>
<figcaption>Informationsarchitektur</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/architecture.png" alt="" /></center>
</figure>

#### 5.1.2 Frontend

Das Frontend in der alle Komponenten für die Umfrage zusammenfließen ist im **LoCobSS-platform** Repository zusammengeführt. Es handelt sich hierbei um eine sogenannte Single Page Application (SPA), welche mit dem Framework [SVELTE](https://svelte.dev/)<sup class="print"></a> entwickelt wurde. Die Anwendung lässt sich grob in drei Hauptbereiche unterteilen: 1) Öffentlicher Bereich zum Durchstöbern der Fragen und Fragen stellen, 2) Interner Bereich für Bürger\*innen zur Verwaltung der eigenen Daten und zur Verfolgung von Fragen, sowie 3) der Bereich für Redakteur\*innen zum Verwalten der Fragen und Nutzer\*innen.

**Öffentlicher Bereich**



**Repo: [LoCobSS-platform](https://www.github.com/sebastian-meier/LoCobSS-platform)<sup class="print"></sup>**




- [LoCobSS-text-similarity](https://www.github.com/sebastian-meier/LoCobSS-text-similarity)
- [LoCobSS-text-similarity-dataflow](https://www.github.com/sebastian-meier/LoCobSS-text-similarity-dataflow)
- [LoCobSS-text-profanity](https://www.github.com/sebastian-meier/LoCobSS-text-profanity)
- [LoCobSS-text-sentiment](https://www.github.com/sebastian-meier/LoCobSS-text-sentiment)
- [LoCobSS-authentication-UI](https://www.github.com/sebastian-meier/LoCobSS-authentication-UI)
- [LoCobSS-dwd-transform](https://www.github.com/sebastian-meier/LoCobSS-dwd-transform)
- [LoCobSS-co2-data](https://www.github.com/sebastian-meier/LoCobSS-co2-data)
- LoCobSS-stories...

#### 5.2 Daten-gestütztes Storytelling

