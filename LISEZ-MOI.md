# ACSI2STM-Guide De Démarrage Rapide.

Ce documents explique, au plus simple, les étapes recommandées pour faire fonctionner la carte ACSI2STM.

Attention: Ce GitHub est spécifique pour la carte ACSI2STM que je vends sur EBay, Facebook et LeBonCoin.
Voir le répertoire `Photos` pour les images de ma version.
Si vous avez construis votre propre carte ou vous l'avez acheté ailleurs, veuillez vous diriger vers le GitHub officiel https://github.com/retro16/acsi2stm

## 1 - Pile pour la sauvegarde de la date/heurey

Avant d’installer la carte, vous pouvez inserer une pile CR2032 dans le support de pile. La pile est utilisée pour la sauvegarde de la date et de l’heure quand l’Atari ST est etteint. Elle n’est pas necessaire au fonctionnement de la partir disque.


## 2 - Installation sur le port ACSI DB19
*	Branchez la carte sur le port ACSI à l’arrière du ST. La face avec les composants vers vous.
*	Branchez une source 5V sur la prise USB-C de la carte. Vous pouvez utiliser un charge de téléphone avec un câble USB-C.


## 3A - Utilisation d'une carte microSD au format FAT32 en mode GemDrive.

Vous pouvez utiliser une carte microSD formattée en FAT ou FAT32 sans autre action. Ce fonctionnement est nommé GemDrive. C'est le plus simple à mettre en oeuvre. Vous n'avez pas besoin de driver.
La carte microSd est lisible sur Windows (pour transférer des fichiers entre Atari et PC par exemple).
Ce mode GemDrive fonctionne bien sur Atari ST, STE, Mega ST et Mega STE avec un TOS egal ou supérieure à 1.04. Il n'a pas été testé sur Atari TT030 et Falcon030. Le mode GemDrive peut ne pas fonctionner sur Atari TT030 et Falcon030.

### 3A1 - Changer la date et l'heure
En mode GemDrive, vous pouvez utiliser les outils comme `CONTROL.ACC` ou `XCONTROL.ACC`. Le mode GemDrive renvoi tous les appels systèmes liés à la date/heure vers le STM32.





## 3B - Utilisation d'une carte microSD en mode ACSI.
Le mode ACSI devrait normallement fonctionner sur Atari TT030 et Falcon030.
En ACSI, la taille des partitions sont limitées par le système d’exploitation TOS. 
16Mb pour le disque C est une bonne limite car elle marchera avec tous les Atari ST/TT
256 ou 512Mb pour les autres en fonction de la version du TOS.

Il y a plusieurs méthodes pour configurer une carte SD en mode ACSI. En voila 2 simples.
Vous aurez besoin d'un fichier image de disque `img`.

### 3B.1  - Utilisation d'un image directement.
* Formattez une carte microSD sur Windows au format FAT ou FAT32.
* Créez un répertoire `acsi2stm` sur la carte microSD. 
* Copiez une (ou plusieurs) image(s) de disque dure Atari sur cette carte SD, dans le repertoire `acsi2stm`. 
Les mêmes images utilisées par l’émulateur HATARI fonctionnent aussi.
* Renommez le fichier image que vous souhaitez utiliser en `hd0.img`
* Retirez la carte microSD du PC (assurez vous que vous pouvez l’éjecter)
* Insérez la carte microSD sur le slot 0 de la carte ACSI2STM
* Branchez la carte ACSI2STM et démarrez l’Atari
* Voià!
  
The format du ficher `img` est le même que celui utilisé par l'émulateur HATARI.
La carte microSD peut être de toute taille, du moment qu'elle est formatée en FAT, FAT32 ou ExFAT. L'Atari ne verra que le contenu de l'image `hd0.img`.
Vous pouvez copier d'autres fichiers image sur la carte microSD, seule `hd0.img` serra visible sur Atari.



#### 3B.2 - En Transférant une image sur carte SD
Ici, lu but est d’utiliser un utilitaire pour transférer un fichier `img` sur une carte microSD brute.

* Installez [Raspberry Pi Imager] sur votre PC https://www.raspberrypi.com/software/
* Lancer [Raspberry Pi Imager]
* Clickez sur `Choose OS` sous `Operating System` et sélectionnez `Use custom` tout en bas
* Choisissez le fichier img que vous souhaitez utiliser
* Sous `Storage`, cliquez `Choose storage` et sélectionnez la carte microSD
* Cliquez sur `Write` et confirmez.
* Une fois terminé, la carte est prête pour être utilisée sur Atari ST
* Retirez la carte microSD to PC (assurez-vous que vous pouvez l’éjecter)
* Insérez la carte microSD sur le slot 0 de la carte ACSI2STM
* Branchez la carte ACSI2STM et démarrez l’Atari


#### 3B.3 - Changer la date et l'heure.
En mode ACSI, la carte ACSI2STM fonctionne comme les carte UltraSATA. Vous pouvez donc utiliser les programmes UltraSATAN comme `US_SETCL.PRG` et `US_GETCL.PRG`. 
quand le système est éteint, la pile CR2032 garde l'horloge active.





Si vous voulez en savoir plus sur les options et les modes ACSI ou GemDrive, veuillez vous diriger vers ces liens (en Anglais):

* Comment insérer la pile CR2032 https://youtu.be/rgAsQ0IYjlg  
* Le site GitHub principale sur ACSI2STM  https://github.com/retro16/acsi2stm  
* Une page Atari ST par PP https://atari.8bitchip.info/  
* Une image de carte SD avec le driver  http://joo.kie.sk/?page_id=332  
* Commet lancer une image de disquette ST depuis le disque: https://atari.8bitchip.info/imgrun.php  
* Pages Atari WIKI: https://www.atari-wiki.com/  
