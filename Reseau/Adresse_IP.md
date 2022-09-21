# 🖥️ Adressage IPv4

## 📌 Introduction

Les adresses IP (pour Internet Protocol) sont des numéros d'identifications. Ces adresses permettent d'identifier les périphériques qui y sont connectés (aussi appelé des nœuds), peuvent être permanentes ou temporaires (avec un bail fixé par le DHCP). Leurs attributions peuvent être automatiques (via le DHCP) ou manuelles.  
Elles sont codés sur 32bits et leur représentation consiste a une suite de 4 chiffres décimaux compris entre 0 et 255. Ces chiffres sont séparés par des points. Voici un exemple : `192.168.1.1`

Il existe différentes classes d'adresses :

| **Classe** | **Premiers bits** | **Première adresse IP** | **Dernière adresse IP** | **Masques par défauts** |
|:----------:|:-----------------:|:-----------------------:|:-----------------------:|:-----------------------:|
|      A     |         0         |         0.0.0.0         |     126.255.255.255     |        255.0.0.0        |
|      B     |         10        |        128.0.0.0        |     191.255.255.255     |       255.255.0.0       |
|      C     |        110        |        192.0.0.0        |     223.255.255.255     |      255.255.255.0      |
|      D     |        1110       |        224.0.0.0        |     239.255.255.255     |     255.255.255.255     |
|      E     |        1111       |        240.0.0.0        |     255.255.255.255     |           N/A           |

ℹ️ Exeptions :  

- L'adresse `127.0.0.1` est réservé au test de connexion.
- La classe D est une classe réservé pour le multicast.
- La classe E est réservé pour des test.

## Calculer le nombre d'hôte d'un masque

Voici un exemple de calcul des sous-réseaux :

Pour un masque de sous réseau `255.255.240.0`, il faut déjà le passer en binaire, ce qui donne :  
`1111 1111.1111 1111.1111 0000.0000 0000`.

Il faut prendre la partie hôte qui est `240.0` donc `1111 0000.0000 0000`.

On veut y ajouter 8 sous réseaux donc on va chercher la puissance de 2 qui correspond. Celle-ci est 3 car 2^3 = 8.  
On va donc ajouter 3 bits à `1111 0000` ce qui donne `1111 1110`.
