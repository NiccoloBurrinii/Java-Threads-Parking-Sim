# Java Threads: Priority Clinic

Progetto Java per la gestione di un ambulatorio veterinario con logiche di esclusione e priorità.

## Descrizione
Il programma gestisce l'accesso di cani e gatti a un ambulatorio seguendo regole di incompatibilità tra specie e implementando una logica di precedenza per i gatti in attesa.





## Funzionamento dei Thread:
* **Thread Animale**: Ogni thread rappresenta un animale definito dal tipo ("cane" o "gatto").
* **Logica di Ingresso**: L'accesso è regolato in modo che un cane non possa entrare se nell'ambulatorio è presente un gatto o se vi è almeno un gatto in coda d'attesa.

Il programma utilizza il metodo `.notifyAll()` per risvegliare tutti i thread in attesa ogni volta che un animale lascia l'ambulatorio, permettendo una nuova valutazione globale delle condizioni di ingresso.

## Tecnologie e Concetti
* **Java Core**: Utilizzo della classe `Thread` e monitoraggio degli stati tramite variabili di controllo.
* **Sincronizzazione Avanzata**: Gestione di condizioni di attesa multiple e politiche di priorità di categoria.
* **Thread Coordination**: Utilizzo strategico di `wait()` e `notifyAll()` per garantire la correttezza della simulazione.
