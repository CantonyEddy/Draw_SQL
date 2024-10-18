# SQL - Examen II - Plateforme E-commerce - README

## Vue d'ensemble
Ce dépôt contient la base de données pour une plateforme de commerce en ligne comme demandé dans le TP. L'objectif de ce projet est de créer un modèle de base de données relationnelle complet qui peut gérer les produits, les clients, les commandes, les fournisseurs, l'inventaire, et d'autres éléments essentiels nécessaires aux opérations d'un détaillant en ligne.

## Décisions de Conception
Voici une brève explication des principales décisions de conception pour le schéma de la base de données, en se concentrant sur les aspects qui n'étaient pas spécifiés explicitement dans les exigences initiales :

1. **Table Payments** : J'ai ajouté une table `Payments` pour assurer une traçabilité financière complète pour chaque commande et pour m'amuser un peu. Cette table aide à gérer les informations de paiement, y compris la méthode de paiement, le montant et le statut, ce qui améliore la fiabilité du suivi des données financières.

2. **Table Consumption List** : La table `Consumption List` a été ajoutée pour suivre l'historique des achats des clients. Cela permet une meilleure analyse du comportement des consommateurs et aide à mettre en place des stratégies de marketing ciblé. Elle permet également à l'entreprise d'analyser les habitudes d'achat pour la gestion des stocks et des ventes.

3. **Gestion de l'Inventaire** : La table `Inventory` est conçue pour suivre la disponibilité des produits en reliant les produits à des emplacements d'entrepôts spécifiques. Cette configuration permet à l'entreprise d'optimiser la distribution des stocks et d'éviter les ruptures de stock ou les situations de surstock.

4. **Produits et Catégories** : Pour offrir une flexibilité dans la classification des produits, j'ai implémenté une relation plusieurs-à-plusieurs entre `Products` et `Categories`. La table de jonction `ProductCategories` facilite la gestion efficace des produits à travers plusieurs catégories, ce qui est crucial pour un catalogue en expansion et une meilleure fonctionnalité de recherche.

## Aperçu des Tables
La base de données se compose des tables suivantes :
- **Products** : Stocke les détails des produits tels que le nom, la description, le prix et le statut.
- **Categories** : Contient des informations sur les catégories de produits.
- **Customers** : Stocke les informations des clients, y compris les coordonnées et l'adresse.
- **Orders** : Contient les commandes des clients avec leur statut et les informations de livraison.
- **Order Details** : Stocke les produits spécifiques associés à une commande, y compris la quantité et le prix unitaire.
- **Inventory** : Gère les niveaux de stock des produits pour différents entrepôts.
- **Suppliers** : Stocke les détails des fournisseurs qui fournissent les produits.
- **Customer Reviews** : Stocke les retours des clients sur les produits.
- **Warehouse Locations** : Contient des informations sur les différents sites d'entrepôts.
- **Consumption List** : Suit les produits achetés par chaque client.
- **Payments** : Stocke les détails de paiement liés à chaque commande.

## Comment Utiliser Ce Dépôt
1. **Schéma de la Base de Données** : Consultez le diagramme UML fourni dans le dépôt pour comprendre les relations entre les différentes entités.
2. **Moteur SQL** : La conception utilise **SQLite** comme moteur SQL, qui est léger et facile à configurer.
3. **Explication des Relations** : Les relations entre les entités, y compris leur cardinalité (un-à-un, un-à-plusieurs, et plusieurs-à-plusieurs), ont été documentées pour garantir que la base de données répond aux exigences fonctionnelles d'une plateforme de commerce électronique.

## Diagramme UML
Le diagramme UML représente la conception de la base de données e-commerce, y compris toutes les entités, attributs, et relations. Assurez-vous d'utiliser des flèches de relation appropriées pour représenter les connexions un-à-un, un-à-plusieurs, et plusieurs-à-plusieurs.

## Contribution
N'hésitez pas à ouvrir des issues ou à soumettre des pull requests pour des améliorations, en particulier si vous avez des idées pour étendre les fonctionnalités de la base de données.

## Licence
Ce projet est sous licence MIT.
