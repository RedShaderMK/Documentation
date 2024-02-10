# 🛡️ Utilisation de Windows Defender en ligne de commande

Il est possible de contrôler Windows Defender avec PowerShell.

- [🛡️ Utilisation de Windows Defender en ligne de commande](#️-utilisation-de-windows-defender-en-ligne-de-commande)
  - [✅ État](#-état)
  - [⌛ Mise à jour](#-mise-à-jour)
  - [🔬 Analyses](#-analyses)
    - [🟢 Rapide](#-rapide)
    - [🟢 Complète](#-complète)
    - [🟢 Personnalisé](#-personnalisé)
    - [🟢 Hors-ligne](#-hors-ligne)

## ✅ État

Il est possible de consulter les informations de l'antivirus directement avec une ligne de commande.  
On y retrouve la version, l'état d'activation ainsi que la version de la base de données de définition.  

`Get-MpComputerStatus`

## ⌛ Mise à jour

Pour lancer manuellement la mise à jour de la base de données de définition :

`Update-MpSignature`

## 🔬 Analyses

Il est possible de lancer plusieurs types d'analyses :  

### 🟢 Rapide

`Start-MpScan -ScanType QuickScan`

### 🟢 Complète

`Start-MpScan -ScanType FullScan`

### 🟢 Personnalisé

`Start-MpScan -ScanType CustomScan -ScanPath <URI du fichier ou répertoire>`

### 🟢 Hors-ligne

`Start-MpWDOScan`

> ℹ️ Remarque : l'ordinateur doit redémarrer pour effectuer cette analyse.
