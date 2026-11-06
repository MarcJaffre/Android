--------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# <p align='center'> Installation d'application </p>
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## I. Téléphone
### A. Mode développeur
#### 1. Débloquer le menu
Aller dans les `paramètres` > `A propos du téléphone` puis cliquer 7 fois sur le numéro de la `Build` pour débloquer le menu.
#### 2. Mode débogage USB
Aller dans les `paramètres` > `Paramètres supplémentaires` > `Options développeur` et cocher `Débogage USB` et brancher votre téléphone sur le PC.
### B. Télécharger des applications 
#### 1. Rooter le téléphone
Télécharger l'APK puis renommer en `.zip` et utiliser le mode Sideload pour l'injecter.
```
https://github.com/topjohnwu/Magisk
```
#### 2. Google Appz
Il existe plusieurs package pour déployer les Google Appz. N'utiliser qu'un package. (La fonction Format Data / Factory Reset permet de nettoyer les apps)
```
https://github.com/MindTheGapps
https://nikgapps.com/
```

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## II. Root, Google Apps
### A. Root
#### 1. Extraire Boot.img
Extraire le fichier `boot.img` de l'image systèmen puis il faut transférer le fichier dans le Téléphone. (PixelOS_sweet-17.0-20261030-2119.zip)

#### 3. Magisk
La copier dans le téléphone puis lancer Magisk puis sélectionner le fichier.
#### 4. Flash
Transférer le fichier sur le PC.
```bash
adb reboot bootloader
# fastboot flash init_boot magisk_patched_XXXXX.img
fastboot flash boot D:\Users\Marc\Downloads\magisk_patched-31100_iKffs.img
fastboot reboot
```
#### 5. Systemless Hosts
Ouvrir Magisk > Paramètres > Fichier d'hôtes hors partition système

#### 6. Autoriser le Shell en root
Ouvrir Magisk > Super-Uilisateur > ajouter le `Shell`. 

#### 7. Débogage Sans fil
Aller dans les `paramètres` > `Paramètres supplémentaires` > `Options développeur` et cocher `Débogage Sans Fil` puis récupérer l'adresse.

```
adb connect 192.168.0.93:NOUVEAU_PORT
adb shell
su
```
#### 8. Hosts
L'application `PCAPdroid ` ou `RethinkDNS` permettent de relever les adresses utiliser des applications
```bash
nano /data/adb/modules/hosts/system/etc/hosts
```

```
# Nova Launcher
0.0.0.0 googleads.g.doubleclick.net
0.0.0.0 pagead2.googleadservices.com
0.0.0.0 logs.afs.vungle.com
```

```bash
clear;
# Tuer le processus Nova Launcher
am force-stop com.teslacoilsw.launcher
```
