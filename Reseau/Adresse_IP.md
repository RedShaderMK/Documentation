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

- L'adresse <span style="color:blue">`127.0.0.1`</span> est réservé au test de connexion.
- La classe D est une classe réservé pour le multicast.
- La classe E est réservé pour des test.
