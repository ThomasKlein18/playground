
### 0. Einleitung

In diesem Beispiel wollen wir ein künstliches Neuronales Netzwerk nutzen, um zwei exotische Blumenarten zu erkennen.
Professor Floralis hat im Amazonas-Delta einige tausend Orchideen vermessen: Für jede Pflanze hat er den Durchmesser der Blüten und die Länge der Blätter notiert. Die Pflanzen sind entweder Alraunen oder Drachenwurzeln.
Er hat also eine Tabelle:

Blütendurchmesser  |  Blattlänge  |  Art
------------------------------------------
       0.5               0.65        Alraune
       0.23              0.42        Drachenwurzel
       0.7               0.81        Alraune
       0.45              0.9         Alraune
       0.18              0.39        Drachenwurzel
 ...

 Leider sind einige Datensätze kaputt gegangen: Blütendurchmesser und Blattlänge sind zwar vorhanden, aber zu welcher Art die Blumen gehören, lässt sich nicht mehr erkennen. 

 Professor Floralis möchte nun einem Computer beibringen, die Art der Blume anhand der vorhandenen Informationen zu erkennen. 

### 1. Daten

Hier sehen wir die Daten, mit denen das Netzwerk trainiert werden soll, also die Teile der Tabelle, die nicht kaputtgegangen sind. Jeder Punkt entspricht einer Blume: blaue Punkte sind Alraunen, orangene Punkte sind Drachenwurzeln. Je weiter rechts der Punkt ist, desto größer sind seine Blüten. Je weiter oben der Punkt ist, desto länger sind seine Blätter. 

Wir haben hier vier verschiedene Szenarien vorbereitet, in ansteigender Schwierigkeit. (Dass die Punktwolken anders angeordnet sind bedeutet dass andere Regeln definieren, wie die Blumen aussehen und wie sie sich unterscheiden: Im Datensatz unten links z.B. haben die blauen Alraunen große Blüten und kurze Blätter, während die orangenen Drachenwurzeln kleine Blüten und lange Blätter haben.)


### 2. Eigenschaften

Hier sehen wir, mit welchen Eigenschaften Professor Floralis sein Netzwerk trainiert: Wir können einfach den Blütendurchmesser oder die Blattlänge übergeben (für manche Aufgaben reicht das schon) oder kompliziertere Transformationen dieser Daten, wie die Blütenlänge zum Quadrat oder den Sinus der Blattlänge.


### 3. Versteckte Schichten

Ein kNN ist aufgebaut wie ein Gehirn: Aus Neuronen, die über unterschiedlich starke Nerven verbunden sind. Die Neuronen sind in Schichten angeordnet, sodass die Informationen das Netzwerk von links nach rechts durchwandern. Sie können hier neue Schichten hinzufügen oder wegnehmen, und innerhalb der Schichten mehr oder weniger Neuronen ausprobieren. Klicken sie auf die Play-Taste oben links um das Training zu starten.

<Buttons: Loslegen oder mehr Informationen>


### 4. Gewichte und Neuronen 

Innerhalb eines Neurons können Sie die Entscheidungsgrenze des Neurons sehen, also die Bereiche, in denen die Blumen von diesem Neuron als Alraune oder Drachenwurzel klassifiziert werden. 

Jedes Neuron kombiniert die gewichteten Entscheidungsgrenzen der Neuronen in den vorhergegangenen Schichten: Je dicker die Verbindungen, desto größer das der Betrag des Gewichts (also z.B. 3 > -2 > 1 > 0). Negative Gewichte sind orange dargestellt, positive Gewichte blau. 


### 5. Ergebnis

Ganz rechts sehen Sie die finale Entscheidungsgrenze, die das Netzwerk als Ganzes gelernt hat. Das Netzwerk funktioniert richtig, wenn alle orangenen Punkte in einem orangenen Bereich liegen und alle blauen Punkte in einem blauen Bereich. Der Trainingsfehler muss möglichst gering werden. Die Test-Daten sind die verloren gegangenen Daten, bei denen wir wirklich nicht wissen, zu welcher Pflanzenart sie gehören. 


### 6. Text unten

#### Warum ist diese Technologie wichtig? 

Unser Professor Floralis mit seinen Orchideen ist zwar ein niedliches Beispiel, aber Orchideen erkennen zu können ist nicht besonders nützlich. Das Tolle an neuronalen Netzwerken ist jedoch, wie allgemein sie sind. Stellen Sie sich vor, wir hätten hier die Daten von Krebspatienten: Den Anteil ihrer weißen Blutkörperchen und ihren Blutzuckerspiegel. Blaue Punkte sind Patienten, bei denen Behandlungsmethode A anschlägt, während bei orangenen Punkten Methode B besser funktioniert. Für einen neuen Patienten könnten wir nun vorhersagen, welche Methode wir anwenden sollten. Natürlich funktionieren neuronale Netzwerke nicht bloß mit zweidimensionalen Daten, sondern mit beliebig vielen Dimensionen. Wir könnten also mit allen relevanten Informationen zum genetischen Profil arbeiten, mit Blutwerten und bekannten Erkrankungen, Allergien, Körpergewicht, Behandlungshistorie... Außerdem können wir nicht bloß zwischen zwei Klassen unterscheiden wie im Beispiel, sondern zwischen beliebig vielen, und es gibt viele weitere Entscheidungen, die wir beim Design eines neuronalen Netzwerks treffen können. 

<b>Machen Sie sich die Tragweite dieser Eigenschaften bewusst: Wir können die implizit in den Daten vorhandenen Informationen ohne Vorschriften von außen nutzen. Ich muss als Forscher nichts über das inhaltliche Themengebiet (Orchideen oder Krebszellen) wissen, um korrekte Vorhersagen treffen zu können. Das Netzwerk lernt Dinge von selbst.</b>

#### Warum sollten wir neuronale Netzwerke erforschen? 

Die Technologie funktioniert und hat ihren Wert schon unter Beweis gestellt, aber viele Fragen sind noch offen. Wir wissen zum Beispiel oft nicht, was im Inneren des Netzwerks passiert und worauf die Neuronen achten, wenn sie ihre Entscheidungsgrenze lernen. Im Krebs-Beispiel: Wir wissen zwar, wie wir einen Patienten behandeln sollten, aber verstehen nicht, warum. Welche Eigenschaften sind entscheidend für die Diagnose, und was sind die biologischen Gründe dafür? Es ist noch viel Forschung nötig, bis wir diese Geheimnisse entschlüsseln können. 