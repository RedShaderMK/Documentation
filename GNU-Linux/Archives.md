# 🗄️ Archivage sous GNU/Linux

_To-do :_

- [x] Gzip
- [x] bzip2
- [ ] LZMA
- [ ] LZW
- [ ] TAR
- [ ] PAX

## 🗜️ gzip

Gzip (GNU zip) est un utilitaire de compression créer à partir de 1991 et il est basé sur l'algorithme deflate. Il est développé par le [Projet GNU](https://fr.wikipedia.org/wiki/Projet_GNU).

Pour compresser un ou plusieurs fichier :

```bash
gzip 'fichier' ['fichier2' 'fichier3']
```

Pour décompresser un ou plusieurs fichiers :

```bash
gzip -d 'fichier.gz' ['fichier2.gz' 'fichier3.gz']
```

Compresser la sortie d'une commande :

```bash
 echo "Lorem ipsum dolor sit amet sed consetetur" | gzip -c > file.txt.gz
 ```

 > ℹ️ La sortie de la commande `echo` sera directement compressé par gzip.

 Arguments :

 ```text
  -c, --stdout      write on standard output, keep original files unchanged
  -d, --decompress  decompress
  -f, --force       force overwrite of output file and compress links
  -h, --help        give this help
  -k, --keep        keep (don't delete) input files
  -l, --list        list compressed file contents
  -L, --license     display software license
  -n, --no-name     do not save or restore the original name and timestamp
  -N, --name        save or restore the original name and timestamp
  -q, --quiet       suppress all warnings
  -r, --recursive   operate recursively on directories
      --rsyncable   make rsync-friendly archive
  -S, --suffix=SUF  use suffix SUF on compressed files
      --synchronous synchronous output (safer if system crashes, but slower)
  -t, --test        test compressed file integrity
  -v, --verbose     verbose mode
  -V, --version     display version number
  -1, --fast        compress faster
  -9, --best        compress better
```

## 🗜️ Bzip2

Bzip2 est un utilitaire de compression développé par Julian Seward entre 1996 et 2000.

Pour compresser un ou plusieurs fichiers :

```bash
bzip2 -z 'fichier' ['fichier2' 'fichier3']
```

Pour décompresser un ou plusieurs fichiers :

```bash
bzip2 -d 'fichier.bz2' ['fichier2' 'fichier3']
```

Compresser la sortie d'une commande :

```bash
 echo "Lorem ipsum dolor sit amet sed consetetur" | bzip2 -c > file.txt.gz
 ```

 > ℹ️ La sortie de la commande `echo` sera directement compressé par bzip2.

Arguments :

```text
   -h --help           print this message
   -d --decompress     force decompression
   -z --compress       force compression
   -k --keep           keep (don't delete) input files
   -f --force          overwrite existing output files
   -t --test           test compressed file integrity
   -c --stdout         output to standard out
   -q --quiet          suppress noncritical error messages
   -v --verbose        be verbose (a 2nd -v gives more)
   -L --license        display software version & license
   -V --version        display software version & license
   -s --small          use less memory (at most 2500k)
   -1 .. -9            set block size to 100k .. 900k
   --fast              alias for -1
   --best              alias for -9
```

## 🗜️ LZMA

Paramètre de LZMA :

Pour compresser :

```bash
xz -z 'file'
```

Pour décompresser :

```bash
xz -d 'file.xz'
```

Compresser la sortie d'une commande :

```bash
 echo "Lorem ipsum dolor sit amet sed consetetur" | xz -c > file.txt.gz
 ```

 > ℹ️ La sortie de la commande `echo` sera directement compressé par xz.

Arguments :

```text
  -z, --compress      force compression
  -d, --decompress    force decompression
  -t, --test          test compressed file integrity
  -l, --list          list information about .xz files
  -k, --keep          keep (don't delete) input files
  -f, --force         force overwrite of output file and (de)compress links
  -c, --stdout        write to standard output and don't delete input files
  -0 ... -9           compression preset; default is 6; take compressor *and*
                      decompressor memory usage into account before using 7-9!
  -e, --extreme       try to improve compression ratio by using more CPU time;
                      does not affect decompressor memory requirements
  -T, --threads=NUM   use at most NUM threads; the default is 1; set to 0
                      to use as many threads as there are processor cores
  -q, --quiet         suppress warnings; specify twice to suppress errors too
  -v, --verbose       be verbose; specify twice for even more verbose
  -h, --help          display this short help and exit
  -H, --long-help     display the long help (lists also the advanced options)
  -V, --version       display the version number and exit
  ```

## 🗜️ Tar

Tar (tape archiver) est un utilitaire d'archivage sans _compression_. Il préserve les droits, les propriétaires ainsi que les groupes des fichiers et des dossiers. Il permet aussi de sauvegarder les liens symboliques.

Pour archiver un ou plusieurs fichiers :

```bash
tar cvf archive.tar 'fichier1' ['fichier2' 'fichier3']
```

Pour archiver un dossier :

```bash
tar cvf archive.tar './dossier/'

Pour extraire une archive :

```bash
tar xvf 'archives.tar'
```

Aruments :

```text
-c                  Permet la construction de l'archive
-x                  Permet l'extraction de l'archive
-v                  Mode verbeux
-f                  Utilise un fichier donné en paramètre
-z                  Compression avec gzip
-j                  Compression avec bzip2
-J                  Compression avec LZMA
```

## 🗜️ Pax

Pax est un utilitaire d'archivage qui gère la compression de fichier très volumineux avec beaucoup de sous-répertoires.

Pour archiver plusieurs fichiers et dossiers :

```bash
pax -wf 'archives.pax' 'fichier1' 'fichier2'
```

```bash
pax -wf 'archives.pax' './dossier/'
```

Extraction d'une archive :

```bash
pax -rf 'archives.pax'
```

Arguments :

```text
-w                  Permet la construction de l'archive
-r                  Permet l'extraction de l'archive
-z                  Compression avec gzip
-j                  Compression avec bzip2
```
