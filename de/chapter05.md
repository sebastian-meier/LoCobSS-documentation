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
- Code refactoring
- In LoCobSS-plattform Trennen von Bürger\*innen-Plattform und Verwaltungsebene in zwei Anwendungen, um den Fußabdruck zu verkleinern. 

#### 5.1 Umfrage-Plattform

#### 5.1.1 Übersicht

In der aktuellen Version wurden die Services und Komponenten für die Google-Cloud-Infrastruktur optimiert. Die meisten Komponenten sind aber völlig plattform-unabhängig. Die einzigen Komponenten die sich nicht ganz so leicht anpassen lassen sind alle Komponenten rund um die Nutzerverwaltung. Da selbige nicht im Fokus der prototypischen Entwicklung, haben wir Googles Firebase Ökosystem genutzt, um möglichst unkompliziert eine Verwaltung von Nutzer\*innen implementieren zu können.

<figure>
<figcaption>Informationsarchitektur</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/architecture.png" alt="" /></center>
</figure>

#### 5.1.2 Frontend

Das Frontend in der alle Komponenten für die Umfrage zusammenfließen ist im **LoCobSS-platform** Repository zusammengeführt. Es handelt sich hierbei um eine sogenannte Single Page Application (SPA), welche mit dem Framework [SVELTE](https://svelte.dev/)<sup class="print"></a> entwickelt wurde. Die Anwendung lässt sich grob in drei Hauptbereiche unterteilen: 1) Öffentlicher Bereich zum Durchstöbern der Fragen und Fragen stellen, 2) Interner Bereich für Bürger\*innen zur Verwaltung der eigenen Daten und zur Verfolgung von Fragen, sowie 3) der Bereich für Redakteur\*innen zum Verwalten der Fragen und Nutzer\*innen.

**Repo: [LoCobSS-platform](https://www.github.com/sebastian-meier/LoCobSS-platform)<sup class="print"></sup>**

**Öffentlicher Bereich**

Nutzer\*innen können die von anderen Teilnehmer\*innen erstellten Inhalte auf der Plattform im öffentlichen Bereich explorieren. Inhalte können nach Taxonomien, Datum, Suchbegriffen und ob es schon eine Antwort für die Frage gibt, gefiltert werden. Um das System möglichst performant zu machen, werden immer nur 10 Fragen angezeigt. Nutzer\*innen die eingeloggt sind, können hier auch schon Fragen markieren. Daten werden über die [API](https://www.github.com/sebastian-meier/LoCobSS-api)<sup class="print"></sup> bereitgestellt.

**Router**: src/lib/routes/survey.ts<br />
**View**: src/views/pages/survey/list.svelte<br />
**API**: /public/questions

<figure>
<figcaption>Prototyp: Fragen erkunden</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/survey_list.png" alt="" /></center>
</figure>

Zu jeder Frage gibt es auch eine Detailansicht. Neben weiteren Details zur Frage, werden hier auch ähnliche Fragen angzeigt. Diese werden über die API abgerufen, welche dafür den [similarity-Service](https://www.github.com/sebastian-meier/LoCobSS-similarity)<sup class="print"></sup> nutzt.

**Router**: src/lib/routes/survey.ts<br />
**View**: src/views/pages/survey/details.svelte<br />
**API**: /public/questions/:id

<figure>
<figcaption>Prototyp: Detailansicht einer Frage</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/survey_detail.png" alt="" /></center>
</figure>

<div class="page-break"></div>

Besucher\*innen der Plattform könne auch direkt Fragen stellen, ohne sich vorher registrieren zu müssen. Das [Recaptcha-Verfahren](https://developers.google.com/recaptcha/docs/display)<sup class="print ignore">11</sup> wird genutzt, um die Seite weitesgehend vor Spam zu schützen.

**Router**: src/lib/routes/survey.ts <br />
**View**: src/views/pages/survey/ask.svelte<br />
**API**: /question/create

<figure>
<figcaption>Prototyp: Frage stellen</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/survey_ask.png" alt="" /></center>
</figure>

**Router**: src/lib/routes/survey.ts<br />
**View**: src/views/pages/survey/ask.svelte<br />
**API**: /question/link

https://www.github.com/sebastian-meier/LoCobSS-text-profanity<sup class="print"></sup>
https://www.github.com/sebastian-meier/LoCobSS-similarity<sup class="print"></sup>
https://www.github.com/sebastian-meier/LoCobSS-text-sentiment<sup class="print"></sup>

<figure>
<figcaption>Prototyp: Crowd-sourced Classification</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/survey_crowd.png" alt="" /></center>
</figure>

**Router**: src/lib/routes/user.ts<br />
**View**: src/views/pages/user/register.svelte

<figure>
<figcaption>Prototyp: Registrierung</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/user_register.png" alt="" /></center>
</figure>

**Router**: src/lib/routes/user.ts <br />
**View**: src/views/pages/user/login.svelte

<figure>
<figcaption>Prototyp: Login</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/user_login.png" alt="" /></center>
</figure>

**Router**: src/lib/routes/user.ts <br />
**View**: src/views/pages/user/view.svelte

<figure>
<figcaption>Prototyp: Benutzer-Account</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/user_welcome.png" alt="" /></center>
</figure>

**Router**: src/lib/routes/survey.ts <br />
**View**: src/views/pages/survey/mylist.svelte<br />
**API**: /user/questions<br />
**API**: /user/question/like/:id

<figure>
<figcaption>Prototyp: Favoriten und eigene Fragen der Benutzer*in</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/user_list.png" alt="" /></center>
</figure>

**Router**: src/lib/routes/admin.ts<br />
**View**: src/views/pages/admin/questions/list.svelte<br />
**API**: /questions<br />
**API**: /question/delete/:id

<figure>
<figcaption>Prototyp: Administration - Liste der Fragen</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/questions_list.png" alt="" /></center>
</figure>

**Router**: src/lib/routes/admin.ts <br />
**View**: src/views/pages/admin/questions/edit.svelte<br />
**API**: /question/update/:id

<figure>
<figcaption>Prototyp: Administration - Detailansicht einer Frage</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/questions_edit.png" alt="" /></center>
</figure>

**Router**: src/lib/routes/admin.ts<br />
**View**: src/views/pages/admin/questions/cluster.svelte<br />
**API**: /related/questions/cluster<br />
**API**: /public/taxonomies<br />
**API**: /taxonomy/assign<br />
**API**: /taxonomy/create

<figure>
<figcaption>Prototyp: Administration - Fragen Klassifzieren</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/questions_cluster.png" alt="" /></center>
</figure>

**Router**: src/lib/routes/admin.ts<br />
**View**: src/views/pages/admin/taxonomy/list.svelte<br />
**API**: /public/taxonomies<br />
**API**: /taxonomy/delete/:id

<figure>
<figcaption>Prototyp: Administration - Liste der Taxonomien</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/taxonomy_list.png" alt="" /></center>
</figure>

**Router**: src/lib/routes/admin.ts<br />
**View**: src/views/pages/admin/taxonomy/edit.svelte<br />
**API**: /taxonomy/edit/:id

<figure>
<figcaption>Prototyp: Administration - Taxonomie bearbeiten</figcaption>
<center><img src="https://sebastian-meier.github.io/LoCobSS-documentation/assets/images/prototype/taxonomy_edit.png" alt="" /></center>
</figure>

- [LoCobSS-text-similarity-dataflow](https://www.github.com/sebastian-meier/LoCobSS-text-similarity-dataflow)<sup class="print"></sup>

#### 5.2 Daten-gestütztes Storytelling
- [LoCobSS-dwd-transform](https://www.github.com/sebastian-meier/LoCobSS-dwd-transform)<sup class="print"></sup>
- [LoCobSS-co2-data](https://www.github.com/sebastian-meier/LoCobSS-co2-data)<sup class="print"></sup>

