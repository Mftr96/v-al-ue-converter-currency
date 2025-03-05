
# TITOLO





## Indice

1. [consegna](#consegna)
2. [considerazioni_pre-progetto](#considerazioni-pre-progetto)
3. [strumenti-aggiuntivi](#strumenti-aggiuntivi )
3. [esecuzione](#esecuzione-milestone)
5. [prossimamente-sul-piccolo-schermo](#roadmap)



## Consegna
esercizio di oggi: Vue 3 Currency Converter nome repo: vue-currency-converter

Stiamo organizzando dei viaggi all’estero e ci farebbe tanto comodo un convertitore di valute molto veloce da usare all’occorrenza.
In una versione di base, abbiamo due input numerici e due select.
L’utente può scrivere in entrambi gli input e convertire nelle valute impostate nelle select. Le valute presenti come options nelle select sono prese dall’API Frankfurter, gratuita e utilizzabile senza API key. Ogni cambiamento in uno degli input chiama l’endpoint relativo alla conversione tra valute.

Per una versione più avanzata possiamo:
disabilitare currency nella select in relazione all’altra selezionata (evitare conversione su due currency uguali) 
aggiungere un’intestazione sfruttando la classe Intl di JS per la formattazione delle currency 
Se neanche la versione avanzata ci basta, possiamo aggiungere un grafico con Apex Charts (o chart.js o vue-chart-js), da customizzare a piacere.
La grafica nell’anteprima è di esempio, potete realizzarla come preferite.

Milestone 1 Creare un componente che contenga un campo di input una select. Questo componente servirà sia per il primo input che per il secondo ricevendo tramite props la lista delle valute.

Milestone 2 Effettuare all’avvio dell’applicazione una chiamata all’API (con axios) per popolare le due select con la lista delle valute. La prima select avrà come valore selezionato di default "Euro" e la seconda "United State Dollar".

Milestone 3 Ogni volta che l’utente scrive qualcosa in uno dei due input bisognerà fare in modo che venga effettuata una chiamata all’API per ottenere il valore convertito nella valuta selezionata.

Milestone 4 Al cambio di un valore selezionato in una delle due select bisognerà effettuare una nuova chiamata all'API per ottenere il nuovo valore convertito nella valuta corretta.

Bonus 1 Disabilitare la currency nella select in relazione all’altra selezionata (evitare conversione su due currency uguali).

Bonus 2 Aggiungere un componente che contenga il grafico (potete utilizzare la libreria Apex Charts) del rapporto dei valori delle due valute selezionate nelle due select.

Bonus 3 Utilizzare axios con async/await al posto della sintassi then/catch.
</aside>
Suggerimenti 
Questa API riceverà il valore del campo appena modificato e le due valute per la conversione quindi la chiamata avverrà al keyup del’input.
Nella chiamata all'API bisogna mettere in from la valuta selezionata e to l'altra. Ad esempio, nella situazione di default se scrivo 5 nelll'input di EUR l'endpoint sarà: /latest?amount=5&from=EUR&to=USD mentre se scivo 5 nel campo relativo a USD l'endpoint sarà /latest?amount=5&from=USD&to=EUR
Diversamente, al cambio della select l’enpoint sarà sempre lo stesso ma l’ordine from/to sarà sempre in relazione al primo e secondo input


## considerazioni pre-progetto


## Esecuzione milestone

## Roadmap
🏳️: da fare 
🔨:in corso d'opera
☑️:fatto

- rileggere la consegna e ripartire con le milestone🏳️
- milestone 1🏳️
- milestone 2🏳️
- milestone 3🏳️
- milestone 4🏳️
- milestone 5🏳️