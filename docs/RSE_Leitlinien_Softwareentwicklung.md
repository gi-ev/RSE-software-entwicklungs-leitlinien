# 						

# 

# 

#     FINAL

# 

 

				

#                             FINAL V1.0

# 

(Diese Seite gehört NICHT zum Text\!)  
GI- und de-RSE Muster-Leitlinie für die effiziente Entwicklung von Forschungssoftware

*Status: Version 1.0 ist abgenommen und wird aktuell veröffentlicht.*  
*Eine Hochglanzversion als pdf ist hier zu finden: [https://dl.gi.de/collections/e491722b-cc33-4155-bcc9-274da9073b65](https://dl.gi.de/collections/e491722b-cc33-4155-bcc9-274da9073b65).*

*Die offizielle Referenzierung:*

\[CEF+25\] A. Czerniak, A. Ehrenhofer, B. Fritzsch, M. Funk, F. Goth, R. Härhnle, C. Haupt, M. Konersmann, J. Linxweiler, F. Lörffler, A. Lürpges, S. Nielebock, B. Rumpe, I. Schieferdecker, T. Schlauch, R. Speck, A. Struck, J. P. Thiele, M. Tichy, I. Ulusoy:  
GI- und DE-RSE Muster-Leitlinie zur effizienten Entwicklung von Forschungssoftware.  
Gesellschaft für Informatik, Technischer Bericht, GI Leitlinien, DOI 10.18420/2025-gi\_de-rse, Gesellschaft für Informatik e.V., Jan. 2025\. 

*Inhaltlich ist diese Fassung identisch (und zB als Quelle gut nutzbar)*

*\[\[Vorab erläuternde Anmerkungen: Das aktuell vorliegende Dokument enthält einen Vorschlag für Leitlinien, die zur Softwareentwicklung in Forschungsprojekten dienen sollen. Diese beinhalten fachliche Themen, aber auch organisatorische Aspekte und sind zum Teil spezifisch in Bezug auf Unterstützung durch die eigene Universität, Hochschule oder Forschungseinrichtung auszugestalten bzw. Inhaltlich anzupassen.*

*Der Arbeitskreis Leitlinien (siehe [https://fg-rse.gi.de/fachgruppe/arbeitskreise](https://fg-rse.gi.de/fachgruppe/arbeitskreise) und [https://de-rse.org/de/working\_groups.html](https://de-rse.org/de/working_groups.html)) hat dieses Dokument erstellt, um Universitäten, Hochschulen und Forschungseinrichtungen Material für eigene Versionen von Leitlinien anzubieten. Den Mitgliedern des Arbeitskreises ist bewusst, dass eine allgemeingültige Leitlinie für alle Forschungskontexte und Softwareformen nicht erstellt werden kann. Deshalb wurden explizit Varianten und optionale Texte an verschiedenen Stellen in dieses Dokument eingefügt. Darüber hinaus besteht in der „Anwendung“ dieses Dokuments immer die Möglichkeit, Texte umzugestalten.* 

*Das Thema KI, insbesondere LLMs wie ChatGPT, wird natürlich zurzeit an vielen Stellen diskutiert. In den internen Diskussionen wurde festgelegt, dass das Thema noch weiterer Diskussionen bedarf und aufgrund der hohen Dynamik des Feldes aktuell stabile Leitlinien noch nicht wirklich gut möglich sind. Wir gehen davon aus, dass das Thema LLMs in und für die Softwareentwicklung, sowie das Thema KI in Softwareprodukten (und ja, das sind jeweils verschiedene Themen) eigenständig adressiert werden. Jedoch gelten für den Einbau von KI in Softwareprodukte sicherlich die gleichen Regeln wie für alle anderen Komponenten: Qualität, Korrektheit, Nachvollziehbarkeit, etc. Der neue Abschnitt 2.4. beinhaltet hierzu eine Abgrenzung.*

*Sollten Sie in der aktuellen Phase des Dokument-Reviews relevante zusätzliche Textstücke oder Verbesserungen finden, die von allgemeinem Nutzen sind, so bitten wir um entsprechende konstruktive Vorschläge (d. h. konkrete Texte, konkrete Verbesserungsvorschläge).*

*Kommentierbare und bearbeitete Quelle dieses Dokuments (bis auf weiteres):*  
	*[https://docs.google.com/document/d/1cSTJcX5NMxuYFwONtPLBiLhU5ogdbh-LEZgR3-vwiEI](https://docs.google.com/document/d/1cSTJcX5NMxuYFwONtPLBiLhU5ogdbh-LEZgR3-vwiEI)*

*Letzte Historie/Aktivitäten an diesem Dokument:*

* *Gesamtfassung V0.8 wurde erstellt am 11\. Mai 2024*  
* *Gesamtfassung V0.9.1 wurde erstellt am 25\. Mai 2024*  
* *Fassung 0.9.3 ist aktuell weitgehend abgeschlossen*   
* *Fassung 0.9.4 ist abgeschlossen und wartet auf ein Votum der Gremien*  
* *de-RSE hat darüber abgestimmt und das Dokument genehmigt.*  
* *der GI-Gremienlauf ist mit Version 0.9.9 unterwegs*  
* *verabschiedet: V1.0 ist rausgegeben*

*Nächste Schritte / Plan:*

* *Verabschiedung und Veröffentlichung sind erfolgt*

*Ende Anmerkungen\]\]*  
(Alles nach hier gehört zum Text\!)

[Präambel: Zweck dieser Muster-Leitlinie	6](#präambel:-zweck-dieser-muster-leitlinie)

[Nutzung der Muster-Leitlinie & Lizenz	7](#nutzung-der-muster-leitlinie-&-lizenz)

[Mitwirkende und Dank für die Mitarbeit	9](#mitwirkende-und-dank-für-die-mitarbeit)

[Wichtigste genutzte Quellen	9](#wichtigste-genutzte-quellen)

[1 Executive Summary (für Entscheidende)	10](#1-executive-summary-\(für-entscheidende\))

[1.1. Lesehinweise	13](#1.1.-lesehinweise)

[2 Einleitung	15](#2-einleitung)

[2.1. Charakteristika von Software, speziell Forschungssoftware	16](#2.1.-charakteristika-von-software,-speziell-forschungssoftware)

[2.2. Charakteristika von Research Software Engineering	17](#2.2.-charakteristika-von-research-software-engineering)

[2.3. Aufgaben der Leitlinie	18](#2.3.-aufgaben-der-leitlinie)

[2.4. Abgrenzung, Nicht-Aufgabe der Leitlinie	19](#2.4.-abgrenzung,-nicht-aufgabe-der-leitlinie)

[2.5. Damit abgestimmte Rahmen Guidelines for Safeguarding, Good Research Practice, Code of Conduct-Bedingungen	20](#2.5.-damit-abgestimmte-rahmen-guidelines-for-safeguarding,-good-research-practice,-code-of-conduct-bedingungen)

[2.6. Fazit	21](#2.6.-fazit)

[3 Fachliche Leitlinien der Softwareentwicklung	22](#3-fachliche-leitlinien-der-softwareentwicklung)

[3.1. Einleitung	22](#heading=)

[3.1.1. Forschungssoftware: Demonstrator, Produkt, Infrastruktur	23](#forschungssoftware:-demonstrator,-produkt,-infrastruktur)

[3.2. Kategorisierung von Forschungssoftware	24](#3.2.-kategorisierung-von-forschungssoftware)

[3.2.1. Art der Software bzw. Softwarekomponente (Dimension Art)	24](#3.2.1.-art-der-software-bzw.-softwarekomponente-\(dimension-art\))

[3.2.2. Nutzungsgrad der Software bzw. Softwarekomponente](#3.2.2.-nutzungsgrad-der-software-bzw.-softwarekomponente-\(dimension-ng\))   
[(Dimension Ng)	25](#3.2.2.-nutzungsgrad-der-software-bzw.-softwarekomponente-\(dimension-ng\))

[3.2.3. Einordnung in die Technology Readiness Levels (TRL) entsprechend der EU	27](#3.2.3.-einordnung-in-die-technology-readiness-levels-\(trl\)-entsprechend-der-eu)

[3.2.4. Anwendungsklassen	29](#3.2.4.-anwendungsklassen)

[3.2.5. Status der Software	31](#3.2.5.-status-der-software)

[3.2.6. Weitere Einflüsse	32](#3.2.6.-weitere-einflüsse)

[3.3. Minimalanforderungen an Kernkompetenzen, Entwicklungsprozesse und Projektplanung in der Softwareentwicklung	33](#3.3.-minimalanforderungen-an-kernkompetenzen,-entwicklungsprozesse-und-projektplanung-in-der-softwareentwicklung)

[3.3.1. Minimalanforderungen an den Technologie-Reifegrad auf Basis des Nutzungsgrads (Ng) und der Softwareart (Art)	34](#3.3.1.-minimalanforderungen-an-den-technologie-reifegrad-auf-basis-des-nutzungsgrads-\(ng\)-und-der-softwareart-\(art\))

[3.3.2. Minimalanforderungen an Handlungsfelder und notwendige Kernkompetenzen in der Softwareentwicklung auf Basis des Technologie-Reifegrads	35](#3.3.2.-minimalanforderungen-an-handlungsfelder-und-notwendige-kernkompetenzen-in-der-softwareentwicklung-auf-basis-des-technologie-reifegrads)

[3.4. Methodische Grundlagen der Softwareentwicklung	37](#heading=)

[3.4.1. Softwareentwicklungsprozesse	37](#heading=)

[3.4.2. Qualitätsmanagement (Testen, Validierung, etc.)	38](#3.4.2.-qualitätsmanagement-\(testen,-validierung,-etc.\))

[3.4.3. Anforderungen verstehen	39](#heading=)

[3.4.4. Softwarearchitektur	39](#heading=)

[3.4.5. Softwaremodellierung	40](#heading=)

[3.4.6. Versionierung	41](#3.4.6.-versionierung)

[3.4.7. Testkonzept und \-Automatisierung	41](#3.4.7.-testkonzept-und--automatisierung)

[3.4.8. Management der Software-bezogenen Daten und Datengrundlage	42](#3.4.8.-management-der-software-bezogenen-daten-und-datengrundlage)

[3.4.9. Best Practices, Design Pattern, Issue-Tracking, Coding Guidelines	43](#heading=)

[3.5. Technische Grundlagen	45](#heading=)

[3.5.1. Git Versionsverwaltungssystem	45](#3.5.1.-git-versionsverwaltungssystem)

[3.5.2. Continuous Integration / Continuous Delivery	46](#3.5.2.-continuous-integration-/-continuous-delivery)

[3.5.3. Test-Frameworks	47](#3.5.3.-test-frameworks)

[3.5.4. Verbreitung / Dissemination	47](#heading=)

[3.5.5. Software Discovery	48](#3.5.5.-software-discovery)

[4 Lizenz-Vergabe und \-Nutzung (Juristische Absicherung)	50](#4-lizenz-vergabe-und--nutzung-\(juristische-absicherung\))

[4.1. Wissenschaftliche Verwertung und Lizenzwahl \-- Allgemeines	51](#4.1.-wissenschaftliche-verwertung-und-lizenzwahl----allgemeines)

[4.2. Anmerkungen zur wirtschaftlichen Verwertung	53](#4.2.-anmerkungen-zur-wirtschaftlichen-verwertung)

[4.3 Lizenz-Arten	54](#4.3-lizenz-arten)

[4.3.1 Open Source Lizenzen	54](#4.3.1-open-source-lizenzen)

[4.3.2 Permissive Open Source Lizenzen	55](#4.3.2-permissive-open-source-lizenzen)

[4.3.3  Copyleft Open Source Lizenzen (Best Practice Beispiele)	56](#4.3.3-copyleft-open-source-lizenzen-\(best-practice-beispiele\))

[4.3.4  Proprietäre Lizenzen	57](#4.3.4-proprietäre-lizenzen)

[4.4. Beratungsangebote und Vorgehensweise zur Auswahl	58](#4.4.-beratungsangebote-und-vorgehensweise-zur-auswahl)

[4.5.  Nutzung von Software Dritter	59](#4.5.-nutzung-von-software-dritter)

[4.5.1. Rechte und Pflichten durch Lizenzen	59](#4.5.1.-rechte-und-pflichten-durch-lizenzen)

[4.5.2. Kompatibilität von Lizenzen	60](#4.5.2.-kompatibilität-von-lizenzen)

[5\. Unterstützungsleistungen durch \[\[die Universität | Hochschule | das Forschungszentrum | Einrichtung\]\]	60](#5.-unterstützungsleistungen-durch-[[die-universität-|-hochschule-|-das-forschungszentrum-|-einrichtung]])

[5.1. Personelle Unterstützung bei der Erstellung und Erweiterung von Forschungssoftware	62](#5.1.-personelle-unterstützung-bei-der-erstellung-und-erweiterung-von-forschungssoftware)

[5.2. Unterstützungsleistungen bei der langfristigen Pflege von Software	64](#5.2.-unterstützungsleistungen-bei-der-langfristigen-pflege-von-software)

[5.3. Unterstützungsleistungen in der Weiterbildung	65](#5.3.-unterstützungsleistungen-in-der-weiterbildung)

[5.4. Würdigung der Research Software Engineers	65](#5.4.-würdigung-der-research-software-engineers)

[5.5. Unterstützungsleistungen bei Lizenzen	67](#5.5.-unterstützungsleistungen-bei-lizenzen)

[5.6. Unterstützungsleistungen durch technische Services	67](#5.6.-unterstützungsleistungen-durch-technische-services)

[5.7. Finanzierung der Unterstützungsleistungen bei der Entwicklung und Pflege von Software	68](#5.7.-finanzierung-der-unterstützungsleistungen-bei-der-entwicklung-und-pflege-von-software)

[5.7.1. Übernahme auf RSE-Zentrums-Kosten (“Universitäts-Software”)	69](#5.7.1.-übernahme-auf-rse-zentrums-kosten-\(“universitäts-software”\))

[5.7.2 Übernahme auf Kosten der Forschungseinheit (“Instituts-Software”)	70](#5.7.2-übernahme-auf-kosten-der-forschungseinheit-\(“instituts-software”\))

[5.7.3 Ausgestaltung der Unterstützung	70](#5.7.3-ausgestaltung-der-unterstützung)

[5.8. Weitere Unterstützungsleistungen	70](#5.8.-weitere-unterstützungsleistungen)

[Referenzen	72](#referenzen)

[Anhang A: Kategorisierungsmöglichkeiten	76](#anhang-a:-kategorisierungsmöglichkeiten)

[Anhang B: Checkliste für die Weitergabe von Software	78](#anhang-b:-checkliste-für-die-weitergabe-von-software)

[Anhang C: Grundlagen und Mitwirkende	82](#anhang-c:-grundlagen-und-mitwirkende)

# Präambel: Zweck dieser Muster-Leitlinie {#präambel:-zweck-dieser-muster-leitlinie}

Diese Muster-Leitlinie bietet einen Rahmen für die Entwicklung, Verwaltung und Weitergabe von Software an der jeweils nutzenden Universität, Hochschule oder dem Forschungszentrum. Sie eignet sich auch für standortübergreifende Verbundforschungsvorhaben, insbesondere wenn die Projektbeteiligten der verschiedenen Universitäten, Hochschulen und Forschungszentren kompatible Fassungen nutzen. 

Der Fokus der Muster-Leitlinie liegt auf dem Schaffen eines softwaretechnischen Rahmens für die Entwicklung, ohne zu sehr in fachspezifische Anforderungen einzelner Forschungsgebiete zu gehen. Sie ist vollständig kompatibel mit den Richtlinien der DFG \[DFG22\] und bietet Präzisierungsoptionen insbesondere die DFG-Handreichung zum Umgang mit Forschungssoftware \[DFG24\]. Es ist daher normalerweise sinnvoll, diese Aspekte in spezifischen Leitlinien nach den spezifischen Anforderungen der Einrichtung oder der Fachdomäne genauer auszuformulieren. Ein Beispiel hierfür sind erhöhte Anforderungen an Medizinprodukte. Andere, auch fachübergreifende Themen, die weniger dem softwaretechnischen Rahmen zuzuordnen sind, stehen hier nicht im Fokus und sollten daher vor allem in Abhängigkeit der Bedarfe der jeweiligen Institution zusätzlich betrachtet werden.

**Research Software Engineering** (kurz: RSE) ist die Verwendung von Software Engineering (SE)-Praktiken für Forschungssoftware, d. h. Software, die für wissenschaftliche Forschungsprojekte erstellt wurde und hauptsächlich in diesen verwendet wird. \[Wik24b\] 

RSE ist dabei nicht einfach eine Teilmenge der klassischen Softwaretechnik, sondern beinhaltet als Schnittstellendisziplin Elemente der Informatik (insbesondere Programmierung und Softwaretechnik), der verschiedenen Fachwissenschaften und der Offenen Wissenschaft (Open Science) \[Lam24\]. 

Konsequenterweise bildet sich aktuell in Deutschland der Begriff „Research Software Engineers“ als eigenständiges Berufsprofil heraus \[GAB+24\], welches sich als Mischung aus der eigentlichen Forschungsdomäne (MINT, Geologie, Robotik, Medizintechnik, Soziologie, etc.) und von Software Engineering-Methoden zusammensetzt. RSE ist nicht identisch, aber verwandt zu High-Performance Computing (HPC), Computational Science and Engineering (CSE), Artificial Intelligence oder Data Science, weil es sowohl eigenständige Ziele als auch Methoden zur Zielerreichung hat.

Aufgrund der gestiegenen Relevanz und Komplexität der Forschungssoftware in einer Vielzahl an Forschungsvorhaben, sowie der häufig notwendigen Zuverlässigkeit und Langlebigkeit hat sich gezeigt, dass die effiziente und qualitativ hochwertige Erstellung von Software auch für Forschungssoftware eine Reihe von **organisatorischen, methodischen und juristischen Maßnahmen** erfordert.

Mit dem nachfolgenden Dokument wird ein Vorschlag für die Ausprägung eigener Leitlinien innerhalb von Universitäten, Hochschulen und Forschungseinrichtungen gemacht. Dieser versucht einerseits konkrete Hilfestellungen für die Definition eigener Leitlinien und andererseits den unterschiedlichen Kulturen in einzelnen Fächern und Forschungseinrichtungen durch explizite Variabilität Freiraum zur weiteren Präzisierung zu geben. Dennoch ist dieses Dokument  für Leitlinien relativ detailliert und ausführlich, weil es im Bereich RSE viel zu klären und zu verstehen gibt, sowie zahlreiche auswählbare Alternativen existieren. Die tatsächlich “selektierte” Leitlinie wird damit deutlich weniger umfangreich.

Diese Muster-Leitlinie sollte daher genutzt werden, um daraus ein eigenständiges Dokument zu selektieren und dieses in der eigenen Universität, Hochschule oder Forschungseinrichtung idealerweise zur Leitlinie zu erklären. Sie konzentriert sich ausschließlich auf den Softwareentwicklungsteil und vernachlässigt den Forschungsteil in “RSE”, der ggf. eigene Leitlinien hat, die aber wegen der hochgradigen Individualität nicht Teil dieses Dokuments sein können. 

Daraus ergeben sich sowohl Konsequenzen für die Leitungen zur organisatorischen Unterstützung, als auch für die operativ in der Softwareentwicklung tätigen Personen. Diese Leitlinien wurden auf der Basis des bisher destillierten Wissens (Stand 2024\) über die Entwicklung von Software im Allgemeinen (Software Engineering) und Forschungssoftware im Speziellen (Research Software Engineering) erstellt. Es ist geplant, diese Leitlinien regelmäßig weiterzuentwickeln und neue Erkenntnisse einfließen zu lassen.

Diese variantenreiche Muster-Leitlinie zur Entwicklung von Forschungssoftware wurde seitens des gleichnamigen Arbeitskreises der gemeinsamen Fachgruppe RSE der Gesellschaft für Informatik e. V. (GI) und der Gesellschaft für Forschungssoftware e. V. (de-RSE) erarbeitet. 

Die Muster-Leitlinie des de-RSE und der GI wird explizit unterstützt durch den Fachausschuss Medizinische Informatik der GMDS – Deutsche Gesellschaft für Medizinische Informatik, Biometrie und Epidemiologie e.V. und die Arbeitsgruppe Medizinische Software und Medizinprodukterecht (MSM) der TMF – Technologie- und Methodenplattform für die vernetzte medizinische Forschung e.V..

### Nutzung der Muster-Leitlinie & Lizenz {#nutzung-der-muster-leitlinie-&-lizenz}

Die Personen, die zu diesem Dokument beigetragen haben, sind unter Mitwirkende aufgezählt. Soweit gesetzlich möglich, verzichten die Personen, die diese Guideline mit CC0 1.0 DEED assoziiert haben, auf alle Nutzungs- und Verwertungsrechte an dieser Guideline. Die Lizenz ist unter [https://creativecommons.org/publicdomain/zero/1.0/](https://creativecommons.org/publicdomain/zero/1.0/) zu finden.

Zwar besteht keine Zitationspflicht, jedoch würden sich die Autor:innen wünschen, auf diesem Muster-Dokument basierte Leitlinien mit dem Hinweis zu versehen: “Erstellt auf Basis der Muster-Leitlinien der GI-Fachgruppe RSE und de-RSE, Version 1.0”.

Alle Formulierungen können daher frei übernommen werden. Lücken in den Formulierungen sind mit \[\[...\]\] markiert. Stehen Alternativen zur Auswahl, so sind diese markiert mittels \[\[Text 1 | Text 2\]\], zum Beispiel in \[\[ Universität | Hochschule | Forschungszentrum \]\]. Komplette, alternative Passagen sind markiert als 

\[\[Variante A1\]\]  
	Text Passage 1  
\[\[Variante A2\]\]  
	Text Passage 2  
\[\[Variante A Ende\]\]

Optionale Texte werden analog markiert:

\[\[Option B\]\]  
	Optional nutzbarer Text   
\[\[Option B Ende\]\]

Darüber hinaus sind gegebenenfalls \[\[Regieanweisungen\]\] in den Text eingestreut:

\[\[Anmerkung für Leitlinienerstellende/Hochschullleitungen: Die gesamte Präambel (also dieser Abschnitt 0\) ist nicht Teil der eigentlichen Leitlinie und daher zu löschen \]\]

Eine Leitlinie zur Forschungssoftwareentwicklung besteht sinnvollerweise aus den folgenden Abschnitten, ggf. ergänzt durch weitere Abschnitte, die auch verwandte Themen integrieren. Aus diesem Grund ist diese Muster-Leitlinie auch genauso organisiert. Zweck und Inhalt der Abschnitte ist jeweils:

1. Executive Summary ist **vor allem für Entscheidende und Führungspersonal**.  
2. Einleitung beschreibt Software-Charakteristika, Research Software Engineering und skizziert die Aufgaben und Anwendungsbereiche der Leitlinie.  
3. Methodische und fachliche Grundsätze zur Forschungssoftwareentwicklung beschreiben Definition von verschiedenen Klassifikationen (u.a., TRL-Level, Anwendungsklassen), dafür jeweils notwendige Mindeststandards und Maßnahmen methodischer und organisatorischer Art sowie die Umsetzung der Software-Weitergabe.  
4. Rechtliche Fragen behandeln die Nutzung und Definition von Lizenzen und deren Konsequenzen.  
5. Organisatorische Unterstützungsleistungen durch \[\[die Universität | die Hochschule | das Forschungszentrum\]\] beinhalten unter anderem methodische Unterstützung durch Expert:innen, personelle Unterstützung durch Entwickler:innen und technische Unterstützung durch Services, sowie Weiterbildungsmaßnahmen für relevantes RSE-Wissen. Fokus liegt dabei sowohl auf der Befähigung von Forschenden mit dem Ziel der Unterstützung bei der Entwicklung, als auch bei der Pflege der Software als Infrastruktur.  
6. Anhang 

Darüber hinaus gibt es natürlich eine Reihe von fachspezifischen Ergänzungen. Falls diese die gesamte Forschungseinheit betreffen, so bietet sich ein Einbau oder ein entsprechender Verweis innerhalb dieser Leitlinien natürlich an. Verweise auf fachspezifische Leitlinien zur Behandlung von Verlässlichkeit (Safety), Cybersecurity, etc. sind da gegebenenfalls relevant. Gibt es mehrere verschiedene fachspezifische Ergänzungen (Hinweise auf Verfahren, Normen, etc.) ist es wahrscheinlich sinnvoller, diese in eigenen, ergänzenden Richtlinien zu dokumentieren. 

### Mitwirkende und Dank für die Mitarbeit {#mitwirkende-und-dank-für-die-mitarbeit}

Siehe dazu Anhang C, der gern Teil einer finalen Leitlinie sein kann.

Wir freuen uns auch über eine Rückmeldung, an welcher Universität, Hochschule, Forschungszentrum der Text in welcher Form zum Einsatz kommt, welche Erfahrungen man macht, was verbessert werden kann.

### Wichtigste genutzte Quellen {#wichtigste-genutzte-quellen}

In die Erstellung dieses Leitlinien-Vorschlags sind im Besonderen die folgenden Dokumente eingeflossen:

* Umgang mit Forschungssoftware im Förderhandeln der DFG. \[DFG24\]	  
* Guidelines for the development and distribution of software at Forschungszentrum Jülich. \[BOSS22\]   
* Muster-Richtlinie Nachhaltige Forschungssoftware an den Helmholtz-Zentren. \[BBB19\]  
* Research Software Engineering \- Forschungssoftware effizient erstellen und dauerhaft erhalten. \[GLHR24\]  
* Software-Engineering-Empfehlungen des DLR (1.0.0) \[SMH18\]   
* Nutzung von Open-Source-Software im DLR. 2022\.  \[DLR22\]  
* Research Software Alliance (ReSA) Web Collection of Guidelines. \[RESA24\] 

\[\[Anmerkung für Leitlinienerstellende/Hochschullleitungen: Ende der Präambel: bis hier kann gelöscht werden, denn die Präambel ist nicht Teil der eigentlichen Leitlinie. Aus diesem Grund werden relevante Teile der Präambel in der eigentlichen Einleitung wiederholt.\]\]

# 1 Executive Summary (für Entscheidende) {#1-executive-summary-(für-entscheidende)}

\[\[Anmerkung für Leitlinienerstellende/Hochschullleitungen: Das Executive Summary soll eine kurze Zusammenfassung des Inhalts darstellen und vor allem Entscheidenden einen Überblick geben. Das Dokument ist jedoch variantenreich, was gegebenenfalls die Anpassung der Zusammenfassung erfordert\]\]

\[\[Anmerkung für Leitlinienerstellende/Hochschullleitungen: Kapitel 2\]\]

→→ Für Führungskräfte und Entscheidende (= Instituts-, Lehrstuhl-Leiter:innen) besonders relevante Teile sind im Dokument grün markiert. ←← 

Software ist sowohl ein zentraler Bestandteil, ein Werkzeug als auch ein wichtiges Ergebnis der modernen akademischen Forschung. Sie sollte langlebig und nachvollziehbar nutzbar sein und besitzt aufgrund kontinuierlichen Ausbaus mittlerweile oft eine hohe Komplexität. Auch deshalb hat die DFG im Oktober 2024 die Handreichung zum Umgang mit Forschungssoftware \[DFG24\] herausgegeben, zu der diese Richtlinien als vollständig kompatible organisatorische und fachliche Präzisierung zu verstehen sind.

**Forschungssoftware** umfasst alle Formen von Beschreibungen, Dokumentation, ausführbaren Modellen, Konfigurationsdateien, darin eingebettete Daten/-sätze, Skripte und daraus generierte ausführbare Programme, die im Rahmen der Forschung oder für Forschungszwecke entwickelt und genutzt werden. \[GKL+21\]

**Research Software Engineering** (kurz: RSE) ist die Verwendung von Software Engineering (SE)-Praktiken für Forschungssoftware, d. h. Software, die für wissenschaftliche Forschungsprojekte erstellt wurde und hauptsächlich in diesen verwendet wird. \[Wik24b\] 

RSE ist dabei nicht einfach eine Teilmenge der klassischen Softwaretechnik, sondern beinhaltet als Schnittstellendisziplin Elemente der Informatik (insbesondere Programmierung und Softwaretechnik), der verschiedenen Fachwissenschaften und der Offenen Wissenschaft (Open Science) \[Lam24\]. 

RSE adressiert daher die organisatorische, fachliche und methodische Einbettung effizienter und qualitativ hochwertiger Softwareentwicklung in den Forschungsprozess. Das bedeutet, dass alle jeweils relevanten Entwicklungsaktivitäten unter der Berücksichtigung der wissenschaftlichen-technischen Zielsetzung und jeweiliger Richtlinien und Normen so gewählt werden, dass die Qualität des Ergebnisses und Effizienz der Entwicklung (also Arbeitzeit pro Output)  adäquat adressiert werden. 

Dies beinhaltet die professionelle **Qualifikation der Entwickelnden**, um gegebenenfalls **Projektplanung, fachliche Anforderungen, fachliche und informationstechnische/mathematische Korrektheit, Architektur, Entwurf, Modellierung, Konstruktion, Programmierung, Qualitätssicherung, Dokumentation, Optimierung, Evolution, Wartung, Versionierung, Bereitstellung in Varianten und Nachnutzung** ökonomisch und ökologisch effizient zu managen und damit zu nachhaltiger Forschungssoftware beizutragen. Hervorzuheben sind Aktivitäten wie:

* Projektmanagement,   
* Architektur und Entwurf, also die Strukturierung der Funktionalität in modulare, wiederverwendbare und parallel entwickelbare Einheiten, sowie die kluge Einbeziehung bereits entwickelter (möglicherweise externer) Softwarekomponenten,  
* das Erfassen und Festlegen der funktionalen und technischen Anforderungen von allen Stakeholdern (Entscheidende, Fördergeber, Nutzende und Entwickler:innen) an die Software,   
* die Auswahl der Nutzungsbestimmungen und Lizenzen und die Absicherung der Kompatibilität der Lizenzen eigener und möglicherweise externer Softwarekomponenten sowie  
* Qualitätssicherung, also Verifikation und Validierung (u.a. Korrektheit, Nutzbarkeit, Wartbarkeit) der Software und damit der wissenschaftlichen Erkenntnisse.

RSE hat ein **eigenständiges Berufsprofil** und eine eigene Fachcommunity mit den notwendigen üblichen Austauschformaten wie Konferenzen und Workshops. 

Diese Leitlinie \[\[der Universität | Hochschule | des Forschungszentrums\]\] definiert einen praktischen und handlungssicheren Rahmen, in dem sich Mitarbeitende bei der Entwicklung von Software bewegen können. Sie trägt unterstützend dazu bei, qualitativ hochwertige Forschungssoftware effizient zu entwickeln, zu verwalten und damit wissenschaftliche Wirkung zu erzielen. Die Leitlinie unterstreicht die Wertschätzung für qualitativ hochwertige Software in einer sich digitalisierenden Wissenschaft und unterstützt eine Professionalisierung der Softwareentwicklung im Forschungskontext. Sie fördert die langlebige Nutzbarkeit von Forschungssoftware, deren Veröffentlichung und Weiterverwendbarkeit und damit eine gute wissenschaftliche Praxis durch Verifizierbarkeit und Reproduzierbarkeit von Forschungsergebnissen.

Die Leitlinie beinhaltet **allgemeine Richtlinien** sowie auch **konkrete organisatorische Maßnahmen** zur Entwicklung, Weiterentwicklung und Pflege der Software, die juristische **Absicherung der Lizenzierung** für die Weitergabe der Software als Forschungsergebnisse an die Öffentlichkeit bzw. die Fachcommunity und Unterstützungsleistungen der \[\[universitären Infrastruktur | Forschungseinrichtung\]\]. Gegebenenfalls sind zusätzliche fachspezifische Richtlinien und technische Normen zu beachten, die bei kritischer Software wie z.B. in der Medizintechnik eine besondere Rolle spielen.

\[\[Anmerkung für Leitlinienerstellende/Hochschullleitungen: Quelle: Kapitel 3 (allgemein gehalten weil ja Variantenreichtum, also viele Alternativen existieren\]\]

**Kapitel 3:** Die Leitlinien enthalten eine **Kategorisierung der Software** nach Nutzungsgrad, Art der Software (Demonstrator, Produkt, Infrastruktur) und Technology-Readiness (TRL gemäß EU-Klassifikation), weil diese auch die notwendigen Entwicklungsaktivitäten bestimmen. Es ist sinnvoll, die Ziele von Forschungssoftware und die langfristige Strategie frühzeitig festzulegen, um auf dieser Basis unterschiedliche Entwicklungsmethoden auszuwählen und relevante Kompetenzen  der Entwickler:innen sicherzustellen. Die Leitlinien definieren dazu **Minimalanforderungen an Kompetenzen, Entwicklungsprozesse und Projektplanung** in der Softwareentwicklung und legen so auch das Qualifikationsprofil der Beteiligten und die Verfügbarkeit technischer Services, wie etwa Versionskontrolle oder Fehlermanagementsysteme fest. Eine Ausdifferenzierung der Kompetenzen bei mehreren Projektbeteiligten ist dabei sinnvoll.

Die Leitlinien beinhalten damit eine erste Handreichung für Führungskräfte(\!) und Entwickler:innen, um ihre Software einzuordnen und daraus abzuleiten, was für die Entwicklung an Grundwissen und Fähigkeiten vorhanden sein muss und welche Techniken / Werkzeuge eingesetzt werden sollen.

\[\[Anmerkung für Leitlinienerstellende/Hochschullleitungen: Quelle: Kapitel 4 (Lizenzen)\]\]

**Kapitel 4:** Um die effiziente Entwicklung von Forschungssoftware mit hohen Qualitätsstandards zu unterstützen, gestaltet \[\[die Universität | die Hochschule | das Forschungszentrum\]\] den regulatorischen Rahmen aus und stellt \[\[Beratungs-, Unterstützungs- und Weiterbildungsangebote\]\] bereit. 

Für die Auswahl der Lizenzen, unter denen eigene Forschungssoftware zur Verfügung gestellt werden kann, werden die wichtigsten vorgestellt, die einen Großteil auftretender Fälle abdecken sollten und von \[\[der Universität | der Hochschule | dem Forschungszentrum\]\] als verwendbar angesehen werden.  Dazu gehören permissivere und restriktivere Open Source Lizenzen.

\[\[Anmerkung für Leitlinienerstellende/Hochschullleitungen: Quelle: Kapitel 5 (Unterstützungsangebote)\]\]

*\[\[Anmerkung für Leitlinienersteller: Ein “RSE-Zentrum” ist nach informellen Aussagen (Stand Mai 2024\) ein auch von der DFG angeregtesKonstrukt, das die Relevanz des Themas RSE adäquat adressiert und in Kombination mit Forschungsanträgen förderfähig werden soll. Details siehe Kapitel 5.\]\]  \[\[Ende Anmerkungen\]\] \[\[Variante Zentrum\]\]*

**Kapitel 5:** Weil viele Softwareentwickler:innen ihre Heimat als Wissenschaftler:innen in der Fachdomäne sehen, ist Softwareentwicklung ein zusätzliches Qualifikationsmerkmal, das Personen-individuell unterschiedlich ausgeprägt ist. Deshalb ist die Bereitstellung und Nutzung der methodischen Hilfsangebote sowie der Werkzeuge und technischen Services \[\[der Universität | der Hochschule | des Forschungszentrums\]\] sehr wichtig, um die gesteckten Ziele der Softwareentwicklung zu erreichen. Darauf wird in der DFG-Handreichung \[DFG24\] explizit hingewiesen und dafür auch die Förderfähigkeit geklärt.

\[\[Die Universität | Die Hochschule | Das Forschungszentrum \]\] bietet deshalb kontinuierlich verbesserte und ausgebaute Angebote, die die Entwicklung unterstützen. Dazu gehören 

* Konzeptionierung, Entwicklung, Weiterentwicklung und Wartung von Forschungssoftware durch professionelle Research Software Engineers in Zusammenarbeit mit Forschenden, also den Mitentwickelnden und gleichzeitig Nutzer:innen von Forschungssoftware (im Rahmen personeller Verfügbarkeit),  
* die technische Aufwertung vorhandener Forschungssoftware durch Verbesserungsmaßnahmen (Architektur, Security, Safety, User Experience, etc.),  
* organisatorische, fachliche und methodische Beratung für die Softwareentwicklung durch einen Expert:innen-Pool.  
* Weiterbildung der in Forschungssoftware involvierten Personen und Teams,  
* Beratung im Umgang mit Lizenzen (siehe Kapitel 4),  
* Bereitstellung, Betrieb und Wartung technischer Ressourcen,  
* Veröffentlichung von Software und  
* weitere Aspekte, bspw. Cybersicherheit, Ethik und Datenschutzfragen.

\[\[Die Universität | Hochschule | Das Forschungszentrum\]\] hat für diese Zwecke \[\[das RSE-Zentrum | dezentrale RSE-Einheiten | RSE-Ansprechpartner\]\]  eingerichtet, \[\[das | die\]\] Forschende aller Fachrichtungen in den oben genannten Punkten durch Beratung und Entwicklungsleistungen unterstützt und förderfähig bei Forschungsanträgen mitfinanziert werden kann. Die \[\[Liste:Bibliothek, das Rechenzentrum, die Rechtsberatung, das Center für Doctoral Studies, die Forschungsdatenmanagementberatung und weitere forschungsnahe Dienstleistungen\]\] werden bei der Umsetzung der Leitlinie eingebunden. Die Finanzierung der RSE-Expert:innen im Bereich der Softwareentwicklung kann (a) durch Übernahme auf RSE-Zentrums-Kosten (“Universitäts-Software”) oder durch (b) Übernahme auf Kosten der Forschungseinheit (“Instituts-Software”) erfolgen und ist abhängig von der Verfügbarkeit. Details regelt ein Vergabeverfahren. 

*\[\[Variante Zentrum (siehe auch Kapitel 5)\]\]*

Das RSE-Zentrum koordiniert die Aus- und Weiterbildung von Research Software Engineers sowie die aktive Mithilfe bei der Konzeptionierung, Entwicklung, Weiterentwicklung und Verwaltung von Forschungssoftware, der Etablierung neuer Werkzeuge und allen mit der Entwicklung zusammenhängenden Aktivitäten. Das RSE-Zentrum bietet insbesondere fachliche Unterstützung für dezentrale Forschungseinheiten, die sich eine eigene RSE-Stelle nicht leisten können oder wollen. Die Expert:innen des RSE-Zentrums sind entsprechend für einzelne Zeiträume buchbar und erarbeiten kollaborativ mit den Mitgliedern der Forschungseinheit zielgerichtet gute Software.

*\[\[Ende Variante Zentrum\]\]*

Wichtige technische Services für kollaborative Entwicklung, Dokumentation, Projektmanagement, Ticketverwaltung, Datenverwaltung, Kommunikation, etc. stellt \[\[die Universität | Hochschule | Das Forschungszentrum\]\] via ihren IT-Services zur Verfügung.

## **1.1. Lesehinweise** {#1.1.-lesehinweise}

Diese Leitlinie richtet sich 

* (1) an alle **Entwickler:innen** von Forschungssoftware und   
* (2) deren **Führungskräfte** bzw. **Entscheidende**, die \[\[an der Forschungseinrichtung\]\] an der Entwicklung, Verwaltung und Weitergabe von Software direkt oder indirekt beteiligt sind sowie   
* (3) an die **Leitung** \[\[der Forschungseinrichtung\]\].

Für Führungskräfte bzw. Entscheidende ist insbesondere die Executive Summary gedacht, die einen Überblick über die relevanten Themen gibt und auch einen Einblick, welche Kompetenzen in den jeweiligen Forschungsprojekten vorhanden sein bzw. ausgebildet werden sollten.

Entwickler:innen erhalten einen Überblick über mögliche verwendbare Themen der Softwareentwicklung, zur Verfügung gestellte Werkzeuge und Hilfsangebote im Sinne von methodischer und Ausbildungsunterstützung sowie Hilfe bei konkreten Fragestellungen. 

# 2 Einleitung {#2-einleitung}

Software ist ein zentraler Bestandteil der Forschung geworden und ist oftmals essentiell für die Durchführbarkeit von Forschungsprojekten. Hohe Datenmengen und durch immer leistungsfähigere Hardware ermöglichte Simulationen stellen Anforderungen an speziell für Forschungszwecke entwickelte Software, die wiederum die Durchführung exzellenter Forschung ermöglicht. Solche Forschungssoftware \[GKL+21\] beinhaltet alle Formen von Quellcodes, Beschreibungen, Dokumentationen, ausführbaren Modellen, Konfigurationsdateien, darin eingebetteten Daten/-sätzen, Skripten und daraus generierte ausführbare Programme, die im Rahmen der Forschung oder für Forschungszwecke \[BHK22\] entwickelt werden.  Auch deshalb hat die DFG im Oktober 2024 die Handreichung zum Umgang mit Forschungssoftware \[DFG24\] herausgegeben, zu der diese Richtlinien als vollständig kompatible organisatorische und fachliche Präzisierung zu verstehen sind.

Research Software Engineering (RSE) adressiert u.a. die Einbettung von Maßnahmen rund um die Forschungssoftware in die Forschungsarbeit. Die *Einbettung* umfasst dabei organisatorische, juristische und insbesondere fachliche und methodische Elemente. Die *Maßnahmen* beziehen sich auf qualitativ hochwertige und effiziente Softwareentwicklung sowie die Qualifikation der Forschenden im Bereich der Softwareentwicklung. Ziel ist es, die Aktivitäten zur Entwicklung der Forschungssoftware ökonomisch effizient zu managen und jene nachhaltig zu erstellen und zu nutzen. Dazu gehören Anforderungsmanagement, Architektur, Entwurf, Modellierung, Konstruktion, Programmierung, Dokumentation, Qualitätssicherung, Evolution, Wartung, Versionierung, Variantenmanagement und Vorbereitung der Nachnutzung.

Zur Definition eines praktischen und handlungssicheren Rahmens, in dem sich Mitarbeitende bei der Entwicklung von Software bewegen können, liegt für \[\[die Universität | die Hochschule | das Forschungszentrum\]\] diese Leitlinie vor, die unterstützend dazu beiträgt, Software mit hohen Qualitätsstandards effizient zu entwickeln, zu managen und damit Forschung zu stärken.

Diese Leitlinie richtet sich 

(1) an alle Entwickler:innen von Forschungssoftware und 

(2) deren Führungskräfte, die \[\[an der Universität | an der Hochschule | am Forschungszentrum\]\] an der Entwicklung, Verwaltung und Weitergabe von Software direkt oder indirekt beteiligt sind.

Die Leitlinie dient außerdem als Grundlage für

(3) die Verwaltung, die einen juristischen Rahmen für die Weitergabe und Lizenzierung von Forschungssoftware als komplettes oder teilweise eigenständig entwickeltes Softwarepaket \[\[der Universität | der Hochschule | des Forschungszentrums\]\] definiert und so unbürokratisch kooperative Forschungsvorhaben oder Forschungstransfer mittels Weitergabe von Software ermöglicht, 

(4) forschungsnahe Serviceeinrichtungen, die einen Rahmen für Beratung, Weiterbildung und ggf. Beteiligung an langfristig nachnutzbarer Entwicklung von Forschungssoftware schaffen, und

(5) die Leitung \[\[der Universität | der Hochschule | des Forschungszentrums\]\] als Organisationsrahmen für die finanzielle und organisatorische Unterstützung der Entwicklung, Pflege und Wartung von Forschungssoftware.

Ziel dieser Leitlinie ist es, einen handlungssicheren und nachhaltigen Umgang mit selbst entwickelter/angepasster Forschungssoftware zu etablieren, die Softwarequalität zu verbessern beziehungsweise diese langfristig zu halten und damit effizientere Forschung mit besserem Impact zu ermöglichen. Dies wiederum erhöht die Wertschätzung qualitativ hochwertiger Software und die Sichtbarkeit und Akzeptanz Forschungssoftware-basierter akademischer Leistungen. Die Leitlinie unterstützt deshalb die Professionalisierung im Bereich der Softwareentwicklung und fördert die  gute wissenschaftliche Praxis im Sinne von Verifizierbarkeit und Reproduzierbarkeit von Forschungsergebnissen in Zusammenhang mit Forschungssoftware.

Diese Leitlinie beinhaltet konkrete organisatorische Maßnahmen zur Entwicklung, Weiterentwicklung und Pflege der Forschungssoftware sowie auch die juristische Absicherung der Lizenzierung für die Weitergabe der Software an die Öffentlichkeit beziehungsweise die Fachcommunity.

## **2.1. Charakteristika von Software, speziell Forschungssoftware** {#2.1.-charakteristika-von-software,-speziell-forschungssoftware}

**Software** beinhaltet im Allgemeinen alle Formen von Quellcodes, Beschreibungen, Dokumentationen, ausführbaren Modellen, Konfigurationsdateien, darin eingebettete/verknüpfte Daten/-sätze, Skripte und daraus generierte ausführbare Programme sowie die Tests und Testbeschreibungen zu ihrer Qualitätssicherung.

**Forschungssoftware** muss also so verstanden werden, dass sie alle Formen von Beschreibungen, Dokumentation, ausführbaren Modellen, Konfigurationsdateien, darin eingebettete/verknüpfte Daten/-sätze, Skripte und daraus generierte ausführbare Programme, die im Rahmen der Forschung oder für Forschungszwecke entwickelt und genutzt werden, umfasst \[GKL+21\].

Zur Abgrenzung wird Software klassischerweise in drei wesentliche Bereiche: Systemsoftware, Anwendungssoftware und Entwicklungswerkzeuge unterteilt. Anwendungssoftware beinhaltet zum Beispiel Office-Produkte wie Textverarbeitung und Tabellenkalkulation. Technische Software und Systemsoftware beinhalten Betriebssysteme, Datenbank- und Kommunikationssoftware und Entwicklungswerkzeuge wie Versionskontrollsysteme oder auch in anderen Softwarearten verfügbare Bibliotheken zur Visualisierung, zum Datentransfer oder zur Datenspeicherung. Sie gehören nicht unter die Kategorie Forschungssoftware, können aber dennoch wesentlicher Bestandteil des Werkzeugkastens von Wissenschaftler:innen sein. 

Die Entwicklung von Forschungssoftware (im Folgenden: Software) ist meist Teil eines kreativen Prozesses und generiert in diesem Sinne ausführbares Wissen. Auch deshalb ist Software-Entwicklung im Allgemeinen eine intellektuelle und urheberrechtlich geschützte Leistung und im Kontext der Forschung ein eigenständiges Produkt der wissenschaftlichen Arbeit. 

Software ist darüber hinaus ein integraler Bestandteil moderner Publikationen. Deshalb ist ein agil anpassbares Verfahren zur Veröffentlichung und Mitarbeit bei der Entwicklung und Weiterentwicklung von Software \- in Form geeigneter Lizenzen und Kooperationsverträge \-  essenziell. 

Forschungssoftware kann einem langen, evolutionären Weiterentwicklungsprozess unterliegen. Neben dem Hinzufügen neuer Funktionen oder anderer Formen ausführbaren Wissens wird die Ausführungseffizienz optimiert, der Nutzungsbereich verallgemeinert oder die in Software immer vorhandenen Fehler behoben. Evolutionäre und qualitativ hochwertige Weiterentwicklung ist zeitlich aufwändig und bedarf anderer methodischer Vorgehensweisen als die initiale Erstellung. 

Die bei der Entwicklung von Forschungssoftware involvierten Wissenschaftler:innen (Research Software Engineers) sind bei den Ergebnissen der wissenschaftlichen Arbeit zu würdigen. So ist gemäß den Standards guter wissenschaftlicher Praxis (vgl. Leitlinie 14 \[DFG22\]) bei Publikationen, deren Erkenntnisse wesentlich auf der Basis der Forschungssoftware entstanden sind, eine gemeinsame Autorenschaft geboten. Siehe auch Abschnitt 5.4.

## **2.2. Charakteristika von Research Software Engineering** {#2.2.-charakteristika-von-research-software-engineering}

Die meisten Wissenschaftler:innen, die Software entwickeln, sind keine ausgebildeten Softwareentwickler:innen, sondern exzellente Forscher:innen in ihrer Fachdisziplin. Sie orientieren sich beim Software Engineering häufig an ihrem unmittelbaren Arbeitsumfeld und den Erfahrungen im Kollegium, ohne dabei zwangsläufig die Beratungsangebote, Instrumente, Best Practices und Erfahrungen \[\[der Universität | der Hochschule | des Forschungszentrums\]\] zu kennen, so sie denn existieren. 

Um diese Wissenschaftler:innen in ihrer Eigenständigkeit und Handlungsfähigkeit zu unterstützen, bietet RSE ein Bündel von Maßnahmen an, das die Probleme der Softwareentwicklung im Allgemeinen, aber auch unter den akademischen Rahmenbedingungen adressiert. Dabei ist zu beachten, dass fachspezifische und wissenschaftliche Richtlinien hier außen vor gelassen werden, da sich diese Richtlinien ausschließlich auf den Softwareentwicklungsteil konzentrieren:

* Welche Qualitätsattribute sind für eine konkrete Forschungssoftware relevant?  
* Wie lässt sich sicherstellen, dass die Software richtig und korrekt funktioniert?  
* Wie wird die regulatorische Compliance der Software, bzw. des Softwareentwicklungsprozesses sichergestellt?  
* Wie lässt sich die Software effizient entwickeln (Arbeitszeit)?  
* Wie lässt sich effiziente Software entwickeln (Compute)?  
* Wie kann Software weiterentwickelt und langfristig nutzbar erhalten werden?  
* Wie lassen sich Zeitvorgaben und Budgetbeschränkungen einhalten?  
* Wie kann Software verallgemeinert werden, um mehr Nutzer:innen zu erreichen?

RSE adressiert die organisatorische, fachliche und methodische Einbettung effizienter und qualitativ hochwertiger Softwareentwicklung unter Einbeziehung aller jeweils relevanten Entwicklungsaktivitäten des Software Engineering. Dies beinhaltet auch die Qualifikation der Entwickelnden, um Anforderungen, Architektur, Entwurf, Modellierung, Konstruktion/Programmierung, Qualitätssicherung, Dokumentation, Evolution, Wartung/Pflege, Versionen, Varianten und Nachnutzung ökonomisch effizient zu managen und damit Forschungssoftware nachhaltig zu erstellen und erhalten.

RSE adressiert dabei mehrere Besonderheiten bei der Entwicklung von Forschungssoftware: Diese ist typischerweise hochspezialisiert und erfordert sowohl in der Entwicklung als auch in der Anwendung entsprechende wissenschaftliche Expertise. Weil die Erkenntnisse fortschreiten und sich damit Forschungsfragestellungen und Versuchsbedingungen signifikant verändern, ist Forschungssoftware außerdem änderungsintensiv. Weil die Community der Nutzenden und Entwickelnden mit der Zeit wächst und sich weltweit organisieren muss, verändern sich Vorgehensweise, technische und organisatorische Rahmenbedingungen, und es potenzieren sich die Vielzahl unterschiedlicher, teilweise in Konflikt stehender und allzu oft nicht präzise ausformulierbarer Anforderungen.

Daraus entstehen spezifische Herausforderungen für die Softwareentwicklung. Die Vorgehensweise der Anforderungserhebung im RSE ist anders zu organisieren, weil diese untrennbar mit dem Forschungsprozess verzahnt ist. Dies hat deutliche Auswirkungen auf die anwendbaren Methoden, zum Beispiel der agilen Entwicklung, das oft notwendige Refactoring der Architektur oder die Qualitätssicherung durch automatisiertes Testen. Forschungsspezifische Qualitätskriterien beinhalten Transparenz und Reproduzierbarkeit der berechneten Ergebnisse und die Nachnutzbarkeit der Software selbst und damit Robustheit, Konfigurierbarkeit und Variabilität sowie die Evolutionsfähigkeit der Software. 

## **2.3. Aufgaben der Leitlinie** {#2.3.-aufgaben-der-leitlinie}

Diese Leitlinie bietet einen Rahmen für die Entwicklung, Verwaltung und Weitergabe von Software an \[\[der Universität | der Hochschule | dem Forschungszentrum\]\]. Sie eignet sich auch für standortübergreifende Verbundforschungsvorhaben, wenn die Projektbeteiligten kompatible Fassungen der Leitlinie nutzen. Diese Leitlinie 

* legt grundsätzliche Anforderungen an die Entwicklung, Verwaltung und Weitergabe von Software fest (Kapitel 3),  
* definiert das sinnvolle und notwendige Grundwissen von Wissenschaftler:innen, die Forschungssoftware in der jeweils gebotenen Qualität effizient zu entwickeln (Kapitel 3),  
* beschreibt praktische sowie organisatorische Abläufe (Kapitel 3),  
* liefert eine Entscheidungsgrundlage zur Wahl geeigneter Lizenzen (Kapitel 4),  
* legt fest, wie \[\[die Universität | die Hochschule | das Forschungszentrum\]\] Forschende in der Entwicklung von Forschungssoftware unterstützt (Kapitel 5\) und   
* präzisiert die Handreichung zum Umgang mit Forschungssoftware im Förderhandeln DFG \[DFG24\].

Diese Leitlinie behandelt wesentliche Teile des Software-Lebenszyklus, von der Softwareentwicklung und ihren Teil-Aktivitäten, wie Design, Qualitätssicherung, Abnahme, Dokumentation bis hin zur Archivierung, Weitergabe und Pflege der Software. 

Die Leitlinie soll unterstützend dazu beitragen, hohe Standards bei Softwareentwicklung, Softwarequalität und Management zu ermöglichen und gleichzeitig helfen, die beschränkten arbeitszeitlichen Ressourcen der beteiligten Stakeholder effizient einzusetzen. Mit dieser Professionalisierung wird mehr Nachhaltigkeit erreicht, eine bessere Nachnutzung von Investitionen erzielt und eine gute wissenschaftliche Praxis im Sinne von Verifizierbarkeit und Reproduzierbarkeit von Forschungsergebnissen gefördert.

Diese Leitlinie richtet sich an alle Stakeholder an der Softwareentwicklung, vor allem aber an alle Entwickler:innen und Führungskräfte, die an der \[\[Universität | Hochschule | Forschungseinrichtung\]\] an der Nachnutzung, Entwicklung, Verwaltung und Weitergabe von Software direkt oder indirekt beteiligt sind. Ziel der Leitlinie ist es, einen handlungssicheren und nachhaltigen Umgang mit Forschungssoftware zu etablieren, die Softwarequalität zu verbessern, die Entwicklungseffizienz zu steigern und die Wertschätzung für qualitativ hochwertige Software zu erhöhen.

Im Sinne von Open Science sind der Zugang zu und die Nachnutzung von Software die Basis für Nachvollziehbarkeit, Verifizierbarkeit und Reproduzierbarkeit von wissenschaftlichen Ergebnissen. Die FAIR-Prinzipien (Findable, Accessible, Interoperable, Reusable) \[FAIR20\], die für Forschungsdaten gelten, sind entsprechend auch auf Forschungssoftware anzuwenden \[BHK+22\], wobei zusätzlich die Weiterentwicklung, Fehlerkorrektur, Security-Updates und Versionierung der eigentlichen Software, aber auch genutzter Softwarekomponenten, des Betriebssystems, der Firmware und gegebenenfalls der Hardware zu berücksichtigen sind. Deshalb ermutigt \[\[die Universität | die Hochschule | das Forschungszentrum\]\] die Forschenden dazu, Software nach den FAIR Prinzipien für Forschungssoftware beispielsweise als „Open Source“ mit weitgehenden Zugangs- und (Nach-)Nutzungsrechten offen zugänglich zu machen, und dabei die Weiterentwicklung, Fehlerkorrektur, Security-Updates und Versionierung der Software zu berücksichtigen. 

## **2.4. Abgrenzung, Nicht-Aufgabe der Leitlinie** {#2.4.-abgrenzung,-nicht-aufgabe-der-leitlinie}

Zu beachten ist, dass die Leitlinie sich nicht mit den spezifischen gesetzlichen und untergesetzlichen Regelungen von Software der Wissenschaftsdomäne befasst. Dafür sind die fachspezifischen weiterführenden Richtlinien und technischen Normen zu beachten, die bei kritischer Software wie z. B. in der Medizintechnik eine besondere Rolle spielen.

Die Leitlinie adressiert nicht die betriebswirtschaftlichen Rahmenbedingungen für den Kauf von Software oder die Kosten der Ausführung von Software auf gemieteter oder gekaufter Hardware. Total Cost of Ownership Betrachtungen zu diesem Themenkomplex finden sich in entsprechender Fachliteratur, zum Beispiel zu “Make Or Buy”-Prozessen oder dem “Not Invented Here Syndrom” der Softwareentwicklung. 

\[\[Optional: Abgrenzung zur KI. \-- Dynamisches Feld erlaubt aktuell noch kaum stabile Aussagen\]\]

Das Thema KI, insbesondere die Nutzung von LLMs, wird aktuell sehr intensiv diskutiert. Je nach Betrachtungsweise kann eine LLM-basierte KI einfach nur als weiteres Werkzeug gesehen werden, das bei der Softwareentwicklung unterstützt, um schneller und effizienter Anforderungen in Modelle und Modelle in Code zu übersetzen, Testfälle zu erstellen, Qualitätsprobleme zu identifizieren, Erklärungen und Dokumentation zu generieren, etc. Die Verwendung von LLMs obliegt denselben Regeln wie jedes andere Werkzeug auch, also der Lizenzierung, der Verwertungsregelung, der Plagiat-Vermeidung, etc. Detaillierte Handreichungen hierzu werden mit einer Konsolidierung der LLM-Verwendung und nach einer besseren Klärung des Umgangs damit verfeinert. \[\[Die Universität | der Hochschule | das Forschungszentrum\]\] bietet auch hierzu Beratung und Unterstützung an (Kapitel 5).

Unabhängig davon können KI-Komponenten, also zum Beispiel Neuronale Netze oder Erklärungs-generierende LLMs, in Softwareprodukte eingebaut werden. Hier können die jeweiligen Fachexpert:innen weiterhelfen, denn auch für den Einbau von KI in Softwareprodukte gelten die gleichen Regeln wie für alle anderen Softwarekomponenten zum Thema Qualität, Korrektheit, Nachvollziehbarkeit, etc.

\[\[Option Ende\]\]

## **2.5. Damit abgestimmte Rahmen Guidelines for Safeguarding, Good Research Practice, Code of Conduct-Bedingungen** {#2.5.-damit-abgestimmte-rahmen-guidelines-for-safeguarding,-good-research-practice,-code-of-conduct-bedingungen}

Bei der Entwicklung der Leitlinie wurden sowohl interne Rahmenbedingungen als auch weitere Empfehlungen berücksichtigt: 

\[\[Varianten: ggf. ergänzen\]\]

* der “GI- und de-RSE-Vorschlag für Leitlinien zur effizienten Entwicklung von qualitativ hochwertiger und langlebiger Forschungssoftware an Universitäten, Hochschulen und Forschungseinrichtungen” \[GI24\]  
* Handreichung zum Umgang mit Forschungssoftware der Schwerpunktinitiative Digitale Information der Allianz der deutschen Wissenschaftsorganisationen \[KF18\]

* die DFG-Leitlinien zur Sicherung guter wissenschaftlicher Praxis \[DFG22\]

* die Handreichung: “Umgang mit Forschungssoftware im Förderhandeln der DFG \[DFG24\]  
* \[\[Option: die Regeln zur Sicherung guter wissenschaftlicher Praxis, \[hausintern?\] \]\]  
* \[\[Option: die internen Vorgaben der „Veröffentlichungsrichtlinie“, \[hausintern?\] \]\]  
* \[\[Option: die „Leitlinie Forschungsdaten“, \[hausintern?\] \]\]  
* die „Checkliste zur Unterstützung der Helmholtz-Zentren bei der Implementierung von Richtlinien für nachhaltige Forschungssoftware“ des Arbeitskreises Open Science der Helmholtz Gemeinschaft \[MPB+21\].

\[\[Varianten Ende\]\]

## **2.6. Fazit** {#2.6.-fazit}

Die Implementierung dieser Software-Leitlinie \[\[der Universität | der Hochschule | des Forschungszentrums\]\] ermöglicht den Mitarbeitenden in einem praktischen und handlungssicheren Rahmen, Software mit hohen Qualitätsstandards zu entwickeln und weiterzugeben.

Durch die Einteilung gemäß mehrerer Kategorien, wie zum Beispiel Anwendungsklassen und Technology Readiness Leveln (TRLs), das Aufzeigen von Qualitätsstandards und entsprechend empfohlener Maßnahmen, der Berücksichtigung von möglichen Transferwegen beziehungsweise Lizenzarten und die damit einhergehenden rechtlichen Aspekte wird eine Professionalisierung \[\[in der Universität | in der Hochschule | im Forschungszentrum\]\] in der notwendigen Breite realisiert.

\[\[Optional: Zusagen, die eine moderne Forschungseinrichtung geben sollte\]\]

Ergänzt wird dies durch die \[\[an der Universität | an der Hochschule | am Forschungszentrum\]\] bereitgestellten Entscheidungshilfen und Beratungsangebote für organisatorische und insbesondere methodische Entwicklungsunterstützung. 

Interne Schulungsangebote zu Softwareentwicklungs-Methodiken und Best Practices werden hierfür kontinuierlich ausgebaut und nach dem Stand der Technik aktualisiert, um so den wissenschaftlichen Nachwuchs zu hohen Standards in der Softwareentwicklung und Dokumentation zu befähigen.

Komplexe softwaretechnische Fragestellungen werden durch fachliche Expert:innen im Sinne eines Coachings und Trainings-On-The-Job unterstützt. Eine entsprechende Expert:innengruppe ist hierfür \[\[an der Universität | an der Hochschule | am Forschungszentrum\]\] eingerichtet. Die damit verfügbaren Expert:innen sind DFG-förderfähig.

\[\[Ende Optionen\]\]

Mit der durch diese Leitlinie generierten Wirkung wird Nachhaltigkeit und gute wissenschaftliche Praxis bei der Entwicklung und Weitergabe von Software und somit ein Mehrwert in der Gesellschaft, Wirtschaft, Wissenschaft und Politik geschaffen.

# 

# 3 Fachliche Leitlinien der Softwareentwicklung {#3-fachliche-leitlinien-der-softwareentwicklung}

Der fachliche Teil der Leitlinien ist für **Führungskräfte und Entscheidende** (= Instituts-, Lehrstuhl-Leiter:innen) sowie auch **Entwickler:innen** bestimmt, um Software effizient und nachhaltig entwickeln zu können.

→→ Für **Führungskräfte und Entscheidende** (= Instituts-, Lehrstuhl-Leiter:innen) besonders relevante Teile sind markiert. ←← 

Die Leitlinien beinhalten eine Handreichung für Führungskräfte(\!) und Entwickler:innen, um ihre Software einzuordnen und daraus abzuleiten, was für die Entwicklung an Grundwissen und Fähigkeiten vorhanden sein muss und welche Techniken / Werkzeuge eingesetzt werden sollen.

## **3.1. Einleitung**

Für die Softwareentwicklung existieren sowohl themenübergreifend als auch für einzelne Aktivitäten verschiedene, jeweils gut ausgearbeitete Vorgehensmodelle, Methoden, Praktiken und Werkzeuge, um diese Aktivitäten, von der Erhebung von Anforderungen bis zur Abwicklung eines Softwaresystems, zu unterstützen. Eine umfassende (und daher nicht direkt zu empfehlende) Übersicht über diese Aktivitäten des Software Engineering bietet der „Guide to the Software Engineering Body of Knowledge“ der IEEE Computer Society \[BF14\]. Software Engineering kann gut durch entsprechende Vorlesungen oder Standard-Bücher erlernt werden. Praktische Erfahrung ist dabei sehr relevant. Gute Lesebücher für Entwickler:innen mit gewisser Erfahrung und Interesse an Vertiefung sind z.B. Lichter/Ludewig (“Software Engineering: Grundlagen, Menschen, Prozesse, Techniken”) \[LL23\] oder Sommerville (“Software Engineering”) \[Som18\], sowie ein detailliertes Nachschlagewerk von Balzert/Ebert (“Lehrbuch der Softwaretechnik”) \[Bal25\]. Zahlreiche themenspezifische Bücher sind ebenfalls hilfreich.

→→ Für **Entscheidende** ←← 

Auf Basis der besonderen Herausforderungen für Forschungssoftware ist es notwendig, die Ziele von Forschungssoftware und die langfristige Strategie frühzeitig festzulegen, um auf dieser Basis unterschiedliche Methoden zu Erstellung und Management auszuwählen und relevante Entwickler-Kernkompetenzen  sicherzustellen. Wichtiges Element ist dabei, die potentiell unterschiedlichen Ziele aller Stakeholder (u.a. Entwickler:innen, Entscheider:innen, Förderorganisationen und Forschungseinheiten) zu akzeptieren und gemeinsam zu antizipieren. Beispiele sind kurzfristiger Erfolg mit wissenschaftlichen Publikationen versus langlebige, nachhaltig verfügbare Infrastruktur (im Sinne von Forschungssoftware) für weitere Forschungsaktivitäten; diese stehen zum Teil im Widerspruch und können vor allem durch die Anwendung von Techniken im Software Engineering-Portfolio adressiert werden. 

Schritt 1: Ziele der Software/des Projekts gemeinsam festlegen. Dazu dienen die in den folgenden Abschnitten definierten Formen der Einordnung bzw. Kategorisierung der Software. 

\[\[Anmerkung: manche der vier Schritte sind zu streichen, wenn der entsprechende Abschnitt gestrichen wurde; zum Beispiel ist die Auswahl der Anwendungsklasse nicht mehr notwendig, wenn Dimension und Soll-TRL gewählt wurden.\]\]  
---

→→ Für **Entscheidende** zur Übersicht ←←

Es folgen noch drei weitere Schritte, die Entscheidende durchführen sollten, um die Randbedingungen für die Entwicklungsergebnisse sowie auch die Vorgehensweise zu klären. Die Schritte sind in den nachfolgenden Abschnitten erklärt:

Schritt 2: Klassifikation der Software vornehmen: welche Dimension (Art) und (Ng) soll die Software nach/bei Projektende(\!) haben? Dabei ist auch der bisherige Software-Bestand zu berücksichtigen und geeignete Softwarekomponenten sind effizient weiter zu nutzen bzw. weiterzuentwickeln. (siehe 3.2.2)

Schritt 3: Soll-TRL festlegen oder Vorgabe vom Fördergeber übernehmen und dabei die konkreten Kriterien zu Robustheit, Skalierung, Anbindung an Nachbarsysteme, flexible Erweiterbarkeit, Security, usw. definieren.  (siehe 3.2.3)

Schritt 4: Gewünschte Anwendungsklasse identifizieren. (siehe 3.2.4)  
---

1. ### Forschungssoftware: Demonstrator, Produkt, Infrastruktur {#forschungssoftware:-demonstrator,-produkt,-infrastruktur}

Software, die in Forschungsprojekten entsteht und für darauf aufbauende Forschung weiterverwendet werden soll, nimmt mittelfristig die Rolle von Infrastruktur für die Forschung ein. Nicht jede Software wird Infrastruktur, sondern hat ggf. nur eine beschränkte Reichweite. Deshalb ist frühzeitig zu überlegen, welchen Reifegrad (TRL, siehe unten) die Software erzielen soll. Neben der Festlegung eines Softwareentwicklungsprozesses kann ein Software Management Plan (SMP) helfen, Strukturen und Ziele zu definieren, sodass die Entwicklung einer langlebigen und nachnutzbaren Software gestützt wird.

Die Qualität und Reproduzierbarkeit der mit langlebiger Software erzeugten Forschungsergebnisse hängt ebenso von der eingesetzten Software und ihrer Qualität ab, wie die darauf aufbauenden Arbeiten. Damit bildet diese Art von Software eine durchaus teuer erstellte und deshalb langfristig zu erhaltende Forschungsinfrastruktur, die systematisch, diszipliniert und professionell entwickelt, fortlaufend gewartet und betrieben werden muss (oder eben abgekündigt wird). Software ist immer in einem technischen Kontext im Einsatz: z. B. ist sie für ein Betriebssystem und ggf. eine bestimmte Hardwarearchitektur entwickelt. Sie nutzt idealerweise existierende Programmbibliotheken und Frameworks. Der technische Kontext wird unabhängig vom Forschungsvorhaben laufend weiterentwickelt und steht in der verwendeten Konfiguration irgendwann nicht mehr zur Verfügung. Dadurch entsteht die Notwendigkeit, Forschungssoftware auch aktiv zu warten, wenn Forschungsergebnisse reproduzierbar zu halten sind. Ist die Software nicht wartbar, ist weder die Reproduzierbarkeit der Forschungsergebnisse noch die langfristige Weiternutzung gewährleistet.

Wird Forschungssoftware als Infrastruktur geplant und gewartet, erhöht sich die Effektivität und Effizienz der Forschung. So können wiederkehrende technische Aufgaben schneller entwickelt werden. Neben der Einsparung von Entwicklungsaufwand kann auch der Lernaufwand von Forschenden für die Bedienung und Entwicklung einer Forschungssoftware verringert werden, wenn wiederkehrende oder ähnliche Aufgaben nicht immer neu und anders umgesetzt werden. Durch fortlaufende Qualitätssicherungsmaßnahmen der Forschungssoftware wird die interne Validität des Forschungsprozesses gestärkt.

## **3.2. Kategorisierung von Forschungssoftware** {#3.2.-kategorisierung-von-forschungssoftware}

Forschungssoftware nimmt vielfältige Formen an und kann je nach ihrem Anwendungsbereich und ihrer Zweckbestimmung unterschiedlichen Kategorien zugeordnet werden. Diese Kategorisierung hat eine entscheidende Bedeutung, da sie hilft, die Anforderungen an die Software zu bestimmen und damit eine Grundlage für die Auswahl geeigneter Software Engineering-Methoden bietet. Wir empfehlen die Kategorisierung entlang folgender Dimensionen vorzunehmen: 

\[\[Nicht benutzte Teile rausnehmen (siehe nachfolge Varianten 1-4): 

* Die Art der Forschungssoftware (Art),   
* den Nutzungsgrad (Ng),   
* den Reifegrad (Technology Readiness Level gemäß EU-Einteilung (TRL)) und   
* der Anwendungsklasse (Ak).

\]\] 

\[\[Variante 1: Die Nutzung der Kategorisierung ist optional; spätere Definitionen basieren jedoch darauf\]\]  
Fördergeber, wie die DFG in \[DFG24\], empfehlen bei der Antragstellung eine explizite Einordnung des Softwaretyps/der Kategorie und die daraus ableitbare Vorgehensweise beim Entwicklungsprozess und der Pflege der Software. 

### 3.2.1. Art der Software bzw. Softwarekomponente (Dimension Art)  {#3.2.1.-art-der-software-bzw.-softwarekomponente-(dimension-art)}

Eine Dimensionsvariante definiert sich durch die Art der Software, oder stark verwandt damit der Zweckbestimmung der Software. Eine detaillierte Kategorisierung ist in \[HDB+24\] zu finden, deshalb folgt hier nur sehr grobe Unterscheidung, die nicht immer trennscharf ist:

| (Art:MSD) | Modellierung/Simulation/Datenanalyse: Software, die Modellierungen von Systemen oder Prozessen darstellt, Simulationen oder komplexe Datenanalysen durchführt. |
| :---- | :---- |
| (Art:PoC) | Technology Research Software: Software, die als Proof-Of-Concept (Prototyp) für ein in Erfindung oder Entwicklung befindliches System oder einen Prozess genutzt wird. |
| (Art:Ctrl) | (Embedded) Control Software: Software, die in Maschinen, Sensoren oder ähnlichen Geräten eingebettet ist und deren Steuerung und Regelung übernimmt, um Experimente durchzuführen und Daten zu sammeln. |
| (Art:Tool) | Software-Werkzeuge, \-Bibliotheken und \-Frameworks, die zur Entwicklung und zum Betrieb von Software genutzt werden. |
| (Art:User) | User Apps, um Interaktion mit menschlichen Probanden und Nutzenden zu erlauben. |

Komplexe Software kann durchaus Komponenten mehrerer Arten beinhalten. Die Art der Software hat Einfluss auf Aspekte wie Kritikalität (siehe Anhang A), Security und Privacy, Usability and Accessibility oder den notwendigen Reifegrad (TRL). 

\[\[Ende Variante 1\]\]

\[\[Variante 2: Die Nutzung der Software-Arten ist optional; spätere Definitionen basieren jedoch darauf; sie benötigt/ergänzt Variante 1\]\]

### 3.2.2. Nutzungsgrad der Software bzw. Softwarekomponente  (Dimension Ng)  {#3.2.2.-nutzungsgrad-der-software-bzw.-softwarekomponente-(dimension-ng)}

| (Ng:TI) | Technische Infrastruktur: Weitgehend ausgereifte Software, die als grundlegende Forschungsinfrastruktur dient, beispielsweise für Daten-, Konfigurations-, Change-Management, Modellierungswerkzeuge, allgemeine Tools oder bereitgestellte Bibliotheken. |
| :---- | :---- |
| (Ng:FI) | Fachliche Infrastruktur: Weitgehend ausgereifte Software, die fachliche Funktionalitäten zur Verfügung stellt, die für verschiedene Zwecke wiederverwendet werden kann. Sie kann durch externe Nutzende unabhängig von den Entwickelnden angewendet werden. |
| (Ng:Growing) | Software zur Anwendung durch externe Nutzende vorgesehen; sie hat aber aktuell nur eine begrenzte Nutzer:innenschaft außerhalb der ursprünglichen Auftraggebenden/Kernentwickelnden. Die Anwendung durch externe Nutzende unabhängig von den Entwickelnden ist nur eingeschränkt möglich. |
| (Ng:Ind) | Individualsoftware: In einem begrenzten (Forscher:innen-)Kreis im Einsatz befindliche Software. |
| (Ng:Dem) | Demonstration Software: Demonstration von Software-Funktionen und/oder  Konzepten bzw. von Simulationsansätzen/mathematischen Modellen in erster laufender Software, ohne bereits in Produktionsumgebungen angewandt zu werden. |

(Ng:Ind) hat möglicherweise das Potenzial über den Zwischenschritt (Ng:Growing) zur Infrastruktur zu werden, ist aber aktuell nur im lokal begrenzten Einsatz und erlaubt es noch, direkt mit Nutzenden zu interagieren, diese auf Defizite im Einsatz hinzuweisen, zu schulen, und auf weitere Anforderungen einzugehen. Die Phase (Ng:Growing) benötigt explizite Dissemination, Community-Bildung und Nutzenden-Training und kann typischerweise nur erfolgreich sein, wenn Robustheit im Einsatz, Anpassbarkeit und Erweiterbarkeit der Software durch fremde Entwickelnde, und einige weitere Qualitätsattribute adressiert sind. Dies ist aber frühzeitig zu planen, weil auch in der Software nachträgliche Qualitätssteigerung nur schwer zu erreichen ist. Spätestens für die Phase (Ng:TI) bzw. (Ng:FI) sind hier auch organisatorische Maßnahmen notwendig, um Verantwortlichkeiten adäquat zu definieren und ggf. die Software als Service oder Werkzeug zur Verfügung zu stellen. Dies ist eine organisatorische wie auch eine Finanzierungsfrage, die unter Unterstützungsleistungen in Abschnitt 5 zu diskutieren ist. 

(Ng:Dem)-Software wird von vornherein so gebaut, dass sie schnell ihren Demonstrationszweck erfüllt und typischerweise danach entsorgt wird. Es liegt in der Natur von (Ng:Dem), keine vernünftige innere Architektur und damit auch nicht die Fähigkeit zur Weiterentwicklung mit sich zu bringen.

→→ Für **Entscheidende** ←←   
Ggf. für Komponenten individuell zu klärende Frage:

* Welche Kategorie soll der Software am Ende der aktuell geplanten Entwicklungsphase zugeordnet sein?

Schritt 2: Klassifikation der Software vornehmen: welche Dimension (Art) und (Ng) soll die Software nach/bei Projektende(\!) haben? Dabei ist auch der bisherige Software-Bestand zu berücksichtigen und geeignete Softwarekomponenten sind effizient weiter zu nutzen bzw. weiterzuentwickeln. 

\[\[Ende Variante 2\]\]

\[\[Variante 3: Die Nutzung von TRLs ist optional; spätere Definitionen basieren jedoch darauf\]\]

### 3.2.3. Einordnung in die Technology Readiness Levels (TRL) entsprechend der EU {#3.2.3.-einordnung-in-die-technology-readiness-levels-(trl)-entsprechend-der-eu}

Der **Technology Readiness Level** (**TRL**) (deutsch: Technologie-Reifegrad, \[DIN20\]) ist eine von Fördergebern wie z.B. der EU verwendete Skala zur Bewertung des aktuellen oder anvisierten Entwicklungsstandes von Technologien. Die TRLs werden auch auf Software und konkret auf Forschungssoftware angewendet. Siehe z.B. die Einordnung seitens des Earth Science Technology Office (ESTO) der NASA \[NAS20\]. Konkret gibt sie auf einer Skala von 1 bis 9 an, wie einsatzfähig, auf Basis von definierten Kriterien, eine Forschungssoftware ist. 

Bei TRLs wird die Einstufung typischerweise auf Basis der aktuellen bzw. geplanten Anwendungsform der Forschungssoftware getroffen, z.B. ist bereits im praktischen Einsatz, und stellt nicht direkt ein Gütesiegel für die Software selbst dar. Die Forschungssoftware muss üblicherweise evolutionär alle Grade bis zum geforderten TRL durchlaufen. Agile Entwicklungsmethoden sorgen allerdings für frühzeitige hohe TRLs und bauen die Software dann sukzessive aus.

Die Zuordnung von Software zu TRLs ist individuell für jede Forschungssoftware zu prüfen und es kann in begründeten Ausnahmefällen von der Zuordnung zu TRLs abgewichen werden. Bei größeren Änderungen der Software ist der TRL neu zu bestimmen, denn er kann sowohl steigen als auch abnehmen.

Die Tabelle der TRL für Forschungssoftware: 

| Tabelle der Technology Readiness Levels (TRLs) für Research Software |
| :---- |
| **TRL 7-9: Auslieferung & Nutzung** |
| 9: Stabiles Produkt unter fortlaufender Qualitätskontrolle im allgemeinen Einsatz |
| 8: Stabile Version verfügbar; Software robust und qualitätsgesichert |
| 7: Beta Version für externe Nutzende erfolgreich im kontinuierlichen produktiven Einsatz  |
| **TRL 4-6: Entwicklung & Härtung** |
| 6: Beta Version durch ausgewählte Nachnutzende unter kontrollierten Bedingungen getestet |
| 5: Alpha Version außerhalb des Entwicklungsteams in einem externen Forschungs-Lab getestet und validiert  |
| 4: Alpha Version intern von Entwicklungsteam erfolgreich genutzt  |
| **TRL 1-3: Exploration und Prototyping** |
| 3: Erster Prototyp (Proof Of Concept)       			 |
| 2: Technologie (Software Stack) und wichtigste Anforderungen geklärt  |
| 1: Erste Ideen entwickelt  |

→→ Für **Entscheidende**  ←←   
Ggf. für Komponenten individuell zu klärende Fragen:

* Welche Kategorie soll der Software nach der aktuell geplanten Entwicklungsphase zugeordnet sein? Was ist der Soll-TRL?  
* Wenn die Softwareentwicklung bereits gestartet ist: Welche Kategorie (also Ist-TRL) hat die Software aktuell? (Konsequenz: Was ist zu tun, um ausgehend vom Ist-TRL den Soll-TRL zu erreichen?)

TRL-1 bis TRL-3 der Forschungssoftware bedeuten, dass diese den Stand eines experimentellen Prototyps erreicht hat, der das prinzipielle Funktionieren der Grundideen der Forschungssoftware nachweist. Dieser hat allerdings nur limitierte Funktionalität und nicht die Robustheit, die für eine allgemeine, zuverlässige Anwendung im Forschungskontext notwendig ist (Ng:Dem). Zumeist fehlen Schnittstellen und die Aufbereitung von  Ergebnissen. Für die Nutzung der Forschungssoftware zur Erzielung von reproduzierbaren, korrekten Forschungsergebnissen in einem Lab (also (Ng:Ind)) sind mindestens TRL-5 bis TRL-6 notwendig, wobei das “relevante, kontrollierte Forschungs-Lab” typischerweise das auftraggebende Forschungsteam aus \[\[ der | dem \]\] eigenen \[\[Universität | Hochschule | Forschungszentrum\]\] darstellt, und damit Entwickelnde und Nutzende kommunikative Kanäle besitzen oder sogar dieselben Personen sind. Forschungssoftware (Ng:Ti) und (Ng:FI), die langfristig genutzt werden soll, muss ein TRL-7 bis TRL-9 erreichen, wobei “mehrere Forschungs-Labs” insbesondere fremde Labs einschließt, die keine beratende Unterstützung bei der Anwendung von Software haben. Bei TRL-9 nutzen fremde Labs die Software selbständig als vertrauenswürdiges Werkzeug.

Ein Soll-TRL klärt die notwendigen Konsequenzen für den Entwicklungsprozess und die zu verwendenden Aktivitäten und Werkzeuge, denn hohe TRL erfordern andere Methoden zur Entwicklung, Test- und Validierungskonzepte, sowie Softwarearchitekturen zur Sicherung der Qualität und Anwendbarkeit. Wichtig ist dabei, dass beides frühzeitig in die Software eingebaut werden muss und sich nicht oder nur schwer nachträglich anpassen lässt. 

Ein Software Management Plan hilft dabei, diese Zielsetzungen frühzeitig zu konzipieren und dann strukturiert umzusetzen. Vertrauenswürdige Forschungsergebnisse benötigen sichere, anwendbare, robuste und korrekte Software. Extern wiederverwendbare Software sollte TRL-8 erreicht haben, erste Forschungsergebnisse im eigenen Lab sind ab TRL-4 verlässlich publizierbar. Fachspezifische TRL-Definitionen können im Einzelfall massiv davon abweichen (siehe Beispiel Medizintechnik).

Man beachte:  

* Der TRL hängt von zwei Kriterien ab: (a) dem Entwicklungszustand und der Robustheit der Software und (b) von dem extern validierten Nachweis, dass Software erfolgreich im Einsatz ist.  
* In TRL 1-3 ist die Definition der Software stark verzahnt mit dem eigentlichen Forschungsprozess, während ab TRL 4 der Fokus mehr auf der Softwareentwicklung selbst und der praktikablen Anwendung im Forschungsprozess liegt.

Schritt 3: Soll-TRL festlegen oder Vorgabe vom Fördergeber übernehmen und dabei die konkreten Kriterien zu Robustheit, Skalierung, Anbindung an Nachbarsysteme, flexible Erweiterbarkeit, Security, usw. definieren. 

\[\[Ende Variante 3\]\]

\[\[Variante 4: Optional: Anwendungsklassen passen z.B. zu Großforschungseinrichtungen; sie bilden eine starke Vereinfachung z.B. im Vergleich zu den TRLs der Fördergeber, Empfehlung: ggf. nicht beides inkludieren\]\]

\[\[Anmerkung zu Variante 4: In Diskussionen bei der Erstellung dieser Leitlinie wurde festgehalten, dass diese Anwendungsklassen vor allem in Großforschungseinrichtungen mit der Kapazität, alles Inhouse zu entwickeln, nutzbar sind. Für Universitäten/Hochschulen, die mehr mit externen Partnern arbeiten, sind sie weniger geeignet, denn sie aggregieren einerseits mehrere Dimensionen, sind aber in dieser Aggregation insbesondere für verteilte Entwicklung und verteilte Verantwortung unvollständig, was zu einem unglücklichen Gesamtbild führen kann.\]\]

### 3.2.4. Anwendungsklassen   {#3.2.4.-anwendungsklassen}

In Anlehnung an \[SMH18\] lässt sich eine Skala von vier Anwendungsklassen definieren, die eine grobe, linearisierte Einordnung mehrerer Metriken für Software, aktuelle und geplante Nutzung sowie die Entwickler:innen-Basis darstellen und für kritische Softwarekategorien gegebenenfalls nicht geeignet sind.  Die Erklärungen in diesem Abschnitt werden weitgehend aus \[SMH18\] übernommen.

Die Anwendungsklassen (AK) helfen, geeignete Maßnahmen hinsichtlich der Software-Qualität festzulegen. Sie erlauben es, Aktivitäten und Werkzeugeinsätze bedarfsgerecht zu gestalten, die notwendigen Entwicklungskills für die Entwickler:innen zu identifizieren, und strukturieren die Kommunikation der Beteiligten zu Anforderungen, Randbedingungen und Qualität. Den Anwendungsklassen zugeordnet sind jeweils Empfehlungen, die teilweise aufeinander aufbauen, teilweise sich aber auch ersetzen müssen, um eine angemessene Entwicklungs-Effizienz und Ergebnisqualität sicherzustellen. Sie adressieren den Investitionsschutz, Minderung von Risiken, Wissenserhalt und die langfristige Erhaltung und Nutzbarkeit der entstandenen Software. 

Es folgt die Unterteilung in vier Anwendungsklassen 0-3, wobei typischerweise der Grad der Qualität und der notwendigen Maßnahmen steigen. Maßgeblich für die Einordnung ist der Aspekt “Fokus”, Umfang und Maßnahmen ändern sich ggf. nur zum Teil im Gleichklang damit.

**Definition Anwendungsklassen**

*Anwendungsklasse Ak0:*

* Fokus: Persönlicher Gebrauch und keine Weitergabe der Software geplant, vereinzelte Detaillösungen von Forschungsinhalten  
* Umfang der Software: Gering   
* Maßnahmen: Selbstbestimmt mit Beachtung der guten wissenschaftlichen Praxis  
* Beispiel: Skripte zur eigenen Organisation von Daten


*Anwendungsklasse Ak1:*

* Fokus: An der Entwicklung unbeteiligte Forschende sollen die Software in definiertem Rahmen nutzen können  
* Umfang der Software: Wenige Funktionalitäten bzw. geringer Funktionsumfang, der seitens der Forschungseinrichtung bereitgestellt bzw. weiterentwickelt werden soll  
* Maßnahmen: Mit Zielsetzung auf Nachvollziehbarkeit und Reproduzierbarkeit, d. h. unter anderem, dass Anforderungen und Probleme bekannt sind  
* Beispiel: Datenanalyseskripte für Publikationen; Software aus Abschlussarbeiten bzw. Projekten, die nicht für eine längerfristige Nutzung geplant sind


*Anwendungsklasse Ak2:*

* Fokus: Längerfristige Weiterentwicklung und Wartbarkeit, Nutzbarkeit für neue Szenarien, umfangreicherer Nutzerkreis  
* Umfang der Software: Größerer Umfang der Software, die längerfristig seitens \[\[der Universität | der Hochschule | der Forschungseinrichtung\]\] bereit gestellt und weiterentwickelt werden soll  
* Maßnahmen: Randbedingungen, Anforderungen sowie Qualitätsstandards sind in einer angemessenen Softwarearchitektur festzuhalten,   
* Beispiel: Frameworks, die für mehrere Forschungsgruppen relevant sind

*Anwendungsklasse Ak3:*

* Fokus: Für die Einrichtung relevante oder kritische Forschungssoftware, typischerweise ein hohes Risiko für die Einrichtung bei Fehlfunktionen der Software, umfangreicher Nutzendenkreis, die bei Fehlfunktion kritisch betroffen sein können  
* Umfang der Software: Großer Umfang mit Produktcharakter  
* Maßnahmen: Risikominimierung, Fehlerreduktion für den Betrieb der Software, hoher Grad der Nachvollziehbarkeit der Funktionalität  
* Beispiel: Kritische Software für aeronautische Missionen 

Diese Klassifizierung bildet mehrere Kriterien auf vier Klassen ab und lässt dabei Spielraum bei der Einordnung. Zum Beispiel ist ein kompaktes Skript (eigentlich Ak0) für aeronautische Missionen dann nach Ak3-Kriterien einzuordnen. Weitere Einflussgröße ist die Verteilung der Entwickler:innen-Basis von institutsintern bis international verteilt. Es ist auch zu unterscheiden zwischen aktueller und geplanter Ziel-Anwendungsklasse.

Anwendungsklassen stellen einen einfachen Ansatz dar, Forschungssoftware zu kategorisieren, um daraus Anforderungen für den Entwicklungsprozess abzuleiten. Sie nutzen bei der Einschätzung der Klasse primär inhärente Charakteristika und externe Anforderungen, bspw. Kritikalität, potenzielle Nutzende oder geplante Nutzungsdauer. Somit sind die Kriterien zur Einschätzung der Anwendungsklassen und der in \[DIN20\] definierten TRLs nicht deckungsgleich. Beispielsweise kann jede Software der Ak0 bis Ak3 einen TRL-9 erreichen, aber auch bei TRL-3 verbleiben. 

→→ Für **Entscheidende**  ←← 

Die Definition der gewünschten Anwendungsklasse ist eine Projektion in die Zukunft und damit abhängig von der Planung der Entscheider.

Schritt 4: Gewünschte Anwendungsklasse identifizieren. 

\[\[Ende Variante 4\]\]

\[\[Variante 5\]\]

### 3.2.5. Status der Software  {#3.2.5.-status-der-software}

Folgendes Bild zeigt verschiedene Zustände, die eine Software bzw. ihr Entwicklungsprojekt einnehmen kann, siehe auch: \[YGJ24\]:  
                
![][image1]  
Auch dieser Ansatz kann zur Festlegung von Entwicklungsaktivitäten und Methoden beitragen.  
\[\[Ende Variante 5\]\]

### 3.2.6. Weitere Einflüsse  {#3.2.6.-weitere-einflüsse}

Einfluss auf den Entwicklungsprozess haben zudem:

* Community Scope: Beschaffenheit und Größe der Nutzendenbasis: von kleinen Forschungsteams bis hin zu globalen, diversen Gemeinschaften.  
* Developer Scope: Die Anzahl, Hintergründe und organisatorische Zugehörigkeit der beteiligten Entwickler:innen: einzelne:r Doktorand:in, ein Institut oder weltweit verteilte Open Source Gemeinschaft. Wichtig ist hier insbesondere, ob eine hierarchische oder eine föderative Projektstruktur und damit gewisse Unsicherheiten bezüglich der Personalstruktur vorliegen.  
* Kritikalität: adressiert die Auswirkungen von Problemen mit der Software, also Risiken wie die Fehleinschätzung der Entwicklungskomplexität auf die Kosten, bis hin zur Stilllegung eines Institutsbetriebs, Sach- und Personenschäden, oder die Zerstörung eines Experiments (siehe auch Anhang A).  
* Komplexität und Zukunftsfähigkeit des zu nutzenden Software-Stacks und der zur Verfügung stehenden Hardware-Varianten.

\[\[Variante 6: Optional alle oben nicht verwendeten Basis-Kategorisierungsgrößen können als Einflussfaktoren hier aufgelistet werden\]\]

* \[\[nicht Variante 1, dann:\]\] Art der Software  
* \[\[nicht Variante 2, dann:\]\] Nutzungsgrad der Software: Wie viele interne und vor allem externe Nutzer hat die Software und müssen daher im Projekt beachtet werden?  
* \[\[nicht Variante 3, dann:\]\] Technology Readiness Levels (TRL) entsprechend der EU  
* \[\[nicht Variante 4, dann:\]\] Anwendungsklassen laut DLR-Report  
* \[\[nicht Variante 5, dann:\]\] (Ziel-)Status der Software

\[\[Ende Variante 6\]\]

→→ Für **Entscheidende**  ←← 

Die Kategorisierung von Forschungssoftware ermöglicht eine bessere Einschätzung, welche Werkzeuge des Software Engineerings benötigt werden. Es ist wichtig zu beachten, dass die Perspektive der kategorisierenden Person die Kategorisierung beeinflusst, denn die Festlegung der  SOLL-Kategorien ist eine Projektion in die Zukunft und damit abhängig von der Planung der Entscheidenden.

## **3.3. Minimalanforderungen an Kernkompetenzen, Entwicklungsprozesse und Projektplanung in der Softwareentwicklung** {#3.3.-minimalanforderungen-an-kernkompetenzen,-entwicklungsprozesse-und-projektplanung-in-der-softwareentwicklung}

Die oben und im Anhang A genannten Klassifikationen, die geplante zukünftige Nutzung sowie die beteiligten Stakeholder (Nutzer:innen, Entwickler:innen und Finanzmittelgeber) bilden die Grundlage für die Auswahl an notwendigen anzuwendenden Software Engineering Praktiken. Diese adressieren organisatorische, methodische und technische Maßnahmen, um die Software zu realisieren, weiterzuentwickeln und einzusetzen. Solche Maßnahmen bieten daher **Investitionsschutz** und dienen der **Minimierung von Risiken** und dem Erhalt und der Weitergabe von Wissen. Und es leiten sich Vorgaben und Abnahmekriterien für die Erstellung von Forschungssoftware durch Externe (z.B. Softwareentwicklungsfirmen) sowie Vorgaben und Bewertungskriterien für studentische Arbeiten ab. Die hier eingeführten Praktiken sind eine Ausgestaltung der in \[DFG24\] definierten leitenden Prinzipien bei der Entwicklung von Forschungssoftware.

Aufgrund der vielen Einflussfaktoren sollte die Maßnahmenauswahl von erfahrenen Research Software Engineers vorgenommen oder zumindest vorgeschlagen werden. Die Software Engineering Praxis zeigt, dass zum Beispiel agile Methoden sehr effizient sind, aber nur mit einem Mindestmaß an Erfahrung der Beteiligten funktionieren. Es gibt außerdem Abhängigkeiten zwischen den Maßnahmen, die aufeinander aufbauen oder sich ausschließen.

Die Rollenverteilung in Team-basierten Projekten erlaubt die unterschiedliche Ausprägung von Kompetenzen bei den Projektbeteiligten. “Scientists who code”, also Wissenschaftler:innen, deren Hauptfokus der wissenschaftliche Erkenntnisgewinn (Publikation) in der eigenen Domäne ist, kommen unter Umständen damit aus, grundlegende Algorithmen formulieren zu können, wenn sie von einem oder mehreren erfahrenen Research Software Engineers unterstützt werden. Dennoch ist zumindest die Kenntnis der Existenz und des Zwecks von Software Engineering Methoden, wie Refactoring, auch für “scientists who code” hilfreich.

Schritt 5: Aus der bisherigen Klassifikationen gemeinsam mit erfahrenen Softwareentwicklungs-Manager:innen des Supports (siehe Kapitel 5\) die notwendigen Software Engineering Practices (siehe folgende Abschnitte) ableiten. 

Die nachfolgenden Kataloge stellen ausdrücklich nur eine erste Hilfestellung für eine solche Sammlung von Maßnahmen dar.

### 

### 3.3.1. Minimalanforderungen an den Technologie-Reifegrad auf Basis des Nutzungsgrads (Ng) und der Softwareart (Art) {#3.3.1.-minimalanforderungen-an-den-technologie-reifegrad-auf-basis-des-nutzungsgrads-(ng)-und-der-softwareart-(art)}

Dieser Abschnitt verbindet Nutzungsgrad (Ng) und Softwareart (Art) mit den dann normalerweise gebotenen TRLs und skizziert Einschränkungen dieser Zuordnung. 

| (Ng:TI) | TRL-8+ | Technische Infrastruktur: Tools sollten TRL-8 erreicht haben. Sonst kann ein Tool kaum als Infrastruktur bezeichnet werden.  |
| :---- | :---- | :---- |
| (Ng:FI) | TRL-8+ | Fachliche Infrastruktur: Komplette Systeme: TRL-8.  |
| (Ng:Growing) | TRL-7+ | Software zur Anwendung durch externe Nutzende vorgesehen; sie hat aber aktuell nur eine begrenzte Nutzer:innenschaft außerhalb der ursprünglichen Auftraggebenden/Kernentwickelnden. Die Anwendung durch externe Nutzende unabhängig von den Entwickelnden ist nur eingeschränkt möglich. |
| (Ng:Ind) | TRL-6 | Individualsoftware: Da der Nutzendenkreis begrenzt ist, können ggf. bestimmte Defizite akzeptiert werden  |
| (Ng:Dem) | TRL-5 (TRL-3) | Demonstration: Für empirische Validierung ist TRL-5 notwendig. Ohne Validierung würde TRL-3 reichen. |

Software startet oft in Kategorie (Ng:Dem) als Proof-of-concept und bleibt auf dieser Stufe. Während einer Wachstumsphase (Ng:Growing) und letztlicher Übernahme in die Infrastruktur (Ng:TI,Ng:TF) benötigt sie eine substantielle und damit normalerweise auch zeitintensive technische Überarbeitung. In der industriellen Praxis geht man davon aus, dass von TRL-5 zu TRL-8 also die Härtung der Software zur Produktreife etwa der Faktor 3 an Aufwand anfällt. Eine solche Härtung zur Produktreife kann auch durch Weiterbearbeitung als Open Source Software mit zunächst niedrigerem TRL verfolgt werden, aber dies ist keine Garantie für eine Verbesserung. 

Die TRL-Einordnung gilt grundsätzlich für Systeme, kann aber im Allgemeinen auf deren Komponenten, Frameworks und Programmbibliotheken übertragen werden, wenn diese Komponenten, Frameworks und Bibliotheken in einem System eingebaut sind und dadurch intensiv genutzt werden. 

Jede Art von Software kann auf jedem TRL stehen. Vertrauen sollte man Software aber erst nach ausreichender Qualitätssicherung, weshalb normalerweise TRL-6 mindestens zu erreichen ist. Bei modernen Softwarekomponenten (z.B. solche, die KI-gestützt sind), müssen spezielle Strukturen zur Kontrolle von zum Beispiel Bias, Reproduzierbarkeit und Datenschutz oft erst entwickelt werden. KI-Kolleg:innen können hier helfen. 

| (Art:MSD)(Art:PoC) | TRL-6+ | Simulation/Analyse/Data Processing/Proof-Of-Concept: kann auf jedem TRL stehen, vertrauen sollte man ihr aber erst nach ausreichender Qualitätssicherung (TRL-6). |
| :---- | :---- | :---- |
| (Art:Ctrl) | TRL-8+ | (Embedded) Control Software: Abhängig von der Kritikalität (Risiko); es ist oft TRL-8 üblich. Safety-relevante eigenständige Klassifizierungen und Normen existieren (z.B. Safety Integrity Level).  |
| (Art:Tool) | TRL-6+ | Software-Werkzeuge: Bei hoher Kritikalität ggf. auch höher. Wenn der Werkzeuganwendung eine anderweitige Qualitätssicherung des Ergebnisses folgt, so ist auch ein niedrigerer TRL-4/5 ausreichend. |
| (Art:User) | TRL-9 | User Apps: Wenn externe User die Software (z.B. als Handy-App) nutzen, ist TRL-9 relevant. DSGVO, Security, Safety und vor allem User Experience-Themen sind hier besonders zu adressieren. |

### 3.3.2. Minimalanforderungen an Handlungsfelder und notwendige Kernkompetenzen in der Softwareentwicklung auf Basis des Technologie-Reifegrads  {#3.3.2.-minimalanforderungen-an-handlungsfelder-und-notwendige-kernkompetenzen-in-der-softwareentwicklung-auf-basis-des-technologie-reifegrads}

Für Softwareentwicklung ist das SWEBOK (Software Engineering Body of Knowledge, \[BF14\]) die wesentliche Referenz aller zu beachtenden Aktivitäten, Fähigkeiten, nützlichen Werkzeuge und Vorgehensweisen.  Typische SE-Bücher (s.o.) basieren darauf und bereiten die jeweils wichtigsten Aktivitäten und Kernkompetenzen für die praktische Nutzung auf. 

Nachfolgend eine Zuordnung, welche der 15 Handlungsfelder des SWEBOK wie relevant in welchem der TRLs sein sollten. Die wichtigsten dieser Handlungsfelder sind in den Abschnitten 3.4 und 3.5 skizziert. Die so beschriebenen Kompetenzen sollten in der Forschungsgruppe existieren und zum Einsatz kommen. Dabei kann eine abhängig von der Entwicklungsmethodik heterogene Verteilung der Rollen und Fähigkeiten sinnvoll sein. Manche Fähigkeiten können auch durch Expert:innen der Softwaretechnik als Coaching partiell hinzugezogen werden (siehe Kap. 3.4 und Kapitel 5 zu Unterstützungsleistungen). Die konkrete Ausprägung der Kernkompetenzen hängt natürlich auch von gewählten Entwicklungsmethoden, Programmiersprachen und Werkzeugen ab. Der Bedarf an mathematischen, algorithmischen und informationstechnischen Grundlagen hängt stark von der Art der Software und dem Forschungsproblem ab.

| SWEBOK-Handlungsfelder | TRL 1-3 | TRL 4-6 | TRL 7-9 |
| :---- | :---- | :---- | :---- |
| Software Requirements | \+ | \+ | \+ |
| Software Design | \+ | \+ | \++ |
| Software Construction | \++ | \++ | \++ |
| Software Testing | \+ | \++ | \++ |
| Software Maintenance |  | \+ | \++ |
| Software Configuration Management | \+ | \++ | \++ |
| Software Engineering Management |  | \+ | \++ |
| Software Engineering Process | \+ | \+ | \++ |
| Software Engineering Models and Methods | \+ | \+ | \++ |
| Software Quality |  | \+ | \++ |
| Software Engineering Professional Practice |  | \+ | \++ |
| Software Engineering Economics | ? | ? | ? |
| Computing Foundations | ? | \+ | \+ |
| Mathematical Foundations | ? | ?? | ?? |
| Engineering Foundations |  | \+ | \+ |

Legende: 	?: möglicherweise zu beachten (themenabhängig)  
		??: möglicherweise stark zu beachten (themenabhängig)  
\+: zu beachten  
\++: stark zu beachten

→→ Für **Entscheidende**  ←← 

* Haben die beteiligten Entwickler:innen die gebotenen Kernkompetenzen in Methodik und Tooling? Welche Schulung, Weiterbildung, Hinzuziehung von externen, ausgebildeten Research Software Engineers ist sinnvoll? Sind gegebenenfalls spezielle herstellerspezifische Zertifizierungen für Entwickler:innen notwendig (und diese von verschiedenen Personen zu adressieren)?

## **3.4. Methodische Grundlagen der Softwareentwicklung**

Im nachfolgenden Teil werden die für RSE wichtigsten SE-Aktivitäten und SE-Kernkompetenzen skizziert. Sie ersetzen keine echte Ausbildung. Grundsätzlich gilt, dass eine Fähigkeit praktischer Erfahrung bedarf, um sie adäquat und flexibel einzusetzen. Coaching durch erfahrene Mitarbeitende oder externe Unterstützung sollte, wann immer möglich, hinzugezogen werden.

Anbei werden nur die wichtigsten, eher generell wirkenden methodischen Grundlagen diskutiert. Für vertiefende Techniken des Software Engineering, wie etwa Traceability, Usability-Management, Risikomanagement, Validierung und Verifikation, Machbarkeitsanalysen, exploratives Prototyping, etc. wird auf die Literatur des Software Engineering und Weiterbildungsangebote verwiesen.

 

### 3.4.1. Softwareentwicklungsprozesse 

\[SWEBOK: Software Engineering Process | Software Engineering Models and Methods\]

**Warum ist das wichtig?** Die Etablierung eines adäquaten Softwareentwicklungsprozesses ist die Kerngrundlage für effiziente, zielgerichtete Entwicklung. Bei komplexer Software mit verschiedenen User- und rechtlichen Anforderungen sind besser angepasste Methoden notwendig.

**Was ist das?** Softwareentwicklungsprozesse beschreiben das Vorgehen bei der Entwicklung von Software, um möglichst effizient zum qualitativ ausreichenden Ziel zu kommen.

Kurzlebige Einzelpersonenprojekte (bspw. Skripte) bedürfen keiner gesonderten Methodik. Entwickler:innen können – unter Berücksichtigung der FAIR-Prinzipien und der guten wissenschaftlichen Praxis (Reproduzierbarkeit) –  selbst entscheiden, welche Qualität ein derartiges Projekt haben sollte. Für längerfristige Projekte und solche mit einer größeren Zahl von Stakeholdern (insbesondere auch studentische Arbeiten, die nachgenutzt werden sollen) empfehlen sich agile Methoden, um effektiv die Ziele zu erreichen. Für Großprojekte ist Agilität zu reduzieren und aus dem Pool von vorhandenen validierten Entwicklungsprozessen ein adäquates Vorgehen zu wählen. Ein derartiger Plan kann im Rahmen eines Softwaremanagementplans beim Initiieren eines Forschungsprojekts bereits mit den Stakeholdern verhandelt werden.

Hohe Agilität ist für RSE oft am geeignetsten: Das Ziel und der Lösungsweg der Software werden während der Entwicklung oft erst iterativ exploriert, Forschung und Softwareentwicklung sind daher stark verzahnt. 

                

Kurze Inkremente (sog. „Sprints“) von wenigen Wochen iterieren die Entwicklung, es wird primär am Code und an den gleichzeitig definierten, automatisierten Tests gearbeitet \[Pic08\]. Es gilt Common Code Ownership mittels eines gemeinsamen Repositories, wenig Dokumentations-Overhead, Refactoring-Techniken zum inkrementellen Architekturerhalt, agile Anpassung der Ziele, Planung und Change Management-Unterstützung auf Basis von Tickets. Es gibt dazu mittlerweile sehr gute Werkzeuge (siehe GitLab, GitHub, Unit-Testframeworks, CI/CD).

### 3.4.2. Qualitätsmanagement (Testen, Validierung, etc.)       {#3.4.2.-qualitätsmanagement-(testen,-validierung,-etc.)}

\[SWEBOK: Software Testing | Software Quality\]

**Warum ist das wichtig?** Ohne ausreichende Qualität kann nicht gewährleistet werden, dass Forschungsergebnisse korrekt und reproduzierbar sind (vgl. FAIR-Prinzipien). Außerdem ist die Wiederverwendbarkeit der Software eingeschränkt.

**Was ist das?** Unter Softwarequalität versteht man die Gesamtheit der Merkmale und Merkmalswerte eines Softwareprodukts, die sich auf dessen Eignung beziehen, festgelegte oder vorausgesetzte Erfordernisse zu erfüllen \[Wik24c\]. In der Softwareentwicklung unterscheidet man zwischen Produktqualität und Prozessqualität und definiert zumeist ein Netz von konkreten Qualitätsattributen, wie zum Beispiel Verstehbarkeit des Codes, Codekomplexität, Security, Privacy, Robustheit, Nutzbarkeit sowie natürlich funktionale Korrektheit und Ausführungseffizienz (Performance) \[ISO23\]. 

Teile der Produktqualität sind schwer zu messen. Es besteht  jedoch eine starke Korrelation zur Prozessqualität. Deshalb ist die adäquate Wahl und Ausübung eines Entwicklungsprozesses wichtig.

Je nach Softwarearten (Art), TRLs und  des Levels der Kritikalität (siehe Anhang A) werden passende Qualitätsziele definiert, um daraus Entscheidungen für Architektur, Testformen und deren Automatisierungsgrade, Review-Prozesse, etc. festzulegen. Eine gesonderte Betrachtung ist notwendig für die Qualitätsbewertung einzubindender Fremdsoftware wie z.B. Bibliotheken sowie die Qualitätssicherung in gemeinschaftlichen Entwicklungsprozessen ohne gemeinsame Projektleitung.

### 3.4.3. Anforderungen verstehen   

\[SWEBOK: Software Requirements\]

**Warum ist das wichtig?** Die Anforderungen zu verstehen ist von entscheidender Bedeutung, damit sichergestellt wird, dass ein System die Bedürfnisse und Erwartungen seiner Nutzenden erfüllt. Modernes Requirements Engineering (RE) adressiert die Perspektiven aller Stakeholder, darunter den Entwickelnden, den Nutzenden, den Projekt- bzw. Fördergebern, aber auch relevante rechtliche Vorschriften und wissenschaftliche Anforderungen.

RE hilft, Missverständnisse zwischen Entwicklungsteam und Entscheidenden zu reduzieren und kann sehr agil und effizient ausgeführt werden.

**Was ist das?** Requirements Engineering ist ein strukturierter Prozess mit dem Ziel, die Anforderungen an ein System systematisch zu verstehen und zu verwalten. 

RE beinhaltet funktionale Aspekte (“Was soll die Software können?”) aber auch technische Aspekte (“Welcher Hardware/Software-Stack?”, Performanz-Anforderungen) oder Anforderungen an den Entwicklungsprozess (Programmiersprache, Lizenzen, Werkzeuge) und externe, rechtliche Rahmenbedingungen. 

Neben der Identifikation der Anforderungen ist auch die Priorisierung, das Erkennen von Konflikten in Anforderungen und die Harmonisierung von Anforderungen verschiedener Stakeholder ein wesentliches Grundelement. Im Projektverlauf sind diese Anforderungen effizient zu managen.

Bei RSE ist die Anforderungsermittlung intrinsisch verzahnt mit dem eigentlichen Forschungsprozess. Dies ist in der zu wählenden Entwicklungsmethodik zu reflektieren. Techniken der agilen Entwicklung passen oft gut, weil sie gut mit sich verändernden Anforderungen umgehen können und wenig organisatorischen Overhead produzieren. Nichts führt zu mehr Entwicklungseffizienz als frühzeitiges gutes Verstehen der Anforderungen. Größe von Software und Team sowie die Kritikalität induzieren den nötigen Präzisionsgrad des Anforderungsmanagements.

Ältere Formen des RE basierten auf einem zu dokumentierenden Pflichtenheft. Dies ist in agilen Formen des RE durch kommunikative Workshops und Ticket-Sammlungen ersetzt worden.

### 3.4.4. Softwarearchitektur   		

\[SWEBOK:  Software Design\]

**Warum ist das wichtig?** Die Struktur eines Softwaresystems wird als Architektur bezeichnet. Um eine hohe Effektivität und Effizienz der Softwareentwicklung zu erreichen, ist eine saubere Struktur notwendig. Nur hierdurch sind leichte Änderbarkeit, hohe Produktqualität, Wiederverwendung, parallele Entwicklung durch mehrere Entwickler:innen und die Weiterentwicklung einzelner Komponenten, ohne das gesamte System kennen zu müssen, möglich. Dies erfordert meist klare und minimale Schnittstellen, die neben den zuvor genannten Aspekten zudem die Fehleranfälligkeit reduzieren und zu wesentlich einfacheren Teststrategien führen.

**Was ist das?** Softwarearchitektur bezieht sich auf die grundlegenden Strukturen eines Softwaresystems. Diese Strukturen bestehen aus den Softwarekomponenten und deren Beziehungen untereinander sowie ihren Eigenschaften. Wichtig sind klare und eindeutige Aufgaben einzelner Komponenten sowie minimale und klar definierte Schnittstellen zwischen den Komponenten. Dementsprechend umfasst Softwarearchitektur die Entscheidungen über das Design und die Organisation eines Systems, die das Erfüllen gegebener Anforderungen sicherstellen. Architektur ist damit ein wesentlicher Treiber für Produktqualität. Das Software Engineering bietet Architekturmuster und \-stile, im Sinne  wiederverwendbarer Lösungen für wiederkehrende Probleme \[Som18\]. Wesentliche Hilfsmittel sind die Separierung von Softwarefunktionen in Komponenten mit loser Kopplung, die explizite Festlegung von stabilen Schnittstellen zur ausschließlichen Nutzung durch andere Komponenten und explizite Deprecation-Prozesse zur Entfernung alter Schnittstellen. Dedizierte Erweiterbarkeit wird durch den Einsatz von Erweiterungsmechanismen wie Hot Spots in Frameworks, Template-Hook Design Patterns oder Plugin-Architekturen gefördert. Ein Projekt benötigt normalerweise eine:n weisungsbefugte:n Softwarearchitekt:in. Für Details wird auf entsprechende Literatur \[Mar17, Fow19\] verwiesen. Bei kritischen Systemen wird durch die Separation/Kapselung in unabhängige Komponenten auch ein risikoadaptiertes Qualitätsmanagement möglich.

### 3.4.5. Softwaremodellierung  	

\[SWEBOK: Software Engineering Models and Methods\]

**Warum ist das wichtig?** Komplexe Systeme lassen sich am besten beherrschen, wenn man abstrakte Modelle zu ihrer Beschreibung benutzt. Dies gilt auch für Software. Deshalb ist es sinnvoll, sich für komplexe Datenstrukturen, Abläufe, Interaktionsprotokolle, Zustandsmodelle oder Workflows, entsprechende Modelle anzulegen. 

**Was ist das?** Die Unified Modeling Language (UML) bietet hierfür eine Sammlung von geeigneten Modellierungssprachen. UML-Modelle beschreiben verschiedene Aspekte einer Software und sind deshalb geeignet, um die Architektur, die Datenstrukturen, etc. von Software zu entwerfen, zu verstehen und zu pflegen. Des Weiteren unterstützen sie, die dabei entstehenden Probleme schneller zu erkennen und zu beheben. Der Industriestandard UML besteht aus 14 Modellarten, von denen Klassen- und Workflow-Diagramme am hilfreichsten sind. Modellierungswerkzeuge helfen, Modelle zu erstellen, Modelle aus Code zu extrahieren, oder Code und Testfälle zu generieren. Moderne Low Code/No Code-Methoden und \-Werkzeuge basieren darauf, dass sie explizit formulierte Modelle als Ersatz für langwierige und fehleranfällige Programmiertätigkeiten nutzen.

### 3.4.6. Versionierung {#3.4.6.-versionierung}

**Warum ist das wichtig?** Versionierung ist die Grundlage für Kollaboration, sichere, verlustfreie Verwaltung von Arbeitsständen und fördert die Nachvollziehbarkeit und Reproduzierbarkeit von Forschungsergebnissen. Versionierung erlaubt effizientes Release-Management, Variantenmanagement (d.h. mehrere verschiedene Softwarestände sind im Einsatz) sowie Versionshistorien und bildet damit  eine Grundlage für die Qualitätsanalyse. Ohne Versionierung ist es enorm schwierig, auftretende Fehler systematisch zu beheben.


**Was ist das?** Versionierung von Software bedeutet, dass unterschiedliche Stände einer Software eindeutig bezeichnet werden und jederzeit rekonstruierbar sind. Das sichert Nachvollziehbarkeit sowie auch Vergleichbarkeit von modifizierten Ergebnissen, die gegen ältere Versionen abgeglichen werden können. Später eingebaute Fehler können so identifiziert, betroffene Ergebnisse erkannt und Fehlerursachen behoben werden. Kollaboratives, also gemeinsames Arbeiten am selben Code wird durch projektspezifische Verfahren zur Planung von Releases, temporären Abspaltung von Branches und automatisierbaren Merge-Verfahren wesentlich vereinfacht. Damit erlauben Versionierungssysteme auch das parallele Arbeiten an verschiedenen Softwareversionen. Die Versionierungssysteme machen die Änderungen zwischen Versionen transparent und erlauben so auch die Nachvollziehbarkeit der Versionsunterschiede. Insbesondere im Publikationsprozess ermöglicht die Versionierung eine erweiterte Nachvollziehbarkeit der eigenen Ergebnisse, z.B. bei Wiederholungen von Simulationen während des Review-Prozesses, als auch eine Reproduzierbarkeit durch Außenstehende, sofern die genutzten Versionen auch in der Veröffentlichung dokumentiert sind.   Als Werkzeug zur Versionsverwaltung (vgl. Abschnitt 3.5.1) ist aktuell Git stark verbreitet. Dabei sind öffentliche Dienste wie etwa die von github.com oder gitlab.com von an Universitäten lokal gehosteten Instanzen (z.B. gitlab) zu unterscheiden, die jeweils Vor- und Nachteile beispielsweise bei der Integration in Veröffentlichungswerkzeugen aufweisen. 

### 3.4.7. Testkonzept und \-Automatisierung 	 {#3.4.7.-testkonzept-und--automatisierung}

\[SWEBOK: Software Testing | Software Configuration Management\]

**Warum ist das wichtig?** Während eine Software (weiter-)entwickelt wird, wird die Qualität der Software inklusive der Funktionsfähigkeit der Algorithmen durch Tests überprüft; eine Automatisierung macht diesen Vorgang einfach wiederholbar. Testen ist die primäre Aktivität zur Qualitätssicherung, (a) die Qualität der Software (z.B. Korrektheit, Performanz) nachzuweisen und (b) um ggf. Fehler zu finden. Automatisierte Tests können jederzeit wiederholt werden und so bei Modifikationen der Software die Korrektheit nachhaltig sicherstellen und ggf. neu entstandene Fehler schnell aufzeigen. Werden Tests als Ausgangspunkt der Entwicklung von Softwarekomponenten genommen, spricht man auch von Test-driven Development. 

**Was ist das?** In Tests werden jeweils ausgesuchte Teile der Software bzw. die gesamte Software auf Testszenarien und \-daten angewendet und das erhaltene Ergebnis auf (Software-)Korrektheit, Sicherheit, Robustheit, etc. geprüft. Ein Testkonzept kann skizzieren, welche Tests durchgeführt werden sollen. Die Automatisierung der Tests kann auch die Automatisierung der Ergebnisprüfung beinhalten, womit eine regelmäßige, unbeaufsichtigte Ausführung der Tests möglich wird (zum Beispiel in einer Continuous Integration über Nacht oder bei jedem Commit). Das Vertrauen der Entwickler:innen und Stakeholder in die Softwareentwicklung und \-anpassungen steigt, wenn Tests rigoros durchgeführt werden. Werkzeuge zur automatischen Messung der Testabdeckung helfen abzuschätzen, wie gut die Testqualität tatsächlich sein kann.

Die folgenden Teststufen sind bei Forschungssoftware üblicherweise zu unterscheiden:

* Unit-Tests prüfen unabhängig voneinander einzelne Einheiten des Systems, z.B. einzelne Methoden, Klassen oder Komponenten, sie dienen zur Fehlersuche bzw. zum Nachweis der Abwesenheit von Fehlern.  
* Integrationstests prüfen die Integration der voneinander abhängigen Einheiten, z.B. ob das Zusammenspiel zweier Pakete oder Subsysteme funktioniert wie erwartet.  
* Systemtests (und Usertests) prüfen, ob die Integration aller Einheiten des Systems funktioniert wie erwartet.  
* Akzeptanztests prüfen, ob die (ursprünglichen) Anforderungen an die Software erfüllt sind (sie werden von Endnutzenden durchgeführt und können eine Teilmenge der Systemtests sein)).

Das Testkonzept legt die Grundlage zur Qualitätssicherung und Continuous Integration. Eine Automatisierung der Tests ist unabdingbar, um diese regelmäßig durchzuführen und Testergebnisse unter gleichbleibenden Bedingungen zu reproduzieren. Automatisierte Tests können auch direkt zur Reproduktion der veröffentlichten Forschungsergebnisse aufgesetzt werden.

### 3.4.8. Management der Software-bezogenen Daten und Datengrundlage 	 {#3.4.8.-management-der-software-bezogenen-daten-und-datengrundlage}

\[SWEBOK: Data Persistence | Data Structures | Database Management | Data-Centered Design | Data Safety, Security, Integrity, Protection, and Controls | Data Privacy\]

**Warum ist das wichtig?** Daten sind die operationelle Grundlage jeder Software. Daten werden von Software erzeugt, verarbeitet, laufend ergänzt bzw. ggf. aktuell gehalten und verwaltet. Neben Forschungsdaten sind auch Metadaten, Stammdaten, Transaktionsdaten, Referenzdaten, Strukturdaten und Inventardaten sowie Ablaufprotokolle oder Konfigurationsdaten und viele weitere Datenarten in der Softwareentwicklung relevant. Relevante Daten dürfen nicht verloren gehen und bedürfen daher besonderer Aufmerksamkeit. Für Forschungsdaten wird dies mit den FAIR-Prinzipien \[FAIR20\] nochmal besonders betont \[DFG15\] und ist ein eigenständiges, hier nicht vertieftes Thema. 

**Was ist das?** Je nach Art und Volumen der Daten sowie den primären Verwendungszwecken sind grundlegende Eigenschaften relevant: Korrektheit, Vollständigkeit, Genauigkeit, Konsistenz, Aktualität, Relevanz, Zeitnähe, Auffindbarkeit, Verfügbarkeit, Langlebigkeit, Glaubwürdigkeit, Objektivität, Datensparsamkeit, Datentransparenz, Zugriffssicherheit, und mehr. Abhängig von den Zielen der Software ist eine dafür adäquate Datenqualität zu identifizieren und organisatorische und softwaretechnische Maßnahmen zu ergreifen, um diese Qualitätsziele zu gewährleisten. Dazu stehen verschiedene Speicher-, Backup- und Daten-Finde-Systeme lokal, remote oder in der Cloud zur Verfügung:  Dateisysteme, Datenbanken, Repositories und virtualisierte Speicher der Cloud sowie darauf aufgesetzte Sicherungsmechanismen gegen Datenverluste (z.B. vollständiges und inkrementelles Backup), Konsistenzsicherung (z.B. Transaktionskonzept), eindeutige Kennzeichnung (z.B. UUID) und passende Formen von Metadaten sind im Einsatz. Zum Effizienzgewinn bei der Softwareausführung kommen verschiedene Hilfsstrukturen, wie etwa Caches und Daten-Indizes, auf verschiedenen Ebenen zum Einsatz. Sie alle haben gemeinsam, dass die Ausführungszeit dadurch deutlich reduziert werden kann, aber die Komplexität der nun redundant zu verwaltenden Daten und damit auch der Software steigt. Datenbankmanagementsysteme und Repositories bieten hier gute Unterstützung für jeweils bestimmte Arten von Daten.  
Im Bereich der Forschungsdatenmanagement-Initiativen entsteht speziell für Forschungsdaten eine Reihe von Services und weiterführenden Materialien, die entsprechend genutzt werden können, um auch die förderungspolitischen Aspekte des Datenmanagements zu betrachten. Eine Übersicht findet sich in  
	https://forschungsdaten.info/ 

*\[\[Anmerkung für Leitlinienersteller: eine detaillierte Liste an Services, Materialien, Unterstützungen, die die eigene Forschungseinheit bzw. das Bundesland oder deutschlandweit angeboten wird kann hier oder unter Abschnitt 5.6 eingebracht werden, oder alternativ (und damit dynamischer erweiterbar) auf der RSE-Seite abgelegt werden.\]\]  \[\[Ende Anmerkung\]\]*

### 3.4.9. Best Practices, Design Pattern, Issue-Tracking, Coding Guidelines

\[SWEBOK: Computing Foundation | Software Construction | Software Design | Software Engineering Professional Practice | Software Configuration Management | Software Maintenance\]

**Warum ist das wichtig?** Es gibt eine Vielzahl von kleineren Methoden, Best Practices für verschiedene Aktivitäten der Softwareentwicklung sowie für die Architektur geeignete Entwurfsmuster, Architektur-Pattern, die je nach konkreter Situation zum Einsatz kommen können und deshalb nicht ganz unbekannt sein sollten. 

**Was ist das?** Im Folgenden sind kurze Beispiele aufgezeigt, für Details wird auf entsprechende Literatur \[WAB+14, WBC+17\] bzw. Kurse verwiesen.

* Es gibt eine große Sammlung von Best Practices, die teilweise spezifisch zur verwendeten Software, Programmiersprache oder den genutzten Werkzeugen sind.  
* Eine **Best Practice-Sammlung** anlegen. Dies ist selbst eine Best Practice: In komplexeren Projekten entstehen mit der Zeit eigene Erfahrungsschätze, die zu dokumentieren für nachfolgende Projektmitglieder immer hilfreich ist. Wikis wurden 1995 von Softwaretechnikern genau dafür erfunden.  
* **Software Management Pläne** (SMP) nutzen. Ein SMP hilft, Entwicklungsziele, \-strategien und Strukturen festzulegen, und kann während des Forschungsprojektes zur Evaluation und Festlegen von Meilensteinen dienen und ggf. angepasst werden. Er kann auch als eigenständiges Antragsdokument für eine Projektförderung eingereicht werden. Nach Projektende unterstützt ein SMP mit Informationen bei der langfristigen Erhaltung von Software.  
* **Design Patterns** kodieren Softwarestrukturen, mit denen sich bestimmte Probleme geschickt lösen lassen. Sie erleichtern den Bau  erweiterbarer, konfigurierbarer und adaptierbarer Software und gehören zum Grundwissen der Softwareentwicklung.  
* **Technische Schulden** (“Technical Debt”): Diese Metapher beschreibt den Mehraufwand (Zinsen), der bei der Entwicklung durch noch nicht korrigierte ungünstige Strukturen der Software (Schulden) entsteht. Jede funktionale Ergänzung oder Änderung an der Software hat die Tendenz, die technischen Schulden zu vergrößern.   
* **Refactoring** der Software vereinfacht die Ergänzung weiterer neuer Funktionalität, hält die Architektur gut strukturiert, erhöht das Programmverständnis und reduziert technische Schulden. Es ist deshalb möglichst kontinuierlich durchzuführen.  
* **Kodierungsrichtlinien** (“Coding Conventions”) sind wichtig, denn Software wird wesentlich öfter gelesen als geschrieben. Deshalb ist Software aus der Sicht der Lesenden zu schreiben. Gemeinsame Kodierungsrichtlinien sind die Grundlage kollaborativen Arbeitens und schließen vernünftige Namensgebung, Strukturierungsformen, aber auch Layout mit ein. Es existieren Tools, die automatisiert Konformität mit Teilen der Kodierungsrichtlinien überprüfen oder sogar erzeugen können (Linter, Code Formatter).  
* **Ticket-Verwaltung** ist das allgemeine Verfahren, um sowohl Anforderungen in kleinen, realisierbaren Portionen, als auch Fehlerberichte, sowie Defizite und Probleme aller Art effizient digital zu managen. Explizite Issue-Verwaltung kann dabei genauso eingesetzt werden wie eine vereinfachte, aber Editor-unterstützte Markierung mit “TODO” oder “FIXME”.  
* **Dokumentation** sollte in adäquater Form, also mit Augenmaß und projektabhängig vom intendierten Nachnutzungsgrad der Software entstehen. Inhalte können sowohl reine Entwicklungsdokumentation relevanter Entscheidungen, aber auch Dokumentation zur Installation, zum zulässigen Anwendungsbereich, den Schnittstellen, usw. sein. Auch die Kommentierung von Code ist eine Form der Dokumentation. Es gibt je nach Programmiersprache und Entwicklungsumgebung Werkzeuge, die die Dokumentationserstellung aus Kommentaren automatisieren. Kommentare sollten gut geschriebenen selbsterklärenden Code kompakt ergänzen.  
* **Variantenmanagement** wird dann notwendig, wenn mehrere verschiedene Versionen der Software parallel im Einsatz sind und gegebenenfalls parallel weiterentwickelt, gewartet oder betrieben werden müssen. Das Produkt wird dann zur Produktlinie mit unterschiedlichen Feature-Konfigurationen. Die Softwaretechnik bietet hierfür eigene Techniken.  
* **Glossar** ist ein Teil der Dokumentation, der anfangs erstellt wird und es den verschiedenen, gegebenenfalls heterogenen Gruppen von Entwickler:innen erlaubt, eine gemeinsame Sprachbasis zu entwickeln. Ist die Entwickler:innengruppe außerdem über Wissenschaftsdisziplinen hinweg aufgestellt, bietet sich die Entwicklung einer Ontologie an.   
* **Software- und Hardware-Stack klar verstehen** und reproduzierbar machen. Dazu gehören ggf. der Einsatz von Containern, die Klärung aller Abhängigkeiten zu Laufzeitumgebungen, das Testen der Software auf verschiedenen Betriebssystemen und unter Nutzung verschiedener Compiler-Versionen und \-Varianten/-Flags, und weiteres.

## 3.5. **Technische Grundlagen**

Die in einer Methodik gegebenen Aktivitäten sind oft stark verzahnt mit entsprechenden technischen Werkzeugen, die größere Teile der Aktivität automatisieren und damit wiederholter Anwendung zugänglich machen. Werkzeuge sind wichtige Hilfsmittel zur Effizienzsteigerung. Dazu gehören Editoren, Compiler, Workflow- und Pipeline-Manager mit iterativer, inkrementeller Ausführungslogik, Versionsverwaltung, Refactoring-Tools, Code-Analyse-Tools, Modellbasierte Codegeneratoren, Test-Metriken, etc. Die Wahl der richtigen Tools im Team ist Aufgabe des initialen Projekt-Setups. Hier eine Auswahl:

### 3.5.1. Git Versionsverwaltungssystem  {#3.5.1.-git-versionsverwaltungssystem}

\[\[Anmerkung für Leitlinienersteller: Git ist nicht das einzige Versionsverwaltungssystem, aber z. Z. so dominant und verbreitet, dass sich eine explizite Nennung hier lohnt. Einsatz eines anderen Systems ist natürlich möglich.\]\]

**Warum ist das wichtig?** Git ist ein sehr flexibles und mächtiges Versionsverwaltungssystem. Es ist seit vielen Jahren erfolgreich im Einsatz und ausgereift. Versionsverwaltung ist wie oben erklärt die Grundlage für moderne Softwareentwicklung. 

\[\[Anmerkung für Leitlinienersteller: Variante\]\]

Allen Wissenschaftler:innen und Studierenden steht grundsätzlich unter der \[\[einrichtungszentralen| universitätszentralen| institutionszentralen\]\] Adresse

	\[\[https://gitlab….\]\]

eine Installation der Gitlab-Services zur Verfügung, die für wissenschaftliche Zwecke genutzt werden kann. Weitere Details dazu auch in Kapitel 5\.

\[\[ende Variante\]\]

**Was kann das?** Git kann Versionen verwalten und parallele Entwicklung auch an denselben Dateien unterstützen. Weiterhin ermöglicht Git, Änderungen zwischen Versionen effizient nachzuvollziehen, Branches zu managen und damit Releases, Haupt- und Nebenentwicklung, Experimente, u.ä.m. weitgehend zu automatisieren. Viele Editoren und Programme bieten eine einsteigerfreundliche Integration von Git.

Git-Repositorien werden häufig mit Hilfe von Web-Frontends verwaltet, die zusätzlich effiziente Ticket-Verwaltung, Wikis, Rechteverwaltung und vieles mehr in die Codeverwaltung integrieren. Gitlab und Github sind die bekanntesten Anbieter. Einige der Angebote werden in der Cloud angeboten (z.B. Github), während andere lokal betrieben werden können (z.B. Gitlab). Als besonders hilfreich sind hier die Automatisierungstechniken zur kontinuierlichen Prüfung der Codequalität, der Testausführung und der Integration (Continuous Integration) zu betrachten. Viele Editoren und Programme bieten eine einsteigerfreundliche Integration von Git.

Abgesehen von Git gibt es weitere Versionskontrollsysteme, zum Beispiel Subversion oder Mercurial.

\[\[Optional\]\]

Repositories können im Prinzip auch Forschungsdaten verwalten, sind aber nicht für große Datenmengen aufgestellt. (Passive) Forschungsdaten benötigen normalerweise auch keine Versionierung. Quellcode-Versionen können aber in GitLab- und GitHub-Repositories gemäß Forschungsdatenmanagement-Richtlinien gespeichert werden. Genaueres regeln die \[\[einrichtungszentralen| universitätszentralen| institutionszentralen\]\] Richtlinien \[\[des Forschungsdatenzentrums\]\]. 

\[\[ende Optional\]\]

### 3.5.2. Continuous Integration / Continuous Delivery  {#3.5.2.-continuous-integration-/-continuous-delivery}

**Warum ist das wichtig?** Continuous Integration und Continuous Delivery (CI/CD) sind Praktiken der Softwareentwicklung, bei denen Änderungen am Code regelmäßig automatisiert in einer gemeinsamen Umgebung getestet und in die Produktion überführt werden, um schnell und zuverlässig neue Features und Updates bereitzustellen.

Diese Praktiken sind wichtig, weil sie Entwickelnden ermöglichen, Software schneller, effizienter und mit weniger Risiko für Fehler zu entwickeln und zu veröffentlichen, indem sie den Entwicklungs- und Bereitstellungsprozess automatisieren und optimieren. Sie fördern auch eine kollaborative Arbeitsweise, die die Softwarequalität verbessert und die Zeit bis zur Nutzung in der Forschung verkürzt.

**Was kann das?** Wenn ein:e Entwickler:in eine in sich abgeschlossene möglichst kleine Entwicklungsarbeit mittels des Versionierungssystems in das Produkt übernimmt, wird automatisch der Code kompiliert und die Qualität der Änderungen geprüft, z. B. durch notwendige  Code-Analyse sowie Ausführung von automatisierten Tests (Continuous Integration). Im Erfolgsfall wird die Software als Snapshot zum Download aktualisiert oder z. B. bei webbasierten Systemen direkt für den Nutzer verfügbar gemacht (Continuous Deployment/Delivery). GitLab und GitHub haben diese Ansätze durch sogenannte “Build Pipelines” gut integriert.

### 3.5.3. Test-Frameworks	 {#3.5.3.-test-frameworks}

**Warum ist das wichtig?** Ein Test-Framework unterstützt die effiziente Entwicklung und effektive Ausführung automatisierter Tests. Durch die gute Integration in die jeweilige Programmiersprache ist der Aufwand zur Testfallerstellung deutlich gesunken, sodass direkt parallel zur eigentlichen Entwicklung oder sogar vorher (“Test First” Ansatz, ”Test-Driven Development”) automatisierte Tests als einfache Methoden/Funktionen geschrieben werden können. Speziell für Unit-Tests, Integrationstests bis hin zu System-Tests sind xUnit-Frameworks der entsprechenden Programmiersprachen (JUnit, unittest/pytest, cppunit, etc.) geeignet. Für Akzeptanztests gibt es auch andere Frameworks, die z. B. GUI-User-Interaktionen simulieren (z. B. Selenium).

**Was kann das?** Ein Test-Framework hilft, Tests für Software zu erstellen, auszuführen, Tests in Sammlungen zu organisieren und Testergebnisse zu berichten, wodurch der Prozess der Softwareentwicklung effizienter und effektiver wird.

Ergänzende Test-Werkzeuge erlauben das Aufsetzen von Hilfsstrukturen für Tests, zum Beispiel Mocks für die Emulation von Umgebungskomponenten.

Die Idee von "Testen durch automatisches Ausführen" kann zum Beispiel mit Jupyter Notebooks auf User-Dokumentation und auf (reproduzierbare) Forschungsergebnisse erweitert werden \[BTK+21\]. 

### 3.5.4. Verbreitung / Dissemination	

**Warum ist das wichtig?** Software ist in ausführbare Form gegossenes Wissen und daher genau wie wissenschaftliche Texte und Daten als Artefakte des wissenschaftlichen Prozesses zu publizieren. Das entspricht guter wissenschaftlicher Praxis und in Teilen den Anforderungen der Forschungsförderorganisationen. Open Science und Open Source sind konzeptuell eng verzahnt. 

**Was kann das bewirken?** Erst eine Publikation ermöglicht die Nachnutzung von Forschungssoftware z. B. zur Reproduktion wissenschaftlicher Ergebnisse. Gleichzeitig macht eine Publikation die Softwarefunktionalität bekannt und kann Mehrfachentwicklungen verhindern. Außerdem kann auf entsprechenden Plattformen eine (internationale) Kollaboration zur Weiterentwicklung initiiert werden. Eine Publikation in zitierbarer Form kann zudem die Anerkennung als wissenschaftliches Ergebnis befördern. (Siehe auch Findability in \[BHK+22\].) 

Ein Bibatex-Softwarepaket \[DC20\] unterstützt Forschende, Software als Veröffentlichung zu zitieren. 

**Wie kann man vorgehen?** Es haben sich verschiedene Bereitstellungsformen etabliert, z. B. als Quellcode in git-basierten Repositories wie GitHub oder DOI-fähigen Publikationsplattformen wie Zenodo, als ausführbare Dateien, containerisierte Umgebungen oder in programmiersprachenorientierten Paketmanagementplattformen. Forschungssoftware zur Nachnutzung in anderen Experimenten (Reproduzierbarkeit) zur Verfügung zu stellen, erfordert oft eine umfangreichere Publikation (Quellen, Dokumente, Tickets, etc.) und die Software ist teils komplexer, weil Qualitätskriterien wie Robustheit, Erweiterbarkeit und Anpassbarkeit wichtiger werden. Eine Publikation erfolgt unter Beachtung der in Abschnitt 4 beschriebenen  \[\[einrichtungszentralen | universitätszentralen | institutionszentralen\]\] Lizenz- und Veröffentlichungsrichtlinien.

\[\[Optional: In Abschnitt 5 werden Unterstützungsleistungen der Einrichtung bei der Publikation besprochen.\]\]

### 3.5.5. Software Discovery 	 {#3.5.5.-software-discovery}

**Warum ist das wichtig?** Die Suche nach existierender Software bzw. Funktionalität kann unnötige Mehrfachentwicklung verhindern, alternative Problemlösungen inspirieren und einen Überblick zum Stand der Forschung schaffen. 

**Was kann das bewirken?** Die Nachnutzung gefundener Forschungssoftware kann ressourcenschonender sein, auch wenn diese einer Evaluierung bedarf. 

**Wie kann man vorgehen?** Ähnlich den heterogenen Publikationsplattformen sind auch die Ansätze zur Software Discovery vielfältig und teils vom Forschungsfeld und der Forschungseinrichtung (In House-Nutzung) abhängig. Generische Suchmaschinen und das soziale Forschungsnetzwerk können einen Einstieg darstellen. Einige Disziplinen stellen online Kataloge oder Registries bereit, die Softwareveröffentlichungen an verschiedenen Standorten erschließen (z. B. swMATH.org, ASCL.net) und so einfacher zugänglich machen. In der Literatur vieler Disziplinen werden regelmäßig Reviews bekannter Software veröffentlicht. \[\[Optional: Die Universität | Die Hochschule | Das Forschungszentrum\]\] betreibt \[\[eine Gitlab-Instanz | einen jeweilig verfügbarer Versionsservice\]\], auf \[\[dem | der \]\] öffentliche Projekte zu finden sind.

Verschiedene Standorte, uneinheitliche Metadaten und Terminologien/Ontologien erschweren bisher die Suche. Die Unüberbrückbarkeit von Technologien (verschiedene Programmiersprachen, Bibliotheksversionen, Softwarestacks, etc.) oder Lizenzprobleme stellen manchmal Hindernisse in der Nachnutzbarkeit dar. Schwer zu klären ist die Frage der Qualität und wie weit Software angepasst bzw. erweitert werden kann. Hier helfen eine robuste Architektur, gut eingearbeitete Entwurfsmuster sowie eine ausgeprägte Sammlung an Tests für die Grundfunktionalität oder auch das Vertrauen in die Reputation der bisherigen Entwickler:innen (soweit sie bekannt sind).

Die Beschaffung von Software oder Dienstleistungen wie Wartung sind nicht Teil dieses Dokuments und erfordern ggf. eine Einbindung des Einkaufs \[\[der Universität | der Hochschule | des Forschungszentrums\]\]. 

\[\[Optional: In Abschnitt 5 werden Unterstützungsleistungen bei der Suche nach Software und deren Evaluierung besprochen.\]\]

	

# 4 Lizenz-Vergabe und \-Nutzung (Juristische Absicherung) {#4-lizenz-vergabe-und--nutzung-(juristische-absicherung)}

*\[\[Anmerkung für Leitlinien-Ersteller: Von den Autoren/Autorinnen wird betont, dass diese Informationen keine Rechtsberatung darstellen und nur als Anregung dienen. Die Nutzung erfolgt auf eigene Gefahr und es wird keine Haftung übernommen. Die Informationen haben den Stand des Dokuments und werden nicht notwendigerweise aktualisiert.\]\]* 

→→ Für **Entscheidende** ←← 

Um die effiziente Entwicklung von Forschungssoftware mit hohen Qualitätsstandards zu unterstützen, gestaltet \[\[die Universität | die Hochschule | das Forschungszentrum\]\] den regulatorischen Rahmen aus und stellt \[\[Beratungs-, Unterstützungs- und Weiterbildungsangebote\]\] bereit. Dabei beziehen sich Beratung und Informationen auf alle Phasen des Software-Lebenszyklus, inklusive der Einbindung fremder Software, und die Nachnutzung bzw. Weitergabe der Software. 

Die Leitlinie adressiert oder ersetzt keinerlei Anwendungs- und fachspezifische gesetzliche und untergesetzliche Regelungen, Normen und Richtlinien für die Erstellung von Software. Dementsprechend sind auch alle fachspezifischen weiterführenden Richtlinien und technischen Normen zu beachten, die bei kritischer Software wie z.B. in der Medizintechnik eine besondere Rolle spielen.

Der regulatorische Rahmen ergibt sich u. a. aus der Guten Wissenschaftlichen Praxis \[DFG22\], hier die 

* Leitlinie 7 (“Der Quellcode von öffentlich zugänglicher Software muss persistent, zitierbar und dokumentiert sein”),   
* Leitlinie 12 (“Qualitätssicherung bezieht sich insbesondere auf … die Auswahl und Nutzung von Forschungssoftware, deren Entwicklung und Programmierung”; “Bei der Entwicklung von Forschungssoftware wird der Quellcode dokumentiert.”) und vor allem   
* Leitlinie 13 (“Dazu gehört es auch, soweit dies möglich und zumutbar ist, die den Ergebnissen zugrunde liegenden Forschungsdaten, Materialien und Informationen, die angewandten Methoden sowie die eingesetzte Software verfügbar zu machen und Arbeitsabläufe umfänglich darzulegen. Selbst programmierte Software wird unter Angabe des Quellcodes öffentlich zugänglich gemacht.”). 

Diesen Rahmen füllt \[\[die Universität | die Hochschule | das Forschungszentrum\]\] weiter, um lokalen Anforderungen zu entsprechen und den Wissenschaftler:innen praktikable Regeln zu geben. \[\[Optional: \[\[ Die Universität | Die Hochschule | Das Forschungszentrum \]\] betont, dass diese Informationen keine Rechtsberatung darstellen. \]\] 

Ein Leitgedanke der Ausgestaltung ist dabei die im Dokument schon mehrfach erwähnte Offene Wissenschaft (Open Science).

Die verschiedenen Angebote zum Thema Software werden in ausführlicher Form auf \[\[der RSE-Webseite der Einrichtung (zum Beispiel https://research-se.X-university.de)\]\] dokumentiert und regelmäßig aktualisiert. Diese Informationen werden zentral und gemäß aller geltenden Richtlinien abgestimmt und inhaltlich primär von Expert:innen für Softwareentwicklung gestaltet, sodass eine pragmatische und schnelle Entscheidungsfindung vorgenommen werden kann.

	\[\[https://research-se.X-university.de\]\]

Forschungssoftware, die von mehreren Personen genutzt und gegebenenfalls gemeinsam entwickelt und weiterentwickelt werden soll, bedarf einer Definition adäquater Lizenzen. Eine solche Lizenz muss verschiedene unten genannte Einflussfaktoren reflektieren. Lizenzen sind Regelwerke, die definieren, wie Software, die unter diesen Lizenzen veröffentlicht wird, verwendet, modifiziert und geteilt werden kann.

Die rechtlichen und organisatorischen Rahmenbedingungen \[\[ der Universität | der Hochschule | des Forschungszentrums \]\] werden anhand dieses Dokuments in Form von Leitlinien fixiert. Darüber hinaus werden konkrete Entscheidungshilfen und Best Practice Beispiele gegeben. 

### 

## **4.1.	Wissenschaftliche Verwertung und Lizenzwahl \-- Allgemeines** {#4.1.-wissenschaftliche-verwertung-und-lizenzwahl----allgemeines}

\[\[Die Universität | Die Hochschule | Das Forschungszentrum\]\] unterstützt und befürwortet die Veröffentlichung von Software als Open Source Software, um so zu einer Stärkung von „Open Science“ beizutragen und dadurch einen effektiveren und offeneren Informationsaustausch innerhalb der Wissenschaft zu ermöglichen und den Transfer der Ergebnisse in die Gesellschaft zu fördern. Dabei kann auch eine freie Verwertung durch wirtschaftliche Unternehmen, die Verwaltung, und Andere sinnvoll sein.

\[\[Die Universität | Die Hochschule | Das Forschungszentrum\]\] empfiehlt \[\[permissive Lizenzen | Copyleft Lizenzen | eine Reihe von durch die Open Source Initiative anerkannten Lizenzen \[OSI22\] | die durch die Open Source Initiative anerkannten Lizenzen \[OSI22\] | NAMENSNENNUNG\]\], aus denen präferiert nach den Anforderungen des Projekts ausgewählt wird. Die Nutzung dieser wird empfohlen, außer es hat sich in der (wissenschaftlichen disziplinären) Ziel-Community bereits eine bestimmte Lizenz etabliert. In diesem Fall sollte diese nach Möglichkeit übernommen werden. Der/Die Wissenschaftler:in / Research Software Engineer muss im Einzelfall die Lizenzentscheidung mit der entsprechenden berechtigten Stelle abstimmen (bzw. mitteilen) und dies dokumentieren.

\[\[Optional: In den Fällen, in denen eine kommerzielle Verwertung der Software möglich und eine solche wirtschaftliche Verwertung im wissenschaftlichen und sonstigen Interesse der Softwareentwickler:innen und des Instituts liegt, empfiehlt \[\[die Universität | die Hochschule | das Forschungszentrum\]\] eine kommerzielle Verwertung. Sie gibt dabei den Weg der wirtschaftlichen Verwertung vor und hat die Aufteilung der Erlöse geregelt.

Durch ein Dual-Licensing-System (also die Vergabe zweier (oder mehr) verschiedener Lizenzen an Nutzergruppen) können die freie wissenschaftliche Verwendung und die kommerzialisierte wirtschaftliche Verwertung parallel existierende Bausteine einer abgestimmten Verwertungsstrategie für eine Software sein und damit die Interessen der Software-Entwickler:innen und des Instituts für die Erstellung und Weitergabe von Software bestmöglich wahren. \]\]

Die Lizenzart ist idealerweise frühzeitig in der Softwareentwicklung und durch die entsprechend berechtige Stelle der Institution in Abstimmung zwischen Software-Entwickler:innen und Projektverantwortlichen festzulegen. Einflussfaktoren, die teils feste Vorgaben, teils individuell zu gewichten sind, sind oft eine Kombination aus:

* \[\[der  Universität | der Hochschule | des Forschungszentrums\]\] bzw. der Inhaber der Verwertungsrechte,  
* mögliche Verwertungsrechte Dritter von bestehender Software,  
* kooperierende Projektpartner bzw. Konsortialverträge,   
* der rechtliche Rahmen, i.W. Projektanträge und Vorgaben des Fördermittelgebers,   
* Lizenzbedingungen von eingebundener Software,  
* die zusicherbare Qualität der Software,  
* der Technology-Readiness-Level (TRL),  
* die intendierte Nutzer:innen-Zielgruppe (kommerziell vs. wissenschaftlich, einzelne Lizenzvergaben bzw. generell, öffentlich als Infrastruktur verfügbar),  
* die langfristig intendierte Form der Weiterentwicklung und Pflege und die daran Beteiligten,  
* die Art und Weise der Weitergabe (technische Verfügbarkeit). 

Nur wenn \[\[die Universität | die Hochschule | das Forschungszentrum\]\] bzw. die eigenen Einheiten alle notwendigen Nutzungs- und Verwertungsrechte an der Software besitzen, kann diese unter Beachtung ggf. vorbestehender Lizenzbedingungen weitergegeben werden. Bei gemeinsam entwickelten Werken ist eine Weitergabe zum Beispiel im Konsortialvertrag bzw. mit Projektpartnern abzustimmen. 

Die Wahl der Lizenz obliegt dabei der Inhabenden der Verwertungsrechte. Je nach Vertragsverhältnis ist dies \[\[die Universität | die Hochschule | das Forschungszentrum\]\] oder die Urheber:innen z.B. im Falle eines verbeamteten Hochschullehrenden \[BMBF23\]. Das Recht der Lizenzwahl und der Veröffentlichung kann bei Bedarf an die Projektverantwortlichen, Führungskräfte und Software-Entwickler:innen delegiert werden. Bei Fragen und Unklarheiten zur Weitergabe von Software oder zur Lizenzwahl können sich Software-Entwickler:innen und Projektbeteiligte an die auf \[\[der RSE-Webseite\]\] genannten Ansprechpersonen \[\[der Universität | der Hochschule | des Forschungszentrums\]\] wenden, um gemeinsam die jeweilige Situation zu analysieren und die bestmögliche Lösung zu finden.

Sowohl bei Softwareabhängigkeiten als auch bei mehreren Parteien, die existierende Software in eine Zusammenarbeit einbringen, ist es notwendig, auf die Kompatibilität der Lizenzen zu achten. Wenn möglich, sollten deswegen gleiche Lizenzen gewählt werden. Wird Software in Kooperationsprojekte eingebracht, ist diese entweder allgemeingültig oder projektspezifisch vor der Weitergabe an Partner mit einer Lizenz zu versehen, da Software auch in Kooperationen nicht ohne Einräumung expliziter Nutzungsrechte genutzt werden darf.

Regelungen zu Verwertungsrechten der Beitragenden an der Software in Kooperationsprojekten können in einem Contributor License Agreement (CLA) festgelegt werden; bzw. (eher in Sonderfällen) einer Vereinbarung zur Übertragung von ausschließlichen Verwertungsrechten in einem Copyright Assignment Agreement (CAA). Dies ermöglicht den Einbringenden von Software in Kooperationsprojekte die gesamten Verwertungsrechte auch im Fall von Beiträgen Dritter beizubehalten, um eine spätere Umlizensierung zu vereinfachen. Solche Regelungen haben jedoch eine abschreckende Wirkung auf Beitragende, da eine Umlizenzierung ggf. nicht in ihrem Interesse ist. Weiterhin bringt das Eingehen solcher Vereinbarung verwaltungstechnischen Aufwand mit sich.

## **4.2. Anmerkungen zur wirtschaftlichen Verwertung** {#4.2.-anmerkungen-zur-wirtschaftlichen-verwertung}

Bei der Wahl der Lizenzierung und vor allem der Restriktionen sollten mehrere Einflussfaktoren beachtet werden:

1. Die Erlöse aus der Verwertung können der Finanzierung der eigenen Forschung dienen.  
2. Eine wirtschaftliche Verwertung in Zusammenarbeit mit der Industrie fördert den Transfer von Forschungsergebnissen in die Praxis.  
3. Eine wirtschaftliche Verwertung von Software bringt so gut wie immer eine Gewährleistungspflicht mit sich, die wissenschaftliche Einrichtungen regelmäßig nicht erbringen können oder wollen.   
4. Eine proprietäre Lizenzierung kann die praktische Reproduzierbarkeit von wissenschaftlichen Ergebnissen unter Benutzung dieser Software durch andere erschweren.  
5. Eine reine kommerzielle Lizenzierung diskriminiert Wissenschaffende mit weniger finanziellen Mitteln, z.B. in verschiedenen Teilen der Welt.

Einer der heute üblichen und durchaus empfohlenen Vermarktungswege für Software im kommerziellen Bereich ist es, die Software kostenlos allgemein zur Verfügung zu stellen, um so einen Nutzendenstamm aufzubauen und damit die Software erst auszuhärten, abzusichern und ggf. dabei zu verallgemeinern. Ein Startup kann dann auch Ergänzungen, Weiterentwicklungen oder Support kommerzialisieren, ohne die Kernsoftware selbst vermarkten oder besitzen zu müssen. 

Software funktioniert in der Kommerzialisierung anders als viele andere Produkte. Im Bereich von Software-Startups gilt ein massiver und globaler Verdrängungswettbewerb, weshalb “Größe vor Revenue” steht und oft in größeren Ausmaß Investoren nötig sind, um die Software als robustes Produkt verfügbar zu machen, die über die ersten Jahre hinweg keine Erträge erwarten. Dies ist in Deutschland leider aktuell nicht sehr ausgeprägt, und für den beschränkten Markt wissenschaftlicher Software noch komplexer, weshalb empfohlen wird, Impact direkt über Open-Source-Lizenzen zu generieren und allenfalls eine duale Lizenzierung (siehe 4.3.4) oder den Open Core Ansatz für ein Startup zu nutzen. Revenue wird von Seiten \[\[der Universität | der Hochschule | des Forschungszentrums\]\] in so einem Fall nicht erwartet.

### 

## **4.3 Lizenz-Arten** {#4.3-lizenz-arten}

Es werden freizügige (permissive) Open Source Lizenzen, Copyleft Open Source Lizenzen sowie proprietäre Lizenzen und ihre Auswirkungen auf die Verwendbarkeit von Software skizziert. Die Creative Commons Lizenzen sind nicht für Software geeignet und werden daher nicht behandelt. \[CC24\]

### 4.3.1 Open Source Lizenzen {#4.3.1-open-source-lizenzen}

Open Source Lizenzen haben als Ziel, den Quellcode zugänglich zu machen und die Zusammenarbeit zwischen Entwickler:innen zu fördern. Hier sind einige Kernpunkte, welche Open Source Lizenzen abdecken \[OSI06\]:

1. **Zugänglichkeit des Quellcodes**: Der Quellcode muss für die Öffentlichkeit oder mindestens allen Nutzenden zugänglich sein, sodass jede:r ihn einsehen, verwenden und verändern kann.  
2. **Modifikationen:** Nutzende dürfen den Code modifizieren und diese Modifikationen weitergeben. Die Bedingungen dafür können je nach Lizenz variieren.  
3. **Weitergabe:** Nutzende können die Software frei verbreiten. Einige Lizenzen verlangen, dass veränderter Quellcode unter einer kompatiblen Lizenz weitergegeben wird (Copyleft), während andere dies nicht erfordern.  
4. **Nutzung:** Die Lizenz darf die Freiheit zur Nutzung der Software nicht einschränken, selbst wenn sie kommerziell genutzt wird.  
5. **Nutzungsgebühren:** Der Zugang zu Open Source Software kann kostenlos oder kostenpflichtig sein. 

Wichtig ist, zwischen permissiven und Copyleft Open Source Lizenzen zu unterscheiden. Copyleft-Lizenzen (z.B. GPL, LGPL) stellen sicher, dass Derivate unter den gleichen Rahmenbedingungen verfügbar sind wie der Code, von dem sie abgeleitet sind. Permissive Lizenzen (z.B. Apache 2.0, MIT und BSD 4/3/2-Clause) erlauben eine allgemeine Nachnutzung und können als Grundlage von Closed-Source-Produkten verwendet werden. 

In der Praxis hat sich gezeigt, dass unternehmensnahe Softwareentwicklung oft vor der Einbindung von Software unter Lizenzen mit der Verpflichtung, die Weiterentwicklung unter eine kompatible Lizenz zu stellen (Copyleft, z.B. GPL), zurückschreckt (bspw. begründet durch erschwerte kommerzielle Nachnutzung). 

Die am weitesten verbreiteten Lizenzen werden in diesem Kapitel kurz vorgestellt. Die Nutzung dieser Lizenzen wird empfohlen, da sie sich aufgrund ihrer wesentlichen Eigenschaften als meistgenutzte Lizenzen durchgesetzt haben und Entwickler:innen am ehesten bekannt sind, diese somit ein Verständnis der Pflichten und Rechte haben. 

Ist es im Projekt wichtig, dass möglichst viele Partner unkompliziert und schnell Code in ihren Projekten verwenden können und/oder dass Partner bzw. Dritte auf der Software aufbauende Derivate proprietär verbreiten dürfen, dann spricht vieles für eine Lizenz mit allen Rechten, aber möglichst wenig Pflichten (permissiv). Ist es gewollt oder sogar wichtig, dass Weiterentwicklungen stets Open Source bleiben, ist oft eine Copyleft-Lizenz die richtige Wahl. Die wichtigsten Kategorien sind hier anhand von Fragen dargestellt:

1. Wie wird die Software weitergegeben (Source Code oder nur ausführbare Binärdateien)?  
2. Wer darf die Software nutzen? Wer darf die Software weiterentwickeln?  
3. Müssen Veröffentlichungen von Weiterentwicklungen die gleiche Lizenz benutzen?  
4. Wie ist die Nutzung zu dokumentieren (Veröffentlichung zitieren, Lizenz nennen)?

Auf der oben genannten RSE-Webseite sind Lizenztexte und aktuelle Informationen zu den empfohlenen Open Source Lizenzen sowie Tools für Kompatibilitätschecks verlinkt. 

\[\[Variante A1\]\]   
Es wird dringend davon abgeraten, neue Lizenzen zu definieren oder von vorhandenen Lizenztexten ohne wichtigen Grund abzuweichen. Angepasste Lizenztexte dürfen den Namen der Standardlizenz nicht mehr verwenden. Die Verwendung einer neuen Lizenz führt leicht zu Inkompatibilitäten mit den Lizenzen anderer Software, Reputationsverlust durch "noch eine neue Lizenz" oder Hürden, weil neue Lizenzen von potentiellen Nutzenden erst noch geprüft werden müssen.  
\[\[Variante A2\]\]   
Neue Lizenzen oder Lizenzänderungen müssen mit der Rechtsabteilung bzw. dem Justiziariat abgesprochen werden.  
\[\[Ende Varianten A\]\]

### 4.3.2 Permissive Open Source Lizenzen {#4.3.2-permissive-open-source-lizenzen}

Apache 2.0, MIT und BSD Lizenzen sind drei der beliebtesten permissiven Open Source Lizenzen, die leicht unterschiedliche Anforderungen und Freiheiten bieten. Sie alle erlauben die Integration und Nutzung des Codes in proprietären Projekten. Hier ist ein detaillierterer Überblick über jede dieser Lizenzen:

**BSD 2-Clause License**

Es gibt verschiedene Varianten der BSD-Lizenz, die unterschiedlich viele Klauseln enthalten:

* **BSD 2-Clause License** (FreeBSD/Simplified): Diese Version erlaubt nahezu jede Nutzung, solange der Lizenztext und der Urheberrechtshinweis erhalten bleiben.  
* **BSD 3-Clause License** (Modified/New BSD): Diese Version ist ähnlich zur 2-Klausel-Version, jedoch mit einer zusätzlichen Klausel, die verbietet, den Namen des Urhebers oder der Organisation für Werbezwecke ohne vorherige schriftliche Genehmigung zu verwenden.

**MIT License**

Diese Lizenz erfordert lediglich, dass der Lizenztext in allen Kopien oder substantiellen Teilen der Software enthalten ist. Wesentliche Merkmale der MIT-Lizenz sind:

* **Einfachheit und Breite:** Sie hat sehr wenige Einschränkungen, was sie zu einer der freizügigsten verfügbaren Lizenzen macht.

**Apache License 2.0**  

Die Apache License 2.0 wird von der Apache Software Foundation verwaltet. Wesentliche Merkmale der Apache-Lizenz sind:

* **Patentschutz:** Sie gewährt explizit automatisch Patentlizenzen von den Beitragenden an die Nutzenden.  
* **Schutz vor Markenansprüchen:** Sie verbietet Nutzenden die Verwendung markengeschützter Aspekte zu Werbezwecken.   
* **Zustandsänderungen:** Änderungen am Code müssen in modifizierten Dateien dokumentiert werden.

Weitere Merkmale umfassen die Beibehaltung von Attributions- und Rechtsvermerken zur lizenzierten Software, Weitergabe von "NOTICE" Textdateien bei der Distribution; Änderungen der Software dürfen explizit unter anderen Lizenzbedingungen verbreitet werden, solange die Bedingungen der Apache Lizenz 2.0 für die unter dieser lizenzierten ursprünglichen Softwarekomponenten erfüllt werden.

Diese Lizenzen sind alle sehr darauf ausgerichtet, den Code leicht nutzbar und anpassbar zu machen, wobei sie unterschiedliche Grade an Schutz und Anforderungen bieten, um den Bedürfnissen verschiedener Entwickler und Organisationen gerecht zu werden. In diesem Sinne wird auch davon gesprochen, dass permissive Lizenzen versuchen, die Freiheit der Entwickelnden (im Gegensatz zu denen der Nutzenden; siehe Copyleft) so wenig wie möglich einzuschränken.

### 4.3.3 	Copyleft Open Source Lizenzen (Best Practice Beispiele) {#4.3.3-copyleft-open-source-lizenzen-(best-practice-beispiele)}

Die GNU General Public License (GPL), die GNU Lesser General Public License (LGPL) und die GNU Affero General Public License (AGPL) sind drei verwandte, aber unterschiedlich ausgerichtete Lizenzen, die von der Free Software Foundation veröffentlicht wurden \[FSF19\]. Jede dieser Lizenzen vergibt ähnliche Rechte wie die der permissive Lizenzen, stellt aber spezifische Bedingungen, die darauf abzielen, die Freiheiten der Benutzenden zu schützen, also um sicherzustellen, dass der Code und seine Derivate frei zugänglich bleiben. Die Lizenzen reflektieren unterschiedliche Grade von Freiheit und Schutz im Open Source Bereich und wurden entwickelt, um den Bedürfnissen verschiedener Entwicklungsmodelle gerecht zu werden, von einzelnen Bibliotheken bis hin zu vollständigen Anwendungen, die auf Servern oder in der Cloud laufen. Hier ist eine Erläuterung jeder dieser drei Lizenzen:

**GNU General Public License (GPL) Version 3**

Die GPL v3 ist eine Copyleft-Lizenz, die es \- wie alle Open Source Lizenzen \-  allen erlaubt, die Software zu verwenden, zu studieren, zu teilen (kopieren) und zu modifizieren. Wird ein abgeleitetes Werk weitergegeben, muss dies unter derselben Lizenz geschehen, wodurch der Quellcode und seine Änderungen zugänglich bleiben. Wesentliche Merkmale der GPL v3 sind:

* **Starker Copyleft:** Alle modifizierten Versionen der Software sowie Software, welche diese einbindet, müssen im Falle der Weitergabe ebenfalls unter der GPL lizenziert werden.  
* **Schutz vor Tivoisierung**: Die Lizenz verbietet, dass Maßnahmen ergriffen werden, so dass modifizierte Versionen nicht genutzt werden können (zum Beispiel bei Hardware, die das Ausführen modifizierter Versionen verhindert).  
* **Patentrechte**: Die GPL v3.0 gewährt explizit Patentlizenzen von den Beitragenden an alle Nutzer der Software, was Patentklagen verhindert.

**GNU Lesser General Public License (LGPL)**

Die LGPL ist eine weniger strenge Version der GPL v3.0, die speziell für Softwarebibliotheken entwickelt wurde. Während GPL-lizenzierte Software verlangt, dass im Falle der Weitergabe jedes abgeleitete Gesamtwerk unter der GPL lizenziert wird, erlaubt die LGPL, dass die Bibliotheken in nicht-freien Programmen verwendet werden können, solange Änderungen an der LGPL-Komponente selbst unter der LGPL bleiben. Wesentliche Merkmale der LGPL sind:

* **Schwaches Copyleft**: Nur die LGPL-Komponente selbst muss bei Modifikationen unter der LGPL bleiben; das Gesamtprogramm kann unter einer anderen Lizenz stehen.  
* **Förderung der Nutzung**: Sie ermöglicht die Nutzung von Open Source Bibliotheken in sonst proprietären, nicht-freien Softwareprojekten.

**GNU Affero General Public License (AGPL)**

Die AGPL ist der GPL sehr ähnlich, fügt jedoch eine wichtige Klausel hinzu, die speziell für Software gedacht ist, die über ein Netzwerk ausgeführt wird, wie Webanwendungen oder Cloudservices. Wesentliche Merkmale der AGPL sind:

* **Netzwerkklausel**: Jede modifizierte Version der Software, die über ein Netzwerk an andere Benutzer bereitgestellt wird, muss ihren Quellcode unter der AGPL verfügbar machen. Das schließt Software ein, die auf einem Server läuft und Nutzenden über das Internet zugänglich gemacht wird.  
* **Schutz der Nutzerfreiheit**: Diese Lizenz soll sicherstellen, dass Benutzer:innen von netzwerkbasierten Anwendungen die gleichen Freiheiten erhalten, die sie hätten, wenn sie die Software direkt auf ihren eigenen Computern ausführen würden.

#### 

### 4.3.4 	Proprietäre Lizenzen {#4.3.4-proprietäre-lizenzen}

Wird eine stärker individuell ausgestaltete Lizenz angestrebt, weil z. B. die Weitergabe des Codes bzw. die Art der Verwendung der Software eingeschränkt werden soll, empfiehlt \[\[die Universität | die Hochschule | das Forschungszentrum\]\] dafür entweder nur eine einzige proprietäre Lizenz zu verwenden oder im Dual-Licensing eine solche neben einer Open Source Lizenz anzubieten. 

Eine **Proprietäre Lizenz** ist eine individuell definierte Regelung, die alle aktuellen und zukünftig möglichen Nutzungsformen sowie Weitergaben, Konfigurations- und Entwicklungsoptionen adressiert. Sie beschreibt i.A. auch individuelle Pflichten der Gewährleistung, der Nachbesserung und der Aktualisierung durch neue Softwareversionen.

Möglich sind dabei auch Kombinationen (Dual License), die z.B. der Forschung und Lehre eine Open Source Lizenz mit Copyleft zur Verfügung stellen und für eine kommerzielle Nutzung kostenpflichtige Vertragsmodelle definieren. Solche Dual License Modelle können im Bedarfsfall auch ergänzend gebildet werden, nachdem zunächst eine Open Source Lizenz gewählt wurde und später doch der Wunsch nach einer Kommerzialisierbarkeit auftritt. Für eine Umlizenzierung müssen aber alle Entwickelnden, die zu der Software beigetragen haben, zustimmen, soweit kein CLA oder CAA vorliegt.  
Bei der Nutzung von Software unter einer Dual License ist jedoch Vorsicht geboten. Wenn Forschungsprojekte kommerziellen Charakter annehmen, können ggf. Lizenzgebühren anfallen.

Die Erstellung und Verhandlung jeglicher Lizenzverträge, die eine proprietäre Nutzung einräumen, werden \[\[an der Universität | an der Hochschule | am Forschungszentrum\]\] federführend von \[\[Unternehmensentwicklung | Juristische Abteilung | Drittmittelabteilung | Transferabteilung \]\] verantwortet. Ist eine proprietäre Lizenzierung gewünscht, wird gemeinsam mit \[\[dem Institut | der Forschungseinrichtung\]\] über mögliche Lizenzkonditionen, vertragliche Rahmenbedingungen, die Situation geistigen Eigentums usw. beraten und ein entsprechender Lizenzvertrag aufgesetzt. \[\[Das Institut | die Forschungseinrichtung\]\]  kann dabei einen Vorschlag erstellen oder eine Vorlage nutzen.

## **4.4. Beratungsangebote und Vorgehensweise zur Auswahl** {#4.4.-beratungsangebote-und-vorgehensweise-zur-auswahl}

\[\[Optional A: wenn Beratungsunterstützung zur Verfügung steht\]\]

Bei Fragen und Unklarheiten im Umgang mit selbst entwickelter Software kann ein persönliches Beratungsgespräch mit den Ansprechpersonen vereinbart werden, deren aktuelle Kontaktdaten auf der oben genannten RSE-Webseite zu finden sind. In den Beratungsgesprächen werden dabei Fragen geklärt z.B. welche Wirkung die Software entfalten soll, welcher Transfer- oder Publikationsweg geeignet ist (z. B. Open Source Software oder proprietäre Software) und welche (Urheber-)rechtlichen Rahmenbedingungen gegeben sind beziehungsweise berücksichtigt werden müssen. Bei einer gewünschten proprietären Lizenzierung der Software werden in einem diesbezüglichen Beratungsgespräch die Rahmenbedingungen geklärt und anschließend ein geeigneter Lizenzvertrag erarbeitet. Bei einer gewünschten Open Source Lizenzierung wird eine passende Lizenz ausgewählt und deren Umsetzungsbedingungen erläutert.

Wenn notwendig, stehen vertragliche Regelungen für eine zu vereinbarende proprietäre Lizenz zur Verfügung, die von \[\[zuständige Stelle hier eintragen\]\] erfragt werden kann.  
\[\[Ende der Option A\]\]

\[\[Alternative B1: es wurden Vorbilder gezeigt (Best Practices); und es besteht Wahlfreiheit durch die Wissenschaftler:innen   (“Humboldt-Uni-Option” [https://www.cms.hu-berlin.de/de/dl/dataman/teilen/rechtliche-aspekte/lizenzen](https://www.cms.hu-berlin.de/de/dl/dataman/teilen/rechtliche-aspekte/lizenzen) )\]\]

Jede:r Wissenschaftler:in kann die Lizenz für entwickelte Forschungssoftware frei wählen  und diese unverändert übernehmen, solange keine Rechte Dritter an der Software verletzt werden. Die Verwendung einer \[\[Optional: permissiven | Copyleft | (leer)\] / NAMEN / Liste von durch die Open Source Initiative anerkannten Lizenzen | Open Source Initiative anerkannten\] Open Source Lizenz wird explizit empfohlen. Eine Vorgehensweise ist es, sich aus den in dieser Leitlinie genannten Lizenzen eine passende auszusuchen und diese zu verwenden (siehe 4.1).

Weitere Optionen, Best Practices und Fragen auf  zu häufig gestellten Fragen bietet \[\[die Universität | die Hochschule | das Forschungszentrum\]\] auf der oben genannten RSE-Webseite.

\[\[Alternative B2: Absprache mit Abteilung zur Forschungsverwertung (“Mainz-Option”)\]\]

Eine Software kann unter einer Open Source Lizenz veröffentlicht werden, wenn (1) keine Rechte Dritter verletzt werden, (2) eine Zustimmung seitens aller Verwertungsrechteinhabenden vorliegt. Dies kann je nach Vertragsverhältnis die \[\[ Universität | Hochschule | Forschungszentrum\]\] oder der/die Urheber:innen sein. Sowie (3) eventuelle Drittmittelgeber einer solchen Veröffentlichung zustimmen.  
\[\[Ende der Alternativen B\]\]

Bei der gemeinsamen Softwareentwicklung in großen Communities, deren Parteien existierende Software in die Zusammenarbeit einbringen, sollten sich alle Parteien absprechen um eine gemeinsame Lizenz zu bestimmen. Die hauseigene Rechtsabteilung wird hier bei Bedarf unterstützen. 

## **4.5. 	Nutzung von Software Dritter** {#4.5.-nutzung-von-software-dritter}

Wenn in der entwickelten Software Komponenten oder Codestücke enthalten sind, die durch Dritte geschrieben wurden, sind diese urheberrechtlich geschützt und werden in den meisten Fällen bereits eine Lizenz haben. Ist keine Lizenz vergeben, so werden auch keine Rechte eingeräumt. Die Komponente bzw. der Code darf daher nicht genutzt werden. Es besteht die Gefahr, dass der Rechteinhaber Schadensersatz gegen den Nutzer von nicht lizenzierter Software geltend macht.

### 4.5.1. Rechte und Pflichten durch Lizenzen {#4.5.1.-rechte-und-pflichten-durch-lizenzen}

Wie jeder Vertrag regeln Lizenzen Rechte und Pflichten, welche für gängige Open Source Lizenzen in 4.3 beispielhaft beschrieben sind. Es ist wichtig, neben der erlaubten Nutzung auch immer die Pflichten im Auge zu behalten und einzuhalten.

Bei Nicht-Einhalten der Pflichten handelt es sich nicht nur um die Verletzung der guten wissenschaftlichen Praxis, sondern um einen Lizenzverstoß. Die Nutzungsrechte entfallen und der Lizenzinhaber kann zivilrechtliche Schritte einleiten (Schadensersatz). Eine gerichtliche Verfolgung ist bisher nur bei Lizenzverstößen von kommerziellen Verwertern bekannt. Allgemein üblich ist die Bitte um Behebung des Lizenzverstoßes.

Bei Open Source Lizenzen greifen die Pflichten erst bei der Weitergabe von Software (dazu zählt ggf. auch die Bereitstellung als Service). Der “Use” erlaubt die bestimmungsgemäße Nutzung der Software (Ablaufenlassen), ohne dass daran bereits Lizenzpflichten anknüpfen. \[\[Universitäten | Hochschulen | Forschungszentren\]\] sind normalerweise als juristische Person in Gesamtheit dazu berechtigt, so dass eine Weitergabe zwischen den Abteilungen erlaubt ist. 

Trotzdem sollte die Lizenz bereits zum Zeitpunkt der Entscheidung des Einbaus von Software Dritter berücksichtigt werden, da diese die Möglichkeit zur Weitergabe der Software beeinflusst. 

### 4.5.2. Kompatibilität von Lizenzen {#4.5.2.-kompatibilität-von-lizenzen}

Bei der Nutzung von Softwarekomponenten mit unterschiedlicher Lizenz muss auf die Kompatibilität aller Lizenzen geachtet werden. Spätestens im Fall der Weitergabe oder Veröffentlichung kann es hier zu konkurrierenden Pflichten kommen. Vereinfacht lässt sich sagen: Es kann die Schnittmenge aller Rechte genutzt und es muss die Summe aller Pflichten eingehalten werden. So entbindet z.B. die Kombination von Komponenten unter permissiver und starkem Copyleft nicht davon, dass das gesamte Resultat unter starkem Copyleft veröffentlicht werden muss. Ebenso verhindert eine einzige Komponente, die eine Veröffentlichung ihres Quellcodes nicht erlaubt, die Veröffentlichung des Quellcodes als Gesamtpaket.

Eine genaue Prüfung ist in jedem Falle notwendig, da selbst Open Source Lizenzen miteinander inkompatibel sein können. Dies betrifft permissive sowie Copyleft und proprietäre Lizenzen, wobei Copyleft und proprietäre häufiger zu Inkompatibilitäten bzw. Einschränkungen bzgl. der Lizenzwahl führen können. Unterstützen können hierbei Kompatibilitätstabellen (wie z. B.  \[Wik24\]) oder auch Tools für Kompatibilitätschecks, wie sie auf der RSE-Webseite zu finden sind.  

Im Zweifelsfall empfiehlt sich eine Beratung durch die auf der RSE-Webseite \[\[der Universität | Hochschule | des Forschungszentrums\]\] genannten Ansprechpartner.

# 5\. Unterstützungsleistungen durch \[\[die Universität | Hochschule | das Forschungszentrum | Einrichtung\]\]  {#5.-unterstützungsleistungen-durch-[[die-universität-|-hochschule-|-das-forschungszentrum-|-einrichtung]]}

→→ Für **Entscheidende** ←← 

Software ist ein zentraler Bestandteil der akademischen Forschung. Sie wird innerhalb \[\[der Universität | Hochschule | des Forschungszentrums \]\] in der Regel durch \[\[ Institute | Lehrstühle | Forschungseinrichtungen \]\] verantwortet. \[\[Die Universität | Die Hochschule | Das Forschungszentrum \]\] nimmt im Rahmen  der Entwicklung von Forschungssoftware die essentielle Rolle ein, Strukturen und Angebote zu schaffen, die die Entwicklung unterstützen. 

Je nach Software-Stadium (s. Kap. 3\) erfordert gute Forschungssoftware und deren Konzeption bzw. Management unterschiedliche Unterstützungsleistungen, die im Folgenden unterteilt werden in

* Erstellung und Erweiterung von Forschungssoftware,  
* Wartung und Pflege von Forschungssoftware,  
* Weiterbildung der in Forschungssoftware involvierten Personen und Teams,  
* Beratung im Umgang mit Forschungssoftware,  
* Beratung im Umgang mit Lizenzen (siehe Kapitel 4),  
* Bereitstellung, Betrieb und Wartung technischer Ressourcen,  
* Veröffentlichung von Software und  
* weitere Aspekte, bspw. Cybersicherheit, Ethik und Datenschutzfragen.

\[\[Die Universität | Die Hochschule | Das Forschungszentrum\]\] nimmt diese Verantwortung wahr, indem \[\[es | sie\]\] für jeden der oben genannten Bereiche im Rahmen der zur Verfügung stehenden Möglichkeiten Unterstützungsangebote anbietet. Hiermit etabliert \[\[die Universität | die Hochschule | das Forschungszentrum\]\] einen stabilen organisatorischen Rahmen, der auf den hier definierten Leitlinien basiert.

*\[\[Anmerkung für Leitlinienersteller: Aktuell ist die tatsächliche bzw. geplante Unterstützung an den verschiedenen Hochschulen sehr divers. Deshalb ist zu erwarten, dass die konkreten Leitlinien Ihrer Hochschule bzw. Forschungsinstituts sehr unterschiedlich ausfallen. Entsprechend ist der nachfolgende Text eine Sammlung von Bausteinen, aus denen gewählt und ergänzt werden kann. Jede Hochschule muss nach ihren Fähigkeiten, verfügbaren Ressourcen und Plänen mit besserer Forschungssoftware in Zukunft bessere Forschungsarbeit zu leisten eigene Varianten entwickeln\]\]*

*\[\[Anmerkung für Leitlinienersteller: Ein “RSE-Zentrum” ist nach der Handreichung \[DFG24\]  auch von der DFG ein gern gesehenes Konstrukt, das die Relevanz des Themas RSE adäquat adressiert und in Kombination mit Forschungsanträgen förderfähig ist. Ein “Zentrum” ist eine eigenständige Einheit, mit Finanzverantwortung, wissenschaftlicher Leitung, Geschäftsführung und Personal. Dies heißt ggf. in manchen Forschungseinrichtungen anders und ist dann zu ersetzen.* 

*Beispiele zeigen, dass sich Investitionen in ein RSE Zentrum sehr schnell amortisieren (DOI: 10.5281/zenodo.10867903).* 

*Ob das RSE-Zentrum eigenständig in der Universität/Hochschule verankert wird oder als Teil z. B. der Bibliothek, der Informatik oder des Rechenzentrums wird und wie die wissenschaftliche Leitung ausgestaltet wird, ist den lokalen Gegebenheiten anzupassen. Ob das RSE-Zentrum neben der Weiterbildung der Teams auch die Lehre der Studierenden vornimmt, bleibt hier unbehandelt.*  
*Ein eigenständiges RSE-Zentrum entspricht im Folgenden der Text-\[\[Variante Zentrum\]\]. Sollte es nur möglich sein, eine koordinierende RSE-Einrichtung zu starten, so wäre dies Text-\[\[Variante B\]\]. Die GI RSE empfiehlt Einrichtung eines RSE-Zentrums.*

*Der nachfolgende Grundtext zur Auswahl und Gestaltung entsprechender Texte wurde weitgehend aus Sicht eines etablierten RSE-Zentrums formuliert\]\]  \[\[Ende Anmerkungen\]\]*

Bereits vorhandene Infrastruktur wie die Bibliothek, das Rechenzentrum, die Rechtsberatung, und weitere forschungsnahe Dienstleistungen wie existierende Beratungs- und Schulungsangebote zu Forschungsdatenmanagement oder High-Performance-Computing werden bei der Umsetzung der Leitlinie eingebunden. Die zentrale koordinierende Anlaufstelle ist dabei \[\[das RSE-Zentrum | die RSE-Einrichtung | das Rechenzentrum | die Bibliothek | die Rechtsberatung | die Innvovations-Stelle | …\]\].

## **5.1. Personelle Unterstützung bei der Erstellung und Erweiterung von Forschungssoftware**  {#5.1.-personelle-unterstützung-bei-der-erstellung-und-erweiterung-von-forschungssoftware}

\[\[Die Universität | Hochschule | Das Forschungszentrum\]\] bietet Forschenden Beratungs- und direkte Unterstützungsleistungen in den Bereichen

* der Konzeptionierung, Entwicklung und Weiterentwicklung von Forschungssoftware durch professionelle, ausgebildete Research Software Engineers in Zusammenarbeit mit Forschenden,  
* der technischen Aufwertung vorhandener Forschungssoftware durch Verbesserung der Performanz und Einbindung etablierter Praxis (z. B. durch Test-Abdeckung, Continuous Integration, Modularisierung),  
* der Verbesserung der Nutzbarmachung von Forschungssoftware durch Generalisierung, Benutzeroberflächen, breitflächiger Verfügbarkeit (Einrichten eines Servers und Webinterface zum Hosten und Nutzen der Software), Verbesserung der Dokumentation, Publikation der Software sowie Verbesserung der Reproduzierbarkeit von virtuellen Experimenten durch z. B. Containerisierung.

Damit fördert \[\[die Universität | Hochschule | das Forschungszentrum\]\] aktiv sowohl den verantwortungsvollen Einsatz von Personal- und Sachmitteln als auch die Reproduzierbarkeit der Forschung im digitalen Kontext. 

\[\[Variante Zentrum\]\]  
\[\[Die Universität | Hochschule | Das Forschungszentrum\]\] hat für diese Zwecke das RSE-Zentrum eingerichtet, das Forschende aller Fachrichtungen in den oben genannten Punkten durch Beratung und Entwicklungsleistungen unterstützt und dessen Personal zwar (zum Teil) verstetigt im Haushalt \[\[der Universität | der Hochschule | des Forschungszentrums\]\] vorgesehen ist, jedoch auch förderfähig bei Forschungsanträgen mitfinanziert werden kann. Das RSE-Zentrum koordiniert die Aus- und Weiterbildung von Research Software Engineers sowie die aktive Mithilfe bei der Konzeptionierung, Entwicklung, Weiterentwicklung und Verwaltung von Forschungssoftware, der Etablierung neuerer Werkzeuge und allen mit der Entwicklung zusammenhängenden Aktivitäten. Das RSE-Zentrum bietet insbesondere auch fachliche Unterstützung für dezentrale Forschungseinheiten ohne eigene RSE-Stellen. Die Expert:innen des RSE-Zentrums sind entsprechend für Zeiträume buchbar, bzw. betreuen und begleiten auch mehrere Projekte in Bezug auf spezifische technische, organisatorische oder Management-Fragestellungen. Es wird Wert darauf gelegt, kollaborativ mit den Mitgliedern der Forschungseinheit zielgerichtet gute Software zu erschaffen. Wie die Softwareentwicklung aufgeteilt wird, ist im Einzelfall agil zu entscheiden.

\[\[Variante B\]\]  
\[\[Die Universität | Hochschule | Das Forschungszentrum\]\] unterstützt das dezentrale Modell, in dem Research Software Engineers eigenfinanziert in den einzelnen Forschergruppen angesiedelt sind und dort domänenspezifisch an der Entwicklung teilnehmen. Zur Koordination der Research Software Engineers dient eine zentrale Anlaufstelle und Seminare, zu denen alle Software-entwickelnden Wissenschaftler:innen (scientists who code) und alle Research Software Engineers \[\[der Universität | Hochschule | des Forschungszentrums | der Einrichtung\]\] regelmäßig eingeladen sind. Eine domänenspezifische fachliche Beratung im Projekt kann nicht erfolgen.

Der optionale Aufbau eines dezentralen Pools an Research Software Engineers für mehrere Forschergruppen obliegt den jeweiligen Forschungseinheiten (also dem Institut oder der Fakultät).  
\[\[Ende Variante\]\]

Durch die Unterstützung der Research Software Engineers erkennt \[\[die Universität | die Hochschule | das Forschungszentrum\]\] die Wichtigkeit von RSE in software-basierter, qualitativ hochwertiger Forschung an und ermöglicht einen Wissenstransfer – einmal innerhalb \[\[des RSE-Zentrums | der Gruppe der RSEs\]\] an \[\[der Universität | der Hochschule | dem Forschungszentrum\]\], und darüber hinausgehend von den Research Software Engineers an die Forschenden. Das Wissen zum Thema RSE wird so durch \[\[die Universität | Hochschule | das Forschungszentrum\]\] verwaltet und bleibt auch bei personellen Wechseln besser erhalten. 

→→ Für **Entscheidende und Leitende** ←←   
Die Leitenden der Forschergruppen sind angehalten, die Teilnahme ihrer Research Software Engineers auch an lokalen Community Events möglich zu machen und den Austausch der Research Software Engineers zwischen den Forschungsgruppen und den an der \[\[Universität | Hochschule | Forschungseinrichtung\]\] vorhandenen Fachexpertinnen und Fachexperten aktiv zu unterstützen.

Durch die Vernetzung erhalten die Forschergruppen Zugang zu einem breiteren Wissensspektrum und Expertenwissen, auf das sie in ihrem Forschungsalltag zurückgreifen können. 

Zur konkreten personellen Unterstützung von RSE-Projekten bietet \[\[die Universität | die Hochschule | das Forschungszentrum\]\] verschiedene Formen der Unterstützung:

* *\[\[Variante Zentrum\]\]* Organisatorische, fachliche und methodische Beratung für die Softwareentwicklung durch einen Expert:innen-Pool des RSE-Zentrums.   
* *\[\[oder Variante B\]\]* Vermittlung eines gegenseitigen organisatorischen, fachlichen und methodischen Austauschs der lokalen RSE-Community.  
* *\[\[Variante Zentrum\]\]* Basierend auf Verfügbarkeit, Kapazität zur konstruktiven Mithilfe bei der Entwicklung, durch einen Pool an RSE-Entwickler:innen des RSE-Zentrums.  
* *\[\[Variante Zentrum mit wissenschaftlicher Informatikanbindung\]\]* Auf Basis studentischer Projekte organisiert das RSE-Zentrum Praktika, Bachelor- und Master-Arbeiten in \[\[dem Bereich | den Bereichen\]\]  \[\[Informatik | Software Engineering | Software Systems Engineering | Research Software Engineering | Computational Science and Engineering\]\] passende Entwicklungstätigkeiten für Forschungssoftware.  
* *\[\[Variante Zentrum und Variante B mit RSE-Lehre\]\]* Den Wissenschaftler:innen werden Mikrozertifikate für die Teilnahme an Weiterbildungsmaßnahmen im Bereich RSE für die eigene Karriereentwicklung angeboten. Federführend ist hier \[\[das Zentrum für Lehre und Weiterbildung | die Doctoral Graduate School \]\] in Kooperation mit dem RSE-Zentrum.

*\[\[Ende Varianten\]\]*

Aktuelles zu Dienstleistungen, Ansprechpartnern und Informationshilfen findet sich auf der RSE-Webseite: 

		\[\[https://research-se.X-university.de\]\]

## **5.2. Unterstützungsleistungen bei der langfristigen Pflege von Software** {#5.2.-unterstützungsleistungen-bei-der-langfristigen-pflege-von-software}

*\[\[Variante Zentrum\]\]*

\[\[Der Universität | Der Hochschule | Dem Forschungszentrum\]\] ist bewusst, dass im Einsatz befindliche Software anders als passive (gesammelte) und archivierbare Daten eine permanente Pflege und Aktualisierung benötigt. Die Veränderung des Software-Stacks, die Integration an neuen Schnittstellen, extern entwickelte Erweiterungspakete, neue Nachbarsysteme, aber auch Regularien und Cybersecurity erfordern aktive Pflege.

Grundsätzlich ist im Sinne der DevOps-Methodik (=”Integrierter Development und Operations-Lifecycle der Software”) der Übergang zwischen aktiver Entwicklung und langfristiger Pflege sowie die phasenweise immer wieder auftretende aktive Ergänzung fließend, weshalb sinnvollerweise zwischen Entwicklung und Pflege aus Sicht der Unterstützungsleistungen nicht grundsätzlich unterschieden wird. Das in Kapitel 3 eingeführte Zustandsmodell für Software zeigt die jeweiligen Zustandsoptionen. Ist die Software-Infrastruktur am Ende ihres Lebenszyklus angekommen, wird sie adäquat außer Dienst gestellt und langfristig nachhaltig archiviert.

Häufig ist die erwünschte Lebenszeit der Software deutlich länger als die finanzielle Förderung des Projekts, in dem sie entwickelt wurde. Für die Etablierung von Forschungssoftware als langfristig verfügbare Infrastruktur bietet das  RSE-Zentrum personelle Kapazitäten, um Software langfristig lauffähig und damit nachnutzbar zu halten. 

*\[\[Ende Variante Zentrum\]\]*

## **5.3. Unterstützungsleistungen in der Weiterbildung** {#5.3.-unterstützungsleistungen-in-der-weiterbildung}

Weiterbildungsangebote für Entwickler:innen finden sich auf der oben genannten RSE-Webseite. 

Die Weiterbildungsangebote beinhalten unter anderem Einstiegsthemen wie Einführung in das Programmieren für in der Wissenschaft häufig verwendete Programmiersprachen, Versionskontrollsysteme, Erstellen und Strukturieren von Tests, Einführung in Continuous Integration und Kernthemen des Software Engineering zur effizienten Entwicklung, Nutzung von KIs/Copilots, Management von Reviews und Introspektionen, Architekturprinzipien, Agiler RSE-Entwicklungsmethodik auf Basis von z. B. Scrum, Umgang mit Verwaltungswerkzeugen wie GitLab/GitHub, Nutzung von Forschungs-Software-Management-Plänen, und Veröffentlichung und Dissemination von Forschungssoftware (s. Kapitel 3 zur Auswahl der Themen). Diese Softwareentwicklungs-Themen werden komplementiert durch andere fachübergreifende Angebote der oben genannten kooperierenden Einrichtungen.

Auf die Möglichkeit, viele dieser Weiterbildungsangebote bereits als Studierende wahrzunehmen, um so eine fundierte Ausbildung als Research Software Engineer in Kombination mit der eigentlichen Forschungsdomäne zu erhalten, wird hingewiesen. Nicht nur Studierende, auch Doktoranden und Postdoktoranden können \[\[ interne bis hin zu wissenschaftlich oder industriell anerkannte \]\] Zertifikate erwerben und so ihre Position und Wahrnehmung als Research Software Engineers stärken. Details hierzu finden sich auf der RSE-Webseite  
	\[\[https://research-se.X-university.de\]\]  
 bzw. der Webseite \[\[des Zentrum für Lehre und Weiterbildung | der Doctoral Graduate School \]\].

## **5.4. Würdigung der Research Software Engineers** {#5.4.-würdigung-der-research-software-engineers}

\[\[Die Universität | Hochschule | Das Forschungszentrum\]\] unterstützt die Anerkennung der Leistungen der Research Software Engineers (RSEs), also der Personen, die professionell Forschungssoftware entwickeln, betreiben, weiterentwickeln und warten; und ihre akademische Leistungen zu Teilen oder vollständig der Forschungssoftware widmen. Viele RSEs sind selbst Wissenschaffende und planen eine akademische Karriere im eigenen Fachgebiet. Die Wertschätzung der Leistungen dieser RSEs ist auch daher wichtig und kommt diesem Fachgebiet zugute.

*\[\[Ausbaubar und ergänzbar: Nachfolgend exemplarisch Maßnahmen, die in der RSE Community als wertschätzend angesehen werden.\]\]*

* \[\[Die Universität | Hochschule | Das Forschungszentrum\]\] unterstützt gemäß \[DFG24\] die Anerkennung der Leistungen der RSEs je nach Beitragsleistung explizit durch die Sichtbarmachung der Ergebnisse in Form einer Nennung oder **Co-Autorenschaft in wissenschaftlichen Publikationen**. Unterstützt wird dies durch die Berücksichtigung von Software- und Datenpublikationen im wissenschaftlichen Reporting. 

* \[\[Die Universität | Hochschule | Das Forschungszentrum\]\] unterstützt organisatorisch die Gründung von **wissenschaftlichen Nachwuchsgruppen** zu großen, langfristig angelegten Softwareprojekten mit entsprechenden Karrieremöglichkeiten für RSEs.

* \[\[Die Universität | Hochschule | Das Forschungszentrum\]\] bietet Schulungen mit professionellen **Zertifikaten** und unterstützt so die persönliche Entwicklung der RSEs.

* Durch das Herausstellen der RSEs und ihrer Software-Errungenschaften auf einer passenden Webseite oder in Research Software Directories wird die **Sichtbarkeit** der Leistungen und Beiträge der RSEs öffentlich gemacht und wertgeschätzt. 

* \[\[Die Universität | Hochschule | Das Forschungszentrum\]\] fordert **Berufungskommissionen** auf, bei der Bewertung von Kandidat:innen eine explizite Einbeziehung von exzellenter Forschungssoftware als wissenschaftliches Ergebnis vorzunehmen.

* Durch die Vergabe jährlicher **RSE-Preise** in \[\[der Universität | Hochschule | dem Forschungszentrum\]\]  wird die Qualität der Software-Ergebnisse und das Engagement in der Community gewürdigt.

* Sowohl \[\[die Universität | Hochschule | das Forschungszentrum\]\] als auch die Forschergruppen, die RSEs einstellen, erkennen an, dass durch eine **Vernetzung** und bessere Integration der RSEs in die wissenschaftliche Community die Qualität der Forschungssoftware – und damit der Forschungsergebnisse – fundamental verbessert wird.

* In Absprache mit Fördergebern empfiehlt \[\[die Universität | Hochschule | das Forschungszentrum\]\] die explizite Nennung von Softwareentwicklungs-Anteilen in Anträgen ("Wir beantragen Research Software Engineer" statt nur "wir beantragen Doktorand:in who Codes").

* \[\[Die Universität | Hochschule | das Forschungszentrum\]\] bemüht sich, durch adäquate Bezahlung und ansprechende Arbeitsbedingungen ohne überbordende Bürokratie und mit einer gewissen wissenschaftlichen Freiheit exzellente RSEs langfristig im Wissenschaftssystem zu halten. Dabei erkennt \[\[die Universität | die Hochschule | das Forschungszentrum\]\] an, dass es sich bei RSEs um wissenschaftliches Personal handelt.

* \[\[Die Universität | Hochschule | das Forschungszentrum\]\] erkennt Research Software Engineering als eigene Fachdisziplin an. Dies schließt den auch in anderen Disziplinen üblichen regelmäßigen **Austausch mit der Fachcommunity** außerhalb der Einrichtung ein. Daher wird zu Dienstreisen oder aktiver Vorbereitung von Konferenzen, Workshops, oder Ähnlichem explizit ermutigt.

* Ein wichtiger Bestandteil der Arbeit eines RSE besteht in der **Vertrautheit mit modernen Methoden, Werkzeugen und Softwareframeworks**. Daher sollten RSEs \[\[ der Universität | Hochschule | des Forschungszentrums\]\] sich im Rahmen ihrer vertraglichen Arbeitszeit selbständig in ebensolche **einarbeiten** und damit weiterbilden. 

*\[\[Ende Ausbau\]\]*

## **5.5. Unterstützungsleistungen bei Lizenzen** {#5.5.-unterstützungsleistungen-bei-lizenzen}

In Abschnitt 4.4. werden die Unterstützungsleistungen bei der Wahl von Lizenzen erklärt. Ansprechpartner und Empfehlungen sind der RSE-Webseite zu entnehmen.

## **5.6. Unterstützungsleistungen durch technische Services** {#5.6.-unterstützungsleistungen-durch-technische-services}

Als technische Services werden im Wesentlichen Software-Services, Computing-Kapazitäten und Rechner-Infrastruktur bezeichnet, die kostenlos oder gegen eigene Aufwands-Kosten betrieben, gewartet und zur Verfügung gestellt werden und für die wissenschaftliche Softwareentwicklung genutzt werden können. Zum einen wird hier interne Infrastruktur und Support des Rechenzentrums zur Verfügung gestellt, zum anderen können – unter Beachtung der DSGVO und notwendiger Sicherheitsaspekte –  bestimmte, im Netz verfügbare Services für wissenschaftliche Zwecke genutzt werden.

*\[\[Anmerkung für Leitlinienersteller: hier konkrete Webseiten einfügen; nicht angebotene Services gegebenenfalls ablehnen und streichen (oder auch erklären, warum sie nicht angeboten werden: das erspart ggf. Nachfragen); angegeben sind die Links zu öffentlich verfügbaren Services; lokale Alternativen sollten integriert werden. Die Services sind mit absteigender Wichtigkeit sortiert, angefangen von Diensten die unbedingt zur Verfügung stehen müssen, bis hin zu optionalen Services\]\]*

* Kollaboratives Arbeiten mit Versionskontrollsystemen und Kontrolle unterschiedlicher Varianten \[\[[https://git.uni-x.de/](https://github.com/) | https://codebase.helmholtz.cloud\]\]  
* Runner für Continuous Integration verschiedener OS \[\[[https://git.uni-x.de](https://github.com/)\]\]  
* Dokumentation von Software \[\[[https://git.uni-x.de](https://github.com/)\]\]  
* Ticketsystem \[\[[https://git.uni-x.de](https://github.com/)\]\]  
* Projektmanagement \[\[[https://git.uni-x.de](https://github.com/)\]\]  
* Publikation und Archivierung von Software \[\[[https://www.softwareheritage.org/](https://www.softwareheritage.org/), domänenspezifische Repositorien z. B. bei [https://www.re3data.org/](https://www.re3data.org/), Archive of Formal Proofs [https://www.isa-afp.org/](https://www.isa-afp.org/), [https://zenodo.org/](https://zenodo.org/)\]\]  
* Suchmaschinen für Forschungssoftware oder Katalog von verfügbarer Forschungssoftware \[\[z. B. [https://base-search.net/](https://base-search.net/), Betty’s (Re)Search Engine, Research Software Directory\]\]  
* kollaborative Schreibumgebung für wissenschaftliche Papiere auf LaTex-Basis: \[\[[https://www.overleaf.com/](https://www.overleaf.com/), lokale ShareLaTeX Instanz\]\]  
* kollaborative Schreibumgebung im Word-like Stil: \[\[[https://nextcloud.uni-x.de](https://nextcloud.uni-x.de)\]\] oder ohne Extras: \[\[[https://pad.uni-x.de/](https://pad.gwdg.de/)\]\]  
* Kommunikationsplattformen wie   
  * Matrix  [https://matrix.org/](https://matrix.org/),   
  * Slack  [https://slack.com/intl/de-de/](https://slack.com/intl/de-de/),   
  * LinkedIn  [https://www.linkedin.com/](https://www.linkedin.com/)  
* Services zur Verwaltung von Forschungsdaten (RDM, NFDI) wie zum Beispiel  
  * DIM.Ruhr  https://www.dim-ruhr.de/  
  * HERMES  https://hermes-hub.de/  
  * SODa  https://sammlungen.io/de  
  * KODAQS  https://www.gesis.org/forschung/drittmittelprojekte/projektseite-kodaqs  
  * DataNord  https://www.bremen-research.de/en/datanord  
  * DKZ.2R  https://www.dkz2r.de/  
  * QUADRIGA  https://www.quadriga-dk.de/de/  
  * Come2DATA  https://tu-dresden.de/zih/forschung/projekte/Come2Data  
  * WiNoDa  https://winoda.de/  
  * DACE  https://dace-info.de/  
  * de.KCD  [https://datenkompetenz.cloud/](https://datenkompetenz.cloud/)  
* \[\[ Optional: weitere  relevante Services nennen \]\]

Die Zusammenstellung der Services ist auch auf der bereits genannten RSE-Webseite gelistet.  
Daneben gibt es zusätzliche disziplinspezifische Services.

## **5.7. Finanzierung der Unterstützungsleistungen bei der Entwicklung und Pflege von Software** {#5.7.-finanzierung-der-unterstützungsleistungen-bei-der-entwicklung-und-pflege-von-software}

*\[\[Anmerkung für Leitlinienersteller/Hochschullleitungen: Die konkrete Ausgestaltung der Unterstützungsleistung und deren Finanzierung obliegt der Hochschule/ Forschungseinrichtung, ggf. in Koordination mit Land und Bund. Beispiele in den Niederlanden (eScience Center), UK (Sustainable Software Institute) existieren, sind aber universitätsübergreifend organisiert.\]\]*

→→ Für **Entscheidende und Leitende** ←←   
\[\[Der Universität | Hochschule | Dem Forschungszentrum\]\] ist bewusst, dass Entwicklung, Pflege und Weiterentwicklung von Software ähnlich wie technische Infrastruktur (z. B. Gebäude, Anlagen) anders als passive, gesammelte Daten einen deutlichen, vor allem personellen Aufwand haben. 

*\[\[Variante Zentrum\]\]*

Für die Etablierung von Forschungssoftware als langfristig verfügbare Infrastruktur bietet das  RSE-Zentrum personelle Kapazitäten, um Software über längere Zeit lauffähig und damit nachnutzbar zu halten. Zu der aktuell vorherrschenden und weiterhin nutzbaren Lösung, der Finanzierung kompletter Research Software Engineers innerhalb der Forschungseinrichtung ergänzt \[\[die Universität | Hochschule | das Forschungszentrum\]\] das Angebot zentral buchbarer RSE-Expert:innen des RSE-Zentrums. 

Die Buchungsgrößen können sich auf wenige Tage Beratung bis hin zur langfristigen Abstellung kompletter Personen auf z. B. der Basis ganzer, halber und 20%-Stellen, beziehen und sind mit dem RSE-Zentrum abzusprechen. Die auftraggebende Forschungseinheit und RSE-Zentrum nehmen ein Pooling der Ressourcen für die langfristige Stellen- und Projektplanung vor. Gegenüber dem Fördergeber gelten die RSE-Expert:innen als Personalstellen und können als solche in Projekten beantragt werden.

Das RSE-Zentrum stellt diese Expert:innen im Bereich der wissenschaftlichen und technischen Softwareentwicklung mit unterschiedlich ausgeprägten Fähigkeiten zu den Aktivitäten des Programmierens, des Managements, der Pflege, der Qualitätssicherung und der (teilweise interdisziplinären) Kommunikation. Daneben werden Aktivitäten für die Weiterbildung unterstützt. Eine hohe forschungsfachliche Expertise ist wegen der hohen domänenspezifischen Diversität der Forschungsthemen im RSE-Zentrum nur begrenzt vorhanden und es wird erwartet, dass diese weiterhin in der Forschungseinheit verbleibt. Die Methodik zur erfolgreichen und effizienten Kollaboration und die Vertrautheit mit dem Ablauf wissenschaftlicher Projekte bringen die RSE-Expert:innen mit.

Zur Finanzierung der RSE-Expert:innen gibt es grundsätzlich folgende Optionen:

### 5.7.1. Übernahme auf RSE-Zentrums-Kosten (“Universitäts-Software”) {#5.7.1.-übernahme-auf-rse-zentrums-kosten-(“universitäts-software”)}

Die originär erstellende Forschungseinrichtung stellt einen Antrag (siehe Antragsformular) an das RSE-Zentrum zur Übernahme der Softwarepflege. Abhängig von den in Kapitel drei beschriebenen Einordnungen (vor allem TRL, Nutzungsgrad) sowie weiteren Kriterien, wie Qualität und Verständlichkeit der Software und der strategischen Relevanz für die Universität wird aus der Menge der gestellten Anträge jährlich die leistbare Menge an Procurements für jeweils 5 Jahre übernommen. Am Ende der 5 Jahre wird neu entschieden. Die Auswahl übernimmt das RSE-Auswahlgremium.

### 5.7.2 Übernahme auf Kosten der Forschungseinheit (“Instituts-Software”)  {#5.7.2-übernahme-auf-kosten-der-forschungseinheit-(“instituts-software”)}

Das RSE-Zentrum bringt substantielle personelle Ressourcen in die Pflege, Weiterentwicklung, Bug-Fixing und deren Management ein. Finanziert werden diese Ressourcen aber durch ein oder mehrere Institute/Forschungseinheiten. Bei der zu erwartenden Vielzahl an potentiellen Projekten muss auch hier eine Auswahl nach Verfügbarkeit und thematischer Expertise durch das RSE-Auswahlgremium stattfinden.

Es besteht die Möglichkeit, die hier zu buchenden Ressourcen in (1) Berufungs- oder Bleibeverhandlungen, (2) Forschungsanträgen an DFG, EU, BMBF, etc., (3) Stiftungen oder (4) direkt aus F\&E-Verträgen mit industriellen Auftraggebern zu integrieren. Insbsondere ist die DFG-Handreichung zum Umgang mit Forschungssoftware \[DFG22\] im Förderhandeln beachtenswert.

### 5.7.3 Ausgestaltung der Unterstützung  {#5.7.3-ausgestaltung-der-unterstützung}

Unabhängig von der Finanzierung gibt es in Absprache zwischen RSE-Zentrum und Forschungseinheit(en) eine Reihe von organisatorischen Ausgestaltungsoptionen:

1. Wer trägt die zukünftige Verantwortung für entwickelte Forschungssoftware?  Die Forschungseinheit (bevorzugt), oder übernimmt die Pflege-Verantwortung das RSE-Zentrum.  
2. Wer managt die Entwicklung/Pflege? Obwohl i.d.R. Forschende dies selbst tun, kann das RSE-Zentrum auf Wunsch und ggf. mit finanzieller Absicherung die organisatorische Durchführung in agiler Entwicklung (und damit eine Teilprojektleitung) übernehmen oder Research Software Engineers in ein vorhandenes Projekt entsenden.  
3. Dissemination, Community Building: primär in der Fachcommunity durch die Forschungseinheit, ggf. mit Unterstützung des RSE-Zentrums  
4. Ruhendes/Auslauf-Produkt: ist dann eine gemeinsame Entscheidung.

*\[\[Ende Variante Zentrum\]\]*

## **5.8. Weitere Unterstützungsleistungen**  {#5.8.-weitere-unterstützungsleistungen}

Weitere durch \[\[die Universität | die Hochschule | das Forschungszentrum | die Einrichtung\]\] angebotene Unterstützungsleistungen umfassen:

1. Beratung und Hilfestellung bei der Publikation von Forschungssoftware \[\[RSE-Webseite\]\]. \[\[Die Bibliothek | Das RSE-Zentrum | Die Beratungsstelle\]\] bietet Hilfe bei der Veröffentlichung von Forschungssoftware, von der Vorbereitung der Bereitstellung über die Auswahl des geeigneten Publikationsmediums bis zu domänenspezifischen Publikationsplattformen.  
2. Bereitstellung, Weiterbildung und Unterstützung im Erstellen sowie Umsetzung von Softwaremanagement-Plänen (SMPs). SMPs dienen der Projektplanung, aber auch den Berichtspflichten denen Forschende nachkommen müssen (https://www.software.ac.uk/guide/writing-and-using-software-management-plan). \[\[Die Universität | Die Hochschule | Das Forschungszentrum\]\] stellt eine Plattform \[\[z.B. RDMO https://rdmorganiser.github.io/\]\] zur Erstellung neuer SMPs bzw. Nutzung von SMPs-Templates zur Verfügung. Das RSE-Zentrum bietet Unterstützung zum effektiven Management sowie Training bzw. Trainingsmaterial zu deren Nutzung \[\[RSE-Webseite\]\].   
3. Sicherheitsfragen bei Forschungssoftware werden durch \[\[ das IT-Center | das RSE-Zentrum | Stelle nennen\]\] unterstützt \[\[Webseite/Kontakt\]\]  
4. Die Datenschutzbeauftragten sind unter \[\[Webseite/Kontakt\]\] erreichbar.  
5. Ethische Fragen können an \[\[Webseite/Kontakt\]\] gestellt werden.

\[\[ 6\. Weitere Punkte ergänzt durch die Universität | die Hochschule | das Forschungszentrum. \]\]

# Referenzen {#referenzen}

\[Bal25\]	Helmut Balzert, Christof Ebert. Lehrbuch der Softwaretechnik. Springer-Verlag, 2025 (Neue Auflage, in Erscheinung).

\[BBB19\]	Felix Bach, Oliver Bertuch, Christian Busse, Wolfgang zu Castell, Sabine Celo, Michael Denker,Stefan Dinkelacker, Stephan Druskat, Claas Faber, Ants Finke, et al. Muster-Richtlinie Nachhaltige Forschungssoftware an den Helmholtz-Zentren, 2019\. [https://doi.org/10.2312/os.helmholtz.007](https://doi.org/10.2312/os.helmholtz.007).

\[BHK+22\] 	Michelle Barker, Neil P Chue Hong, Daniel S Katz, Anna-Lena Lamprecht, Carlos Martinez-Ortiz, Fotis Psomopoulos, Jennifer Harrow, Leyla Jael Castro, Morane Gruenpeter, Paula Andrea Martinez, et al. Introducing the FAIR Principles for research software. Sci Data, 9(1):622, 2022\. [https://doi.org/10.1038/s41597-022-01710-x](https://doi.org/10.1038/s41597-022-01710-x).

\[BF14\]	Pierre Bourque und Richard E Fairley. SWEBOK V3.0: Guide to the Software Engineering Body of Knowledge. IEEE Computer Society, 2014\.

\[BMBF23\]	Till Kreutzer und Georg Fischer, iRights.Law; Bundesministerium für Bildung und Forschung (BMBF)  Urheberrecht in der Wissenschaft Ein Überblick für Forschung, Lehre und Bibliotheken [https://www.bmbf.de/SharedDocs/Publikationen/de/bmbf/1/31518\_Urheberrecht\_in\_der\_Wissenschaft.pdf](https://www.bmbf.de/SharedDocs/Publikationen/de/bmbf/1/31518_Urheberrecht_in_der_Wissenschaft.pdf) CC BY-SA 4.0.

\[BOSS22\]	Oliver Bertuch, Dennis Oliveira, Ute Schelhaas und Alexander Storm. Guidelines for the development and distribution of software at Forschungszentrum Jülich.   
Technical report, 2022\. [https://hdl.handle.net/2128/33259](https://hdl.handle.net/2128/33259), CC 4.0.

\[BTK+21\]	Marijan Beg, Julietta Taka, Thomas Kluyver, Alexander Konovalov, Min Ragan-Kelley, Nicolas M. Thiery und Hans Fangohr. Using Jupyter for Reproducible Scientific Workflows. Computing in Science & Engineering, March/April 2021, 36, 2021\. [https://doi.org/10.1109/MCSE.2021.3052101](https://doi.org/10.1109/MCSE.2021.3052101) 

\[CC24\]	Creative Commons. Frequently Asked Questions. [https://creativecommons.org/faq/\#can-i-apply-a-creative-commons-license-to-software](https://creativecommons.org/faq/#can-i-apply-a-creative-commons-license-to-software), 2024\. Aufgerufen 2024.07.29.

\[Con68\]	Melvin E Conway. How do committees invent? Band 14, Seiten 28–31. F. D. Thompson Publications, Inc., 1968\.

\[DFG15\] 	Deutsche Forschungsgemeinschaft e.V., Leitlinien zum Umgang mit Forschungsdaten, [https://www.dfg.de/resource/blob/172112/23826608514d73da82622c0a16c842db/leitlinien-forschungsdaten-data.pdf](https://www.dfg.de/resource/blob/172112/23826608514d73da82622c0a16c842db/leitlinien-forschungsdaten-data.pdf), 30\. September 2015

\[DFG22\]	Deutsche Forschungsgemeinschaft e.V., Leitlinien zur Sicherung guter wissenschaftlicher Praxis, Version 1.1. [https://doi.org/10.5281/zenodo.6472827](https://doi.org/10.5281/zenodo.6472827),  2022\. 

\[DFG24\]	Deutsche Forschungsgemeinschaft e.V. Handreichung: “Umgang mit Forschungssoftware im Förderhandeln der DFG”, [https://www.dfg.de/de/grundlagen-themen/grundlagen-und-prinzipien-der-foerderung/forschungssoftware](https://www.dfg.de/de/grundlagen-themen/grundlagen-und-prinzipien-der-foerderung/forschungssoftware), [https://zenodo.org/records/13919790](https://zenodo.org/records/13919790), Oktober 2024\. 

\[DC20\]	Roberto Di Cosmo. biblatex-software – BibLaTeX stylefiles for software products. [https://www.ctan.org/tex-archive/macros/latex/contrib/biblatex-contrib/biblatex-software](https://www.ctan.org/tex-archive/macros/latex/contrib/biblatex-contrib/biblatex-software), 2020\. Aufgerufen 2024.07.01.

\[DIN20\] 	DIN EN 16603-11:2020-02: Raumfahrttechnik \- Definition des Technologie-Reifegrades (TRL) und der Beurteilungskriterien (ISO 16290:2013, modifiziert); Deutsche Fassung EN 16603-11:2019, Februar 2020\.

\[DLR22\]	DLR. Nutzung von Open-Source-Software im DLR. [https://www.dlr.de/de/medien/publikationen/broschueren/opensource-software\_dlr\_2022.pdf](https://www.dlr.de/de/medien/publikationen/broschueren/opensource-software_dlr_2022.pdf), 2022\. Aufgerufen 2024.05.06.

\[FAIR20\]	*GO FAIR*. "FAIR Principles". [https://www.go-fair.org/fair-principles/](https://www.go-fair.org/fair-principles/). Aufgerufen 2020.02.16. 

\[Fow19\] 	Martin Fowler. Software Architecture Guide. [https://martinfowler.com/architecture/](https://martinfowler.com/architecture/), 2019\. Aufgerufen 2024.05.02.

\[FSF19\]	Free Software Foundation, Inc.: Freie Software. Was ist das?, [https://www.gnu.org/philosophy/free-sw.de.html](https://www.gnu.org/philosophy/free-sw.de.html), 2019\. Aufgerufen 2023.12.15.

\[GAB+24\]	Florian Goth, Renato Alves, Matthias Braun, Leyla Jael Castro, Gerasimos Chourdakis, Simon Christ, Jeremy Cohen, Fredo Erxleben, Jean-Noël Grad, Magnus Hagdorn, et al. Foundational Competencies and Responsibilities of a Research Software Engineer, 2024\.

\[GI24\] 	GI- und de-RSE Muster-Leitlinie für die effiziente Entwicklung von Forschungssoftware. GI e.V. (todo: complete). 2024

\[GKL+21\] 	Morane Gruenpeter, Daniel S Katz, Anna-Lena Lamprecht, Tom Honeyman, Daniel Garijo, Alexander Struck, Anna Niehues, Paula Andrea Martinez, Leyla Jael Castro, Tovo Rabemanantsoa, et al. Defining Research Software: a controversial discussion, 2021\. Zenodo. [https://doi.org/10.5281/zenodo.5504016](https://doi.org/10.5281/zenodo.5504016) 

\[GLHR24\]	Lars Grunske, Anna-Lena Lamprecht, Wilhelm Hasselbring und Bernhard Rumpe. Research Software Engineering \- Forschungssoftware effizient erstellen und dauerhaft erhalten. Forschung & Lehre, 24(3):186–188, Februar 2024\.

\[HDB+24\] 	Wilhelm Hasselbring, Stephan Druskat, Jan Bernoth, Philine Betker, Michael Felderer, Stephan Ferenz, Anna-Lena Lamprecht, Jan Linxweiler und Bernhard Rumpe. Toward Research Software Categories, 2024\. [https://doi.org/10.48550/arXiv.2404.14364](https://doi.org/10.48550/arXiv.2404.14364).  

\[ISO23\]	ISO/IEC 25019:2023:	Systems and software Quality Requirements and Evaluation (SQuaRE), Standard, International Organization for Standardization, Geneva, CH, November 2023\.

\[KF18\]	Matthias Katerbow und Georg Feulner. Handreichung zum Umgang mit Forschungssoftware, Februar. 2018\. Zenodo. https://doi.org/10.5281/zenodo.1172970

\[Lam24\]	Anna-Lena Lamprecht. GI-Radar 351: Research Software. [https://gi-radar.de/351-research-software/](https://gi-radar.de/351-research-software/), 2024\. Aufgerufen 2024.07.02

\[LL23\]	Jochen Ludewig und Horst Lichter. Software Engineering: Grundlagen, Menschen, Prozesse, Techniken. 4\. Auflage, dpunkt.verlag, Heidelberg, 2023\.

\[Mar17\] 	Robert C Martin. Clean Architecture: A Craftsman’s Guide to Software Structure and Design. Pearson, 2017\.

\[MPB+21\]	Reinhard Messerschmidt, Heinz Pampel, Felix Bach, W zu Castell, Michael Denker, Ants Finke, Bernadette Fritzsch, Martin Hammitzsch, Uwe Konrad, Yvonne Leifels, et al. Checkliste zur Unterstützung der Helmholtz-Zentren bei der Implementierung von Richtlinien für nachhaltige Forschungssoftware, 2021\.

	[https://gfzpublic.gfz-potsdam.de/pubman/item/item\_5007561](https://gfzpublic.gfz-potsdam.de/pubman/item/item_5007561)

\[NAS20\] 	NASA Earth Science and Technology Office. Technology Readiness Levels. [https://esto.nasa.gov/trl](https://esto.nasa.gov/trl), 2020\. Aufgerufen 2024.04.18.

\[OSI06\]	Open Source Initiative. The Open Source Definition. [https://opensource.org/osd](https://opensource.org/osd), 2006\. Aufgerufen 2024.07.29.

\[OSI22\]	Open Source Initiative. OSI Approved Licenses. [https://opensource.org/licenses](https://opensource.org/licenses), 2022\. Aufgerufen 2024.07.29.

\[Pic08\] 	Roman Pichler: Scrum – Agiles Projektmanagement erfolgreich einsetzen, dpunkt.verlag. 2008\. 

\[RESA24\]	Research Software Alliance (ReSA). Web Collection of Guidelines. (as seen 1.8.2024). 2024\.

\[SMH18\] 	Tobias Schlauch, Michael Meinel und Carina Haupt. Software-Engineering-Empfehlungen des DLR. Technical report, August. 2018\. Zenodo. [https://doi.org/10.5281/zenodo.1344608](https://doi.org/10.5281/zenodo.1344608).

\[Som18\]	Ian Sommerville. Software Engineering, 9”‘ed. Pearson Education, Inc, 2018\.

\[WAB+14\] 	Greg Wilson, Dhavide A Aruliah, C Titus Brown, Neil P Chue Hong, Matt Davis, Richard T Guy, Steven HD Haddock, Kathryn D Huff, Ian M Mitchell, Mark D Plumbley, et al. Best practices for scientific computing. PLoS biology, 12(1):e1001745, 2014\.

\[WBC+17\] 	Greg Wilson, Jennifer Bryan, Karen Cranston, Justin Kitzes, Lex Nederbragt und Tracy K Teal. Good enough practices in scientific computing. PLoS computational  biology, 13(6):e1005510, 2017\.

\[Wik24\] 	Wikipedia. Comparison of free and open-source software licenses — Wikipedia, the free encyclopedia. [https://en.wikipedia.org/wiki/Comparison\_of\_free\_and\_open-source\_software\_licenses](https://en.wikipedia.org/wiki/Comparison_of_free_and_open-source_software_licenses), Aufgerufen 2024.05.15.

\[Wik24b\] 	Wikipedia. Research Software Engineering — Wikipedia, die freie Enzyklopädie. [https://de.wikipedia.org/wiki/Research\_Software\_Engineering](https://de.wikipedia.org/wiki/Research_Software_Engineering), Aufgerufen 2024.05.11.

\[Wik24c\] 	Wikipedia. Softwarequalität  — Wikipedia, die freie Enzyklopädie. [https://de.wikipedia.org/wiki/Softwarequalit%C3%A4t](https://de.wikipedia.org/wiki/Softwarequalit%C3%A4t), Aufgerufen 2024.07.13.

\[YGJ24\]	Yo Yehudi, Carole Goble und Caroline Jay. Individual context-free online community health indicators fail to identify open source software sustainability. 2024\. [https://doi.org/10.48550/arXiv.2309.12120](https://doi.org/10.48550/arXiv.2309.12120) (Preprint)

# Anhang A: Kategorisierungsmöglichkeiten  {#anhang-a:-kategorisierungsmöglichkeiten}

Eine detaillierte Auflistung weiterer nutzbarer Kategorisierungsmöglichkeiten, die zur Klärung von in der Entwicklung notwendigen Maßnahmen beitragen können:

| Kategorie | Ausprägung |
| ----- | ----- |
|  |  |
| **Nutzerbasis** | Persönlich |
|  | Team-Intern |
|  | Teamübergreifend, innerhalb einer Organisation |
|  | Nutzende außerhalb der eigenen Organisation |
|  | Global, divers |
|  |  |
| **Entwicklungs-Community** | Persönlich |
|  | Team-Intern |
|  | Teamübergreifend, innerhalb einer Organisation |
|  | Entwickelnde außerhalb der eigenen Organisation |
|  | Global, divers |
|  |  |
| **Kritikalität** | Keine Auswirkungen |
|  | Leichte Auswirkungen auf die Forschungsfähigkeit oder Forschungsergebnisse  des Teams / Instituts |
|  | Schwerwiegende Auswirkungen auf die Forschungsfähigkeit oder Forschungsergebnisse des Teams / Instituts |
|  | Schwerwiegende Auswirkungen auf die Forschungsfähigkeit oder Forschungsergebnisse mehrerer organisationsinterner Teams / Institute |
|  | Unmittelbare oder mittelbare Auswirkungen auf Dinge (Sachschäden / Finanzschäden) |
|  | Auswirkungen auf Leib und Leben |
|   |  |
| **Maturity** TRLs | TRL 1-9 wie im Dokument definiert, soweit nicht fachspezifisch andere TRLs definiert wurden. |

Eine weitere wichtige Kategorisierung adressiert die Einsatzdomäne der Software. Diese besitzt allerdings sehr viele verschiedene Ausprägungen, zum Beispiel Medizintechnik, Materialwissenschaften, Geologie, Biologie, Astrophysik, Psychologie, etc., weshalb auf eine vollständige Auflistung verzichtet wird. Dennoch ist die Einsatzdomäne wichtig, wie das Beispiel von Software zeigt, die im Gesundheitseinrichtungen eingesetzt wird, und durch durch Seiteneffekte oder Sicherheitslücken zum IT-Ausfall der Einrichtung oder Fehlfunktionen von kritischen Medizinprodukten führen kann \- ohne das die Software selbst eine kritische Zweckbestimmung hat. Die einzelnen Kategorien haben also Wechselwirkungen: Beispielsweise hat die Rolle bzw. Zweckbestimmung der Software Einfluss auf die Kritikalität: Embedded Control Systems können unmittelbar Einfluss auf Auswirkungen auf Güter oder Gesundheit haben.

Eine feingranulare Kategorisierung erfüllt weitere Zwecke über die Auswahl geeigneter Entwicklungsmethoden hinaus. Sie ermöglicht eine präzisere Wertschätzung der Software und ihrer Entwickler. Zudem erleichtert sie die Beurteilung von extern entwickelter Forschungssoftware und unterstützt Entscheidungsprozesse bei der Auswahl solcher Software. Darüber hinaus trägt die Kategorisierung dazu bei, die langfristig benötigten Ressourcen für die Entwicklung besser einzuschätzen.

# 

# Anhang B: Checkliste für die Weitergabe von Software  {#anhang-b:-checkliste-für-die-weitergabe-von-software}

Die folgende Checkliste dient als Grundlage zur Definition und Weitergabe von Software-Lizenzen unter der Annahme, dass die Software komplett in der eigenen \[\[ Universität | Hochschule | Forschungszentrum\]\] erstellt wird. Im Fall externer Beteiligter mit eigenem Interesse an Software-Lizenzen ist eine gemeinsame Vorgehensweise sinnvoll.

|  | Urheber und Rechte Dritter *„Alle Urheberrechte müssen bei \[\[der Universität | Hochschule | dem Forschungszentrum\]\] liegen“ und „Alle Urheber:innen müssen bekannt sein“* |
| ----- | :---- |
| ☐ | Alle Urheber:innen der Software sind bekannt und benannt. |
| ☐ | Alle Urheber:innen haben als Mitarbeiter:innen \[\[der Universität | Hochschule | des Forschungszentrums\]\] programmiert und die Nutzungsrechte liegen bei \[\[der Universität | Hochschule | dem Forschungszentrum\]\]. **Falls Nein:** |
| ☐ | \-	Dritt-Institutionen bzw. Personen (z.B. Studierende) sind bekannt. |
| ☐ | \-	\[\[der Universität | Hochschule | dem Forschungszentrum\]\] liegen Nutzungsrechte dieser Institutionen bzw. Personen in schriftlicher Form vor. |
|  | Die Nutzungsrechte sind unter einer kompatiblen Open Source Lizenz lizenziert: **Weiter unter Kompatibilitäten** |
|  |  |
|  | **Vertragliche Bindungen** |
|  ☐ | Bedingungen zu Publikation und Weitergabe von Software aus Förder- oder Zuwendungsvorgaben, Kooperationsverträgen, und Grant Agreements sind bekannt und werden eingehalten.  |
|  ☐  | Bedingungen aus Arbeitsverträgen sind bekannt und werden eingehalten. |
| ☐ | Es ist bekannt, ob und wo die Software als Background in Projekten eingebracht ist. |
| ☐ | Gesetzliche Vorgaben und Normen (z.B. bei medizinischer Software) und ihre Limitationen sind eingehalten. |
| ☐ | Die Regelungen zur Exportkontrolle wurden geprüft und werden eingehalten. |
|  |  |
|  | **Kompatibilitäten** |
| ☐ | Die Software wurde ohne Einbindung von vorbestehenden Softwareteilen oder Bibliotheken geschrieben. **Falls Nein:** |
|  ☐ | \-	Die Lizenzbedingungen der vorbestehenden/veränderten Software bzw. der verknüpften Bibliotheken sind bekannt und Kompatibilitäten werden beachtet. |
|  ☐ | \-	Falls für die Lizenzierung/Weitergabe der eigenen Software eine kostenpflichtige Entwicklerlizenz für die vorbestehende Software/Bibliothek benötigt wird, liegt diese vor. |

|  | Transferweg, Verwertung |
| ----- | :---- |
| ☐ | Die Zielgruppe ist bekannt. |
| ☐ | Das Interesse und die Zielsetzung der Entwickler:innen ist bekannt. |
| ☐ | Die zukünftige Nutzung/Behandlung und Zugänglichkeit der Software im Institut ist geklärt. |
| ☐ | Die Zustimmung der \[\[Forschungsverantwortlichen | Institutsverantwortlichen\]\] liegt vor und ein entsprechender Freigabeprozess wurde eingehalten. |
|  |  |
|  | **Lizenzwahl** |
| ☐ | Es ist geklärt, welches Maß an Zugriff die Urheber auf die Software zulassen wollen (source code oder object code). |
| ☐ | Es ist entschieden, ob die Software proprietär oder als Open Source Software weitergegeben werden soll. |
|  ☐ | **Für Open Source Software Lizenzen:** Die ausgewählte Lizenz entspricht den in den hauseigenen Richtlinien oder zumindest den „approved licenses“ (siehe Seite der Open Source Initiative https://opensource.org/) **Falls Nein:** |
| ☐ | \-	Es wurde Rücksprache mit den Ansprechpersonen \[\[der Universität |       Hochschule | des Forschungszentrums\]\] bzgl. einer proprietären Lizenz       gehalten. |
|  ☐ | **Für Open Source Software Lizenzen:** Der Text der ausgewählten Lizenz wurde gelesen und verstanden und passt zur Zielgruppe und zur Zielsetzung der Weitergabe. **Falls Nein:** |
| ☐ | \-	Es wurde Rücksprache mit den Ansprechpersonen \[\[der Universität |      Hochschule | des Forschungszentrums\]\] bzgl. einer proprietären Lizenz       gehalten. |

**Erläuterungen zur Checkliste**

Grundsätzlich stehen zwei Aspekte in rechtlicher Hinsicht im Vordergrund. Bestehende Rechte \[\[der Universität | der Hochschule | des Forschungszentrums\]\] an der Software vor Lizenzierung und die Rechte, die ein Dritter durch die Lizenzierung erhalten soll.

Bevor eine \[\[an der Universität | an der Hochschule | am Forschungszentrum\]\] entwickelte Software weitergegeben und dabei mit einer Lizenz versehen werden kann, muss sichergestellt werden, dass \[\[die Universität | Hochschule | das Forschungszentrum\]\]  die Verwertungsrechte daran hält. Die Leitlinie beschreibt die dazu notwendigen Vorkehrungen.

Weiterhin müssen die rechtlichen Rahmenbedingungen geklärt werden. Dies betrifft insbesondere Vorgaben durch Förderbedingungen, welche z.B. eine Veröffentlichung als Open Source Software erzwingen, aber auch ausschließen können.

Software unterliegt unter Umständen einer Exportkontrolle, wenn diese in kritischer Form (z. B. für militärische Zwecke oder zur digitalen Überwachung) Verwendung finden kann. In solchen Fällen ist zu prüfen, ob es grundsätzlich einer Exportgenehmigung durch das Bundesamt für Wirtschaft und Ausfuhrkontrolle (BAFA) bedarf. Beinhaltet die Software direkt oder indirekt internationale Beiträge, muss neben dem europäischen auch das Exportkontrollrecht dritter Staaten berücksichtigt werden. Nach dem europäischen und US-amerikanischen Exportkontrollrecht gelten Ausnahmen für allgemein zugängliche Technologien, zu denen insbesondere Open Source Software zählt, wenn sie frei im Internet abgerufen werden kann. \[\[Die Universität | Hochschule | Das Forschungszentrum\]\] hat hierfür ein Merkblatt mit Verweisen auf Verweisen einschließlich Information zur Rechtsabteilung erarbeitet, das unter der RSE-Webseite zu finden ist.

Kann ein Teil der Fragen nicht befriedigend beantwortet werden, so empfiehlt sich eine Beratung durch die auf der RSE-Webseite \[\[der Universität | Hochschule | des Forschungszentrums\]\] genannten Ansprechpartner.

# 

# Anhang C: Grundlagen und Mitwirkende  {#anhang-c:-grundlagen-und-mitwirkende}

Die hier vorliegenden Leitlinien wurden auf Basis des

# GI- und de-RSE-Vorschlag für  Leitlinien zur effizienten Entwicklung von qualitativ hochwertiger und langlebiger Forschungssoftware an Universitäten, Hochschulen und Forschungseinrichtungen

erstellt. Mitwirkende hierfür waren:

* Andreas Czerniak, Universität Bielefeld  
* Adrian Ehrenhofer, TU Dresden  
* Bernadette Fritzsch, Alfred-Wegener-Institut,   
  Helmholtz-Zentrum für Polar- und Meeresforschung Bremerhaven  
* Maximilian Funk, Max-Planck-Gesellschaft e.V., Generalverwaltung München  
* Florian Goth, Universität Würzburg  
* Reiner Hähnle, TU Darmstadt  
* Carina Haupt, Deutsches Zentrum für Luft- und Raumfahrt (DLR)  
* Marco Konersmann, RWTH Aachen  
* Jan Linxweiler, TU Braunschweig  
* Frank Löffler, Friedrich-Schiller-Universität Jena  
* Alexander Lüpges, RWTH Aachen  
* Sebastian Nielebock, OVGU Magdeburg  
* Bernhard Rumpe, RWTH Aachen  
* Ina Schieferdecker, TU Berlin   
* Tobias Schlauch, Deutsches Zentrum für Luft- und Raumfahrt (DLR)  
* Robert Speck, Forschungszentrum Jülich GmbH  
* Alexander Struck, Humboldt-Universität zu Berlin   
* Jan Philipp Thiele, Weierstrass Institut Berlin  
* Matthias Tichy, Universität Ulm  
* Inga Ulusoy, Scientific Software Center, Universität Heidelberg

Wir danken Patrick Brunner, Christian Busse, Rene Caspart, Andreas Czerniak, Jan Philipp Dietrich, Adrian Ehrenhofer, Hans Fangohr, Michael Goedicke, Yves Vincent Grossmann, Wilhelm Hasselbring, Dorothea Iglezakis, Stephan Janosch, Jan Kapunkt, Uwe Konrad, Leen Lambers, Anna-Lena Lamprecht, Axel Loewe, Myriam Lipprandt, Azzouz-Thuderoz Maxence, Heinz Pampel, Barbara Paech, Lutz Prechelt, R.M. Raschkowski, Dirk Riehle, Rainer Röhrig, Philipp Schaefer, Carsten Scharfenberg, Birgit Schulze, Martin Sievers, Jörg F. Unger, Harald von Waldow und Philipp Zumstein sowie vielen weiteren anonymen Kommentierenden, die mit konstruktiven Beiträgen  und Kommentaren an diesem Dokument mitgewirkt haben.

Als Ansprechpartner für Kommentare und Hinweise dient aktuell die Koordination der Arbeitsgruppe „Software-Leitlinien“, Sebastian Nielebock, Bernhard Rumpe, Inga Ulusoy, erreichbar unter der Funktionsadresse   
			[rse-entwicklungs-leitlinien@gi.de](mailto:rse-entwicklungs-leitlinien@gi.de). 

Weiterführende Informationen, praktische Beispiele, ein Glossar und Akronyme, etc. sind auch zu finden unter:  
			 [https://github.com/gi-ev/RSE-software-entwicklungs-leitlinien](https://github.com/gi-ev/RSE-software-entwicklungs-leitlinien)

[image1]: <data:image/png;base64,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PmEwGAyGKkekUdaNdhxT+QOOHz8+kiYdX3/99YgN/uc///GOP/74ErbevXtH0r3yyisRWyHzoIMOitiKkSVriqG6Y1ki+cMOLzJtMBgMhsJApFHWjXYcN99882B/0qRJ3jnnnBNJk45TpkyJ2GA6AXfjjTdG0k2ePDliK2T2798/YitG6rpiMBgMBoOhahBplHWjHcewgIMHH3yw29aqVcu76KKLvPnz53t7772387hdd9113ogRI9x58cBtu+22XuPGjb3tttvOe+mllwIB9/DDD3u77LKLN2zYMO+EE07w2rVrV+I+4oF78sknvXPPPdcd4+U66aSTXBmwcY+tttrKe/XVV70DDzzQO/bYY72XX37ZO+aYY1ze3XbbzatXr54r10477eRsW265pXfNNdd4zz//fHCv2rVrB/vrrbeet2DBApfn7rvv9g4//HCvbt263j333OPykubQQw/17rzzTve5/v73vzubeOA23nhj76677vL22msvdy1slOGdd97xHnvsMa9nz57OtvXWW3sXX3xxic9cCNR1xWAwGAwGQ9Ug0ijrRjuOiJArrrjCEWHUvn17Z0d0sX3xxRe9PfbYI0jPjGW2iKuFCxd6nTp1csetW7d2YksE3O677+48epxL54ELC7jly5e7fcTk4sWLvRYtWnjbb7+9u8emm27qzjVv3tz76quv3P7666/vtoi6FStWuP2jjz7abUWEhUn6UaNGuWvvu+++rsw77LCD69pFaC1atMilu+yyy9wWASd5uQdbEXA33HCD2yJk+e4HDRrkrb322kH6k08+ucS20KjrisFgMBgMhgKBbrTjqD1wwn/84x9ue/3113sNGjQI7HXq1HFbxNXAgQO9Dh06eB999FFABNyOO+7o/eUvf/Heffddl7Y0ASe2/fff3207d+7shBX3EI+gCEW4zjrruC3dveF7Y0sn4PDanXnmmc7L1rZtW/cZrr32WncOD5y+RljA4X1kKwIOb6Cc22STTdzn4PNKfvHA/fOf/4yUoxCo64rBYDAYDIYCgW6041iagENESfckRNCJHc/VBx984I4RXWeccUbggUPo/PWvf3Xnbr755sj1K0PA7bnnnt6SJUvc/pVXXum26QTc1KlTnScPb9q8efOcRw7hybktttgi8Ozde++9bhsn4PiMeP06duzoPHBDhw4t4YGTLlcTcAaD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x48fX0J4sdg2AUPD6ViMW44JEir7LKI9cODA4JjrTJo0yVu4cGFgg5988on7p4H9pUuXui3BSWUtR0hEef6pMAFnKAboOmDMP/UzSaRrL3WjbTQKCw26gsdx7733dttLL73Uiairr77aHW+xxRZe9+7dvW7durlI3yzZIt6sevXqeQ8++KATWTvttJOztWnTxm1Z+oVlYTbZZBMXZbx///7e559/7h166KHuGiwPo8vw6KOPllhK5tZbb3Vp2T/55JO9J554wttwww1dXqKNs3YgAoBySR7KSZnYv+WWW5znaeuttw4EHELw4osvduW766673Ll9993XnSPeEgtBU4Zzzz3XiQgimB9zzDEuDhP55D7/+9//XN7wOoUVpX5+cdB548jnkkjsf//7390WkXv88ce7fb5DludBcImIOuOMM9wWUd2rVy9v0aJFLg7Vf/7zH2e/4oor3JbvS65LGvZlEe369eu7AKQsxn3ddde575vnzznWg0RAItxEcG+//fZuoW/E5j//+U8n/CRCfTFRPytD9Ydfz3/R9cCYV67QzySRLmqDbrSNRmGhIU0lz8g111zTeVMQKnSD0phiZzkXvC4Isddee815VGrXru3OHXfccd5uu+3mzl922WXO1qxZM7d9/fXXXfcrDbhfFCcOEHn33Xef8+7hXdNl+O9//+udddZZwTFBK0XA7bfffm574YUXui0i7sYbb3TXFdE3btw41+gj3DhmKRm8PXiFEHCINsTYvHnznEil7KRDNOARGj58uBMifB7u++6773p169Z1i17zuVn6hvSdO3cOlrlhWRyEqf4s5aF+fnHQeeN47733Ou8Y5HPxHaUTcBMmTHDCNez1ku8IwUUd6dixo/OyiqdUBJykgwhftp06dXJbBDXXRWjz/ZIfNm3a1Ak4Fu0mHSL98ccfd/VFBGeuvZ65oH5WBoOhQKAbbaNRmAdkdRPdsMQR0UNjzLItHJ966qneCy+84D3//PPueIMNNnACTIgNASfek1atWrmtCLh99tknuDbpEVrrrLNO5BphIuAQV3TjiZcvk4DD24OIQggi0rj+aaed5s6FBZxc2/86XFqJZP7Xv/7ViVUpC6IFASceKD4/Hj/yiWdJxtadcMIJ3uabbx7kZd1B/VnKQ/384qDzZiJlxmspx3jCDjnkEPdsxbuFOEXAjR07Nki31lpr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>