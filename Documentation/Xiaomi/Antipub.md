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
android.clients.google.com
connectivitycheck.gstatic.com
gstatic.com
play.fe.googleapis.com
play.googleapis.com
play.lh.googleusercontent.com
playstoregatewayadapter-pa.googleapis.com
prod-it.playstoregatewayadapter-pa.googleapis.com
i.ytimg.com
```

### B. Services Google Play
```bash
android.googleapis.com
googleapis.com
quake-pa.googleapis.com
mtalk.google.com
spot-pa.googleapis.com
```


### A. Global
```
firebaselogging.googleapis.com
googleads.g.doubleclick.net
pagead2.googleadservices.com
pagead2.googlesyndication.com
```

### X. Nova Launcher
```bash
fonts.googleapis.com
web.facebook.com
api.novalauncher.com
logs.ads.vungle.com
ncmrsa-ag-in-f2.1e100.net
pubsads.g.doubleclick.com
redirector.gvt1.com
static.doubleclick.com
s0.2mdn.net
s1.2mdn.net
tpc.googlesyndication.com
googletagservices.com
```


--------------------------------------------------------------------------------------------------------------------------------------------------
## IV. Blocage

```
# --- BLOCAGE GLOBAL & NOKIA LAUNCHER ---
0.0.0.0 ://googleapis.com
0.0.0.0 googleads.g.doubleclick.net
0.0.0.0 ://googleadservices.com
0.0.0.0 ://googlesyndication.com
0.0.0.0 ://googleapis.com
0.0.0.0 ://facebook.com
0.0.0.0 ://novalauncher.com
0.0.0.0 ://vungle.com
0.0.0.0 ncmrsa-ag-in-f2.1e100.net
0.0.0.0 ://doubleclick.com
0.0.0.0 ://gvt1.com
0.0.0.0 ://doubleclick.com
0.0.0.0 s0.2mdn.net
0.0.0.0 s1.2mdn.net
0.0.0.0 ://googlesyndication.com
0.0.0.0 googletagservices.com

# --- OBSERVATION (NON BLOQUÉS POUR PRÉSERVER LE SYSTÈME) ---
# ://google.com
# ://gstatic.com
# gstatic.com
# ://googleapis.com
# ://google.com
```
