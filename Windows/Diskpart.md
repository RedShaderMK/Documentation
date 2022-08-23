# 🛠️ Utilisation de [Diskpart](https://docs.microsoft.com/fr-fr/windows-server/administration/windows-commands/diskpart)

## 💽 Formatage d'un disque

1. Lancer Diskpart dans le terminal en tant qu'administrateur
2. Lister les disque avec `List disk`
3. Sélectionner le disque avec `Select Disk n`, n est le numéro du disque
4. Écrire la commande `clean`, cela efface le disque.
5. Ensuite, il faut créer une partition avec `Create partition primary`
6. Il faut sélectionner la partition avec `select partition 1`
7. L'activer avec `active`
8. Pour format, il faut écrire `format fs=X label=MonDisque quick`  
    Différents systèmes de fichiers sont disponible :
    - NTFS
    - FAT32
    - exFAT
    - UDF

9. Pour assigner une lettre de lecteur, il faut écrire `assign letter=UneLettre`

## 🛠️ Assigner une lettre à un lecteur

Si un lecteur ne possède pas de lettre, il est possible de lui en assigner une :

1. Lancer diskpart en administrateur
2. Lister les volume avec `list volume`
3. Sélectionner le bon volume avec `select volume n` (n est le numéro du volume)
4. Écrire `assign letter=UneLettre`
