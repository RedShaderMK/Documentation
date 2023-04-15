# 📋 Liste des commandes pratiques de CMD

![CMD](../res/cmd/cmd_illu.png)

## 📜 Introduction

L’invite de commande (cmd.exe) est un interpréteur de commandes pour les systèmes d’exploitation Windows qui permet aux utilisateurs d’exécuter des commandes et des scripts à partir d’une interface en ligne de commande. Il est souvent utilisé pour effectuer des tâches de maintenance système, telles que la gestion de fichiers et de dossiers, la configuration du réseau et la résolution des problèmes. La disponibilité des commande cmd.exe dépendent de la version de Windows. Ici, je ne vais donner les commandes disponibles qu'à partir de Windows 10 et Windows 11.

## 📁 Système de fichiers

1. **CD** ou **CHDIR**

    Cette commande permet de se déplacer dans l'arborescence.  
    `CD chemin du répertoire`

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
