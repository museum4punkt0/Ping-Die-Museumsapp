# Ping! Die Museumsapp

# Kurzbeschreibung
Ping! ist eine eine mobile Anwendung auf dem Smartphone, die eine personalisierte und spielerische Exploration von Exponaten in Museen und Ausstellungen erlaubt. Im Mittelpunkt der User Experience steht das Kennenlernen von Exponaten über Chats und das Anlegen einer eigenen Sammlung von Objekten. 
Mit den Mitteln des Gamedesigns wird die Motivation der NutzerInnen zu einem eigenaktiven Erschließen der Exponate hergestellt: Die häufig überwältigende Masse an Objekten und die Komplexität des Wissens wird spielerisch reduziert und anschließend dialogisch vermittelt. Gleichzeitig erlaubt die App sowohl eine personalisierte Informationsübermittlung über die herkömmlichen museale Wissensvermittlung hinaus, als auch eine Konzentration auf eine individuelle Auswahl an Museumsobjekten. Der Besucher oder die Besucherin lernt das einzelne Objekt im wahrsten Sinne des Wortes persönlich kennen.


# Aufteilung
Dieses Repository gibt Informationen zur Zusammensetzung der Teile der App inkl. Backend. Da die Applikation auf in mehrere Teile geteilt ist, wird hier ein Überblick hergestellt, der dann in den einzelnen Repositories detailliert wird.


# Entstehungskontext 
Die native App auf Basis des React Native Frameworks ist entstanden im Verbundprojekt museum4punkt0 – Digitale Strategien für das Museum der Zukunft, Teilprojekt: Der humboldt’sche Raum im digitalen Raum.


# Förderung 
Das Projekt museum4punkt0 wird gefördert durch die Beauftragte der Bundesregierung für Kultur und Medien aufgrund eines Beschlusses des Deutschen Bundestages.

# Inhaltsverzeichnis
1. Name der Anwendung 
2. Kurzbeschreibung 
3. Aufteilung
4. Entstehungskontext
5. Förderung
6. Inhaltsverzeichnis 
7. Technische Dokumentation der Programmierung
8. Installation 
9. Benutzung 
10. Credits
11. Markenname
12. Lizenz 


# Technische Dokumentation der Programmierung 
React Native 
Die technische Entwicklung basiert auf React Native. Diese Entscheidung wurde nach sorgfältiger Abwägung verschiedener Möglichkeiten gewählt und bietet die Performance nativer Komponenten sowohl von iOS als auch von Android sowie eine gemeinsame Codebasis unter Nutzung von Webtechnologie. Im Ergebnis ist eine performante, flüssige App mit nativem Look&Feel entstanden, die für beide wichtigen Betriebssysteme verwendet werden kann. Die App ist bereit, um im geschlossenen Betatest in den Appstores verfügbar gemacht zu werden. Technisch beinhaltet die App bereits folgende Module: 

1. Swiping Modul 
Über Wischgesten können Objekte ausgewählt und bewertet werden. 
Die Objekte werden mit Zoom-In-Animationen dargestellt und betonen so den gezeigten Detailausschnitt. Darüber hinaus stellen sie sich mit einem beschreibenden Spruch, einem Objekttyp und einer Distanzangabe zur letzten bekannten Position des/der Besuchers/Besucherin vor. 
2. Chat Modul 
Über eine Textengine können dynamische Dialoge mit dem/der BesucherIn integriert werden, die verzweigende Dialogstrukturen ermöglichen und sich so nach dem Interesse der/die NutzerIn ausrichten lassen. Der Chat kann zoombare Bilder enthalten, Emoticons und buttonbasierte Verzweigungen. Die Chats können darüber hinaus Quiz Elemente enthalten, Blickführung übernehmen, interessensbasiert informieren und den/die NutzerIn zu Aktionen im physischen Raum anregen. 
3. Kartenmodul 
Das Kartenmodul zeigt eine Übersichtskarte des Museumsraums, in der der/die NutzerIn alle gesammelten Objekte verzeichnet sieht. Zudem laden die Objekte den/die BesucherIn ein, in einer markierten Region der Karte nach ihnen zu suchen. Ebenfalls sichtbar sind Objekte mit semantischen Beziehungen zu bereits gesammelten Objekten. Auf diese Art wird Orientierung geschaffen und Beziehungen zwischen Objekten werden aufgezeigt. Die Karte ist zoombar und die Icons können per Tap eine Vollansicht aufrufen. Zudem unterstützt die Karte mehrere Stockwerke. 
4. Chatübersichts-Modul 
Im Chatübersichts-Modul werden werden alle Chats mit Objekten gezeigt, die begonnen und abgeschlossen wurden. So kann jederzeit in bereits geführte Dialoge gesprungen werden und unterbrochene können wiederaufgenommen werden. 
5. Sammlungsmodul 
Im Sammlungsmodul finden sich alle Objekte, die man bereits gefunden hat. Sie sind Kategorien zugeordnet, die man komplettieren kann, um so ein Level aufzusteigen. Ein tap auf ein Objekt ruft die detaillierten Objektinformationen auf. 
6. Tensor-Flow-Modul 
Durch die Integration des Bildererkennungsalgorithmus Tensor Flow können die von den NutzerInnen fotografierten Objekte erkannt und die passenden Objekte in der App aktiviert werden. Dazu werden pro Objekt ca. 100 Fotos als Trainingsdaten verwendet. 
7. Backend 
Das Backend ist als ein grafisches Content-Management-System umgesetzt.
8. Vorgehensmodell 
Verwendet wird circle.ui für automatisiertes building, testing, migrating and deployment. Im Anschluss wird die App und die dazugehörigen Daten auf Amazon Web Services installiert, der alle wesentlichen Services automatisch auf deutschen Servern bereitstellt. Ein Hosting auf einem eigenen Server oder einer VM ist jederzeit möglich. 


# Installation 
Zur Benutzung werden Smartphones benötigt, die entweder über ein iOS oder ein Android Betriebssystem verfügen. Die Anwendung läuft ab folgenden Betriebssystemen: Android Oreo 8.0 und iOS 10.3.3.. Nach Veröffentlichung der App im Playstore bzw. Appstore kann die Anwendung von jedem/r SmartphonebesitzerIn heruntergeladen und installiert werden. 
Der Sourcecode gliedert sich in zwei Repositorien: Mein-Objekt-Backend und Mein-Objekt-MOB-GPL. Mein-Objekt-Backend enthält das Python Backend, das TensorFlow Modul (Unterverzeichnis Tensorflow) zur Berechnung der Fotoerkennungs-KI und den Chatbuilder (Unterverzeichnis Chatbuilder) zum Verfassen und Bearbeiten von Dialogen. Das Repositorium Mein-Objekt-MOB-GPL enthält die React Native App zum Deployment auf iOS und Android.

https://github.com/museum4punkt0/Ping-APP-MIT

https://github.com/museum4punkt0/Ping-APP-GPL

https://github.com/museum4punkt0/Ping-Backend

https://github.com/museum4punkt0/Ping-TensorFlow

# Benutzung  
1. Start Screen: Sprachauswahl und Start der Anwendung 
2. Onboarding I: In den vier Onboarding-Screens wird die grundsätzliche Funktionsweise der App beschrieben.
3. Museums-Auswahl oder Planmodus: Hier stellt die App per GPS fest, dass sich der/die BesucherIn nicht im Museum befindet. Es wird der Wahl Screen mit folgenden Möglichkeiten angezeigt: a) Tour-Plan - Hier kann der/die BesucherIn z.B. von zuhause aus den nächsten Museumsbesuch mit Ping! planen b) Wählen Sie Museum und Tour starten - Hier kann ein Museum händisch ausgesucht und die Anwendung für dieses Museum gestartet werden.
4. Museums-Auswahl: Hier können die in der App verfügbaren Museen ausgewählt werden. 
5. Begrüßung: Der/Die BesucherIn wird in der Chatlogik begrüßt. Die wesentliche Interaktion des Chats mit Auswahl von vorgegebenen Antworten wird erlernt. Der/Die UserIn gibt sich einen Namen. Ein eigener Avatar bzw. ein Selfie wird zur Verwendung in der App gewählt. 
6. Onboarding II: Erläuterung der Wischgesteninteraktion und der Schaltflächen. 
7. Wischgesteninteraktion: Der Screen bietet a) Wischen nach links oder alternativ das Berühren des linken Funktionsbuttons. Dies bedeutet: Dieses Exponat interessiert mich gerade nicht. b) Wischen nach rechts oder alternativ das Berühren des rechten Funktionsbuttons. Dies bedeutet: Dieses Exponat interessiert mich. 
8. Match mit dem Exponat: Ein auf das Userprofil passendes Exponat wird gefunden. Wahl zwischen: a) Unterhaltung starten. Der erste Chat mit einem Exponat wird gestartet. oder b) Nein.Danke. Rückkehr zur Wischengestenfunktion.
9. Chat mit dem Exponat I: In dem Chat unterhält sich der/die UserIn mit dem Exponat. Hier können über das Exponat auch Fragen bezüglich z.B der Besucherforschung gestellt werden. 
10. Aufsuchen des Exponats: Wenn der Chat nach beiderseitigem Verständnis positiv war, kann man sich zu einem Treffen verabreden. Auf der dann angezeigten Karte wird der Standort des Exponats nur ungefähr angezeigt, so dass der Museumsraum sich zum Suchraum wandelt.
11. Chat mit dem Exponat II: Hat der/die UserIn das Exponat gefunden, findet ein weiterer Chat statt. Hier können qua Chat u.a. folgende Aktionen stattfinden: Detail (Hinweisen des/der Users/Userin) auf z.B. Beschädigungen oder Restaurierungsspuren am Exponat), Werkinformationen (Hinweisen auf Bildaufbau, Komposition, Farbgebung, Sammlungsgeschichte), Sammlungszusammenhang (Hinweisen des/der Users/Userin auf die benachbarten Exponate und Kontextualisierung des Standortes), Architektur (Thematisieren der Ausstellungsarchitektur)
12. Abschluss des Chats und Beginnen der eigenen Sammlung: Zum Ende des Chats macht der/die UserIn ein Foto des Exponats. Dieses wird in die persönliche Sammlung eingefügt. Hier können auch Metainformationen über das Exponat zur Verfügung gestellt werden. 
13. Plan Modus: Auch hier werden zunächst die in der App verfügbaren Museen zur Auswahl vorgeschlagen. Nach der Wischgesteninteraktion (>>>7.), dem Match (>>>8.) und dem ersten Chat (>>>9.) wird das Exponat in die Sammlung integriert. Von hier aus kann der Chat im Museum (Chat mit dem Exponat II >>>11.) fortgesetzt werden. Im Planmodus gibt es unten den Reiter Mein Plan. Von hier aus können die bereits von außerhalb des Museums begonnenen Chats im Museum gestartet werden, der weitere Prozess ist dann wie >>>10 - >>>12. 
14. Info Screen: Der Info Screen ist über die untere Bedienleiste immer erreichbar und bietet folgende Funktionen: Name (Der/Die UserIn kann seinen/ihren Namen eintragen/ändern), Bild/ Avatar (Der/Die UserIn kann einen Avatar auswählen oder ein Foto von sich schießen), Sprachauswahl (Die Sprache der App kann ausgewählt werden), Font Size (Die Größe der Schrift kann ausgewählt werden), Chat Interval (Die Geschwindigkeit des Chatverlaufs kann variiert werden), Quit (Hierüber ist der Wechsel zwischen Discovery Modus und Plan Modus möglich), Geschäftsbedingungen (Anzeige der AGB), Visitor Guide (Möglichkeit in ein ergänzendes digitales Angebot zu wechseln), Gerät zurücksetzen (Alle Einstellungen und Vorgänge werden gelöscht) 


# Credits 
Auftraggeber*in/Rechteinhaber*in 
Stiftung Humboldt Forum im Berliner Schloss 
Urheber*innen 
Humboldt-Universität zu Berlin, gamelab.berlin am Helmholtz-Zentrum für Kulturtechnik, Zentralinstitut der HU. 

# Markenname 
„Ping! Die Museumsapp“ ist eine Marke der Stiftung Humboldt Forum im Berliner Schloss. Die Marke kann von anderen Institutionen, die die App einsetzen, verwendet werden. In diesem Fall wird um Angabe des folgenden Nachweises gebeten:

    „Ping! Die Museumsapp“ ist eine Marke der Stiftung Humboldt Forum im Berliner Schloss.

# Lizenz
Alle Codeteile sind unter der GPLv3 Lizenz veröffentlicht.
Zusätzlich dazu wurde das Frontend noch einmal mit der MIT-Lizenz lizensiert.
Die entsprechenden Versionen finden sie sowohl im Namen der Repositories als auch in der jeweiligen Readme und Lizenzdatei.
