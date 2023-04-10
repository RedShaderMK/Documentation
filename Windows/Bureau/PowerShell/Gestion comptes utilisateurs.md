# 🧑‍💻 Gestion des utilisateurs

PowerShell permet de gérer les utilisateurs ainsi que les groupes locaux de Windows avec des cmdlets PowerShell. Microsoft propose une collection de cmdlets appelée Microsoft.PowerShell.LocalAccounts pour gérer plus facilement les utilisateurs et groupes locaux avec PowerShell. Vous pouvez ajouter, supprimer et modifier des utilisateurs et des groupes locaux avec PowerShell.

## 1. Pour ajouter un utilisateur

Pour ajouter un utilisateur, il faut utiliser la commande `New-LocalUser`. Il est possible de spécifier où non un mot de passe. Si l'on veut créer un utilisateur sans mot de passe, il faut utiliser le paramètre `-NoPassword`au lieu de `-Password`.

```powershell
$Password = Read-Host –AsSecureString
New-LocalUser "NomUtilisateur" -Password $Password -FullName "NomUtilisateur" -Description "CompleteVisibility"
```

> ℹ️ La première ligne va demander à l'utilisateur d'entrer un mot de passe. Celui-ci va ensuite être utilisé comme mot de passe par le paramètre `-Password`.

## 2. Pour modifier un utilisateur


