--------------------------------------------------------------------------------------------------------------------------------------------------
# <p align='center> Guide la lutte de la Publicité </p>
--------------------------------------------------------------------------------------------------------------------------------------------------
## I. Analyse
### A. Application
L'application `PCAPdroid ` ou `RethinkDNS` permettent de relever les adresses utiliser des applications

<br />

--------------------------------------------------------------------------------------------------------------------------------------------------
## II. Edition
### A. Débogage Sans fil
Aller dans les `paramètres` > `Paramètres supplémentaires` > `Options développeur` et cocher `Débogage Sans Fil` puis récupérer l'adresse.
### B. Se connecter
```
adb connect 192.168.0.93:XXXXX
adb -s      192.168.0.93:XXXXX shell
adb shell
su
```

### B. Hosts
```bash
nano /data/adb/modules/hosts/system/etc/hosts
```

```bash
clear;

# Vider DNS
ndc resolver clearnetdns wlan0
```

### C. Tuer le processus Nova Launcher
```
am force-stop com.teslacoilsw.launcher
```


--------------------------------------------------------------------------------------------------------------------------------------------------
## III. Liste de Blocage
### A. Nova Launcher
```bash
0.0.0.0 api.novalauncher.com
0.0.0.0 logs.ads.vungle.com
0.0.0.0 ncmrsa-ag-in-f2.1e100.net
```

### B. Global
```
0.0.0.0 firebaselogging.googleapis.com
0.0.0.0 googleads.g.doubleclick.net
0.0.0.0 pagead2.googleadservices.com
0.0.0.0 pagead2.googlesyndication.com
```
