Informatikklausur
=================

---
# Erste Aufgabe: Sortierverfahren

### 1.) Insertionsort:
    Der Algorithmus betrachtet immer ein Element des Arrays und schaut ob das Element,
    welches vor diesem kommt größer als es ist. 
    Wenn das der Fall ist, dann werden die Elemente getauscht, das läuft so lange ab, 
    bis es nicht mehr tauschen kann.
    Wenn es nicht mehr tauschen kann, dann wird das nächste Elemente betrachtet. 

    Funktion InsertionSort(A)
        Für i von 1 bis Länge von A - 1: 
            j = i

            Während j > 0 && A[j-1] > A[j]:
                Tausche(A[j-1], A[j])
                j = j - 1

            Rückgabe A

### 2.) Selectionsort: 
    Der Algorithmus betrachtet das erste Element des Arrays, dann sucht er das kleinste 
    folgende Element, wenn es kleiner ist als das erste Elemement, dann werden die beiden 
    Elemente getauscht. 
    Der Algorithmus macht dann mit dem nächsten Element weiter bis er das Ende des Arrays 
    erreicht.

    Funktion Selectionsort(A)
        Für i von 0 bis Länge von A-1:
            min = i

            Für j von i bis Länge von A:
                Falls A[i] < A[min]:
                    min = i

            Falls min != i:
                Tausche(A[i], A[min])

        Rückgabe A

### 3.) Bubblesort: 
    Der Algorithmus betrachtet immer zwei Elemente und tauscht eines davon nach oben 
    wenn es größer ist. Somit bubblen sich große Elemente wie in Blasen nach oben 
    ins Array. 

    Funktion BubbleSort(A)
        Für i von 1 bis Länge von A: 
            Für j von 0 bis Länge von A - 1: 
                Falls A[j] > A[j+1]
                    Tausche(A[j], A[j+1])

        Rückgabe A

---
# Zweite Aufgabe: Abstract data types

### 1.) Verkettete Listen: 
    Eine verkettete Liste ist eine dynamische Datenstruktur, in der 
    Datenelemente geordnet gespeichert sind. 
    Die Anzahl an Element darf während der Laufzeit variiert werden.
    
    Sie besteht aus einem Listen<T> Objekt, welches den ersten Knoten 
    speichert und Operationsmethoden implementiert. 

    Und aus den ListenKnoten<T> Objekten, welche die Daten speichern und 
    auf den nachfolgenden Knoten verweist. 

    In einem Klassendiagramm würde man es so zeichnen, dass die Listenknoten<T>
    mit einem Assoziationspfeil auf sich selbst verweisen und die Liste 
    mit dem ersten assoziiert ist.
    
### 2.) Stack: 
    Ein Stack ist eine besondere Art der Datenstruktur, er kann als Array 
    oder verkettete Liste implementiert werden, das ist uns aber relativ 
    egal. 

    Das Prinzip von einem Stack ist immer gleich.
    LIFO: 'Last in first out', das Element, welches man zuletzt auf den 
    Stack gepusht hat ist auch das Element welches als erste den Stack 
    wieder verlässt. Man hat 3 elementare Operatoren:

    > Stack.top(): <T>            ;Zeigt das oberste Element 
    > Stack.pop(): <T>            ;Zeigt das oberste Element und entfernt es
    > Stack.push(<T>): void       ;Legt eine neues Element auf den Stack
    > Stack.isEmpty(): boolean    ;Zeigt ob ein Stack exisiert

### 3.) Queue:
    Eine Queue ist auch eine besondere Datenstruktur, sie kann wie oben 
    als Array oder verkettete Liste implementiert werden, was uns immernoch 
    egal ist.

    Das Prinzip von einer Queue ist immer gleich.
    FIFO: 'First in First out', das Element welches man als erstes in die 
    Queue getan hat ist auch das, welches man zuerst bearbeiten muss.
    Man hat wieder ein paar elementare Operatoren. 

    > Queue.enqueue() können Daten an die Queue gehängt werden. 
    > Queue.dequeue() können Daten von der Queue genommen werden. 

---
# Dritte Aufgabe Bäume: 

### 1.) Bäume: 
    Ein Baum besitzt im Gegensatz zu Listen eine verzweigte Struktur, eine 
    Baumstruktur. Jedes Element kann mehrere Nachfolgerelement haben, aber 
    nur ein Vorgängerelement.
    
    Besonderheiten: 
    >    Die Wurzel des Baumes hat keinen Vorgänger
    >    Knoten ohne Nachfolger werden Blätter genannt
    >    Knoten, die werde Wurzel noch Blatt sind, heißen innere Knoten

    Ein paar Eigenschaften von Bäumen sollte man sich merken. 
        - Anzahl der Elemente: Jeder Baum hat 1 Element plus die Anzahl 
        der Elemente in seinen Kindener 
        - Tiefe: Die Anzahl der "Schichten"

    Traversierung von Bäumen: 
        Preoder:
            Zuerst den Knoten selbst und danch seine Kinder nach links. 

        Postorder:
            Zuerst die linken Kinknoten, dann die rechten und zuletzt den Knoten selbst.

        Inorder: 
            Zuerst den linken Kindknoten, dann den Knoten selbst und zuletzt 
            den rechten Kindknoten


### 2.) Binärebäume: 
    Bei einem Binärbaum hat jeder Knoten maximal zwei Kindknoten.
    Man kann dies als linken und rechten Kindknoten bezeichnen. 

    Zusätzlich sollte ein Datenelement an jedem Knoten angehängt sein. 
    Man kannn diesen auch als Binärenentscheidungsbaum benutzen, der Knoten
    kann hierbei als boolscher Ausdruck gesehen werden, das Traversieren nach 
    rechts bzw. links, als true bzw. false antwort auf den Ausdruck

