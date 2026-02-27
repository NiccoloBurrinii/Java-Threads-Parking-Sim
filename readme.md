# Java Parking Simulation (Thread Concurrency)

Una simulazione multi-thread di un sistema di gestione parcheggi sviluppata in Java.

## Descrizione del Progetto
Il software modella un parcheggio con una capacità limitata (4 posti) servito da più processi indipendenti (8 automobili) rappresentati da Thread. Il sistema gestisce l'accesso alla risorsa condivisa evitando conflitti e gestendo i tempi di attesa.



## Logica di Funzionamento
* **Gestione Capacità**: Se il parcheggio è pieno (`is_Full`), i nuovi thread in arrivo entrano in uno stato di attesa (`wait`) per un tempo casuale.
* **Sincronizzazione**: Quando un'auto libera un posto, viene inviata una notifica (`notify()`) per risvegliare uno dei thread in attesa.
* **Tempi Random**: Ogni auto rimane parcheggiata per un tempo variabile, simulando un comportamento reale.

## Tecnologie Utilizzate
* **Java Concurrency**: Estensione della classe `Thread`.
* **Monitor Objects**: Uso dei metodi nativi `wait()` e `notify()`.
* **Resource Locking**: Gestione dello stato della risorsa condivisa `RisorsaParcheggio`.
