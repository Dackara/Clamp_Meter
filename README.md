![Static Badge](https://img.shields.io/badge/Work_In_Progress-Projet_en_cours_de_r%C3%A9alisation-red?logo=adblock&logoColor=red&style=plastic)

[![Static Badge](https://img.shields.io/badge/Realease-Beta-blue?style=plastic)](https://github.com/Dackara/Clamp_Meter)
[![Static Badge](https://img.shields.io/badge/License-Beerware-yellow?style=plastic)](https://fr.wikipedia.org/wiki/Beerware)
[![Static Badge](https://img.shields.io/badge/Donate-ko--fi_%E2%99%A5-pink?logo=kofi&style=plastic)](https://ko-fi.com/dackara)
[![Static Badge](https://img.shields.io/badge/Sponsor-On_Github-darkgreen?logo=github&logoColor=lightgrey&style=plastic)](https://github.com/sponsors/Dackara)


# Clamp_Meter
> [!IMPORTANT]
> Carte de **Contrôle/Mesure du Courant** 
> 
> Projet initié en complément de ma carte [Fil_Pilote](https://github.com/Dackara/Fil_Pilote) car je voulais savoir quels sont les chauffages qui sont actuellement en train de consommer.
>
> Design conçus pour être [monté](../main/Image/Exemple/PVBRAIN2_and_Clamp_Meter.png) sur la carte [![Static Badge](https://img.shields.io/badge/PvBrain-v2.0-black?style=social&logo=quasar)](https://github.com/SeByDocKy/pvbrain2) développé par [![Static Badge](https://img.shields.io/badge/Bandit--17-black?logo=git&style=flat)](https://github.com/Bandit-17) et [![Static Badge](https://img.shields.io/badge/SeByDocKy-black?logo=git&style=flat)](https://github.com/SeByDocKy) de la chaine [![Static Badge](https://img.shields.io/badge/Youtube-e--2--nomy-black?style=social&logo=youtube)](https://www.youtube.com/@e2nomy).

> [!NOTE]
> La carte `Camp Meter` est néanmoins totalement utilisable sans la carte [![Static Badge](https://img.shields.io/badge/PvBrain-v2.0-black?style=social&logo=quasar)](https://github.com/SeByDocKy/pvbrain2) (le hardware fonctionne avec n'importe quel ESP32 / ESP8266, ou tout autre système compatible **i2c**).
>
> L'intérêt est que les trous de fixation des deux carte correspondent. Cela permet de les imbriquer l'une sur l'autre, tout en profitant de l'[esp32](https://amzn.to/3RCapBQ) déjà présent sur le PvBrain.
> 
> Montage sur le [![Static Badge](https://img.shields.io/badge/PvBrain-v1.0-black?style=social&logo=quasar)](https://github.com/Bandit-17/PVBRAIN) également [possible](../main/Image/Exemple/PVBRAIN1_and_Clamp_Meter.png).

> [!TIP]
> Développé pour :
> - [![Static Badge](https://img.shields.io/badge/ESPHome-_-black?logo=esphome&style=social)](https://esphome.io).
> - [![Static Badge](https://img.shields.io/badge/Home_Assistant-_-black?logo=homeassistant&style=social)](http://homeassistant.io).

## Ce que permet la carte :
 > - 1 à 16 Clamp (2 montage possible pour chaque sorties : JST-XH pour clamp 2brin ou Jack pour SCT013)
 > - 1 à 4 ADS1115 pré adressé.
 > - 1 TCA9548A (optionel -pontage si pas utilisé) pour multiplexé l'I2C (utile en cas de + de 4 ADS ou conflit d'adresse I2C) avec toutes ses sorties déporté pour utilisation externe.
 > - 1 ESP possible en entrée pour les non utilisateur du PVbrain ou autres raison ... 6 montage possible : (déport de toutes les sorties et récupération de l'i2c via pontages) :
 >   - ESP8266 D1 Mini
 >   - ESP32 D1 Mini
 >   - ESP32 S2 Mini
 >   - ESP32 C3
 >   - ESP32 C3 Zero
 >   - ESP32 S3 Zero

## Le code ESPHome :
Le code est simplifié pour la modification via `packages:` et `substitutions:`. 

Tout se passe dans le fichier [clamp_meter.yaml](../main/Software_esphome/clamp_meter.yaml) présent à la racine.

L'intégralité des fichiers présents dans [ce répertoire](../main/Software_esphome) est nécessaire à son bon fonctionnement.

## La carte :
| Face avant                | Face arrière              |
| :-----------------------: | :-----------------------: |
| ![alt text](../main/Image/TopSide.png) | ![alt text](../main/Image/BottomSide.png) |
| __Vue 3D__                | __Circuit__               |
| ![alt text](../main/Image/3D_View.png) | ![alt text](../main/Image/Circuit.png) |
| __Schematic__             | __Support DIN 3D__         |
| ![alt text](../main/Image/Schematic.png) | ![alt text](../main/Image/3D_DIN_mount.png) |

- Fichier **Gerber** et **BOM** : [Dossier Hardware](../main/Hardware)
- [Fichier 3D](../main/Hardware/3D_Print) à imprimer pour montage de la carte sur rail DIN (tableau électrique).

### Crédit :
- Schéma électronique, Designe PCB & code esphome : [![Static Badge](https://img.shields.io/badge/Dackara-black?logo=git&style=flat)](https://github.com/Dackara)
