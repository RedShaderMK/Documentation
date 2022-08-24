# 🛠️ Utilisation de [Diskpart](https://docs.microsoft.com/fr-fr/windows-server/administration/windows-commands/diskpart)

## 💽 Formatage d'un disque

1. Lancer Diskpart dans le terminal en tant qu'administrateur
2. Lister les disques avec `List disk`
3. Sélectionner le disque avec `select Disk n`
    > n est le numéro du disque.
4. Entrer la commande `clean`
    > Cela va efface les partitions du disque.
5. Ensuite, il faut créer une partition avec `create partition primary`
    > La partition nouvellement créer va être automatiquement sélectionné.
6. Pour formater, il faut écrire `format fs=X label=MonDisque`  
    > Il est possible d'ajouter l'argument `quick` pour faire un formatage rapide.

    🗃️ _Différents systèmes de fichiers sont disponibles :_
    >
    > - NTFS (compatible Windows uniquement).
    > - FAT32 (Pour les périphériques de stockage USB, largement compatible mais limité à des fichiers de 4 Giga-octets).
    > - exFAT (successeur de FAT32, conçu pour les périphériques de stockage USB sans la limitation de 4 Giga-cotets).
    > - UDF (Universal Disk Format; format ouvert et compatible avec Windows, macOS et GNU/Linux).

7. Pour assigner une lettre de lecteur, il faut écrire `assign letter=UneLettre`

## 🛠️ Assigner une lettre à un lecteur

Si un lecteur ne possède pas de lettre, il est possible de lui en assigner une :

1. Lancer diskpart en administrateur
2. Lister les volumes avec `list volume`
3. Sélectionner le bon volume avec `select volume n`  
    > n est le numéro du volume.
4. Écrire `assign letter=UneLettre`
