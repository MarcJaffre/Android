

```
adb connect 192.168.0.93:NOUVEAU_PORT
adb -s 192.168.0.93:40937 shell
adb shell
su
```
#### 8. Hosts
L'application `PCAPdroid ` ou `RethinkDNS` permettent de relever les adresses utiliser des applications
```bash
nano /data/adb/modules/hosts/system/etc/hosts
```

```
# Gestionnaire de fichiers
# Nova Launcher
0.0.0.0 api.novalauncher.com
0.0.0.0 firebaselogging.googleapis.com
0.0.0.0 googleads.g.doubleclick.net
0.0.0.0 logs.afs.vungle.com
0.0.0.0 ncmrsa-ag-in-f2.1e100.net
0.0.0.0 pagead2.googleadservices.com
0.0.0.0 pagead2.googlesyndication.com
```

```bash
clear;

# Vider DNS
ndc resolver clearnetdns wlan0

# Tuer le processus Nova Launcher
am force-stop com.teslacoilsw.launcher
```
