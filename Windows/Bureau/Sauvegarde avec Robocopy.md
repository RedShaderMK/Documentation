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
robocopy "C:\Works" "D:\Backup" /MIR /FFT /XA:SH /XD AppData /XJD /R:5 /W:15 /MT:32 /V /NP /Z /LOG:RapportSauvegarde.log
```

|   Paramètres         |                     Description                       |
|:-------------------- |:----------------------------------------------------- |
| /MIR                 | Permet de créer un mirroir du dossier copié           |
| /FFT                 | Calcule l'heure des fichiers FAT                      |
| /XA:SH               | Permet l'exclusion des fichiers systèmes et cachés    |
| /XD `nom du dossier` | Permet l'exclusion d'un dossier (ici AppData)         |
| /XJD                 | Permet d'exclure les jonctions de répertoires         |
| /R:`n`               | Nombre d'essai maximale si la copie échoue            |
| /W:`n`               | Délai entre chaque essai                              |
| /MT:`n`              | Permet de définir le nombre de threads                |
| /Z                   | Permet de copié les fichiers en mode redémarrable     |
| /V                   | Mode verbeux                                          |
| /NP                  | Permet de ne pas affiché la progression de la copie   |
| /LOG:`fichier.log`   | Permet de créer un log de la copie                    |

## 📎 Autres ressources

[Plus de détails sur robocopy](https://learn.microsoft.com/fr-fr/windows-server/administration/windows-commands/robocopy)
