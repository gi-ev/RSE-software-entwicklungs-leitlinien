# GI- und de-RSE Muster-Leitlinie für die effiziente Entwicklung von Forschungssoftware {#gi-und-de-rse-muster-leitlinie-für-die-effiziente-entwicklung-von-forschungssoftware}
**FINAL V1.0**

![Titelseite](./images_ger/frontpage.png)

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

*Ende Anmerkungen\]\]

## Inhaltsverzeichnis

[Präambel: Zweck dieser Muster-Leitlinie](#praeambel-zweck-dieser-muster-leitlinie)

[Nutzung der Muster-Leitlinie & Lizenz](#nutzung-der-muster-leitlinie-lizenz)

[Mitwirkende und Dank für die Mitarbeit](#mitwirkende-und-dank-für-die-mitarbeit)

[Wichtigste genutzte Quellen](#wichtigste-genutzte-quellen)

[1 Executive Summary (für Entscheidende)](#1-executive-summary-für-entscheidende)

&ensp; [1.1. Lesehinweise](#11-lesehinweise)

[2 Einleitung](#2-einleitung)

&ensp; [2.1. Charakteristika von Software, speziell Forschungssoftware](#21-charakteristika-von-software-speziell-forschungssoftware)

&ensp; [2.2. Charakteristika von Research Software Engineering](#22-charakteristika-von-research-software-engineering)

&ensp; [2.3. Aufgaben der Leitlinie](#23-aufgaben-der-leitlinie)

&ensp; [2.4. Abgrenzung, Nicht-Aufgabe der Leitlinie](#24-abgrenzung-nicht-aufgabe-der-leitlinie)

&ensp; [2.5. Damit abgestimmte Rahmen Guidelines for Safeguarding, Good Research Practice, Code of Conduct-Bedingungen](#25-damit-abgestimmte-rahmen-guidelines-for-safeguarding-good-research-practice-code-of-conduct-bedingungen)

&ensp; [2.6. Fazit](#26-fazit)

[3 Fachliche Leitlinien der Softwareentwicklung](#3-fachliche-leitlinien-der-softwareentwicklung)

&ensp;[3.1. Einleitung](#31-einleitung)

&ensp;&ensp;[3.1.1. Forschungssoftware: Demonstrator, Produkt, Infrastruktur](#311-forschungssoftware-demonstrator-produkt-infrastruktur)

&ensp;[3.2. Kategorisierung von Forschungssoftware](#32-kategorisierung-von-forschungssoftware)

&ensp;&ensp;[3.2.1. Art der Software bzw. Softwarekomponente (Dimension Art)](#321-art-der-software-bzw-softwarekomponente-dimension-art)

&ensp;&ensp;[3.2.2. Nutzungsgrad der Software bzw. Softwarekomponente](#322-nutzungsgrad-der-software-bzw-softwarekomponente-dimension-ng)
[(Dimension Ng)](#322-nutzungsgrad-der-software-bzw-softwarekomponente-dimension-ng)

&ensp;&ensp;[3.2.3. Einordnung in die Technology Readiness Levels (TRL) entsprechend der EU](#323-einordnung-in-die-technology-readiness-levels-trl-entsprechend-der-eu)

&ensp;&ensp;[3.2.4. Anwendungsklassen](#324-anwendungsklassen)

&ensp;&ensp;[3.2.5. Status der Software](#325-status-der-software)

&ensp;&ensp;[3.2.6. Weitere Einflüsse](#326-weitere-einflüsse)

&ensp;[3.3. Minimalanforderungen an Kernkompetenzen, Entwicklungsprozesse und Projektplanung in der Softwareentwicklung](#33-minimalanforderungen-an-kernkompetenzen-entwicklungsprozesse-und-projektplanung-in-der-softwareentwicklung)

&ensp;&ensp;[3.3.1. Minimalanforderungen an den Technologie-Reifegrad auf Basis des Nutzungsgrads (Ng) und der Softwareart (Art)](#331-minimalanforderungen-an-den-technologie-reifegrad-auf-basis-des-nutzungsgrads-ng-und-der-softwareart-art)

&ensp;&ensp;[3.3.2. Minimalanforderungen an Handlungsfelder und notwendige Kernkompetenzen in der Softwareentwicklung auf Basis des Technologie-Reifegrads](#332-minimalanforderungen-an-handlungsfelder-und-notwendige-kernkompetenzen-in-der-softwareentwicklung-auf-basis-des-technologie-reifegrads)

&ensp;[3.4. Methodische Grundlagen der Softwareentwicklung](#34-methodische-grundlagen-der-softwareentwicklung)

&ensp;&ensp;[3.4.1. Softwareentwicklungsprozesse](#341-softwareentwicklungsprozesse)

&ensp;&ensp;[3.4.2. Qualitätsmanagement (Testen, Validierung, etc.)](#342-qualitätsmanagement-testen-validierung-etc)

&ensp;&ensp;[3.4.3. Anforderungen verstehen](#343-anforderungen-verstehen)

&ensp;&ensp;[3.4.4. Softwarearchitektur](#344-softwarearchitektur)

&ensp;&ensp;[3.4.5. Softwaremodellierung](#345-softwaremodellierung)

&ensp;&ensp;[3.4.6. Versionierung](#346-versionierung)

&ensp;&ensp;[3.4.7. Testkonzept und -Automatisierung](#347-testkonzept-und-automatisierung)

&ensp;&ensp;[3.4.8. Management der Software-bezogenen Daten und Datengrundlage](#348-management-der-software-bezogenen-daten-und-datengrundlage)

&ensp;&ensp;[3.4.9. Best Practices, Design Pattern, Issue-Tracking, Coding Guidelines](#349-best-practices-design-pattern-issue-tracking-coding-guidelines)

&ensp;[3.5. Technische Grundlagen](#35-technische-grundlagen)

&ensp;&ensp;[3.5.1. Git Versionsverwaltungssystem](#351-git-versionsverwaltungssystem)

&ensp;&ensp;[3.5.2. Continuous Integration / Continuous Delivery](#352-continuous-integration-continuous-delivery)

&ensp;&ensp;[3.5.3. Test-Frameworks](#353-test-frameworks)

&ensp;&ensp;[3.5.4. Verbreitung / Dissemination](#354-verbreitung-dissemination)

&ensp;&ensp;[3.5.5. Software Discovery](#355-software-discovery)

## 4. **Lizenz-Vergabe und -Nutzung (Juristische Absicherung)** {#4-lizenz-vergabe-und-nutzung-juristische-absicherung}

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


### **4.1. Wissenschaftliche Verwertung und Lizenzwahl \-- Allgemeines** {#41-wissenschaftliche-verwertung-und-lizenzwahl--allgemeines}


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

Nur wenn \[\[die Universität | die Hochschule | das Forschungszentrum\]\]  die notwendigen Nutzungs- und Verwertungsrechte an der Software besitzen, kann diese unter Beachtung ggf. vorbestehender Lizenzbedingungen weitergegeben werden. Bei gemeinsam entwickelten Werken ist eine Weitergabe zum Beispiel im Konsortialvertrag bzw. mit Projektpartnern abzustimmen.

Die Wahl der Lizenz obliegt dabei der Inhabenden der Verwertungsrechte. Je nach Vertragsverhältnis ist dies \[\[die Universität | die Hochschule | das Forschungszentrum\]\] oder die Urheber:innen z.B. im Falle eines verbeamteten Hochschullehrenden \[BMBF23\]. Das Recht der Lizenzwahl und der Veröffentlichung kann bei Bedarf an die Projektverantwortlichen, Führungskräfte und Software-Entwickler:innen delegiert werden. Bei Fragen und Unklarheiten zur Weitergabe von Software oder zur Lizenzwahl können sich Software-Entwickler:innen und Projektbeteiligte an die auf \[\[der RSE-Webseite\]\] genannten Ansprechpersonen \[\[der Universität | der Hochschule | des Forschungszentrums\]\] wenden, um gemeinsam die jeweilige Situation zu analysieren und die bestmögliche Lösung zu finden.

Sowohl bei Softwareabhängigkeiten als auch bei mehreren Parteien, die existierende Software in eine Zusammenarbeit einbringen, ist es notwendig, auf die Kompatibilität der Lizenzen zu achten. Wenn möglich, sollten deswegen gleiche Lizenzen gewählt werden. Wird Software in Kooperationsprojekte eingebracht, ist diese entweder allgemeingültig oder projektspezifisch vor der Weitergabe an Partner mit einer Lizenz zu versehen, da Software auch in Kooperationen nicht ohne Einräumung expliziter Nutzungsrechte genutzt werden darf.

Regelungen zu Verwertungsrechten der Beitragenden an der Software in Kooperationsprojekten können in einem Contributor License Agreement (CLA) festgelegt werden; bzw. (eher in Sonderfällen) einer Vereinbarung zur Übertragung von ausschließlichen Verwertungsrechten in einem Copyright Assignment Agreement (CAA). Dies ermöglicht den Einbringenden von Software in Kooperationsprojekte die gesamten Verwertungsrechte auch im Fall von Beiträgen Dritter beizubehalten, um eine spätere Umlizensierung zu vereinfachen. Solche Regelungen haben jedoch eine abschreckende Wirkung auf Beitragende, da eine Umlizenzierung ggf. nicht in ihrem Interesse ist. Weiterhin bringt das Eingehen solcher Vereinbarung verwaltungstechnischen Aufwand mit sich.

### **4.2. Anmerkungen zur wirtschaftlichen Verwertung** {#42-anmerkungen-zur-wirtschaftlichen-verwertung}


Bei der Wahl der Lizenzierung und vor allem der Restriktionen sollten mehrere Einflussfaktoren beachtet werden:

1. Die Erlöse aus der Verwertung können der Finanzierung der eigenen Forschung dienen.
2. Eine wirtschaftliche Verwertung in Zusammenarbeit mit der Industrie fördert den Transfer von Forschungsergebnissen in die Praxis.
3. Eine wirtschaftliche Verwertung von Software bringt so gut wie immer eine Gewährleistungspflicht mit sich, die wissenschaftliche Einrichtungen regelmäßig nicht erbringen können oder wollen.
4. Eine proprietäre Lizenzierung kann die praktische Reproduzierbarkeit von wissenschaftlichen Ergebnissen unter Benutzung dieser Software durch andere erschweren.
5. Eine reine kommerzielle Lizenzierung diskriminiert Wissenschaffende mit weniger finanziellen Mitteln, z.B. in verschiedenen Teilen der Welt.

Einer der heute üblichen und durchaus empfohlenen Vermarktungswege für Software im kommerziellen Bereich ist es, die Software kostenlos allgemein zur Verfügung zu stellen, um so einen Nutzendenstamm aufzubauen und damit die Software erst auszuhärten, abzusichern und ggf. dabei zu verallgemeinern. Ein Startup kann dann auch Ergänzungen, Weiterentwicklungen oder Support kommerzialisieren, ohne die Kernsoftware selbst vermarkten oder besitzen zu müssen.

Software funktioniert in der Kommerzialisierung anders als viele andere Produkte. Im Bereich von Software-Startups gilt ein massiver und globaler Verdrängungswettbewerb, weshalb “Größe vor Revenue” steht und oft in größeren Ausmaß Investoren nötig sind, um die Software als robustes Produkt verfügbar zu machen, die über die ersten Jahre hinweg keine Erträge erwarten. Dies ist in Deutschland leider aktuell nicht sehr ausgeprägt, und für den beschränkten Markt wissenschaftlicher Software noch komplexer, weshalb empfohlen wird, Impact direkt über Open-Source-Lizenzen zu generieren und allenfalls eine duale Lizenzierung (siehe 4.3.4) oder den Open Core Ansatz für ein Startup zu nutzen. Revenue wird von Seiten \[\[der Universität | der Hochschule | des Forschungszentrums\]\] in so einem Fall nicht erwartet.

### **4.3 Lizenz-Arten** {#43-lizenz-arten}


Es werden freizügige (permissive) Open Source Lizenzen, Copyleft Open Source Lizenzen sowie proprietäre Lizenzen und ihre Auswirkungen auf die Verwendbarkeit von Software skizziert. Die Creative Commons Lizenzen sind nicht für Software geeignet und werden daher nicht behandelt. \[CC24\]

#### **4.3.1 Open Source Lizenzen** {#431-open-source-lizenzen}


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

1. Wie wird die Software weitergegeben (Source Code oder object code)?
2. Wer darf die Software nutzen? Wer darf die Software weiterentwickeln?
3. Müssen Veröffentlichungen von Weiterentwicklungen die gleiche Lizenz benutzen?
4. Wie ist die Nutzung zu dokumentieren (Veröffentlichung zitieren, Lizenz nennen)?

Auf der oben genannten RSE-Webseite sind Lizenztexte und aktuelle Informationen zu den empfohlenen Open Source Lizenzen sowie Tools für Kompatibilitätschecks verlinkt.

\[\[Variante A1\]\]
Es wird dringend davon abgeraten, neue Lizenzen zu definieren oder von vorhandenen Lizenztexten ohne wichtigen Grund abzuweichen. Angepasste Lizenztexte dürfen den Namen der Standardlizenz nicht mehr verwenden. Die Verwendung einer neuen Lizenz führt leicht zu Inkompatibilitäten mit den Lizenzen anderer Software, Reputationsverlust durch "noch eine neue Lizenz" oder Hürden, weil neue Lizenzen von potentiellen Nutzenden erst noch geprüft werden müssen.
\[\[Variante A2\]\]
Neue Lizenzen oder Lizenzänderungen müssen mit der Rechtsabteilung bzw. dem Justiziariat abgesprochen werden.
\[\[Ende Varianten A\]\]

#### **4.3.2 Permissive Open Source Lizenzen** {#432-permissive-open-source-lizenzen}


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

#### **4.3.3 	Copyleft Open Source Lizenzen (Best Practice Beispiele)** {#433-copyleft-open-source-lizenzen-best-practice-beispiele}


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

#### **4.3.4 	Proprietäre Lizenzen** {#434-proprietäre-lizenzen}


Wird eine stärker individuell ausgestaltete Lizenz angestrebt, weil z. B. die Weitergabe des Codes bzw. die Art der Verwendung der Software eingeschränkt werden soll, empfiehlt \[\[die Universität | die Hochschule | das Forschungszentrum\]\] dafür entweder nur eine einzige proprietäre Lizenz zu verwenden oder im Dual-Licensing eine solche neben einer Open Source Lizenz anzubieten.

Eine **Proprietäre Lizenz** ist eine individuell definierte Regelung, die alle aktuellen und zukünftig möglichen Nutzungsformen sowie Weitergaben, Konfigurations- und Entwicklungsoptionen adressiert. Sie beschreibt i.A. auch individuelle Pflichten der Gewährleistung, der Nachbesserung und der Aktualisierung durch neue Softwareversionen.

Möglich sind dabei auch Kombinationen (Dual License), die z.B. der Forschung und Lehre eine Open Source Lizenz mit Copyleft zur Verfügung stellen und für eine kommerzielle Nutzung kostenpflichtige Vertragsmodelle definieren. Solche Dual License Modelle können im Bedarfsfall auch ergänzend gebildet werden, nachdem zunächst eine Open Source Lizenz gewählt wurde und später doch der Wunsch nach einer Kommerzialisierbarkeit auftritt. Für eine Umlizenzierung müssen aber alle Entwickelnden, die zu der Software beigetragen haben, zustimmen, soweit kein CLA oder CAA vorliegt.
Bei der Nutzung von Software unter einer Dual License ist jedoch Vorsicht geboten. Wenn Forschungsprojekte kommerziellen Charakter annehmen, können ggf. Lizenzgebühren anfallen.

Die Erstellung und Verhandlung jeglicher Lizenzverträge, die eine proprietäre Nutzung einräumen, werden \[\[an der Universität | an der Hochschule | am Forschungszentrum\]\] federführend von \[\[Unternehmensentwicklung | Juristische Abteilung | Drittmittelabteilung | Transferabteilung \]\] verantwortet. Ist eine proprietäre Lizenzierung gewünscht, wird gemeinsam mit \[\[dem Institut | der Forschungseinrichtung\]\] über mögliche Lizenzkonditionen, vertragliche Rahmenbedingungen, die Situation geistigen Eigentums usw. beraten und ein entsprechender Lizenzvertrag aufgesetzt. \[\[Das Institut | die Forschungseinrichtung\]\]  kann dabei einen Vorschlag erstellen oder eine Vorlage nutzen.

### **4.4. Beratungsangebote und Vorgehensweise zur Auswahl** {#44-beratungsangebote-und-vorgehensweise-zur-auswahl}


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

### **4.5. 	Nutzung von Software Dritter** {#45-nutzung-von-software-dritter}


Wenn in der entwickelten Software Komponenten oder Codestücke enthalten sind, die durch Dritte geschrieben wurden, sind diese urheberrechtlich geschützt und werden in den meisten Fällen bereits eine Lizenz haben. Ist keine Lizenz vergeben, so werden auch keine Rechte eingeräumt. Die Komponente bzw. der Code darf daher nicht genutzt werden. Es besteht die Gefahr, dass der Rechteinhaber Schadensersatz gegen den Nutzer von nicht lizenzierter Software geltend macht.

#### **4.5.1. Rechte und Pflichten durch Lizenzen** {#451-rechte-und-pflichten-durch-lizenzen}


Wie jeder Vertrag regeln Lizenzen Rechte und Pflichten, welche für gängige Open Source Lizenzen in 4.3 beispielhaft beschrieben sind. Es ist wichtig, neben der erlaubten Nutzung auch immer die Pflichten im Auge zu behalten und einzuhalten.

Bei Nicht-Einhalten der Pflichten handelt es sich nicht nur um die Verletzung der guten wissenschaftlichen Praxis, sondern um einen Lizenzverstoß. Die Nutzungsrechte entfallen und der Lizenzinhaber kann zivilrechtliche Schritte einleiten (Schadensersatz). Eine gerichtliche Verfolgung ist bisher nur bei Lizenzverstößen von kommerziellen Verwertern bekannt. Allgemein üblich ist die Bitte um Behebung des Lizenzverstoßes.

Bei Open Source Lizenzen greifen die Pflichten erst bei der Weitergabe von Software (dazu zählt ggf. auch die Bereitstellung als Service). Der “Use” erlaubt die bestimmungsgemäße Nutzung der Software (Ablaufenlassen), ohne dass daran bereits Lizenzpflichten anknüpfen. \[\[Universitäten | Hochschulen | Forschungszentren\]\] sind normalerweise als juristische Person in Gesamtheit dazu berechtigt, so dass eine Weitergabe zwischen den Abteilungen erlaubt ist.

Trotzdem sollte die Lizenz bereits zum Zeitpunkt der Entscheidung des Einbaus von Software Dritter berücksichtigt werden, da diese die Möglichkeit zur Weitergabe der Software beeinflusst.

#### **4.5.2. Kompatibilität von Lizenzen** {#452-kompatibilität-von-lizenzen}


Bei der Nutzung von Softwarekomponenten mit unterschiedlicher Lizenz muss auf die Kompatibilität aller Lizenzen geachtet werden. Spätestens im Fall der Weitergabe oder Veröffentlichung kann es hier zu konkurrierenden Pflichten kommen. Vereinfacht lässt sich sagen: Es kann die Schnittmenge aller Rechte genutzt und es muss die Summe aller Pflichten eingehalten werden. So entbindet z.B. die Kombination von Komponenten unter permissiver und starkem Copyleft nicht davon, dass das gesamte Resultat unter starkem Copyleft veröffentlicht werden muss. Ebenso verhindert eine einzige Komponente, die eine Veröffentlichung ihres Quellcodes nicht erlaubt, die Veröffentlichung des Quellcodes als Gesamtpaket.

Eine genaue Prüfung ist in jedem Falle notwendig, da selbst Open Source Lizenzen miteinander inkompatibel sein können. Dies betrifft permissive sowie Copyleft und proprietäre Lizenzen, wobei Copyleft und proprietäre häufiger zu Inkompatibilitäten bzw. Einschränkungen bzgl. der Lizenzwahl führen können. Unterstützen können hierbei Kompatibilitätstabellen (wie z. B.  \[Wik24\]) oder auch Tools für Kompatibilitätschecks, wie sie auf der RSE-Webseite zu finden sind.

Im Zweifelsfall empfiehlt sich eine Beratung durch die auf der RSE-Webseite \[\[der Universität | Hochschule | des Forschungszentrums\]\] genannten Ansprechpartner.

## **5\. Unterstützungsleistungen durch \[\[die Universität | Hochschule | das Forschungszentrum | Einrichtung\]\]** {#5-unterstützungsleistungen-durch-die-universität-hochschule-das-forschungszentrum-einrichtung}


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

*Der nachfolgende Grundtext zur Auswahl und Gestaltung entsprechender Texte wurde weitgehend aus Sicht eines etablierten RSE-Zentrums formuliert\]\]  \[\[Ende Anmerkungen\]\*

Bereits vorhandene Infrastruktur wie die Bibliothek, das Rechenzentrum, die Rechtsberatung, und weitere forschungsnahe Dienstleistungen wie existierende Beratungs- und Schulungsangebote zu Forschungsdatenmanagement oder High-Performance-Computing werden bei der Umsetzung der Leitlinie eingebunden. Die zentrale koordinierende Anlaufstelle ist dabei \[\[das RSE-Zentrum | die RSE-Einrichtung | das Rechenzentrum | die Bibliothek | die Rechtsberatung | die Innvovations-Stelle | …\]\].

### **5.1. Personelle Unterstützung bei der Erstellung und Erweiterung von Forschungssoftware** {#51-personelle-unterstützung-bei-der-erstellung-und-erweiterung-von-forschungssoftware}


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

### **5.2. Unterstützungsleistungen bei der langfristigen Pflege von Software** {#52-unterstützungsleistungen-bei-der-langfristigen-pflege-von-software}


*\[\[Variante Zentrum\]\]*

\[\[Der Universität | Der Hochschule | Dem Forschungszentrum\]\] ist bewusst, dass im Einsatz befindliche Software anders als passive (gesammelte) und archivierbare Daten eine permanente Pflege und Aktualisierung benötigt. Die Veränderung des Software-Stacks, die Integration an neuen Schnittstellen, extern entwickelte Erweiterungspakete, neue Nachbarsysteme, aber auch Regularien und Cybersecurity erfordern aktive Pflege.

Grundsätzlich ist im Sinne der DevOps-Methodik (=”Integrierter Development und Operations-Lifecycle der Software”) der Übergang zwischen aktiver Entwicklung und langfristiger Pflege sowie die phasenweise immer wieder auftretende aktive Ergänzung fließend, weshalb sinnvollerweise zwischen Entwicklung und Pflege aus Sicht der Unterstützungsleistungen nicht grundsätzlich unterschieden wird. Das in Kapitel 3 eingeführte Zustandsmodell für Software zeigt die jeweiligen Zustandsoptionen. Ist die Software-Infrastruktur am Ende ihres Lebenszyklus angekommen, wird sie adäquat außer Dienst gestellt und langfristig nachhaltig archiviert.

Häufig ist die erwünschte Lebenszeit der Software deutlich länger als die finanzielle Förderung des Projekts, in dem sie entwickelt wurde. Für die Etablierung von Forschungssoftware als langfristig verfügbare Infrastruktur bietet das  RSE-Zentrum personelle Kapazitäten, um Software langfristig lauffähig und damit nachnutzbar zu halten.

*\[\[Ende Variante Zentrum\]\]*

### **5.3. Unterstützungsleistungen in der Weiterbildung** {#53-unterstützungsleistungen-in-der-weiterbildung}


Weiterbildungsangebote für Entwickler:innen finden sich auf der oben genannten RSE-Webseite.

Die Weiterbildungsangebote beinhalten unter anderem Einstiegsthemen wie Einführung in das Programmieren für in der Wissenschaft häufig verwendete Programmiersprachen, Versionskontrollsysteme, Erstellen und Strukturieren von Tests, Einführung in Continuous Integration und Kernthemen des Software Engineering zur effizienten Entwicklung, Nutzung von KIs/Copilots, Management von Reviews und Introspektionen, Architekturprinzipien, Agiler RSE-Entwicklungsmethodik auf Basis von z. B. Scrum, Umgang mit Verwaltungswerkzeugen wie GitLab/GitHub, Nutzung von Forschungs-Software-Management-Plänen, und Veröffentlichung und Dissemination von Forschungssoftware (s. Kapitel 3 zur Auswahl der Themen). Diese Softwareentwicklungs-Themen werden komplementiert durch andere fachübergreifende Angebote der oben genannten kooperierenden Einrichtungen.

Auf die Möglichkeit, viele dieser Weiterbildungsangebote bereits als Studierende wahrzunehmen, um so eine fundierte Ausbildung als Research Software Engineer in Kombination mit der eigentlichen Forschungsdomäne zu erhalten, wird hingewiesen. Nicht nur Studierende, auch Doktoranden und Postdoktoranden können \[\[ interne bis hin zu wissenschaftlich oder industriell anerkannte \]\] Zertifikate erwerben und so ihre Position und Wahrnehmung als Research Software Engineers stärken. Details hierzu finden sich auf der RSE-Webseite
	\[\[https://research-se.X-university.de\]\]
 bzw. der Webseite \[\[des Zentrum für Lehre und Weiterbildung | der Doctoral Graduate School \]\].

### **5.4. Würdigung der Research Software Engineers** {#54-würdigung-der-research-software-engineers}


\[\[Die Universität | Hochschule | Das Forschungszentrum\]\] unterstützt die Anerkennung der Leistungen der Research Software Engineers (RSEs), also der Personen, die professionell Forschungssoftware entwickeln, betreiben, weiterentwickeln und warten; und ihre akademische Leistungen zu Teilen oder vollständig der Forschungssoftware widmen. Viele RSEs sind selbst Wissenschaffende und planen eine akademische Karriere im eigenen Fachgebiet. Die Wertschätzung der Leistungen dieser RSEs ist auch daher wichtig und kommt diesem Fachgebiet zugute.

*\[\[Ausbaubar und ergänzbar: Nachfolgend exemplarisch Maßnahmen, die in der RSE Community als wertschätzend angesehen werden.\]\]*

* \[\[Die Universität | Die Hochschule | Das Forschungszentrum\]\] unterstützt gemäß \[DFG24\] die Anerkennung der Leistungen der RSEs je nach Beitragsleistung explizit durch die Sichtbarmachung der Ergebnisse in Form einer Nennung oder **Co-Autorenschaft in wissenschaftlichen Publikationen**. Unterstützt wird dies durch die Berücksichtigung von Software- und Datenpublikationen im wissenschaftlichen Reporting.

* \[\[Die Universität | Die Hochschule | Das Forschungszentrum\]\] unterstützt organisatorisch die Gründung von **wissenschaftlichen Nachwuchsgruppen** zu großen, langfristig angelegten Softwareprojekten mit entsprechenden Karrieremöglichkeiten für RSEs.

* \[\[Die Universität | Die Hochschule | Das Forschungszentrum\]\] bietet Schulungen mit professionellen **Zertifikaten** und unterstützt so die persönliche Entwicklung der RSEs.

* Durch das Herausstellen der RSEs und ihrer Software-Errungenschaften auf einer passenden Webseite oder in Research Software Directories wird die **Sichtbarkeit** der Leistungen und Beiträge der RSEs öffentlich gemacht und wertgeschätzt.

* \[\[Die Universität | Die Hochschule | Das Forschungszentrum\]\] fordert **Berufungskommissionen** auf, bei der Bewertung von Kandidat:innen eine explizite Einbeziehung von exzellenter Forschungssoftware als wissenschaftliches Ergebnis vorzunehmen.

* Durch die Vergabe jährlicher **RSE-Preise** in \[\[der Universität | Hochschule | dem Forschungszentrum\]\]  wird die Qualität der Software-Ergebnisse und das Engagement in der Community gewürdigt.

* Sowohl \[\[die Universität | Hochschule | das Forschungszentrum\]\] als auch die Forschergruppen, die RSEs einstellen, erkennen an, dass durch eine **Vernetzung** und bessere Integration der RSEs in die wissenschaftliche Community die Qualität der Forschungssoftware – und damit der Forschungsergebnisse – fundamental verbessert wird.

* In Absprache mit Fördergebern empfiehlt \[\[die Universität | die Hochschule | das Forschungszentrum\]\] die explizite Nennung von Softwareentwicklungs-Anteilen in Anträgen ("Wir beantragen Research Software Engineer" statt nur "wir beantragen Doktorand:in who Codes").

* \[\[Die Universität | Die Hochschule | Das Forschungszentrum\]\] bemüht sich, durch adäquate Bezahlung und ansprechende Arbeitsbedingungen ohne überbordende Bürokratie und mit einer gewissen wissenschaftlichen Freiheit exzellente RSEs langfristig im Wissenschaftssystem zu halten. Dabei erkennt \[\[die Universität | die Hochschule | das Forschungszentrum\]\] an, dass es sich bei RSEs um wissenschaftliches Personal handelt.

* \[\[Die Universität | Hochschule | Das Forschungszentrum\]\] erkennt Research Software Engineering als eigene Fachdisziplin an. Dies schließt den auch in anderen Disziplinen üblichen regelmäßigen **Austausch mit der Fachcommunity** außerhalb der Einrichtung ein. Daher wird zu Dienstreisen oder aktiver Vorbereitung von Konferenzen, Workshops, oder Ähnlichem explizit ermutigt.

* Ein wichtiger Bestandteil der Arbeit eines RSE besteht in der **Vertrautheit mit modernen Methoden, Werkzeugen und Softwareframeworks**. Daher sollten RSEs \[\[ der Universität | Hochschule | des Forschungszentrums\]\] sich im Rahmen ihrer vertraglichen Arbeitszeit selbständig in ebensolche **einarbeiten** und damit weiterbilden.

*\[\[Ende Ausbau\]\]*

### **5.5. Unterstützungsleistungen bei Lizenzen** {#55-unterstützungsleistungen-bei-lizenzen}


In Abschnitt 4.4. werden die Unterstützungsleistungen bei der Wahl von Lizenzen erklärt. Ansprechpartner und Empfehlungen sind der RSE-Webseite zu entnehmen.

### **5.6. Unterstützungsleistungen durch technische Services** {#56-unterstützungsleistungen-durch-technische-services}


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

### **5.7. Finanzierung der Unterstützungsleistungen bei der Entwicklung und Pflege von Software** {#57-finanzierung-der-unterstützungsleistungen-bei-der-entwicklung-und-pflege-von-software}


*\[\[Anmerkung für Leitlinienersteller/Hochschullleitungen: Die konkrete Ausgestaltung der Unterstützungsleistung und deren Finanzierung obliegt der Hochschule/ Forschungseinrichtung, ggf. in Koordination mit Land und Bund. Beispiele in den Niederlanden (eScience Center), UK (Sustainable Software Institute) existieren, sind aber universitätsübergreifend organisiert.\]\]*

→→ Für **Entscheidende und Leitende** ←←
\[\[Der Universität | Hochschule | Dem Forschungszentrum\]\] ist bewusst, dass Entwicklung, Pflege und Weiterentwicklung von Software ähnlich wie technische Infrastruktur (z. B. Gebäude, Anlagen) anders als passive, gesammelte Daten einen deutlichen, vor allem personellen Aufwand haben.

*\[\[Variante Zentrum\]\]*

Für die Etablierung von Forschungssoftware als langfristig verfügbare Infrastruktur bietet das  RSE-Zentrum personelle Kapazitäten, um Software über längere Zeit lauffähig und damit nachnutzbar zu halten. Zu der aktuell vorherrschenden und weiterhin nutzbaren Lösung, der Finanzierung kompletter Research Software Engineers innerhalb der Forschungseinrichtung ergänzt \[\[die Universität | Hochschule | das Forschungszentrum\]\] das Angebot zentral buchbarer RSE-Expert:innen des RSE-Zentrums.

Die Buchungsgrößen können sich auf wenige Tage Beratung bis hin zur langfristigen Abstellung kompletter Personen auf z. B. der Basis ganzer, halber und 20%-Stellen, beziehen und sind mit dem RSE-Zentrum abzusprechen. Die auftraggebende Forschungseinheit und RSE-Zentrum nehmen ein Pooling der Ressourcen für die langfristige Stellen- und Projektplanung vor. Gegenüber dem Fördergeber gelten die RSE-Expert:innen als Personalstellen und können als solche in Projekten beantragt werden.

Das RSE-Zentrum stellt diese Expert:innen im Bereich der wissenschaftlichen und technischen Softwareentwicklung mit unterschiedlich ausgeprägten Fähigkeiten zu den Aktivitäten des Programmierens, des Managements, der Pflege, der Qualitätssicherung und der (teilweise interdisziplinären) Kommunikation. Daneben werden Aktivitäten für die Weiterbildung unterstützt. Eine hohe forschungsfachliche Expertise ist wegen der hohen domänenspezifischen Diversität der Forschungsthemen im RSE-Zentrum nur begrenzt vorhanden und es wird erwartet, dass diese weiterhin in der Forschungseinheit verbleibt. Die Methodik zur erfolgreichen und effizienten Kollaboration und die Vertrautheit mit dem Ablauf wissenschaftlicher Projekte bringen die RSE-Expert:innen mit.

Zur Finanzierung der RSE-Expert:innen gibt es grundsätzlich folgende Optionen:

#### **5.7.1. Übernahme auf RSE-Zentrums-Kosten (“Universitäts-Software”)** {#571-übernahme-auf-rse-zentrums-kosten-universitäts-software}


Die originär erstellende Forschungseinrichtung stellt einen Antrag (siehe Antragsformular) an das RSE-Zentrum zur Übernahme der Softwarepflege. Abhängig von den in Kapitel drei beschriebenen Einordnungen (vor allem TRL, Nutzungsgrad) sowie weiteren Kriterien, wie Qualität und Verständlichkeit der Software und der strategischen Relevanz für die Universität wird aus der Menge der gestellten Anträge jährlich die leistbare Menge an Procurements für jeweils 5 Jahre übernommen. Am Ende der 5 Jahre wird neu entschieden. Die Auswahl übernimmt das RSE-Auswahlgremium.

#### **5.7.2 Übernahme auf Kosten der Forschungseinheit (“Instituts-Software”)** {#572-übernahme-auf-kosten-der-forschungseinheit-instituts-software}


Das RSE-Zentrum bringt substantielle personelle Ressourcen in die Pflege, Weiterentwicklung, Bug-Fixing und deren Management ein. Finanziert werden diese Ressourcen aber durch ein oder mehrere Institute/Forschungseinheiten. Bei der zu erwartenden Vielzahl an potentiellen Projekten muss auch hier eine Auswahl nach Verfügbarkeit und thematischer Expertise durch das RSE-Auswahlgremium stattfinden.

Es besteht die Möglichkeit, die hier zu buchenden Ressourcen in (1) Berufungs- oder Bleibeverhandlungen, (2) Forschungsanträgen an DFG, EU, BMBF, etc., (3) Stiftungen oder (4) direkt aus F\&E-Verträgen mit industriellen Auftraggebern zu integrieren. Insbsondere ist die DFG-Handreichung zum Umgang mit Forschungssoftware \[DFG22\] im Förderhandeln beachtenswert.

#### **5.7.3 Ausgestaltung der Unterstützung** {#573-ausgestaltung-der-unterstützung}


Unabhängig von der Finanzierung gibt es in Absprache zwischen RSE-Zentrum und Forschungseinheit(en) eine Reihe von organisatorischen Ausgestaltungsoptionen:

1. Wer trägt die zukünftige Verantwortung für entwickelte Forschungssoftware?  Die Forschungseinheit (bevorzugt), oder übernimmt die Pflege-Verantwortung das RSE-Zentrum.
2. Wer managt die Entwicklung/Pflege? Obwohl i.d.R. Forschende dies selbst tun, kann das RSE-Zentrum auf Wunsch und ggf. mit finanzieller Absicherung die organisatorische Durchführung in agiler Entwicklung (und damit eine Teilprojektleitung) übernehmen oder Research Software Engineers in ein vorhandenes Projekt entsenden.
3. Dissemination, Community Building: primär in der Fachcommunity durch die Forschungseinheit, ggf. mit Unterstützung des RSE-Zentrums
4. Ruhendes/Auslauf-Produkt: ist dann eine gemeinsame Entscheidung.

*\[\[Ende Variante Zentrum\]\]*

### **5.8. Weitere Unterstützungsleistungen** {#58-weitere-unterstützungsleistungen}


Weitere durch \[\[die Universität | die Hochschule | das Forschungszentrum | die Einrichtung\]\] angebotene Unterstützungsleistungen umfassen:

1. Beratung und Hilfestellung bei der Publikation von Forschungssoftware \[\[RSE-Webseite\]\]. \[\[Die Bibliothek | Das RSE-Zentrum | Die Beratungsstelle\]\] bietet Hilfe bei der Veröffentlichung von Forschungssoftware, von der Vorbereitung der Bereitstellung über die Auswahl des geeigneten Publikationsmediums bis zu domänenspezifischen Publikationsplattformen.
2. Bereitstellung, Weiterbildung und Unterstützung im Erstellen sowie Umsetzung von Softwaremanagement-Plänen (SMPs). SMPs dienen der Projektplanung, aber auch den Berichtspflichten denen Forschende nachkommen müssen (https://www.software.ac.uk/guide/writing-and-using-software-management-plan). \[\[Die Universität | Die Hochschule | Das Forschungszentrum\]\] stellt eine Plattform \[\[z.B. RDMO https://rdmorganiser.github.io/\]\] zur Erstellung neuer SMPs bzw. Nutzung von SMPs-Templates zur Verfügung. Das RSE-Zentrum bietet Unterstützung zum effektiven Management sowie Training bzw. Trainingsmaterial zu deren Nutzung \[\[RSE-Webseite\]\].
3. Sicherheitsfragen bei Forschungssoftware werden durch \[\[ das IT-Center | das RSE-Zentrum | Stelle nennen\]\] unterstützt \[\[Webseite/Kontakt\]\]
4. Die Datenschutzbeauftragten sind unter \[\[Webseite/Kontakt\]\] erreichbar.
5. Ethische Fragen können an \[\[Webseite/Kontakt\]\] gestellt werden.

\[\[ 6\. Weitere Punkte ergänzt durch die Universität | die Hochschule | das Forschungszentrum. \]\]

## **Referenzen** {#referenzen}


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

## **Anhang A: Kategorisierungsmöglichkeiten** {#anhang-a-kategorisierungsmöglichkeiten}


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
| **Entwicklungs-Community** | Persönlich |
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

## **Anhang B: Checkliste für die Weitergabe von Software** {#anhang-b-checkliste-für-die-weitergabe-von-software}


Die folgende Checkliste dient als Grundlage zur Definition und Weitergabe von Software-Lizenzen unter der Annahme, dass die Software komplett in der eigenen \[\[ Universität \| Hochschule \| Forschungszentrum\]\] erstellt wird. Im Fall externer Beteiligter mit eigenem Interesse an Software-Lizenzen ist eine gemeinsame Vorgehensweise sinnvoll.

|  | Urheber und Rechte Dritter |
| ----- | :---- |
|  | „Alle Urheberrechte müssen bei \[\[der Universität \| Hochschule \| dem Forschungszentrum\]\] liegen“ und „Alle Urheber:innen müssen bekannt sein“|
| ☐ | Alle Urheber:innen der Software sind bekannt und benannt. |
| ☐ | Alle Urheber:innen haben als Mitarbeiter:innen \[\[der Universität \| Hochschule \| des Forschungszentrums\]\] programmiert und die Nutzungsrechte liegen bei \[\[der Universität \| Hochschule \| dem Forschungszentrum\]\]. **Falls Nein:** |
| ☐ | \-	Dritt-Institutionen bzw. Personen (z.B. Studierende) sind bekannt. |
| ☐ | \-	\[\[der Universität \| Hochschule \| dem Forschungszentrum\]\] liegen Nutzungsrechte dieser Institutionen bzw. Personen in schriftlicher Form vor. |
|  | Die Nutzungsrechte sind unter einer kompatiblen Open Source Lizenz lizenziert: **Weiter unter Kompatibilitäten** |


|  | Vertragliche Bindungen |
| ----- | :---- |
|  ☐ | Bedingungen zu Publikation und Weitergabe von Software aus Förder- oder Zuwendungsvorgaben, Kooperationsverträgen, und Grant Agreements sind bekannt und werden eingehalten.  |
|  ☐  | Bedingungen aus Arbeitsverträgen sind bekannt und werden eingehalten. |
| ☐ | Es ist bekannt, ob und wo die Software als Background in Projekten eingebracht ist. |
| ☐ | Gesetzliche Vorgaben und Normen (z.B. bei medizinischer Software) und ihre Limitationen sind eingehalten. |
| ☐ | Die Regelungen zur Exportkontrolle wurden geprüft und werden eingehalten. |


|  | Kompatibilitäten |
| ----- | :---- |
| ☐ | Die Software wurde ohne Einbindung von vorbestehenden Softwareteilen oder Bibliotheken geschrieben. **Falls Nein:** |
|  ☐ | \-	Die Lizenzbedingungen der vorbestehenden/veränderten Software bzw. der verknüpften Bibliotheken sind bekannt und Kompatibilitäten werden beachtet. |
|  ☐ | \-	Falls für die Lizenzierung/Weitergabe der eigenen Software eine kostenpflichtige Entwicklerlizenz für die vorbestehende Software/Bibliothek benötigt wird, liegt diese vor. |


|  | Transferweg, Verwertung |
| ----- | :---- |
| ☐ | Die Zielgruppe ist bekannt. |
| ☐ | Das Interesse und die Zielsetzung der Entwickler:innen ist bekannt. |
| ☐ | Die zukünftige Nutzung/Behandlung und Zugänglichkeit der Software im Institut ist geklärt. |
| ☐ | Die Zustimmung der \[\[Forschungsverantwortlichen \| Institutsverantwortlichen\]\] liegt vor und ein entsprechender Freigabeprozess wurde eingehalten. |


|  | **Lizenzwahl** |
| ----- | :---- |
| ☐ | Es ist geklärt, welches Maß an Zugriff die Urheber auf die Software zulassen wollen (source code oder object code). |
| ☐ | Es ist entschieden, ob die Software proprietär oder als Open Source Software weitergegeben werden soll. |
|  ☐ | **Für Open Source Software Lizenzen:** Die ausgewählte Lizenz entspricht den in den hauseigenen Richtlinien oder zumindest den „approved licenses“ (siehe Seite der Open Source Initiative https://opensource.org/) **Falls Nein:** |
| ☐ | \-	Es wurde Rücksprache mit den Ansprechpersonen \[\[der Universität \| Hochschule \| des Forschungszentrums\]\] bzgl. einer proprietären Lizenz gehalten. |
|  ☐ | **Für Open Source Software Lizenzen:** Der Text der ausgewählten Lizenz wurde gelesen und verstanden und passt zur Zielgruppe und zur Zielsetzung der Weitergabe. **Falls Nein:** |
| ☐ | \-	Es wurde Rücksprache mit den Ansprechpersonen der Universität \| Hochschule \| des Forschungszentrumsbzgl. einer proprietären Lizenz gehalten. |

**Erläuterungen zur Checkliste**

Grundsätzlich stehen zwei Aspekte in rechtlicher Hinsicht im Vordergrund. Bestehende Rechte \[\[der Universität \| der Hochschule \| des Forschungszentrums\]\] an der Software vor Lizenzierung und die Rechte, die ein Dritter durch die Lizenzierung erhalten soll.

Bevor eine \[\[an der Universität \| an der Hochschule \| am Forschungszentrum\]\] entwickelte Software weitergegeben und dabei mit einer Lizenz versehen werden kann, muss sichergestellt werden, dass \[\[die Universität \| Hochschule \| das Forschungszentrum\]\]  die Verwertungsrechte daran hält. Die Leitlinie beschreibt die dazu notwendigen Vorkehrungen.

Weiterhin müssen die rechtlichen Rahmenbedingungen geklärt werden. Dies betrifft insbesondere Vorgaben durch Förderbedingungen, welche z.B. eine Veröffentlichung als Open Source Software erzwingen, aber auch ausschließen können.

Software unterliegt unter Umständen einer Exportkontrolle, wenn diese in kritischer Form (z. B. für militärische Zwecke oder zur digitalen Überwachung) Verwendung finden kann. In solchen Fällen ist zu prüfen, ob es grundsätzlich einer Exportgenehmigung durch das Bundesamt für Wirtschaft und Ausfuhrkontrolle (BAFA) bedarf. Beinhaltet die Software direkt oder indirekt internationale Beiträge, muss neben dem europäischen auch das Exportkontrollrecht dritter Staaten berücksichtigt werden. Nach dem europäischen und US-amerikanischen Exportkontrollrecht gelten Ausnahmen für allgemein zugängliche Technologien, zu denen insbesondere Open Source Software zählt, wenn sie frei im Internet abgerufen werden kann. \[\[Die Universität \| Hochschule \| Das Forschungszentrum\]\] hat hierfür ein Merkblatt mit Verweisen auf Verweisen einschließlich Information zur Rechtsabteilung erarbeitet, das unter der RSE-Webseite zu finden ist.

Kann ein Teil der Fragen nicht befriedigend beantwortet werden, so empfiehlt sich eine Beratung durch die auf der RSE-Webseite \[\[der Universität \| Hochschule \| des Forschungszentrums\]\] genannten Ansprechpartner.

## **Anhang C: Grundlagen und Mitwirkende** {#anhang-c-grundlagen-und-mitwirkende}


Die hier vorliegenden Leitlinien wurden auf Basis des

*GI- und de-RSE-Vorschlag für Leitlinien zur effizienten Entwicklung von qualitativ hochwertiger und langlebiger Forschungssoftware an Universitäten, Hochschulen und Forschungseinrichtungen*

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
