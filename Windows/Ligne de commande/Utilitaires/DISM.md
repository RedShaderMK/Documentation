# 🛠️ Utilisation de DISM

## Introduction

DISM pour « Deployment Image Servicing and Management » est un utilitaire en ligne de commande natif de Windows qui permet la maintenance et la gestion des images Windows. Cet outil permet la vérification et réparation des fichiers système corrompus ou endommagés.

## Utilisation

Pour utiliser DISM, il faut dans un premier temps ouvrir une invite de commande en mode administrateur.  

## Vérification des fichiers

Pour la vérification, il faut utiliser la commande :  
`DISM /Online /Cleanup-Image /ScanHealth`

## Réparation des fichiers

Pour corriger les erreurs, il faut utiliser la commande :  
`DISM /Online /Cleanup-Image /RestoreHealth`

## Réparation depuis une source externe

Il est possible de lancer une réparation avec une source externe si la réparation classique ne fonctionne pas.  
Pour ce faire, il faut utiliser la commande :  
`DISM /Online /Cleanup-Image /RestoreHealth /Source:<source du fichier wim`
