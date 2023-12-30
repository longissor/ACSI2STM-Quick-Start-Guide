# How to partition and format a microSD card in Windows  (Francais plus bas)

This short guide explain how to prepar, partition and format a microSD using `DiskPart` command line. 
This way sometime works better than using Windows GUI

1. Insert your SD card into your computer SD card reader.
1. On Windows bar, search CMD to find the `Command Prompt` and run it as administrator (right click then select run as administrator).
1. Type `diskpart` then enter
1. List all hard drives: type `list disk` then enter.
1. Look for your SD card number.
1. Type `select disk x` where x is your microSD card number. Then enter.
1. Type `clean all` then enter. All data/partitions will now be deleted.
1. Now create a new partition. Type `create partition primary size=32` then enter. This will now create a 32MB partition.
1. Finally, type `active` then enter. This partition will be marked as active.
1. Now format the drive under Windows.

----------------------------------

# Comment partitionner et formater une carte microSD sous Windows.

Ce petit guide explique comment préparer, partitionner et formater une microSD à l'aide de la ligne de commande `DiskPart`. 
Cette méthode fonctionne parfois mieux que l'utilisation de l'interface graphique Windows

1. Insérez votre carte SD dans le lecteur de carte SD de votre ordinateur.
1. Dans la barre Windows, recherchez CMD pour trouver l'`Invite de commandes` et exécutez-la en temps qu'administrateur.
1. Tapez `diskpart` puis Retour
1. Listez tous les disques durs : tapez `list disk` puis Retour.
1. Recherchez votre numéro de carte SD.
1. Tapez `select disk x` où x est le numéro de votre carte microSD. Puis Retour.
1. Tapez `clean all` puis Retour. Toutes les données/partitions seront désormais supprimées.
1. Créez maintenant une nouvelle partition. Tapez `create partition primary size=32` puis Retour. Cela va maintenant créer une partition de 32 Mo.
1. Enfin, tapez `active` puis Retour. Cette partition sera marquée comme active.
1. Formatez maintenant le disque sous Windows.
