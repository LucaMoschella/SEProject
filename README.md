## Progetto di Ingegneria del software 2015/2016, Informatica - La Sapienza

### Il progetto
Progettazione di un portale simile a [Vivino](https://www.vivino.com/), ma focalizzato sui prodotti a base di cioccolato.  
Voto finale: 28

### Le ultime correzioni

1. Da noi il CMS è il sistema, non un attore esterno. Quindi non ha senso metterlo come attore negli use case. Nel caso il sistema è una entità che utilizza un cms, vanno effettuati i relativi use case che gestiscono la comunicazione fra il sistema e il cms. (così come ci sono quelli per gli altri attori)

2. Nella pianificazione dei requisiti, non gli piace la classificazione delle priorità: ALTA MEDIA BASSA. In particolare la parola “[...] superflua [...]” nella descrizione del “BASSA”. A lui piace di più la convenzione MUST SHOULD COULD

3. Durante la gestione dei rischi manca il TRIGGER all’interno della fase di management: cosa devo vedere/verificare affinché mi possa rendere conto che il rischio si è verificato e quindi procedere al management dello stesso? (airbnb l’ha fatto ,vedi lì)

4. {Le classi di analisi le abbiamo dovute rifare tutte implementando il pattern ENTITY CONTROL BOUNDARY  (entity: dati, control: operazioni sui dati, boundary : classi che comunicano con l’esterno; entity e boundary non possono comunicare direttamente), prima le avevamo fatte un po’ a caso come se fossimo in java… e cele ha fatte rifare tutte}

5. Per le classi CONTROL noi abbiamo utilizzato il pattern singleton, ha detto che va bene, ma non è scalabile come soluzione (non permete la parallelizzazione o la distribuzione del sistema su più server… lui si è messo a fare esempi di liste utenti distribuite su più server (?)), quindi va motivato.

6. Nello studio di fattibilità non abbiamo scritto perchè è possibile utilizzare un cms, ha detto che non va bene e avremmo dovuto dire nello specifico per quale motivo è possibile usare un cms

7. Abbiamo fatto solo il login/iscrizione con Facebook, lui ha detto che in fase di analisi (requisiti e use case) era meglio parlare di Social Network in generale e magari implementare solo Facebook, e lasciare gli altri per aggiornamenti futuri

8. Ha detto che ci sono incongruenze con la stima dei costi e quello che realmente abbiamo fatto: abbiamo fatto una stima dei costi per realizzare il sistema, in seguito abbiamo ridotto il problema ad una “semplice” configurazione del CMS; Quindi non servono 4 anni (o quello che erano) come stimato, ma molto meno. Non ho idea di come si faccia a farla per bene… Forse riducendo il fattore di aggiustamento (quel numero che varia intorno al 28 e dipende dal tempo impiegato nei precedenti progetti fatti)

9. Nel diagramma di Gantt non ci va il tempo utilizzato per la stesura dei documenti, ma quello impiegato per ogni attività e fase del RUP

10. Mentre leggeva il progetto si stava incavolando perchè “Avete fatto tutto questo lavoro… ma poi se usate un cms e dovete solo configurarlo, che l’avete fatto a fare? Cosa avete fatto?” (domanda lecita). Ci ha salvato, circa, il mapping fra classi di analisi e plugin, in fase di design, del cms.

11. Il mapping fra classi di analisi e plugin del cms che implementano quella classe di analisi non lo voleva ad alto livello, ma “in modo tale che il programmatore non si deve studiare ogni plugin, deve solo seguire le istruzioni di design per configurare il cms e i suoi plugin”. Pretendeva quindi anche un spiegazione di quale funzionalità si utilizza in ogni plugin, come si configura; non gli basta una descrizione ad alto livello.
