# 📝 To-Do List Web App

Un'applicazione web semplice e intuitiva per la gestione delle attività quotidiane ("To-Do List").
Il progetto è stato realizzato con **HTML**, **CSS** e **Vanilla JavaScript**, focalizzandosi sulla manipolazione del DOM e sulla gestione dello stato dell'applicazione.

![Anteprima Progetto](Immagine%202025-12-14%20174110.png)
*(Sostituisci questo percorso con quello reale della tua immagine se la carichi su GitHub)*

## ✨ Funzionalità

* **Aggiunta Task:** Inserimento dinamico di nuove attività tramite input testuale.
* **Rimozione Task:** Possibilità di cancellare ogni singola attività grazie a un pulsante dedicato ("X").
* **Scroll Personalizzato:** Gestione dell'overflow con scrollbar stilizzate via CSS.
* **Layout Responsivo:** Utilizzo di Flexbox per l'allineamento degli elementi (testo a sinistra, tasto delete a destra).
* **Controlli Input:** Prevenzione dell'inserimento di task vuoti.

## 🛠 Tecnologie Utilizzate

* **HTML5:** Struttura semantica.
* **CSS3:** Styling avanzato (Flexbox, proprietà `overflow`, personalizzazione scrollbar).
* **JavaScript (ES6+):** Logica applicativa.

## 🧠 Dettagli Tecnici

Il progetto non si limita a manipolare l'HTML, ma segue un approccio logico strutturato:

### 1. Gestione dello Stato (State-Based Rendering)
L'applicazione utilizza un **Array** (`lista`) come "unica fonte di verità".
Ogni volta che i dati cambiano (aggiunta o rimozione), la funzione `visualizza()` ridisegna completamente la lista HTML. Questo garantisce che l'interfaccia sia sempre sincronizzata con i dati.

### 2. Dataset API (`data-index`)
Per collegare l'interfaccia grafica (DOM) alla logica dei dati (Array), è stato utilizzato l'attributo `data-*`.
Ogni bottone "delete" porta con sé il proprio indice:
```javascript
button.dataset.index = index;
