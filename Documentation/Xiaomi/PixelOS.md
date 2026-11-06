-------------------------------------------------------------------------------------------------------------------------------------------------
# <p align='center'> Guide d'installation de PixelOS </p>
-------------------------------------------------------------------------------------------------------------------------------------------------
## I. Déploiement de la ROM
### A. Présentation
#### 1. Prérequis
Un téléphone avec le mode Développeur et le mode `Débuggage USB` est actif. Puis les pilotes du PC.
#### 2. Architecture
Le Redmi Note 10 Pro est un mobile sous architecture `Arm64`.


### B. Télécharger les fichiers [PixelOS](https://pixelos.net/download/sweet)
#### 1. Redmi Note 10 Pro
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

### C. Démarrer en Bootloader
Allumer le téléphone et connecter celui-ci au PC, puis taper les commandes suivantes.
```
adb devices
adb reboot bootloader
```

#### D. Installation du Bootloader
Le téléphone est en Fastboot et permet l'installation de l'image Recovery.
```
fastboot devices
fastboot flash boot     "S:\Xiaomi Redmi Note 10 Pro\PixelOS\boot-sweet_20261030_2119.img"
fastboot flash dtbo     "S:\Xiaomi Redmi Note 10 Pro\PixelOS\dtbo-sweet_20261030_2119.img
fastboot flash recovery "S:\Xiaomi Redmi Note 10 Pro\PixelOS\recovery-sweet_20261030_2119.img"
fastboot reboot recovery
```

#### E.Nettoyage
Aller dans le menu `Factory Reset` > `Format Data / Factory Reset` > `Valider`.

#### F. Injection OS
Aller dans le menu `Apply Update` > `Apply From ADB` puis taper la commande pour envoyer l'OS. 

```
adb sideload "S:\Xiaomi Redmi Note 10 Pro\PixelOS\PixelOS_sweet-17.0-20261030-2119.zip"
```

Vérifier sur le téléphone : `Install Completed with status 0`.

Puis sélectionner `Reboot System Now` pour redémarrer le téléphone.
