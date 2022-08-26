# 🗄️ Archivage sous GNU/Linux

_To-do :_

- [x] Gzip
- [ ] bzip2
- [ ] LZMA
- [ ] LZW
- [ ] TAR
- [ ] PAX

## 💾 gzip

Pour compresser un fichier :

```bash
gzip 'fichier'
```

Pour compresser plusieurs :

```bash
gzip fichier1 fichier2 fichier3
```

Pour compresser un répertoire :

```bash
gzip -r './dossier'
```

Pour décompresser un fichier :

```bash
gzip -d 'fichier.gz'
```

Pour décompresser plusieurs fichiers :

```bash
gzip -d fichier1.gz fichier2.gz fichier3.gz
```

Pour décompresser une archive dans un répertoire :

```bash
gzip -dr './dossier'
```

Pour afficher la liste des fichiers d'une archive :

```bash
gzip -lv 'fichier.gz'
```

Compresser la sortie d'une commande :

```bash
 echo "Lorem ipsum dolor sit amet sed consetetur" | gzip -c > file.txt.gz
 ```

Petite liste des paramètres intéressant :

- Le niveau de compression peut être changé via un paramètre via -X  
    > Il va de 1 (plus faible) à 9 (plus fort).
- Par défaut, le fichier original est supprimé après la compression ou la décompression. Pour le conserver, il faut ajouter le paramètre `-k`
    > La commande `gzip -c fichier > fichier.gz` fonctionne aussi
- Pour afficher les informations, on peut utiliser le paramètre `-v`.
