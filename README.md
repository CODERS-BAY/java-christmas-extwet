# Christmas Exercise :santa:
## Wiederholung der Vererbung und der Objektorientierung

Bitte versuche als Übung alles in Markdown zu beantworten. Hier ist ein [Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

### 1. Was ist das Ziel der Objektorientierung?
>Das Ziel ist es eine Software so in seine Grundstrukturen zu zerlegen, dass sie übersichtlich wird. Dabei dienen uns zwei zentrale Begriffe, die ***Klasse*** und das ***Objekt***. Man muss eine Klasse als einen Bauplan für Objekte begreifen. Eine Klasse beschreibt nämlich, wie die aus ihr ins Leben gerufenen Objekte gemacht sein sollen. Die erzeugten Objekte stellen dann ganz individuelle Repräsentation der allgemeinen Klasse dar. Sie können sich aber hinsichtlich der ausgeprägten Werte voneinander unterscheiden, denn es sind verschiedene, zunächst einmal unabhängig voneinander existierende Objekte.
### 2. Gibt es OOP nur in Java?
>Die Objektorientierung existiert auch ausserhalb von Java. Als Prinzip im Softwareentwicklungsprozess von der Analyse über die Programmierung bis hin zur Wartung, das durch eine natürliche Modellierung der Realität, Wiederverwendbarkeit und leichte Erweiterbarkeit die Komplexität von Software beherrschbar machen soll.
### 3. Was ist der Unterschied zwischen Objekt und Klasse?
>* Von einer Klasse können beliebig viele Objekte instanziert werden. Sie sind eine Art Bauanleitung für Objekte und definieren die Struktur der Objekte und deren Funktionalität.
>* Ein Objekt ist eine Instanz ihrer Klasse. Objekte bestehen aus Daten/Attributen und Methoden, welche diese modifizieren, verarbeiten oder zurückgegeben. Die Daten/Attribute enthalten die Eigenschaften und beschreiben über ihre Werte den Zustand/Status eines Objektes, die Methoden die möglichen Funktionen und Handlungen eines Objektes.
### 4. Wie erzeuge ich eine neue Instanz? (Welches Schlüsselwort gibt es dafür)
> * new ();
### 5. Was bedeutet das Schlüsselwort `static` und wo kann es überall verwendet werden?
>Der Modifikator ***static*** kennzeichnet Programmstrukturen, die nicht an ein Objekt gebunden sind. ***static*** deklariert man solche Variablen, die bei jedem Objekt einer Klasse gleich sein sollen. sobald die Variable in einem der Objekte verändert wurde, auch bei allen anderen Objekten der Kalsse verändert werden. Ein solches Attribut existiert genau einmal pro Klasse, ein Objekt ist dabei nicht erforderlich. Ein solches static Element kann existieren ***bevor*** ein Objekt angelegt wird. zB in der Klasse ***Datum*** wird das Attribut anzahl#Wochentage für alle Objekte der Klasse gleich sein. static int anzahlWochentage = 7; hier könnte auch der Modifier ***final*** hinzugefügt werden, da sich die Anzahl der Wochentage nicht ändern wird.
>* ***static bei Methoden:*** es kann aufgerufen werden bevor ein Objekt erzeugt wird
>* ***static bei Attributen:*** es existiert genau einmal pro Klasse
### 6. Wozu dient die Vererbung?
>In Java können mit Hilfe der Vererbung Programmteile wiederverwendet werden, dabei werden die Merkmale bereits vorhandener Klassen auf abgeleitete Klassen übertragen. zB. mit ***extends*** kann man in der Basisklasse *Tier* eine Sonderklasse *Mensch* hinzufügen mit neuen Attributen *Bankkonto*, dabei erbt die Sonderklasse alle Eigenschaften der Basisklasse *Beine, Arme, Alter*. 
### 7. Kann in Java von mehreren Klassen geerbt werden? Wenn ja wie?
>Ja, mit dem Überschreiben einer Methode oder eines Attributs. ***@Override*** Java erlaubt die Methode einer Oberklasse zu überschreiben, das bedeutet sie zu verdecken, wenn die folgenden Bedingungen für die Deklaration der Methode erfüllt sind:
    *Namensgleicher Name
    *Eingabeparameter sind von Anzahl, Reihenfolge und Typ identisch
    *Rückgabeparameter ist identisch
    *Zugriffsrechte der Oberklasse (public, protected, private) werden nicht eingeschränkt
>Private Attribute werden nicht vererbt. Sie sind der Unterklasse weder bekannt noch zugänglich! Der Zugriff auf ein überschriebenes Attribut der Oberklasse geht symmetrisch zu den Methoden mit dem ***super*** Schlüsselwort.
### 8. Welche Vererbungshierarchien kennst du? (Ein Bild reicht aus)
 >* Hierarchical Inheritance In Java
![alt text](https://cdn.softwaretestinghelp.com/wp-content/qa/uploads/2020/08/Hierarchical-inheritance-in-Java.png "Hierarchische Vererbung")
### 9. Was bedeuted Casten und wie ist die Syntax in Java dafür?
>Die Typ-Umwandlung oder Typ-Konvertierung ist die Umwandlung eines Datentyps in einen anderen Datentyp, die beiden Datentypen müssen zueinander kompatibel sein.
### 10. Was ist der Unterschied zwischen explizieten und implizieten Typecasting?
 >* ***Explizite Typumwandlung*** – bei der im Quellcode die Typumwandlung ausdrücklich angewiesen wird. str = (String) objStr;
 >* ***Implizite Typumwandlung*** – bei der die Typumwandlung nicht extra im Quelltext angewiesen wird, sondern automatisch vom Compiler durchgeführt wird.Object objStr = new String("String-Objekt mit Object-Typ Referenz");
### 11. Erkläre die folgenden Schlüsselwörter: `super`, `this`
> * ***super*** Genau wie beim überschreiben einer Methode, wird auch beim Schlüsselwort ***super*** die Parameterliste verwendet um den richtigen Konstruktor aufzurufen. Wenn in einer Klasse ein Konstruktor mit Parametern befüllt wird, wird in der Vererbung der Standardkonstruktor nicht weitergegeben, dabei kann mit  *super* der Konstruktor der Basisklasse selbst aufgerufen werden.
> * ***this*** benötigt man, um Werte, die wir den Variablen in der Methode zuordnen, verwenden möchten und nicht diejenigen, die wir global initalisiert haben. Es bezieht sich auf das aktuelle Obkjekt in der Methode oder einem Konstruktor. Die *this* Referenz ist final. D.h. man kann ihr keinen anderen Wert zuweisen.
### 12. Für was dient der `instanceof` Operator. Gib ein sinnvolles Beispiel.
>Durch die Möglichkeit der Typkonvertierung durch "casten", und "Upcasting" kann man die genaue Information über einen Typ einer Instanz zur Laufzeit verlieren. Das bedeutet, sie ist im Kontext einer Methode oder Klasse nicht mehr bekannt. Mit ***instanceof*** kann zur Laufzeit geprüft werden, ob ein von einem Verweis referenziertes Objekt kompatibel zu einem Objekt einer bestimmten Klasse ist. Es gibt true oder false aus.
