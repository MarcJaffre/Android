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
## III. Analyse réseau
### A. Google Play Store
```
0.0.0.0 android.clients.google.com
0.0.0.0 connectivitycheck.gstatic.com
0.0.0.0 gstatic.com
0.0.0.0 play.fe.googleapis.com
0.0.0.0 play.googleapis.com
0.0.0.0 play.lh.googleusercontent.com
0.0.0.0 playstoregatewayadapter-pa.googleapis.com
0.0.0.0 prod-it.playstoregatewayadapter-pa.googleapis.com
0.0.0.0 i.ytimg.com
```

### B. Services Google Play
```bash
0.0.0.0 android.googleapis.com
0.0.0.0 googleapis.com
0.0.0.0 quake-pa.googleapis.com
0.0.0.0 mtalk.google.com
0.0.0.0 spot-pa.googleapis.com
```


### A. Global
```
0.0.0.0 firebaselogging.googleapis.com
0.0.0.0 googleads.g.doubleclick.net
0.0.0.0 pagead2.googleadservices.com
0.0.0.0 pagead2.googlesyndication.com
```


### X. Nova Launcher
```bash
0.0.0.0 fonts.googleapis.com
0.0.0.0 web.facebook.com
0.0.0.0 api.novalauncher.com
0.0.0.0 logs.ads.vungle.com
0.0.0.0 ncmrsa-ag-in-f2.1e100.net
0.0.0.0 pubsads.g.doubleclick.com
0.0.0.0 redirector.gvt1.com
0.0.0.0 static.doubleclick.com
0.0.0.0 s0.2mdn.net
0.0.0.0 s1.2mdn.net
0.0.0.0 tpc.googlesyndication.com
0.0.0.0 googletagservices.com
```
