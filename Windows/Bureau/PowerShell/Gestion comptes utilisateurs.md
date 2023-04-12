# 🧑‍💻 Gestion des utilisateurs

PowerShell permet de gérer les utilisateurs ainsi que les groupes locaux de Windows avec des cmdlets PowerShell. Microsoft propose une collection de cmdlets appelée Microsoft.PowerShell.LocalAccounts pour gérer plus facilement les utilisateurs et groupes locaux avec PowerShell. Vous pouvez ajouter, supprimer et modifier des utilisateurs et des groupes locaux avec PowerShell.

## Voir la listes des commandes

Il existe une commande qui permet de lister l'intégralité des commandes pour gérer les utilisateurs et les groupes :

```powershell
Get-Command -Module Microsoft.PowerShell.LocalAccounts
```

## 1. Obtenir les utilisateurs

Pour obtenir la liste des utilisateurs, il faut utiliser la commande suivante :

```powershell
Get-LocalUser
```

Pour obtenir les détails d'un compte utilisateur précis :

```powershell
Get-LocalUser -Name 'NomUtilisateur' | Select-Object *
```

> ℹ️ Il est possible de filtrer les champs en remplaçant * par le nom du champs.

## 2. Pour ajouter un utilisateur

Pour ajouter un utilisateur, il faut utiliser la commande `New-LocalUser`. Il est possible de spécifier où non un mot de passe. Si l'on veut créer un utilisateur sans mot de passe, il faut utiliser le paramètre `-NoPassword`au lieu de `-Password`.

```powershell
$Password = Read-Host –AsSecureString

New-LocalUser "NomUtilisateur" -Password $Password -FullName "NomUtilisateur" -Description "CompleteVisibility"
```

> ℹ️ La première ligne va demander à l'utilisateur d'entrer un mot de passe. Celui-ci va ensuite être utilisé comme mot de passe par le paramètre `-Password`.

## 3. Pour modifier un utilisateur

Pour modifier le mot de passe d'un utilisateur :

```powershell
$Password = Read-Host –AsSecureString

Set-LocalUser -Name NomUtilisateur -Password $Password -PasswordNeverExpires $False –Verbose
```

## 4. Suppression d'un utilisateur

Pour supprimer un utilisateur, il faut utiliser :

```powershell
Remove-LocalUser -Name NomUtilisateur -Verbose
```
