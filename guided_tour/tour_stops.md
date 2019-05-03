
### Einleitung

Willkommen im Sandkasten. Hier können Sie ein neuronales Netzwerk darauf trainieren, Blumen zu erkennen. Wir geben dem Netzwerk die Länge das Blattes und den Durchmesser der Blüte und möchten, dass es Alraunen von Drachenwurzeln unterscheiden kann. (Wenn das jetzt unsinnig klang, sollten Sie vielleicht unsere kurze Erklärung zu neuronalen Netzwerken ansehen <Link to Bubble>)
       
### Play Button

Hier geht es los: Beginnen Sie mit dem Training. Die Form des Netzwerk ist vorgegeben, doch in jedem Trainingsschritt werden die Gewichte des Netzwerks verändert.

### Reset Button

Hier können Sie das Training zurücksetzen, um eine andere Architektur auszuprobieren.

### Versteckte Schichten

Hier können Sie das Netzwerk verändern. Sie können dem System mehr oder weniger versteckte Schichten mit mehr oder weniger Neuronen spendieren. Mehr Neuronen sind aber nicht unbedingt besser.

### Daten

Hier sehen wir die Daten, mit denen das Netzwerk trainiert werden soll. Jeder Punkt entspricht einer Blume: blaue Punkte sind Alraunen, orangene Punkte sind Drachenwurzeln. Je weiter rechts der Punkt ist, desto größer sind seine Blüten. Je weiter oben der Punkt ist, desto länger sind seine Blätter. 

(The explanation might get complicated here. We could just give them the above text at first and add a "Mehr erfahren" (learn more) button which expands the textbox)

Mehr erfahren ->

Wir haben hier vier verschiedene Szenarien vorbereitet, in ansteigender Schwierigkeit. (Dass die Punktwolken anders angeordnet sind bedeutet dass andere Regeln definieren, wie die Blumen aussehen und wie sie sich unterscheiden: Im Datensatz unten links z.B. haben die blauen Alraunen große Blüten und kurze Blätter, während die orangenen Drachenwurzeln kleine Blüten und lange Blätter haben.)

### Gewichte und Neuronen 

Innerhalb eines Neurons können Sie die Entscheidungsgrenze des Neurons sehen, also die Bereiche, in denen die Blumen von diesem Neuron als Alraune oder Drachenwurzel klassifiziert werden. 

Jedes Neuron kombiniert die gewichteten Entscheidungsgrenzen der Neuronen in den vorhergegangenen Schichten: Je dicker die Verbindungen, desto größer das der Betrag des Gewichts (also z.B. 3 > -2 > 1 > 0). Negative Gewichte sind orange dargestellt, positive Gewichte blau. 


### Ergebnis

Ganz rechts sehen Sie die finale Entscheidungsgrenze, die das Netzwerk als Ganzes gelernt hat. Das Netzwerk funktioniert richtig, wenn alle orangenen Punkte in einem orangenen Bereich liegen und alle blauen Punkte in einem blauen Bereich. Der Trainingsfehler muss möglichst gering werden. Die Test-Daten sind die verloren gegangenen Daten, bei denen wir wirklich nicht wissen, zu welcher Pflanzenart sie gehören. 
