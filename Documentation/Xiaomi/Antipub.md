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
bash
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
### X. Aurora Store
```
rr3--sn-hgn7m7y.gvt1.com ==> 172.217.133.8 ==> mrs08s09-in-f8.1e100.net
```
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

### X. Gestionnaire de fichier
```
firebaselogging-pa.googleapis.com
report.appmetrica.yandex.net
```


### X. Global
```
firebaselogging.googleapis.com
googleads.g.doubleclick.net
pagead2.googleadservices.com
pagead2.googlesyndication.com
```

### X. Services Google Play
```bash
android.googleapis.com
googleapis.com
quake-pa.googleapis.com
mtalk.google.com
spot-pa.googleapis.com
```


### X. Nova Launcher
```bash
fonts.googleapis.com
web.facebook.com
api.novalauncher.co
lh3.googleusercontent.com
logs.ads.vungle.com
ncmrsa-ag-in-f2.1e100.net
pubsads.g.doubleclick.com
redirector.gvt1.com
redirector.gvt1-cn.com
sdkapi.dsp-api.moloco.com
static.doubleclick.com
s0.2mdn.net
s1.2mdn.net
tpc.googlesyndication.com
googletagservices.com
```


### X. ZX File Manager
```
firebase-settings.crashlytics.com
firebaseinstallations.googleapis.com
graph.facebook.com
fundingchoicesmessages.google.com
marketingplatform.google.com
img.rareprob.com
```


--------------------------------------------------------------------------------------------------------------------------------------------------
## IV. Blocage

```bash

cat > /data/adb/modules/hosts/system/etc/hosts << 'EOF'
cat > /data/adb/modules/hosts/system/etc/hosts << 'EOF'
# ========================================================
# Carte Réseau par défaut
# ========================================================
127.0.0.1       localhost
::1             ip6-localhost

# ========================================================
# APPAREIL GLOBAL & INFRASTRUCTURES PUBLICITAIRES
# ========================================================
0.0.0.0 ://googleapis.com
0.0.0.0 ://googleapis.com
0.0.0.0 ://googleapis.com
0.0.0.0 ://crashlytics.com
0.0.0.0 googleads.g.doubleclick.net
0.0.0.0 securepubads.g.doubleclick.net
0.0.0.0 doubleclick.net
0.0.0.0 ://doubleclick.com
0.0.0.0 ://doubleclick.com
0.0.0.0 ://googleadservices.com
0.0.0.0 ://googlesyndication.com
0.0.0.0 ://googlesyndication.com
0.0.0.0 googletagservices.com
0.0.0.0 s0.2mdn.net
0.0.0.0 s1.2mdn.net
0.0.0.0 ncmrsa-ag-in-f2.1e100.net
0.0.0.0 ://google.com
0.0.0.0 ://google.com

# ========================================================
# TRAQUEURS TIERS & RÉGIES MOBILES LÉGACY
# ========================================================
0.0.0.0 ://facebook.com
0.0.0.0 ://facebook.com
0.0.0.0 vungle.com
0.0.0.0 ://vungle.com
0.0.0.0 ://moloco.com
0.0.0.0 molocoads.com
0.0.0.0 report.appmetrica.yandex.net

# ========================================================
# CONFIGURATIONS SPÉCIFIQUES DES APPLICATIONS
# ========================================================
# --- Nova Launcher & Dépendances ---
0.0.0.0 api.novalauncher.co
0.0.0.0 ://googleusercontent.com

# --- ZX File Manager ---
0.0.0.0 ://rareprob.com

# --- Redirections & Polices ---
0.0.0.0 ://googleapis.com
0.0.0.0 ://gstatic.com
0.0.0.0 ://gvt1.com
0.0.0.0 ://gvt1-cn.com
0.0.0.0 gvt1.com

# ========================================================
# Fin du fichier
# ========================================================

EOF

```
