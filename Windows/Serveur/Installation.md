# Installation de Windows Serveur 2022

Sommaire :  

1. ***Installation de Windows Server***
2. [Configuration de base](./ConfigurationBase.md)
3. [Active Directory](./ActiveDirectory.md)
4. [Le DHCP](./DHCP.md)

Cet article va traiter de l'installation de Windows Server 2022.  

1. Selectionner la langue, le format horaire et monétaire ainsi que la clavier.  
    > ℹ Selectionner la bonne configuration avant l'installation.

    ![Selection langue](./res/Install01.png)

2. Une fenêtre va apparaitre pour commencer l'installation.  

    ![Fenêtre début installation](./res/Install02.png)

3. Une fenêtre va vous demander de saisir une clé de licence. Saisissez là ou cliquer sur le lien en bas pour passer cette étape (dans ce cas, Windows sera activé pour 180 jours).

    ![Fenêtre clé de licence](./res/Install03.png)

4. Une fenêtre va vous demander de sélectionner l'édition à installer (Si vous n'avez pas entré de clé de licence). Selectionner la bonne version.  
    > ℹ En selectionnant Expérience de bureau, Windows Server va installer les éléments du bureau Windows habituel (comme le bureau, le bloc-note, le navigateur internet,etc...)

    ![Fenêtre selection des versions](./res/Install04.png)

5. Cliquer sur `Personnalisé : Installer uniquement le système d'exploitation Microsoft Server (avancé)`

    ![Type d'installation](./res/Install05.png)

6. Selectionner le bon disque ou la bonne partition. Vous pouvez directement en créer depuis cette interface via le bouton `☀ Nouveau`

    ![Selection disque ou partition](./res/Install06.png)

7. L'installation ce lance. Vous devrez patientez quelque minutes (selon la configuration de votre serveur).
    > ℹ Windows va redémarrer automatiquement après cette étape.  

    ![Fenêtre d'installation](./res/Install07.png)

8. Après le redémarrage, Windows va afficher un écran pour la création du mot de passe du compte Administrateur par défaut.

    ![Ecran mot de passe](./res/Install08.png)

9. La confiuration est terminé, vous pouvez vous connecter à Windows Server.  
   > ℹ Ne pas oublier de faire les mises à jour

    ![Bureau Windows](./res/Install09.png)
