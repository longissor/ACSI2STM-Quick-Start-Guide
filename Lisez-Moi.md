#ACSI2STM-Guide De Démarrage Rapide.

Ce documents explique au plus simple, les étapes recommandées pour faire fonctionner la carte ACSI2STM.

##Pile pour la sauvegarde de la date/heurey

Avant d’installer la carte, vous pouvez inserer une pile CR2032 dans le support de pile. La pile est utilisée pour la sauvegarde de la date et de l’heure quand l’Atari ST est etteint. Elle n’est pas necessaire au fonctionnement de la partir disque.

##Installation sur le port ACSI DB19
•	Branchez la carte sur le port ACSI à l’arrière du ST. La face avec les composants vers vous. 
•	Branchez une source 5V sur la prise USB-C de la carte. Vous pouvez utiliser un charge de téléphone avec un câble USB-C.

La carte SD peut être formatée au format Fat32 or ExFat qui sont les standards pour les cartes SD.
Allumez le ST, la carte ACSI2STM devrait normalement afficher un message lors du boot et le disque C doit apparaitre sur le bureau. Vous devez installer les autres disque D ou E manuellement si vous avez d’autres carte SD présentes.
L’utilisation de carte SD utilisant FAT ou FAT32 est connue sous le nom « Mode GemDrive ». C’est le mode le plus simple pour utiliser la carte ACSI2STM. La carte SD est visible sur PC. Vous pouvez donc l’utiliser comme méthode de transfert entre PC et ST par exemple.

Pour changer la date/heure en mode GemDrive, vous pouvez utiliser les outils ST classiques comme CONTROL.ACC ou XCONTROL.ACC. GemDrive re directe tous les appels système vers le STM32. L’horloge internet du ST n’est plus utilisée.
 

En mode ACSI, ACSI2STM simule le fonctionnement de l’horloge comme UltraSatan. Vous pouvez donc utiliser les outils UltraSatan comme par exemple  US_SETCL.PRG et US_GETCL.PRG. 

Si vous voulez en savoir plus sur les options et les modes ACSI ou GemDrive, veuillez vous diriger vers ces liens (en Anglais).

Comment insérer la pile CR2032 https://youtu.be/rgAsQ0IYjlg
Le site GitHub principale sur ACSI2STM  https://github.com/retro16/acsi2stm
Une page Atari ST par PP https://atari.8bitchip.info/
Une image de carte SD avec le driver  http://joo.kie.sk/?page_id=332
