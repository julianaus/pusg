# Styleguide # 

Grundlage für sämtliche Gestaltungsentscheidungen sind die Vorgaben der *Publication Manual* der *American Psychological Assocation* ([2010](#literatur)). Gewisse Aspekte sind dort nicht oder nicht ausreichend geregelt. Deshalb werden sie im Folgenden (genauer) definiert. Darüber erfordert das gewählte Setup einige Besonderheiten, die auch im Folgenden beschrieben werden.  

## Definitionen ## 

Der Gesamttext wird bezeichnet als *Dissertation* oder *Doktorarbeit* oder einfach nur *Text* oder *Arbeit*. 

Ebene 1: Der Text gliedert sich in einzelne …

	# Kapitel # {#i}

(z.B. „1. Einführung”, „7. Resümee”). Das `{#i}` ist ein so genannter „[header identifier](http://pandoc.org/MANUAL.html#header-identifiers)” in Pandoc. Für Kapitelüberschriften werden dafür kleingeschriebene römische Ziffern verwendet. Für alle übrigen Textelemente werden beliebige kurze Worte oder Abkürzungen verwendet, z.B. `{#ff}` für einen Abschnitt zu Forschungsfragen.   

Ebene 2: Ein Kapitel hat …

	## Abschnitte ## {#foo}

– auch bezeichnet als Unterkapitel (z.B. „1.4. Zentrale Fragestellungen”).  

Ebene 3: Ein Abschnitt setzt sich aus verschiedenen …

	### Unterabschnitten ### {#bar}

zusammen. (z.B. „z.B. 1.4.2. Forschungsfragen”).  

Ebene 4: Unterabschnitte bestehen aus…  

	#### Textteilen #### {#foobar}

und haben keine eigene Nummerierung mehr.  

## Abbildungen ##

### Einfügen von Abbildungen ###

Zur Einbindung von Abbildungen wird auf den pandoc-Filter [pandoc-crossref](https://github.com/lierdakil/pandoc-crossref) zurückgegriffen. Er ermöglicht die automatische Nummerierung von Abbildungen und anderen Elementen der Arbeit. Damit sowohl Abbildungstitel als auch Abbildungsbeschreibung angezeigt werden können, wird ein kleiner Trick angewendet: Es werden zwei Bilddateien eingefügt, die obere ist jedoch nur ein Bild in der Größe von 1x1px in weiß. Ein Beispiel:  

    ![**Abbildungstitel**](/Users/ausse/Dropbox/__DISSERTATION/__HAUPTDOKUMENT/1.png){#fig:yolo}

    ![Bildbeschreibung](/Users/ausse/Dropbox/__DISSERTATION/_Abbildungen/5/10_yolo.png)

### Verweis im Text ###

Der Verweis im Text passiert mittels des Ausdrucks `@fig:bildkurzbezeichnung`. Die Bildkurzbezeichnung wird immer kleingeschrieben. Das Wort „Abbildung” wird automatisch bei der Umwandlung von Markdown hinzugefügt. Beispiel für Verweise im Text: 
	
    Zu sehen ist das in @fig:yolo:

Dieser Ausdruck wird nach der Umwandlung in Markdown zu: 

    Zu sehen ist das in Abbildung 1: 

Soll das Wort „Abbildung” weggelassen werden, fügt man es in eckiger Klammer ein. So wird der folgende Text in Markdown

    Schauen Sie sich Bild [-@fig:yolo] an. 

zu

    Schauen Sie sich Bild 1 an.

## Eigennamen ##

ForscherInnen werden gewöhnlicherweise nur mit Familienname erwähnt. Wenn ein ganzer [Abschnitt](Definitonen#abschnitten-auch-bezeichnet-als-unterkapitel) von einer Person handelt, dann soll bei der ersten Verwendung der Vorname verwendet werden. 

Eigennamen bzw. Bezeichnungen von (Medien-)Unternehmen, Buchtiteln, Zeitschriftentiteln, Programmiersprachen etc. werden kursiv gesetzt.

## Fremdsprachige Ausdrücke ##

### Orthografie ###

Englische und andere fremdsprachige Ausdrücke werden kleingeschrieben („sentence case”) und zwischen doppelte deutsche Anführungszeichen gesetzt (bzw. innerhalb einfacher Anführungszeichen, wenn der Ausdruck innerhalb von Anführungszeichen vorkommt). Zum Beispiel:   

> * „structured literature review”  
> * „Ich bin ein Fan von ‚computer-assisted reporting‘”, sagte der Reporter. 

Ausnahme 1: [Eigennamen](Eigennamen) kommen nicht in Anführungszeichen. Sie werden groß geschrieben und für gewöhnlich kursiv gesetzt.  

* _American Psychological Associaton_  
* Der _Guardian_ ist eine britische Zeitung. 

Das Handbuch der APA ([American Psychological Association, 2010](#literatur)) gibt darüber hinaus noch zahlreiche weitere Vorgaben, wann Wörter kursiv gesetzt werden müssen.     

Ausnahme 2: Fremdsprachige Ausdrücke werden wie deutschsprachige Ausdrücke verwendet, wenn sie auch im deutschsprachigen Raum gebräuchlich sind und es keine passable deutsche Übersetzung gibt. 

> * Crowdsourcing  
> * Hacker
> * Leaks 
> * Open Source
> * Open Science
> * Social Media

### Zitate aus fremdsprachigen Quellen ###

Englischsprachige Zitate können im Original bleiben und auch direkt in einen deutschen Satz einfließen.
 
Zitate aus anderen fremdsprachigen Quellen, die in ein Satzgefüge einfließen sollen, werden entsprechend der [Empfehlungen der American Sociological Association](http://blog.apastyle.org/apastyle/2014/11/lost-in-translation-citing-your-own-translations-in-apa-style.html) ins Deutsche übersetzt und formal wie Paraphrasen behandelt, also ohne Anführungszeichen beschrieben. In dieser Form kann auch mit englischen Ausdrücken verfahren werden. 

## Gendersensible Sprache ##

Die Arbeit wird gegendert. 

Folgende Maßnahmen sind dabei möglich (entnommen und adaptiert von Matiasek, Ausserhofer, & Goldgruber, [2015](#literatur)): 

1. Geschlechtsneutrale Personenbezeichnung und Pluralform

> ✅ die Person/die Personen, das Mitglied/die Mitglieder, Belegschaft, Studierende, etc.

2. Binnen-I

> ✅ ProfessorInnen, MitarbeiterInnen, etc.

Aber: Aus Gründen der Lesbarkeit kein Binnen-I bei Komposita. 

> ✖️ JournalistInnenkonferenz  
> ✅ Journalistenkonferenz

Bei Formulierungen im Singular werden beide Geschlechter genannt, das weibliche zuerst. Wörter, bei denen sich kein Binnen-I integrieren lässt (z.B. ein vorangestellter Artikel), werden durch einen Schrägstrich und ohne Leerzeichen getrennt. 

> Kleinere Aufgaben werden allein von einer/einem RedakteurIn erledigt.

Nicht gegendert wird in dieser Arbeit „Akteur” bzw. „Akteure”, weil diese Begriffe in dieser Arbeit als Fachausdrücke gebraucht werden und sich auf die Akteur-Netzwerk-Theorie beziehen sollen. 

3. Kollektiv- und Funktionsbezeichnungen

> ✅ die Geschäftsführung, das Projektteam

4. Passiv

> ✖️ Die Mitglieder des Teams haben die Tools gemeinsam entwickelt.  
> ✅ Die Tools wurden vom Projektteam gemeinsam entwickelt.


## Fachausdrücke ## 

* „soziale Medien” („sozial” wird kleingeschrieben)

## Literatur ##

* American Psychological Association. (2010). Publication manual of the _American Psychological Association_ (6. Aufl.). Washington, DC: American Psychological Association.

* Matiasek, S., Ausserhofer, J., & Goldgruber, E. (2015). [_Guidelines for gender-sensitive language_](http://www.validproject.at/wp-content/uploads/2015/06/151130_Guidelines-for-Gender-Sensitive-Language.pdf) (Deliverable Nr. 6.3). Graz: Visual Analytics in Data-driven Journalism (VALiD) project.
