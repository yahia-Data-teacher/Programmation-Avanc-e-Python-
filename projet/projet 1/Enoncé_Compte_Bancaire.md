# Gestion de Compte Bancaire
- L'objectif est de s'exercer à la spécification et à la programmation de classes élémentaires.
-  En particulier, il s'agit à partir d'un énoncé d'identifier et de définir les caractéristiques d'une classe modélisant un concept donné.

# Cahier des charges
- Il s'agit de définir une classe Python permettant de modéliser des comptes bancaires.
- Cette classe (Compte) doit permettre à une application de créer et utiliser autant de comptes bancaires que nécessaires, chaque compte étant un objet, instance (ou exemplaire) de la classe Compte.

- Un compte bancaire est identifié par un numéro de compte.
- Ce numéro de compte est un entier positif permettant de désigner et distinguer sans ambiguïté possible chaque compte géré par l'établissement bancaire.
-  Chaque compte possède donc un numéro unique. Ce numéro est attribué par la banque à l'ouverture du compte et ne peut être modifié par la suite.
-  Dans un souci de simplicité (qui ne traduit pas la réalité) on adoptera la politique suivante pour l'attribution des numéros de compte :
    - les comptes sont numérotés de 1 à n, n étant le nombre de comptes qui ont été créés.
    - Lorsque un nouveau compte est créé, le numéro qui lui est attribué est n+1.

- Un compte est associé à une personne (civile ou morale) titulaire du compte, cette personne étant décrite par son nom.
- Une fois le compte créé, le titulaire du compte ne peut plus être modifié.

- La somme d'argent disponible sur un compte est exprimée en Euros. 
- Cette somme est désignée sous le terme de solde du compte. 
- Ce solde est un nombre décimal qui peut être positif, nul ou négatif.

- Le solde d'un compte peut être éventuellement (et temporairement) être négatif. 
- Dans ce cas, on dit que le compte est à découvert. 
- Le decouvert d'un compte est nul si le solde du compte est positif ou nul, il est égal à la valeur absolue du solde si ce dernier est négatif.

- En aucun cas le solde d'un compte ne peut être inférieur à une valeur fixée pour ce compte. 
- Cette valeur est définie comme étant - (moins) le découvert maximal autorisé pour ce compte. 
- Par exemple pour un compte dont le découvert maximal autorisé est 2000 €, le solde ne pourra pas être inférieur à -2000 €. 
- Le découvert maximal autorisé peut varier d'un compte à un autre, il est fixé arbitrairement par la banque à la création du compte et peut être ensuite révisé selon les modifcations des revenus du titulaire du compte.

- Créditer un compte consiste à ajouter un montant positif au solde du compte.

- Débiter un compte consiste à retirer un montant positif au solde du compte. 
- Le solde résultant ne doit en aucun cas être inférieur au découvert maximal autorisé pour ce compte.

- Lors d'une opération de retrait, un compte ne peut être débité d'un montant supérieur à une valeur désignée sous le terme de débit maximal autorisé. 
- Comme le découvert maximal autorisé, le débit maximal autorisé peut varier d'un compte à un autre et est fixé arbitrairement par la banque à la création du compte. 
- Il peut être ensuite révisé selon les modifications des revenus du titulaire du compte.

- Effectuer un virement consiste à débiter un compte au profit d'un autre compte qui sera crédité du montant du débit.

- Lors de la création d'un compte seul le nom du titulaire du compte est indispensable.
- En l'absence de dépot initial le solde est fixé à 0. 
- Les valeurs par défaut pour le découvert maximal autorisé et le débit maximal autorisé sont respectivement de 800 € et 1000 €. 
- Il est éventuellement possible d'attribuer d'autres valeurs à ces caractéristiques du compte lors de sa création.

- Toutes les informations concernant un compte peuvent être consultées : numéro du compte, nom du titulaire, montant du découvert maximal autorisé, montant du débit maximal autorisé, situation du compte (est-il à découvert ?), montant du débit autorisé (fonction du solde courant et du débit maximal autorisé).

# Travail demandé
- À partir du "cahier des charges" précédent élaborer une spécification d'une classe Python modélisant un compte bancaire.

- Il s'agira en analysant le texte ci-dessus de :

    - définir les attributs de la classe Compte,

    - d'identifier les méthodes proposées par la classe Compte.
    - Pour chaque méthode on prendra soin, outre la définition de sa signature, de spécifier son comportement sous la forme d'un commentaire.

    - de proposer un ou plusieurs constructeurs pour la classe Compte.
    -  Là aussi on complétera la donnée de la signature de chaque constructeur avec un commentaire détaillant son utilisation.

    - Réaliser une implémentation en langage Python de la classe précédemment spécifiée.

- Ecrire un programme de test permettant de :

    - Créer un compte c1, au nom de J. DUPONT avec un solde initial de 1 000 €

    - Créer un compte c2, au nom de C. DURANT avec un solde inital de 50 000 €, un debit maximal autorisé de 6000 € et un découvert maximal autorisé de 5000 €.

    - D'afficher les caractéristiques des comptes c1 et c2 (c'est à dire les informations suivantes : numéro du compte, nom du titulaire, découvert maximal autorisé, débit maximal autorisé, solde du compte et si le compte est à découvert un message le signalant explicitement).

    - Retirer 300 € du compte c1.

    - Retirer 600 € du compte c2.

    - Déposer 500 € sur le compte c1.

    - D'afficher les caractéristiques des comptes c1 et c2.

    - Virer 1000 € du compte c2 vers le compte c1.

    - D'afficher les caractéristiques des comptes c1 et c2.
