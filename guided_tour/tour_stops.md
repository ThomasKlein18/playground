# Guided Tour

Hier können wir Ideen für die Erklärungstour durch den Playground sammeln.

# Content

+ Daten: die blauen und orangenen Punkte repräsentieren Objekte zweier verschiedenen Kategorien, z.B. exotische Pflanzenarten?
..+ x-Achse und y-Achse Namen geben, idealerweise ist das sogar sinnvoll (Länge der Blätter und Blütendurchmesser)
..+ Bilder von Orchideen
..+ klar machen dass das auch mit mehr Dimensionen geht
+ Eigenschaften: umbenennen in "Blatt" (anstatt X1) und "Blüte" (anstatt X2) etc.
+ Erklärung von Split in Train- und Test-Data?
+ Erklären dass das kleine Fenster eines Neurons seinen Output anzeigt und verdeutlicht, für welchen Teil des Input-Spektrums dieses Neuron Klasse A bzw. Klasse B vorhersagt
+ Erklären dass die Linien zwischen den Neuronen für die positive / negative Gewichtung des Neurons stehen
+ Test-Daten: Netzwerk hat sie nie im Training gesehen, macht aber Vorhersagen mit den Daten um zu gucken ob es funktioniert (d.h. ob es generalisiert)

# Stuff I need to add as hovering hints
+ Epoche muss erklärt werden: Einmal alle Trainingsdaten dem Netzwerk gezeigt
+ Trainingsfehler muss möglichst gering sein


# Offene Diskussionsfragen
+ Wollen wir zwei Varianten der Erklärung machen, für Erwachsene und Kinder? (bestimmte Themen sind zu schwer aber wären cool zu erklären: Overfitting, höherdimensionale Daten (Wortrepräsentationen als Vektor), etc.)


# Realization
+ two different modes: 
..+ explanations that appear when hovering over the respective parts of the site and 
..+ initial guided tour
+ @Chris: What makes more sense, showing the tour as a series of screenshots in which everything is grayed out except for the relevant part, or achieving that effect dynamically? I think the first option makes more sense because Gabi or I can do that, you'd just have to write code that handles displaying a series of images with three buttons (left, right and x)


# Bonus: Intelligent Tour
+ figure out what sort of information people need as they are interacting with the screen
