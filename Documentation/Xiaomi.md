-------------------------------------------------------------------------------------------------------------------------------------------------
# <p align='center'> Installer une ROM custom </p>
-------------------------------------------------------------------------------------------------------------------------------------------------
## I. Préparation
### A. Mode développeur
#### 1. Débloquer le menu
Aller dans les `paramètres` > `A propos du téléphone` puis cliquer 7 fois sur le numéro de la `Build` pour débloquer le menu.
#### 2. Mode débogage USB
Aller dans les `paramètres` > `Paramètres supplémentaires` > `Options développeur` et cocher `Débogage USB` et brancher votre téléphone sur le PC.



### B. Xiamoi
#### 1. Redmi Note 10 Pro/Max
Télécharger et extraire le logiciel [mi Flash Unlock](https://miuirom.xiaomi.com/rom/u1106245679/7.6.727.43/miflash_unlock_en_7.6.727.43.zip)
#### 2. Pilote
Connecter le téléphone et lancer le programme `driver_install_64.exe` pour installer les pilotes. Débrancher et rebrancher le téléphone.

<img width="296" height="53" alt="image" src="https://github.com/user-attachments/assets/9fa9bcad-5a38-4621-91f5-86305ffb834b" />

#### 2. Unlock
Lancer le logiciel `miflash_unlock.exe` puis suivez les étapes.

<br /> <br />

-------------------------------------------------------------------------------------------------------------------------------------------------
## II. Installer une Rom
### A. Présentation
### B. Redmi Note 10 Pro
#### 0. Présentation
Le Redmi Note 10 Pro est un mobile sous architecture `Arm64`.

#### 1. [PixelOS](https://pixelos.net/download/sweet)
```
Menu indispensable pour installer la ROM.
https://download.pixelos.net/seventeen/sweet/recovery/recovery-sweet_20261030_2119.img

# Noyau pour le démarrage du téléphone.
https://download.pixelos.net/seventeen/sweet/recovery/boot-sweet_20261030_2119.img

# Configuration des composants matériels du smartphone.
https://download.pixelos.net/seventeen/sweet/recovery/dtbo-sweet_20261030_2119.img

# Le système d'exploitation Android 17 complet.
https://download.pixelos.net/seventeen/sweet/PixelOS_sweet-17.0-20261030-2119.zip
```
#### 2. Bootloader
Allumer le téléphone et connecter celui-ci au PC, puis taper les commandes suivantes.
```
adb devices
adb reboot bootloader
```

#### 3. Installation du Bootloader
Le téléphone est en Fastboot et permet l'installation de l'image Recovery.
```
fastboot devices
fastboot flash boot     "S:\Xiaomi Redmi Note 10 Pro\PixelOS\boot-sweet_20261030_2119.img"
fastboot flash dtbo     "S:\Xiaomi Redmi Note 10 Pro\PixelOS\dtbo-sweet_20261030_2119.img
fastboot flash recovery "S:\Xiaomi Redmi Note 10 Pro\PixelOS\recovery-sweet_20261030_2119.img"
fastboot reboot recovery
```

#### 4. Nettoyage
Aller dans le menu `Factory Reset` > `Format Data / Factory Reset` > `Valider`.

#### 5. Injection OS
Aller dans le menu `Apply Update` > `Apply From ADB` puis taper la commande pour envoyer l'OS. 

```
adb sideload "S:\Xiaomi Redmi Note 10 Pro\PixelOS\PixelOS_sweet-17.0-20261030-2119.zip"
```

Vérifier sur le téléphone : `Install Completed with status 0`.

Redémarrer le téléphone normalement.

Il doit démarrer

<br /> <br />

-------------------------------------------------------------------------------------------------------------------------------------------------
## III. 
### A. Mode développeur
#### 1. Débloquer le menu
Aller dans les `paramètres` > `A propos du téléphone` puis cliquer 7 fois sur le numéro de la `Build` pour débloquer le menu.
#### 2. Mode débogage USB
Aller dans les `paramètres` > `Paramètres supplémentaires` > `Options développeur` et cocher `Débogage USB` et brancher votre téléphone sur le PC.

### B. Xiamoi
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

