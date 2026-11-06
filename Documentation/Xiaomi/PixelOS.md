
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

Puis sélectionner `Reboot System Now` pour redémarrer le téléphone.

Il doit démarrer

<br /> <br />
