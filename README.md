# Progetto JSP - Lista di persone

Si richiede un progetto che mostri una pagina JSP con una lista di persone inseribili tramite form.

La pagina, con la lista di persone e il form in calce, devono essere implementati interamente con java e JSP.

## Person

Un oggetto Person è composto dai seguenti campi:
- name (Stringa)
- surname (Stringa)
- email (Stringa)

## Funzionamento e validazione

Al primo accesso, la pagina mostra una tabella vuota seguita da un form che permetta l'inserimento del dato. Alla pressione del pulsante "submit" il dato (previa validazione, vedi sotto) viene caricato sul server in una lista memorizzata a livello del controller e visualizzato in tabella.
Ad ogni ciclo di inserimento, il controller esegue una validazione e si assicura che:
- name sia una stringa contenente almeno tre caratteri
- surname sia una stringa contenente almeno tre caratteri
- email sia una stringa non vuota e sintatticamente corretta e che non sia stata già inserita precedentemente.

Se una qualsiasi di queste condizioni viene meno, l'inserimento viene interrotto e viene visualizzato, sotto il form, un messaggio di errore appropriato.

## Requisiti

Per l'HTML non si richiede alcun tipo di styling. Si consiglia di segregare la logica business dalla esposizione. Lo scheletro fornito richiede l'uso di maven, java JRE+SDK versione 8 o superiori e Tomcat 8 o superiore.

Si consiglia di partire con l'implementazione di un Controller nel package "com.example" che erediti da HttpServlet e che implementi le doGet e doPost più una pagina jsp...