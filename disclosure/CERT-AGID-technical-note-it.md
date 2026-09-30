# Nota tecnica per CERT AGID

## Oggetto

Richiesta di verifica della provenienza di un indicatore pubblicato per la campagna MintsLoader del 24 settembre 2026 e condivisione di una correlazione tecnica con un incidente di giugno.

## Sintesi

L'analisi del JSON pubblico relativo all'evento 26383 ha evidenziato due elementi utili per una verifica congiunta.

Il primo riguarda `pesterbdd.com/images/Pester.png`. L'URL compare come `IconUri` nel manifest Pester 3.3.5 della PowerShell Gallery e nel pacchetto Chocolatey Pester 3.3.12, aggiornato nel dicembre 2015. Compare inoltre nella memoria di PowerShell in un report Joe Sandbox del 1 dicembre 2022, accanto al repository GitHub di Pester e alla licenza Apache. Queste evidenze indicano una provenienza storica legittima e rendono plausibile che l'URL sia stato raccolto come metadato o artefatto ambientale.

La richiesta non presuppone che l'indicatore sia errato né che il dominio sia oggi necessariamente sicuro. Sarebbe utile sapere se, durante la campagna, l'URL è stato effettivamente contattato e ha restituito contenuto, oppure se è stato estratto da file, memoria, dipendenze o output automatizzati.

Il secondo elemento riguarda l'indirizzo `165.22.13.227`, presente nel JSON di settembre e nel report Certego sull'incidente GhostWallet del 9 giugno 2026. La catena di giugno presenta diversi elementi compatibili con MintsLoader: esca `Fattura` in JavaScript, PowerShell nascosto, richiesta a `1.php?s=<UUID>`, dominio `.top` di 15 caratteri e consegna di un payload successivo. Il contenuto dello stage remoto non è disponibile pubblicamente; la relazione viene pertanto proposta come correlazione a confidenza moderata, non come attribuzione definitiva.

## Evidenze allegate

- Paper tecnico in formato PDF, DOCX e Markdown.
- Elenco degli indicatori confermati.
- Matrice delle correlazioni con livello di confidenza.
- Elenco degli indicatori esclusi o rumorosi con motivazione.
- Registro delle fonti pubbliche.

## Richiesta di riscontro

Si richiede, se possibile, un riscontro su:

1. modalità di raccolta di `pesterbdd.com/images/Pester.png`;
2. presenza di una richiesta DNS o HTTP osservata durante l'esecuzione;
3. eventuale associazione interna della catena di giugno a MintsLoader;
4. eventuali limitazioni alla pubblicazione delle conclusioni e degli indicatori già pubblici.
