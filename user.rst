Manuale utente
==================================

L'interfaccia grafica
--------------------------------------------

.. image:: ../../manuale_geoportale_concerteaux/img/interfaccia.png

Linterfaccia, intuitiva e user-friendly, è composta da:

* **Area di Mappa** qui vengono visualizzati i dati.
.. seealso:: Per maggiori dettagli sulla configurazione dell'area di mappa si rimanda al manuale di Lizmap https://docs.lizmap.com/current/it/publish/lizmap_configuration.html#configure-the-map

* **Albero dei Layer** qui sono elencati tutti i layer pubblicati e quindi disponibili sul WebGIS. I dati mantnegono la stessa organizzazione (suddivisione in gruppi e sotto-gruppi) del progetto QGIS. I singoli layers, gruppi e sottogruppi possono essere "accesi" e "spenti" cliccando sulla checkbox corrispondente. Cliccando invece sulla freccia accanto alla checkbox è possibile espandere il gruppo e visualizzarne quindi il contenuto oppure, nel caso dei layer, visualizzarne la legenda. Inoltre cliccando sul nome del gruppo o del layer è pissibile accedere a un popup contenete eventuali informazioni, modificarne l'opacità, zoommare all'estensione del layer e se possibile (ovvero definito lato QGIS) scaricare il dato.

.. seealso:: Per maggiori dettagli sulla configurazione di gruppi e layer si rimanda al manuale di Lizmap https://docs.lizmap.com/current/en/publish/lizmap_configuration.html#configure-layers-and-groups

.. image:: img/layer.gif

* **Menù dei layer di base** qui sono elencati tutti gli sfondi cartografici definiti lato QGIS (Plugin Lizmap) per il webGIS.

.. seealso:: Per maggiori dettagli sulla configurazione dei layer di base si rimanda al manuale di Lizmap https://docs.lizmap.com/current/en/publish/lizmap_configuration.html#configure-the-base-layers

.. image:: img/base_layer.gif

* **Toolbar** da qui è possibile accedere a tutti gli strumenti abilitati e quindi disponibili sul webGIS (metadati, editing, selezione, localizzazione, stampa, misura, permalink, tabelle degli attributi, ecc.). I singoli strumenti saranno meglio descritti nella sezione **Strumenti e funzioni**.

.. image:: img/tool.gif

* **Pan e Zoom** strumenti per la navigazione dell'area di mappa (sposta, zoom con rettangolo, zoom alla massima estenzione, zoom-in e zoom-out, zoom precedente e successivo).
* **Scala e Coordinate del mouse** qui vengono mostrate la scala di visualizzazione e le coordinate al puntatore del mouse espresse.

Il pulsante **Login** in alto a destra nell'header, consente appunto all'utente di accreditarsi con il proprio user e password. A seconda dei privilegi attribuiti ai singoli utenti dall'amministratore del Geoportale, l'utente potra accedere a strumenti e funzioni che altrimenti non sono visibili come il download o l'editing dei dati.


Strumenti e funzioni
--------------------------------------------

Modifica
+++++++++
Lo strumento **Modifica** compare nella toolbar solo se l'utente ha eseguito il login e se gli sono stati attribuiti i permessi per la modifica dei dati. Lo strumento consente di:

* creare nuovi elementi (sia la geometria che le relative informazioni alfanumeriche),
* modificare le geometrie e/o le relative informazioni alfanumeriche
* eliminare le geometrie esistenti

Per creare nuovi elementi è sufficiente cliccare sul bottone dello strumento **Modifica** nella toolbar, disegnare la geometria nell'area di mappa e inserire le varie informazioni nella tabella. **Attenzione** i campi della tabella, contrassegnati da un asterisco rosso, sono obbligatori ciò significa che è necessario inserire delle informazioni affinche il nuovo elemento sia correttamente salvato

Per modificare un elemento esistente invece, è ncessario interrogare l'elemento desiderato cliccando con il mouse e si aprirà il pop-up con l'elenco delle informazioni associate all'elemento. Nel pop-up è presente una toolbar, selezionando lo strumento modifica da qui è possibile accedere e quindi modificare le informazioni associate o la geometria. Allo stesso modo è possibile accedere allo strumento di modifica delle informazioni tramite lo strumento **Dati**. Ovviamente è possibile anche modificare la geometria semplicemente attivando la modifica e *trascinando* nella posizione desiderata il punto o, in caso di linee e poligoni, i singoli vertici.

Per eliminare invece un elemento esistente, il procedimento è simile a quello della modifica. Bisogna infatti accedere allo strumento modifica presente nella toolbar del pop-up che compare interrogando l'elemento di interesse e andare a inserire la data in corrispondenza del campo **data_eliminazione**.

In ogni caso per rendere effettiva qualsiasi modifica ai dati (creazione di nuovi elementi, modifica o eliminazione degli esistenti) è necessario premere il pulsante *Salva*. ATTENZIONE: una volta salvate le modifiche non sarà più possibile tornare indietro.

.. image:: img/modifica.gif

Per maggiori dettagli si rimanda al manuale di Lizmap Web Client https://docs.lizmap.com/current/it/user/user_guide.html#editing-spatial-data


Selezione
++++++++++
Lo strumento **Selezione** permette di selezionare le geometrie di un layer a sua volta selezionato tramite il menù a tendina dello strumento. Gli strumenti di selezione disponibili sono:

* selezione tramite riquadro
* slezione tramite cerchio
* selezione tramite poligono
* selezione tramite disegno a mano libera

E' possibile creare una nuova selezione, aggiungere gli elementi selezionati alla selezione esistente oppure rimuovere gli elementi selezionati dalla selezione esistente. Inoltre è possibile deselezionare tutti gli elementi slezionati oppure filtrare gli elementi selezionati. Con il filtro resteranno visibili nell'area di mappa solo gli elementi precedentemente selezionati. ovviamente è possibile rimuovere il filtro per visualizzare nuovamente tutte le geometrie.

.. image:: img/selezione.gif


Localizzazione
+++++++++++++++
Lo strumento **Localizzazione** permette di cercare e selezionare un comune facente parte del bacino del Roia. Una volta selezionato, l'area di mappa viene zoomata e centrata all'estensione del comune. E' sufficiente digitare i primi caratteri del nome del comune per trovarlo all'interno della lista. Altrimenti è possibile aprire il menù a tendina e scorrerlo per trovare il comune di interesse.

.. image:: img/localizzazione.gif

Stampa
+++++++
Lo strumento **Stampa** permette di salvare l'area di mappa in formato immagine (pdf, jpg, ecc.). Al momento sono disponibili 4 layout di stampa (A4 orizzontale e verticale, A3 orizzontale e verticale) da scegliere nel relativo menù a tendina dello strumento. E' possibile definire la scala di stampa da scegliere dal relativo menù a tendina e la risoluzione dell'immagine. Sono disponibili diversi formati file (PDF, JPG, PNG e SVG). Una volta attivato lo strumento, comparirà nell'area di mappa un riquadro rosso la cui forma e dimensione cambierà a seconda del layout e dalla scala scelta per la stampa. E' sufficiente spostare il riquadro per inquadrare la porzione di mappa che si vuole stampare. nella stampa compariranno tutti i layer che sono stati accesi nell'albero dei layer e lo sfondo cartografico scelto.

.. image:: img/stampa.gif

Misura
++++++++
Lo strumento **Misura** permette di misurare:

* una lunghezza
* un'area
* un perimetro

E' sufficiente selezionare il tipo di misura che si vuole fare dal menù a tendina e iniziare a disegnare sull'area di mappa la lunghezza/l'area/ il perimetro che si vuole misurare. Un click del tastro destro del mouse aggiunge un unovo nodo al tracciato della misura, doppio click con il tasto destro del mouse per chiudere il tracciato e quindi interrompere la misura. E' possibile passare da un tipo di misura all'altro semplicemente selezionando quello desiderato dal menù a tendina senza dover chiudere e riaprire lo strumento.

.. image:: img/misura.gif

Dati
++++++
Lo strumento **Dati** permette di visualizzare in un pannello, che viene aperto automaticamente in basso cliccando sul pulsante nella toolbar laterale, la tabella degli attributi associata alle geometrie dei vari layer pubblicati nel geoportale. All'apertura, il pannello mostra l'elenco dei layer per i quali è possibile visualizzare la tabella. E' sufficiente premere sul pulsante *Dettaglio* corrispondente al layer desiderato per visualizzare la tabella. 

Una volta aperta la tabella degli attributi, è possibile agire sulle singole righe tramite i pulsanti in corrispondenza di ciascuna riga. Questi tool permettono di:

* selezionare la riga e quindi la geometria corrispondente, 
* zoomare sulla geometria, 
* centrare l'area di mappa sulla geometria ,
* modificare le informazioni alfanumeriche presenti in tabella (solo se l'utente loggato è abilitato alla modifica dei dati)

E' possibile inoltre filtrare le righe mostrate in tabella digitando ad esempio una parola chiave o anche solo alcuni caratteri nel form *Cerca*. Saranno quindi mostrate solo le righe che rispondono al criterio di ricerca. Per tornare alla visualizzazione totale delle righe è sufficiente cancellare il contenuto dal form *Cerca*. Una volta filtrate le righe secondo un criterio di interesse, tutte le geometrie sono comunque visibili nell'area di mappa mentre saranno visualizzate solo le righe della tabella che rispondono al criterio di ricerca.

Gli strumenti accanto al form *Cerca* permettono di:

* selezionare tutte le righe, 
* deselezionare le righe selezionate, 
* spostare le righe selezionate in cima alla tabella
* filtrare i dati (con questo strumento verranno temporaneamente visualizzate solo le geometrie e le corrispondenti righe in tabella che rispondono al criterio di ricerca. Per tornare alla visualizzazione totale è sufficiente cliccare nuovamente sul pulsante del filto),
* visualizzare i valori della tabella.

.. image:: img/dati.gif

Per maggiori dettagli si rimanda al manuale di Lizmap Web Client https://docs.lizmap.com/current/it/user/user_guide.html#attribute-layers




.. _Gter srl: https://www.gter.it
