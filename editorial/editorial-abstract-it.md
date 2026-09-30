# Abstract editoriale

Una revisione delle campagne malware italiane del 2026 mostra quanto sia facile trasformare una correlazione valida in un'attribuzione eccessiva, oppure un metadato legittimo in un indicatore ostile.

La catena osservata a giugno nell'operazione GhostWallet riproduce diversi elementi distintivi di MintsLoader: un file JavaScript a tema fattura, l'esecuzione nascosta di PowerShell, l'endpoint `1.php?s=`, un dominio `.top` di 15 caratteri e la consegna di un payload successivo. Il contenuto dello stage remoto, tuttavia, non è disponibile. Il collegamento è quindi tecnicamente significativo ma resta una correlazione a confidenza moderata.

Il risultato più solido emerge dalla verifica degli IOC della campagna CERT-AGID del 24 settembre. `pesterbdd.com/images/Pester.png` è documentato almeno dal 2015 come URL dell'icona del modulo PowerShell Pester e ricompare in un report sandbox del 2022 insieme agli altri metadati del progetto. Senza telemetria che dimostri un contatto di rete specifico della campagna, l'URL va trattato come probabile rumore e non come prova di infrastruttura controllata dall'attaccante.

Il case study propone un metodo replicabile per separare destinazioni effettivamente contattate, stringhe estratte, metadati di dipendenze e correlazioni aggiunte dagli analisti.

## Titolo consigliato

MintsLoader e la provenienza degli IOC nelle campagne italiane del 2026

## Sottotitolo

Una correlazione prudente con Operation GhostWallet e il caso di un URL Pester probabilmente estratto fuori contesto
