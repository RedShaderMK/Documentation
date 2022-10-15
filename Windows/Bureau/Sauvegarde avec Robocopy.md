# 💾 Sauvegarder ses fichiers avec Robocopy

> ℹ️ Système minimal : Windows NT 4

Sous Windows, il est possible de sauvegarder ses fichiers avec un simple copié-collé. Cependant, c'est assez fastidieux et peu sûr. Il existe un utilitaire du nom de _robocopy_ qui permet de réaiser assez facilement des sauvegardes de répertoires et de fichiers via l'Invite de commande. Il est aussi possible d'automatiser cela avec des scripts.

> ℹ️ Il existe un utilitaire en ligne de commande similaire mais plus ancien : XCOPY

## 📖 C'est quoi robocopy  

Robocopy (qui veut dire _Robust File Copy_) est un utilitaire en ligne de commande permettant de créer des copies de fichiers plus avancé qu'avec l'utilitaire de copie GUI de Windows. Il est apparu avec le _Windows Resource Kit_ de Windows NT 4.0.  
Robocopy est intégré nativement depuis Windows Vista.

## 🛠️ Utilisation  

Voici la commande base pour utiliser robocopy :  

```dos
robocopy <source> <destination> [<file>[ ...]] [<options>]
```

|   Paramètres    |                     Description                       |
|:--------------- |:----------------------------------------------------- |
| `source`        | Le répertoire source                                  |
| `destination`   | Le répertoire de destination                          |
| `file`          | Les fichiers à copié. Par défaut, la valeur est `*.*` |
| `option`        | Les options de robocopy                               |

Exemple :  

```dos
robocopy 'C:\Works' 'D:\Backup' *.*
```

Exemple pour la sauvegarde du profil utilisateur :  

```dos
robocopy "C:\Works" "D:\Backup" /MIR /FFT /XA:SH /XD AppData /XJD /R:5 /W:15 /MT:32 /V /NP /Z /LOG:Backup.log
```
