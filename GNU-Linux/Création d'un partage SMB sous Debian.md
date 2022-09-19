# Création d'un partage SMB sous Debian

Samba est un logiciel libre dont le but est de créer un serveur de fichier via une implémentation libre du protocole SMB/CIFS de Microsoft Windows (qui lui est propriétaire). Samba permet en plus du partage de fichier, de partager des imprimantes.

## Installation

### 📦 Les paquets

> ℹ️ J'utilise aptitude pour installer les paquets, mais apt-get fonctionne aussi.

Pour commencer, il faut mettre à jour la liste des paquets :

```bash
sudo aptitude update
```

Ensuite, il faut installer les paquets `samba` et `cifs-utils` :

```bash
sudo aptitude install -y samba cifs-utils
```

On va vérifier la version installé avec la commande :

```bash
smbd --version
```

## 🖱 Démarrage

On va démarrer le serveur avec la commande :

```bash
sudo systemctl start smbd
```

Pour vérifier son status :

```bash
sudo systemctl status smbd
```

Pour activer le démarrage automatique :

```bash
sudo systemctl enable smbd
```

## 🗃 Configuration du serveur de fichier

Pour créer nos partage, on va devoir modifier le fichier de configuration de samba :

```bash
sudo vim /etc/samba/smb.conf
```

> ℹ️ J'utilise Vim pour l'édition des fichiers de configuration, mais nano peut aussi convenir.

Pour créer un partage, ajouter les lignes suivante à la fin du fichier :

```bash
[partage]
   comment = Partage de données
   path = /srv/partage
   guest ok = no
   read only = no
   browseable = yes
   valid users = @partage
```

`[Partage]` sert à spécifier le nom du partage.  
`comment` permet de donner une description.  
`path` désigne le chemin du dossier à partager.  
`guest ok` permet d'activer l'accès invité. Si cette option est activé, il faut utiliser le paramètre `guest account`.  
`read only` active ou non la lecture seule sur le partage.  
`browseable` permet de rendre visible ou non le partage dans la découverte réseau.  
`valid users` permet de spécifié les utilisateurs qui ont accès au partage.  

Pour que la modification soit prise en compte, il faut redémarrer le serveur samba :

```bash
systemctl restart smdb
```

## Création de l'utilisateur

Nous allons créer l'utilisateur et le groupe de partage.

Pour créer l'utilisateur :

```bash
adduser userp
```

On va déclarer l'utilisateur à samba et lui créer un mot de passe :

```bash
smbpasswd -a userp
```

On va créer le groupe partage :

```bash
groupadd partage
```

On ajoute ensuite l'utilisateur `userp` au groupe que l'on vient de créer :

```bash
gpasswd -a userp partage
```
