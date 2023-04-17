# 📋 Liste des commandes pratiques de CMD

![CMD](../res/cmd/cmd_illu.png)

## 📜 Introduction

L’invite de commande (cmd.exe) est un interpréteur de commandes pour les systèmes d’exploitation Windows qui permet aux utilisateurs d’exécuter des commandes et des scripts à partir d’une interface en ligne de commande. Il est souvent utilisé pour effectuer des tâches de maintenance système, telles que la gestion de fichiers et de dossiers, la configuration du réseau et la résolution des problèmes. La disponibilité des commande cmd.exe dépendent de la version de Windows. Ici, je ne vais donner les commandes disponibles qu'à partir de Windows 10 et Windows 11.

## 📁 Système de fichiers

1. **CD** ou **CHDIR**

    Cette commande permet de se déplacer dans l'arborescence.  
    `CD chemin du répertoire` : Se déplace vers le répertoire spécifié.  
    `CD \` : Se déplace au début de l'arborescence.  
    `CD \D D:\` ou `D:` : Change de lecteur vers le lecteur spécifié.

2. **DIR**

    Affiche le contenu d'un répertoire.  
    `DIR` : Affiche le contenu du répertoire courant.  
    `DIR dossier` : Affiche le contenu du répertoire du répertoire spécifié.

3. **MD** ou **MKDIR**

    Cette commande permet la création d'un ou plusieurs répertoires.  
    `MD dossier` : Création d'un dossier.  
    `MD dossier1 dossier2 dossier3` : Création de plusieurs dossier.

4. **RD** ou **RMDIR**

   Cette commande permet la suppression de répertoire vide (ou non vide avec `/S`).  
    `RD dossier` : Supprime un dossier vide.  
    `RD /S dossier` : Supprime un dossier non vide.

5. **COPY**

    Permet la copie de fichiers.  
    `COPY .\fichier.txt ..\Desktop\fichier.txt /V` : Copie un fichier avec vérification (`/V`).

6. **XCOPY**

    Permet la copie de fichier et de dossiers.  
    `XCOPY A:\ B:\` : Copie les fichiers et les dossiers du lecteur `A:` vers le lecteur `B:`.

7. **MOVE**

    Permet de déplacer ou renommer un fichier ou un dossier.  
    `MOVE fichier1 fichier2` : Renomme `fichier1` en `fichier2`.

8. **DEL**

    Permet la suppression d'un ou plusieurs fichiers.  
    `DEL fichier1 fichier2 fichier3` : Supprimer les fichiers spécifiés.

9. **REN**

    Permet de renommer les fichiers et les dossiers.  
    `REN fichier1 fichier2` : Renomme `fichier1` en `fichier2`.

10. **TYPE**

    Permet d'afficher le contenu d'un fichier texte (`.txt`, `.csv`, `.xml`, etc...).  
    `TYPE rapport.log` : Affiche le contenu de `rapport.log`.

11. **TREE**

    Permet d'afficher graphiquement la structure de dossiers d’un lecteur ou d’un chemin.  
    `TREE` : Affiche les répertoires uniquement.  
    `TREE /F` : Affiche les répertoires et les fichiers.  
    `TREE /A` : Force l'utilisation de caractères ASCII.

## 💻 Système

1. **CHKDSK**

    Permet de vérifier l'état d'un disque.  
    `CHKDSK C:` : Affiche l'état du disque.  
    `CHKDSK /F C:` : Affiche et corrige l'état du disque.  
    `CHKDSK /R C:` : Localise les secteurs défectueux.  

2. **DOSKEY**

    Permet de créer des macros pour exécuter une ou plusieurs commandes.  
    `DOSKEY LS=DIR` : Créer une macro qui permet d'éxecuter la commande `DIR` avec la macro `LS`.

3. **CLIP**

    Permet de rediriger la sortie d'une commande dans le presse-papier.  
    `DIR | CLIP` : Copie le résultat de la commande `DIR` vers le presse-papier.  
    `CLIP < README.md` : Copie le contenu du fichier dans le presse-papier.  

4. **VER**

    Permet d'afficher la version de Windows.  
    `VER`

5. **ASSOC**

    Permet d'afficher ou de modifier les associations des extensions de fichiers.  
    `ASSOC` : Affiche toutes les association des extensions de fichiers.  
    `ASSOC .txt` : Affiche l'association du type de fichier `.txt`.  
    `ASSOC .log=txtfile` / Associe `.log` au type de fichier texte.  
    `ASSOC .log=` : Supprime l'association de l'extension `.log` (il faut ajouter un esapce après le =).  

6. **FTYPE**

    Affiche ou modifie les types de fichiers utilisés dans les associations d’extension de fichiers.  
    `FTYPE txtfile=C:\Windows\System32\notepad.exe "%1"` : Spécifie le bloc-note comme programme par défaut pour l'ouverture des fichiers de type texte.  

7. **ATTRIB**

    Permet d'afficher, de définir ou de supprimer les attribus de lecture seule, d'archivage, système et masqué assignés aux fichiers et répertoires.  
    `ATTRIB +R fichier.txt` : Ajoute (+) l'attribut de lecture seul au fichier.  
    `ATTRIB -R fichier.txt` : Supprime (-) l'attribut de lecture seul au fichier.  

    Liste des attributs
    | Attribut | Description |
    | --- | --- |
    | `R` | Lecture seule |
    | `A` | Archive |
    | `S` | Système |
    | `H` | Masqué |
    | `I` | Contenu non indexé |

8. **CIPHER**

    Permet le chiffrement des fichiers et des répertoires sur un volume **NTFS** (donc non disponible sur les autres systèmes de fichier).  
    `CIPHER` + fichier ou répertoire : Affiche l'état de chiffre du fichier ou du dossier spécifié.  
    `CIPHER /E` + fichier ou répertoire : Chiffre le fichier ou le dossier spécifié.  
    `CIPHER /D` + fichier ou répertoire : Déchiffre le fichier ou le dossier spécifié.  
    `CIPHER /C` + fichier ou répertoire : Affiche les informations de chiffrement sur+ le fichier ou le dossier spécifié.  
    `CIPHER /S:<répertoire>` : Chiffre le contenu du répertoire et des sous-répertoires.  

9. **COMP**

    Permet de comparer deux fichiers.  
    `COMP fichier1.txt fichier2.txt /L` : Compare deux fichiers texte et affiche les numéros de lignes.  

10. **FC**

    Permet de comparer deux fichiers ou ensembles de fichiers et d'afficher les différences entre eux.  
    `FC fichier1 fichier2` : Compare les deux fichiers spécifié.  

11. **COMPACT**

    Affiche ou modifie la compression de fichiers sur les partitions NTFS.  
    `COMPACT /C /S` : Compresse le contenu du dossier et des sous-dossier où l'on se trouve.  
    `COMPACT /C` + fichier ou dossier : Compresse le fichier spécifié.  

    L'ajout du paramètre `/EXE:<Algorithmes>` permet de spécifier l'algorithme à utiliser.

    Les algorithmes  

    | Algorithme | Description |
    | --- | --- |
    | `XPRESS4K` | Valeur la plus rapide et la valeur par défaut |
    | `XPRESS8K` |  |
    | `XPRESS16K` |  |
    | `LZX` | Le plus compact |

12. **EXPAND**
13. **MKLINK**

## 📌 20 commandes les plus utiles

1. IPCONFIG  
    Cette commande permet d'afficher les informations détaillé sur la configuration IP de la carte réseau de l'ordinateur. Cette commande permet aussi de libérer et de renouveler l'adresse IP de l'ordinateur.

    `/all` : Affiche toutes les informations de condifuration.  
    `/release` : Libère l'adresse IPv4 pour la carte spécifiée.  
    `/renew` : Renouvelle l'adresse IPv4 de la carte spécifié.  
    `/flushdns` : Purge le cache de résolution DNS.  
    `/registerdns` : Actualise tous les baux DHCP et réenregistre les noms DNS.  

2. PING  
    Cette commande permet de tester l'accessibilité d'un périphérique sur le réseau (comme un ordinateurn un serveur ou une imprimante).  

    `ping` + nom de l'hôte ou adresse IP.

3. TRACERT  
    Cette commande permet de déterminer l'itinéraire vers une adresse IP ou d'un nom d'hôte. Cela permet de connaitre en détails le chemin parcouru par le paquets ICMP.

    `tracert` + nom d'hôte ou adresse IP.  

4. NETSTAT  
    Cette commande permet d'afficher les connexions réseau actives et les statistiques de réseau associées. Elle peut être utilisée pour afficher les connexions TCP/IP actives et les ports sur lesquels l’ordinateur local est à l’écoute.

    `netstat -a`

5. NSLOOKUP  
    Cette commande permet d'effectuer une recherche DNS (Domain Name System) pour trouver l’adresse IP d’un nom d’hôte ou le nom d’hôte correspondant à une adresse IP. Elle peut également être utilisée pour afficher des informations sur les serveurs DNS et les enregistrements DNS associés.

    `nslookup` + nom de domaine.  

6. ARP  
    La commande arp est utilisée pour afficher et modifier les tables de cache ARP (Address Resolution Protocol) utilisées pour traduire les adresses IP en adresses MAC (Media Access Control) sur un réseau local.

7. ROUTE  
    La commande route est utilisée pour afficher et modifier la table de routage IP utilisée par le système d’exploitation pour déterminer le chemin que les paquets IP doivent emprunter pour atteindre leur destination.

8. TASKLIST  
    La commande tasklist est utilisée pour afficher une liste des tâches en cours d’exécution sur un ordinateur.

9. TASKKILL  
    La commande taskkill est utilisée pour arrêter un processus en cours d’exécution sur un ordinateur.

10. SYSTEMINFO  
    La commande systeminfo est utilisée pour afficher des informations détaillées sur la configuration système et les paramètres du système d’exploitation.

11. DRIVERQUERY  
    La commande driverquery est utilisée pour afficher une liste des pilotes installés sur un ordinateur.

12. POWERCFG  
    La commande powercfg est utilisée pour gérer les options d’alimentation du système.

13. SCHTASKS  
    La commande schtasks est utilisée pour voir et planifier des tâches à exécuter à une heure ou une date ultérieure.

14. NETSH  
    Cette commande est utilisée pour configurer et afficher les paramètres réseau.

15. REGEDIT  
    Cette commande est utilisée pour afficher et modifier les paramètres du registre Windows.

16. DISKPART  
    Cette commande est utilisée pour gérer les disques et les partitions.

17. CHKDSK  
    Cette commande permet de vérifier l’intégrité du système de fichiers et des disques durs.

18. SFC  
    Cette commande permet la vérification et la réparation des fichiers système (/SCANNOW)

19. SHUTDOWN  
    Cette commande permet d'éteindre l'ordinateur.

20. HELP  
    Cette commande permet d'afficher l'aide.
