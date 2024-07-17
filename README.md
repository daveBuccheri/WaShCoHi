# WaShCoHi

Wazuh, Shuffle, Cortex and The Hive

## Fonte

Part 1: https://redhotcyber.com/post/costruire-un-soc-in-casa-con-100-euro/

Part 2: https://www.redhotcyber.com/post/costruiamo-un-soc-domestico-con-soli-100-euro-simulazione-attacchi-caldera-infection-monkey-e-atomic-test/

Part 3: https://www.redhotcyber.com/post/costruire-un-soc-con-wazuh-the-hive-shuffle-su-un-minipc-da-100e-guida-pratica-al-pentesting-in-ottica-purple-team/

## Componenti

1. Wazuh integrato con VirusTotal: per la gestione delle informazioni di sicurezza e la rilevazione delle minacce in tempo reale.
2. Shuffle: una piattaforma SOAR (Security Orchestration, Automation, and Response) per automatizzare i processi di risposta agli incidenti.
3. Cortex: per la raccolta e l’analisi dell’intelligence di sicurezza.
4. The Hive: per il management dei casi e la collaborazione tra team (voi e voi stessi in questo caso).

## Panoramica Laboratorio

1. Un container Ubuntu con Atomic Red Canary per simulare diversi tipi di attacchi basati sul framework MITRE ATT&CK.
2. Due macchine Kali Linux: una all’interno della rete AD e una all’esterno, per eseguire attacchi manuali e testare le vulnerabilità da diverse prospettive.
3. Un dominio Active Directory con un Domain Controller Windows Server 2019 e due membri del dominio Windows 10.

Per far ciò è stato messo su Proxmox. 

In attività:
- 2 Containers Kali (uno interno alla rete di Active Directory ed uno al suo esterno)
- 2 Macchine Ubuntu Server (che non si sa mai uno non basti)
- 2 Macchine Windows di cui un Server – Domain Controller ed un Client “Batman” (più avanti , nella sezione dedicata agli attacchi ad Active Directory scopriremo che il suo local admin si chiama Bruce Wayne )

## Strumenti di attacco

Strumenti open-source di simulazione di attacchi e violazioni: Caldera, Infection Monkey e Atomic Test.

Sono strumenti che aiutano ad individuare le vulnerabilità e a validare i controlli di sicurezza esistenti. 
- Caldera è noto per la sua capacità di automatizzare vari scenari di attacco, fornendo un’analisi dettagliata delle misure di difesa. 
- Infection Monkey è ampiamente utilizzato per la sua facilità d’uso ed efficacia nel simulare ransomware e valutazioni di fiducia zero. 
- Atomic Test, d’altra parte, offre flessibilità nei test personalizzati su specifici vettori di attacco.