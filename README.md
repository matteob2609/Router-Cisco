# Configurazione di un router Cisco

❗ Prerequisito: avere Packet Tracer (risorsa Cisco) installato sul computer.

[Comandi principali](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#ghost-comandi-principali)

[Modifica dell'hostname](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#ghost-modifica-dellhostname)

[Password Privileged EXEC](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#ghost-password-privileged-exec)

[Password User EXEC](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#ghost-password-user-exec)

[Password linee del terminale virtuale (VTY)](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#ghost-password-linee-del-terminale-virtuale-vty)

[Crittografia delle password](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#ghost-crittografia-delle-password)

[Configurazione di un'interfaccia](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#ghost-configurazione-di-uninterfaccia)

---

### :ghost: COMANDI PRINCIPALI

- _enable_, entra in modalità **Privileged Exec**, passaggio del terminale da > a #;

- _configure terminal_ oppure _conf t_, entra nella modalità di **configurazione globale**, contrassegnata da (config);

- _banner motd #messaggio#_, verrà visualizzato come prima cosa quando si accede alla CLI del router;

- _copy running-config startup-config_, sostituisce la configurazione iniziale con quella attuale modificata;

- _exit_, esce dalla attuale modalità attiva.

[Torna su](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#configurazione-di-un-router-cisco)

---

### :ghost: MODIFICA DELL'HOSTNAME

- _Router(config)#hostname 'nome'_

[Torna su](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#configurazione-di-un-router-cisco)

---

### :ghost: PASSWORD PRIVILEGED EXEC

:heavy_exclamation_mark: **N.B. Se si desidera una lunghezza minima per le password inserire il comando _passwords min-length_ seguito dal valore di lunghezza minima** :heavy_exclamation_mark:

- _Router(config)#enable secret 'password'_

[Torna su](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#configurazione-di-un-router-cisco)

---

### :ghost: PASSWORD USER EXEC

- _Router(config)#line console 0_

- _Router(config-line)#password 'password'_

- _Router(config-line)#login_

[Torna su](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#configurazione-di-un-router-cisco)

---

### :ghost: PASSWORD LINEE DEL TERMINALE VIRTUALE (VTY)

- _Router(config)#line vty 0 15_

- _Router(config-line)#password 'password'_

- _Router(config-line)#login_

[Torna su](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#configurazione-di-un-router-cisco)

---

### :ghost: CRITTOGRAFIA DELLE PASSWORD

- _Router(config)#service password-encryption_

:pushpin:`Checkpoint: verificare che le password siano state criptate inserendo il comando show running-config`.

[Torna su](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#configurazione-di-un-router-cisco)

---

### :ghost: CONFIGURAZIONE DI UN'INTERFACCIA

- _Router(config)#interface 'nome_interfaccia'_

- _Router(config-if)#ip address 'IP' 'subnet_mask'_

- _Router(config-if)#no shutdown_, abilita l'interfaccia.

:pushpin:`Checkpoint: se l'interfaccia è stata abilitata correttamente verrà visualizzato il seguente output:`.

    %LINK-5-CHANGED: Interface 'nome_interfaccia', changed state to up
    
[Torna su](https://github.com/matteob2609/Router-Cisco/blob/main/README.md#configurazione-di-un-router-cisco)
