# 🗄️ Archivage sous GNU/Linux

_To-do :_

- [x] Gzip
- [ ] bzip2
- [ ] LZMA
- [ ] LZW
- [ ] TAR
- [ ] PAX

## 💾 gzip

### 📌 Compression

Pour compresser un fichier :

```bash
gzip 'fichier'
```

Pour compresser plusieurs fichiers :

```bash
gzip fichier1 fichier2 fichier3
```

Pour compresser un répertoire :

```bash
gzip -r './dossier'
```

### 📌 Décompression

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

 > ℹ️ La sortie de la commande `echo` sera directement compressé par gzip.

### 🗒️ Petite liste des paramètres intéressants

- Le niveau de compression peut être changé via un paramètre via `-n` (Remplacer n par un chiffre)
    >  ℹ️ Il va de 1 (compression la plus faible) à 9 (compression la plus forte).
- Par défaut, le fichier original est supprimé après la compression ou la décompression. Pour le conserver, il faut ajouter le paramètre `-k`.
- Pour avoir une sortie plus détaillé, on peut utiliser le paramètre `-v`.
