# Gestion des niveaux d'accès

## Contexte

Le paramétrage des niveaux d'accès est essentiel pour commencer l'exploitation de l'application. C'est ici qu'on définira les groupes de rôles et les fonctionnalités auxquelles chaque groupe aura accès. Ensuite il suffira d'affecter chaque [utilisateur](utilisateurs.md) à un de ces niveaux d'accès pour déterminer l'ensemble de ses privillèges dans l'application.
Il faut comprendre que la création des niveau d'accès (le libellé qu'on donne est complètement libre), mais pour des besoins de simplicité, il vaux mieux donner des désignations qui renseigne sur le rôle. Par exemple `ADMINISTRATEUR`, `COMPTABLE`, `RESP PRODUCTION`, etc.

> [!NOTE]  
> En générale, l'accès à la fonctionnalité se fait en suivant le chemenin **`Données de bases > Utilisateurs > Niveau d'acces`**

### 1. Les Ressources à sécuriser

Une resource à sécuriser au sein de l'application peut être consister à bien de choses distincte. On peut partir de la restriction à une page entière à la restriction d'enregistrement d'une opération.

Voici une liste non exhaustive des ressources sur lesquelles il est possible d'appliquer des restrictions

- Valider une facture de vente
- Annuler une facture validé
- Créer un clients: Donne le droit ou non d'enregistrer un nouveau client
- Changer le statut d'un contrat
- Imprimer l'inventaire valorisé
- etc.
  ![liste-resource2.png](https://i.postimg.cc/FKwW74FT/liste-resource2.png)
  ![liste-resource1.png](https://i.postimg.cc/ZqWsbRm9/liste-resource1.png)

  #### Description

  ![ligne_de_resource.png](https://i.postimg.cc/htSHBchx/ligne_de_resource.png)

### 2. Attribuer/Rétirer les ressources d'un rôle (niveau d'accès)

Comme évoqué plus haut, il s'agit de choisir toutes les resources auxquelles les personnes ayant ce niveau d'accès pouront acceder ou non.
**- Etape1: Selectionner le niveau**
![choix-niveau-resources.png](https://i.postimg.cc/cHQJD6Cb/choix-niveau-resources.png)
Comme sur la capture, lorsque vous choisissez le niveau d'accès que vous voulez configurer, la liste des ressources est mise à jour dans le tableau en dessous. Vous pouvez alors retrouver la ressource que vous souhaitez attribuer et désactiver.
Vous pouvez bien évidemment utiliser les champs de filtre en dessous du tableau pour retrouver une ressource spécifique.

**- Etape2: Attribuer les ressources**

![liste-resource1.png](https://i.postimg.cc/ZqWsbRm9/liste-resource1.png)
Comme sur l'image, il suffit juste de cliquer sur le bouton d'interrupteur. S'il est vert c'est que la ressource est autorisé au niveau d'accès; si par contre il est rouge, la ressource n'est pas autorisé. ![resource_desactive.png](https://i.postimg.cc/k5RGbTm9/resource_desactive.png)

### 3. Filtrer les ressources

![filtrer-resources.png](https://i.postimg.cc/j5V5Qyxf/filtrer-resources.png)

### 4. Créer les niveaux d'accès

![formulaire-niveau-acces.png](https://i.postimg.cc/WzWv7pBd/formulaire-niveau-acces.png)

Lorsque vous êtes sur la page des niveaux d'accès, il faut se placer sur le champs **Niveau** et selectionner l'option _**Plus de choix**_ comme sur la capture.
Lorsque vous selectionnez cette option, une modale s'ouvre et vous permet de voir la liste des niveaux d'accès déjà créée et également d'ouvrir le formulaire de création de nouveaux niveaux

#### **Désignation**

- **Description :** Champ libre de saisie de la désignation du niveau
- **Requis :** ✅
- **Remarque :** choisissez une expression suffisament représentattive du groupe d'utilisateurs devant porter ce rôle
- **exemple :** `ADMIN`, `VENDEURS`, `MAGASINIERS`

#### **Grade**

- **Description :** Choisissez un grade dans la liste de selection
- **Requis :**

#### **Faire hériter des droits du niveau**

- **Description :** Pour simplifier la paramétrage des privillège d'un groupe/niveau d'accès, vous pouvez les faires hériter d'un autre. Lorsque vous faites hériter un niveau d'un autre, l'ensemble des privillèges du groupe selectionné sont attribués au nouveau niveau
- **Requis :**
  > [!IMPORTANT]
  > Cette copie ne se fait qu'à la création. Si plus tard vous faites évoluer un niveau, celà ne modifie pas les privillèges du niveau hérité

#### **Description**

- **Description :** Décrivez si possible le groupe
- **Requis :**

### 2. Ajouter des utilisateurs au niveau d'accès

![form-add-user-in-niveau.png](https://i.postimg.cc/NfTMcSrZ/form-add-user-in-niveau.png)

### 3. Modifier le privillèges d'un niveau

![form-edit-privilleges.png](https://i.postimg.cc/FzT259V0/form-edit-privilleges.png)

#### Menu contextuel des privillèges

![menu-contextuel-privillege.png](https://i.postimg.cc/t4FdcB5z/menu-contextuel-privillege.png)
