<div class="print-hide">
<a href="../EN.html">Back to overview</a>
</div>

# Part 1

## 1.1 Introduction
The LoCobSS research project was funded as part of "[Ideenwettbewerb(s) für innovative analoge und digitale Partizipationsformate und -technologien](https://www.bmbf.de/foerderungen/bekanntmachung-2767.html)" (funding id: [16IP103](https://foerderportal.bund.de/foekat/jsp/SucheAction.do?actionMode=view&fkz=16IP103)).


In 2022, a large-scale participation procedure is to be carried out by the Federal Ministry of Education and Research in order to capture citizens’ perspectives on science and research in Germany. A [similar project](https://www.vraagvoordewetenschap.be/) was launched in Belgium back in 2018. The ideas competition (Ideenwettbewerb) is intended to generate innovative concepts to be implemented in the process in Germany in 2022. The ideas should focus on three phases:

- 1. activation and survey of citizen ideas
- 2. analysis, structuring and evaluation of the questions
- 3. answering and re-using the questions

The LoCobSS project focuses on digital aspects of the process, with a specific focus on **privacy compliant user experience customization, both for citizens and for the Ministry’s editor. To demonstrate the methods and concepts developed, a number of prototypes have been developed that are presented in the following chapters.

## 1.2 Executive summary

A number of methods have been developed and evaluated within the framework of LoCobSS with regard to added value for the participation process. The software components generated can serve as a prototype basis for final implementations (see [technical documentation](chapter04.md)). But even more importantly, the following findings are intended to guide and support invitations to tender and further developments on the participation process:

### 1.2.1 Privacy should be the top priority

As a recent example, the development of the corona app has shown that people are becoming more aware of the issue of privacy. As a public institution, the highest priority should be given to this issue.

The protection of privacy shall not prevent the collection of statistical data. A number of principles should be upheld:

- only data are collected that are actually *necessary* (data austerity and data avoidance).
- If data are not required in a person-related form, separate user data and statistical data (irreversibly).
- avoiding dark design patterns (e.g. opt-in instead of opt-out).

Further assistance can be found in [Chapter 2](chapter02.md).

### 1.2.2 Barrier-free and user-friendly

In order to involve as many people as possible in the process, barriers should be kept low:

- use simple language (Einfache Sprache)
- as few mandatory fields as possible
- as few input restrictions/obligations as possible
- No obligation to register
- supporting multilingualism
- comply with usage habits and requirements (e.g. mobile optimised)

Further guidance on this in the prototype for gathering questions in [Chapter 2](chapter02.md).

**Comment**: This project has focused on digital components of the participation process. To make the process as inclusive as possible, digital components should only be one part of the activation strategy and be combined with analog components and a broad outreach campaign.

### 1.2.3 Also focus on editors

While the focus is clearly on citizens, it should not be forgotten that a well-equipped team is also needed to manage the incoming content. The project in Belgium has generated over 10,000 questions. It can therefore be assumed that more than 50,000 questions can be expected in Germany. The incoming questions must be validated (relevance, insult words, etc.) and categorised. Locobss has evaluated the feasibility of automating these steps on the basis of the data from the Belgian procedure and draws the following conclusions:

- procedures for the automated detection of insults, hate speech, etc. have so far only partially detected these. This can only be applied in a supportive manner and must still be done manually.
- sentimental analyses to record attitudes to specific topics work only to a limited extent and should not be used for critical decisions.
- support for categorisation can be provided by means of content analysis procedures (e.g. word2vec similar procedures). To this end, we have developed a functioning prototype.

Overall, with regard to automated procedures, many have been optimised in English. This can be overcome in many areas by translating the content. However, in the case of language-specific problems such as insults, these approaches are reaching their limits.

Details of the prototype for categorisation in [Chapter 3](chapter03.md).

### 1.2.4 Customization: content recommendation

Using customization methods, user experience can be personalised, leading to a more intensive examination of the platform. In order to facilitate the exploration of content on the platform and promote serendipity, recommendation functions should be integrated in addition to a traditional search. A distinction is made here between content-based recommendation and collaborative recommendation. For the latter approach, users’ interactions must be recorded. For reasons of privacy, this should only be done with caution. As part of this project, we have developed a prototype for content-based recommendation based on the same principles of the editorial tool for categorisation.

Click here for more information on the recommendation in [Chapter 3](chapter03.md).

### 1.2.5 Customization: Science communication

Traditional science communication has traditionally been static, unidirectional and text-driven. As part of LoCobSS, we have developed new formats for communicating scientific insights that can be personalised individually using modern data journalism methods and data-driven storytelling techniques. The readers' everyday life is getting integrated into the communication strategy and, thereby, enables readers to make direct references between their life and the scientific facts. Interactive elements tie users’ attention. Exploratory elements invite users to take a closer look at the subject matter. Personalisation is also carried out with a view to safeguarding privacy.

A detailed explanation of the two prototypes is given in [Chapter 4](chapter04.md).


**Comment** If such formats were to be rolled out more frequently, it would make sense to standardise these concepts and provide corresponding frameworks so that new topics can be easily and sustainably be explored.
