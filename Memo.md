# 📌 Mémo [Markdown](https://daringfireball.net/projects/markdown/syntax)

- [📌 Mémo Markdown](#-mémo-markdown)
  - [📝 La mise en forme du texte](#-la-mise-en-forme-du-texte)
  - [🗒️ Les titres](#️-les-titres)
  - [🔗 Les liens](#-les-liens)
  - [🖼️ Les images](#️-les-images)
  - [📜 Le citations](#-le-citations)
  - [📃 Les listes](#-les-listes)
  - [📑 Les paragraphes](#-les-paragraphes)
  - [📅 Les tableaux](#-les-tableaux)

## 📝 La mise en forme du texte

Markdown permet de réaliser de la mise en forme du le texte.

Pour l'italique :  

```markdown
 _Texte en italique_ ou *Texte en italique*
 ```

Pour le gras :  

```markdown
**Texte en gras**
```

Pour du texte en gras et en italique :  

```markdown
***Texte en gras et en italique***
```

Pour du texte barré :  

```markdown
~~Texte barré~~
```

## 🗒️ Les titres

Comme dans un traitement de texte, il est possible de définir des niveaux de titre :

```markdown
# Titre de niveau 1

## Titre de niveau 2

### Titre de niveau 3

#### Titre de niveau 4

##### Titre de niveau 5

###### Titre de niveau 6
```

> _Remarque : il est possible de mettre un titre en gras et en italique._

## 🔗 Les liens

Il est possible d'insérer des liens avec un texte personnalisé :

```markdown
[Texte qui va s'afficher](http://www.url-de-mon-lien.fr)
```

Exemple :

[Exemple de lien vers mon gitHub](https://github.com/RedShaderMK/RedShaderMK/blob/main/MyProfile.md)

> _Remarque : il est possible de mettre un lien en gras et en italique._

Il est possible d'utiliser une référence pour les liens. Exemple :

```markdown
[Microsoft][docsTerminal] pour configurer mon terminal

[docsTerminal]: https://docs.microsoft.com/fr-fr/windows/terminal/
```

## 🖼️ Les images

Exemple d'une image incorporée :

```markdown
![Alt](https://www.url-de-mon-image.fr)
```

Exemple :

![Mon image](https://am3pap006files.storage.live.com/y4mUMatAILgBbEXiAZ0-Z7w5dDw6klP3hZ_U4n6kC-3dFGROpafNBxo1Q1BxQX9IetHbO9DQd6ScG8xuLQ3wjZ2gWF3nQ-wQhCH_uO557yR59-o23ejynLIoHIO2TnW1iqpQ9fs5VRCuU3W3aCe4GNmifLWHRj8QkSKLGk7qoaNmgDcPpSxlVeixS1Fl1bGDv48?width=500&height=500&cropmode=none)

> _Remarque : Il est possible de faire la même chose qu'avec les liens de références._

## 📜 Le citations

Cela permet de mettre en valeur des extraits de texte comme des citations.

Citation simple :

```markdown
> Démonstration d'une citation
```

Citation d'un paragraphe :

```markdown
> Voici une phrase
>
> En voici une autre
>
> Voici la dernière phrase
```

> _Remarque : il est possible de faire de la **mise en forme** dans une citation_

## 📃 Les listes

Il existe deux types de listes :

1. Les listes non ordonnées (sans chiffres).
2. Les liste ordonnées (avec chiffres).

Exemple de liste non ordonnées :

```markdown
* Item 1
* Item 2
* Item 3
```

Il est possible de faire plusieurs niveaux dans une liste :

```markdown
* Niveau 1
    * Niveau 2
        * niveau 3
```

> _Remarque : mieux vaut ne pas dépasser trois niveau de listes pour des questions de lisibilité_

Il est possible d'insérer des paragraphes sous les listes à puces, exemple :

```markdown
Pour sauvegarder le projet, vous devez :

- Créer le dossier dans le répertoire

    De préférence dans le dossier utilisateur.

- Ensuite faire un `CTRL+S`

    Une fenêtre d'enregistrement doit normalement s'afficher.

- Cliquer sur enregistrer

    Vous pouvez aller vérifier si le fichier a bien été enregistré.
```

Ce qui donne :

Pour sauvegarder le projet, vous devez :

- Créer le dossier dans le répertoire

    De préférence dans le dossier utilisateur.

- Ensuite faire un `CTRL+S`

    Une fenêtre d'enregistrement doit normalement s'afficher.

- Cliquer sur enregistrer

    Vous pouvez aller vérifier si le fichier a bien été enregistré.

Il est possible de créer des listes de cases à cocher :

```markdown
- [ ] Item 1
- [x] Item 2
- [ ] Item 3
```

## 📑 Les paragraphes

Pour passer une ligne, il est possible soit d'insérer un espace entre les lignes, soit d'ajouter deux espaces à la fin de le phrase.

```markdown
Ma phrase..
Une autre phrase
```

[**..** _représentrent deux espaces_]

> _Remarque : il est possible d'utiliser ça pour les paragraphes de listes._

## 📅 Les tableaux

Il est possible de créer des tableaux. Exemple :

```markdown
| Item 1 | Item 2 | Item 3 | Item 4 |
|--------|--------|--------|--------|
| 01     | 01     | 01     | 01     |
| 02     | 02     | 02     | 02     |
| 03     | 03     | 03     | 03     |
```

Le résultat :

| Item 1 | Item 2 | Item 3 | Item 4 |
|--------|--------|--------|--------|
| 01     | 01     | 01     | 01     |
| 02     | 02     | 02     | 02     |
| 03     | 03     | 03     | 03     |
