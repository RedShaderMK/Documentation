# 🗄️ Archivage sous GNU/Linux

_To-do :_

- [x] Gzip
- [ ] bzip2
- [ ] LZMA
- [ ] LZW
- [ ] TAR
- [ ] PAX

## 🗜️ gzip

Gzip (GNU zip) est un utilitaire de compression créer à partir de 1991 et il est basé sur l'algorithme deflate. Il est développé par le [Projet GNU](https://fr.wikipedia.org/wiki/Projet_GNU).

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

### 🗒️ Paramètres intéressants

- Le niveau de compression peut être changé via un paramètre via `-n` (Remplacer n par un chiffre)
    > ℹ️ Il va de 1 (compression la plus faible) à 9 (compression la plus forte).
- Par défaut, le fichier original est supprimé après la compression ou la décompression. Pour le conserver, il faut ajouter le paramètre `-k`.
- Pour avoir une sortie plus détaillé, on peut utiliser le paramètre `-v`.
- Le paramètre `f` permet de forcer la compression ou la décompression.
- Le paramètre `t` permet de tester l'intégrité de l'archive.

## 🗜️ Bzip2

Bzip2 est un utilitaire de compression développé par Julian Seward entre 1996 et 2000.

### 📍 Compression

Pour compresser un fichier :

```bash
bzip2 -z 'fichier'
```

### 📍 Décompression

Pour décompresser un fichier :

```bash
bzip2 -d 'fichier.bz2'
```

### 📃 Paramètres intéressants

- Le paramètre `f` permet de forcer la compression ou la décompression.
- Le paramètre `v` permet d'avoir une sortie verbeuse.
- Le paramètre -n permet d'augmenter ou non la compression.
    > ℹ️ Il va de 1 (compression la plus faible) à 9 (compression la plus forte).
- Le paramètre `t` permet de tester l'intégrité de l'archive.
