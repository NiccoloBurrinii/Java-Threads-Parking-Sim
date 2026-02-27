# Java Threads: Parking Sim

Progetto Java per la simulazione di un parcheggio con posti limitati gestito tramite thread.

## Descrizione
Il programma modella l'accesso di più automobili a un numero ristretto di posti auto, gestendo la coda di attesa e la disponibilità della risorsa in tempo reale attraverso la sincronizzazione dei thread.



## Funzionamento dei Thread:
* **Thread Auto**: Rappresenta un veicolo che tenta di occupare un posto. Se il parcheggio è pieno, il thread entra in attesa per un tempo variabile prima di effettuare un nuovo tentativo.

Il programma utilizza un monitor sulla classe `RisorsaParcheggio` per incrementare e decrementare il numero di posti occupati in modo thread-safe, notificando gli altri thread al momento della liberazione di un posto.

## Tecnologie e Concetti
* **Java Core**: Utilizzo della classe `Thread`.
* **Sincronizzazione**: Gestione di risorse limitate e mutua esclusione su variabili condivise.
* **Concurrency Handling**: Simulazione di tempi di attesa realistici tramite `Thread.sleep()` e `wait(timeout)`.
