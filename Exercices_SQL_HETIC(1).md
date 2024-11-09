# Exercices sur les requêtes de sélection

## Requête simple

0) La liste des bureaux (adresse et ville) triés par pays décroissant puis par état 
   /* RESULTAT ==> 7 lignes / 100 Market Street */

## Requêtes WHERE

1) La liste des avions (code et nom) triés par vendeur et par quantité en stock décroissants 

/* RESULTAT ==> 12 lignes / 1900s Vintage Tri-Plane */

2) La liste des produits (code, nom, échelle et quantité) qui ont une échelle soit de 1:10, soit de 1:18 triés par quantité en stock décroissante 

/* RESULTAT ==> 48 lignes / 1995 Honda Civic */

3) La liste des produits (nom, vendeur et prix de vente) qui sont vendus au moins 132$ triés par nom du produit 

/* RESULTAT ==> 24 lignes / 1903 Ford Model A */

4) La liste des produits (code, nom et prix d'achat) des produits achetés au moins 60$ au plus 90$ triés par prix d'achat

/* RESULTAT ==> 34 lignes / 1937 Lincoln Berline */

5) La liste des avions (code et nom) triés par vendeur et par quantité en stock décroissants 

/* RESULTAT ==> 12 lignes / 1900s Vintage Tri-Plane */

6) La liste des produits (code, nom, échelle et quantité) qui ont une échelle soit de 1:10, soit de 1:18 triés par quantité en stock décroissante

/* RESULTAT ==> 48 lignes / 1995 Honda Civic */

7) La liste des produits (nom, vendeur et prix de vente) qui sont vendus au moins 132$ triés par nom du produit 

/* RESULTAT ==> 24 lignes / 1903 Ford Model A */

8) La liste des produits (code, nom et prix d'achat) des produits achetés au moins 60$ au plus 90$ triés par prix d'achat

/* RESULTAT ==> 34 lignes / 1937 Lincoln Berline */

## Colonnes calculées

9) La liste des motos (nom, vendeur, quantité et marge) triés par marge décroissante 

/* RESULTAT ==> 13 lignes / 2003 Harley-Davidson Eagle Drag Bike */

10) La liste des commandes (numéro, date de commande, date d'expédition, écart en jours entre les deux dates et statut) qui sont en cours de traitement ou qui ont été expédiées et ont un écart de plus de 10j triés par écart décroissant puis par date de commande

/* RESULTAT ==> 33 lignes / 10165 */

11) La liste des produits (nom et valeur du stock à la vente) des années 1960

/* RESULTAT ==> 16 lignes / 1969 Harley Davidson Ultimate Chopper

## Jointures INNER JOIN

12) La liste des employés (nom, prénom et fonction) et des bureaux (adresse et ville) dans lequel ils travaillent

/* RESULTAT ==> 23 lignes / Diane Murphy */

13) La liste des clients français ou américains (nom du client, nom, prénom du contact et pays) et de leur commercial dédié (nom et prénom) triés par nom et prénom du contact

/* RESULTAT ==> 48 lignes / Miguel Barajas */

14) La liste des lignes de commande (numéro de commande, code, nom et ligne de produit) et la remise appliquée aux voitures ou motos commandées triées par numéro de commande puis par remise décroissante

/* RESULTAT ==> 2026 lignes / 34 */

## Agrégations GROUP BY

15) Le prix moyen d'un produit vendu par chaque vendeur triés par prix moyen décroissant

/* RESULTAT ==> 13 lignes / Welly Diecast Productions / 113.9325 */

16) Le nombre de produits pour chaque ligne de produit

/* RESULTAT ==> 7 lignes / Classic Cars / 38 */

17) Le total du stock et le total de la valeur du stock à la vente de chaque ligne de produit pour les produits vendus plus de 100$ trié par total de la valeur du stock à la vente

/* RESULTAT ==> 7 lignes / Ships / 429177.74 */

18) La quantité du produit le plus en stock de chaque vendeur trié par vendeur

/* RESULTAT ==> 13 lignes / Autoart Studio Design / 9354 */

19) Le prix de l'avion qui coûte le moins cher à l'achat

/* RESULTAT ==> 1 ligne / 29.34$ */

20) Le crédit des clients qui ont payé plus de 20000$ durant l'année 2004 trié par crédit décroissant

/* RESULTAT ==> 69 lignes / 141 / 293 765.51 */

## Requêtes complexes

21) Le total des paiements effectués de chaque client (numéro, nom et pays) américain, allemand ou français de plus de 50000$ trié par pays puis par total des paiements décroissant

/* RESULTAT ==> 38 lignes / 146 / 130305.35 */

22) Le montant total de chaque commande (numéro et date) des clients New-Yorkais (nom) trié par nom du client puis par date de commande

/* RESULTAT ==> 16 lignes / Classic Legends / 10115 / 21665.98 */

## Opérations ensemblistes

23) Lister les noms et prenoms de toutes les personnes (clients + employés)

24) Lister les noms de pays où nous avons à la fois des clients et des bureaux

25) Lister les noms des pays des clients où nous n'avons pas de bureaux

## Requêtes imbriquées

26) Liste des noms et prénoms de personnes qui ont passé des commandes dont le montant est supérieur à la moyenne (de toutes les commandes)

27) Je suis client du magasin. Quels sont produits qu'achètent les clients qui ont les mêmes goûts que moi ? (c'est-à-dire qui ont tendance à acheter les mêmes produits que moi)

## Fonctions de fenêtrage OVER(PARTITION ...)

28) Autre version de l'exercice **21** avec partitionnement (ou fonction de fenêtrage)

29) Distribution par déciles des délais de paiement

> Utilisez
> 
> - une requête imbriquée
> - une fonction de fenêtrage avec la fonction d'agrégation NTILE

30) Délais de paiement par commande et par client avec moyenne globale ; Afficher ne n° du client, le pays, le montant de la commande, la date de paiement

31) Pays dans lesquels le délai de paiement est en moyenne supérieur à la moyenne globale ; Afficher aussi l'excès de de délai par rapport à la moyenne

> Utilisez 
> 
> - des expressions de contexte 
> - des fonctions de fenêtrage

## Optimisation

32) Liste des noms et prénoms de personnes qui ont passé des commandes dont le montant est supérieur à la moyenne (de toutes les commandes)

> Utilisez une expression de contexte

33) Je suis client du magasin. Quels sont produits qu'achètent les clients qui ont les mêmes goûts que moi ? (c'est-à-dire qui ont tendance à acheter les mêmes produits que moi)

> Utilisez des expressions de contexte et des variables SQL

34) Même requête

> Version utilisant des vues

35) Les maquettes qui ont été aussi achetées par les clients qui ont acheté une certaine maquette (on retiendra les 10 plus vendues)

> Utilisez 
> 
> - une variable SQL
> - une requête imbriquée
