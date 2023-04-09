# 💾 Comment vérifier l'état de santé d'un HDD ou d'un SSD ?

Les disques durs et les SSD sont des éléments clés de nos ordinateurs car ils stockent toutes nos données. Comme tout élément matériel informatique, ils peuvent tomber en panne et entraîner la perte de toutes les données stockées dessus. Pour prévenir les pannes et défaillances de disque dur ou SSD, un protocole S.M.A.R.T. (*Self Monitoring Analysis and Reporting Technology*) existe qui permet d’effectuer des tests et remontées de pannes.

S.M.A.R.T est une technologie disponible sur tous les disques durs et qui permet de collecter en permanence des informations sur la santé du disque dur: taux d’erreur en lecture, taux d’erreur d’accès aux têtes, température, nombre de secteurs ré-allouées, secteurs défectueux, etc 2. Cela permet de prévenir des pannes et défaillances de disque.

## 1. Vérifier les informations S.M.A.R.T

Sous Linux, il est possible de consulter les informations S.M.A.R.T assez facilement :

- Il faut pour cela installer les paquets `smartctl` ainsi que `smartmontools`. Une fois cela fait, il faut obtenir le nom du disque que l'on veux vérifier :

```bash
lsblk -o name,model,size -d | grep -v loop
```

- Cela va afficher un résultat semblable à cela :

```bash
NAME MODEL                      SIZE
sda  WDC PC SN730 SDBPNTY-512G  480G
sdb  Virtual_Disk                 4G
```

- Il ne reste qu'a taper la commande `sudo smartctl -H /dev/sda` et lire les informations.

## 2. Vérifier les secteurs

`badblocks` est un programme qui permet aux utilisateurs de scanner un périphérique pour détecter les secteurs ou blocs défectueux. Le périphérique peut être un disque dur ou un disque externe.

- Pour utiliser badblocks, il faut lister les disques avec `fdisk` :

```bash
sudo fdisk -l
```

- Ensuite, prendre le nom du disque (comme `/dev/sda`) et écrire la commande :

```bash
sudo badblocks -svn /dev/sda
```

> Les arguments :
>
> -s : Afficher la progression.
>
> -v : Mode verbeux.
>
> -n : Effectue un test de lecture-écriture non destructif.

- La vérification des secteurs peut prendre du temps, surtout si le disque à tester est de grande tailler et peu rapide.
