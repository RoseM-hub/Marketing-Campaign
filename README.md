
---
title: "Segmentation de la Clientèle"

---
![img](img.png)

# Introduction

L'analyse de la personnalité des clients vise à mieux comprendre les divers profils et comportements des consommateurs afin d’adapter les produits et les stratégies marketing de l'entreprise. En segmentant les clients en fonction de leurs besoins, préférences et habitudes d'achat, une entreprise peut cibler plus efficacement ses efforts et personnaliser ses offres.

L'objectif principal de ce projet est d'identifier les segments de clients les plus susceptibles de répondre positivement aux produits et services proposés. Plutôt que d'adopter une approche universelle pour tous les clients, il s'agit de concentrer les efforts marketing sur les groupes les plus pertinents, augmentant ainsi les chances de succès et optimisant l'allocation des ressources. Cette analyse permettra également de mieux prévoir les comportements futurs des clients en fonction de leurs caractéristiques passées.

En somme, l’enjeu est de comprendre les différents types de clients et de les relier aux actions commerciales pour maximiser l'efficacité des stratégies de marketing.

---

# Données

Personnes

- **ID** : Identifiant unique du client
- **Year_Birth** : Année de naissance du client
- **Education** : Niveau d'éducation du client
- **Marital_Status** : État civil du client
- **Income** : Revenu annuel du ménage du client
- **Kidhome** : Nombre d'enfants dans le ménage du client
- **Teenhome** : Nombre d'adolescents dans le ménage du client
- **Dt_Customer** : Date d'inscription du client auprès de l'entreprise
- **Recency** : Nombre de jours depuis le dernier achat du client
- **Complain** : 1 si le client a déposé une plainte au cours des 2 dernières années, 0 sinon

Produits

- **MntWines** : Montant dépensé en vin au cours des 2 dernières années
- **MntFruits** : Montant dépensé en fruits au cours des 2 dernières années
- **MntMeatProducts** : Montant dépensé en viande au cours des 2 dernières années
- **MntFishProducts** : Montant dépensé en poisson au cours des 2 dernières années
- **MntSweetProducts** : Montant dépensé en sucreries au cours des 2 dernières années
- **MntGoldProds** : Montant dépensé en or au cours des 2 dernières années

Promotion

- **NumDealsPurchases** : Nombre d'achats effectués avec une réduction
- **AcceptedCmp1** : 1 si le client a accepté l'offre lors de la 1ère campagne, 0 sinon
- **AcceptedCmp2** : 1 si le client a accepté l'offre lors de la 2ème campagne, 0 sinon
- **AcceptedCmp3** : 1 si le client a accepté l'offre lors de la 3ème campagne, 0 sinon
- **AcceptedCmp4** : 1 si le client a accepté l'offre lors de la 4ème campagne, 0 sinon
- **AcceptedCmp5** : 1 si le client a accepté l'offre lors de la 5ème campagne, 0 sinon
- **Response** : 1 si le client a accepté l'offre lors de la dernière campagne, 0 sinon

Lieu

- **NumWebPurchases** : Nombre d'achats effectués sur le site web de l'entreprise
- **NumCatalogPurchases** : Nombre d'achats effectués en utilisant un catalogue
- **NumStorePurchases** : Nombre d'achats effectués directement en magasin
- **NumWebVisitsMonth** : Nombre de visites sur le site web de l'entreprise au cours du dernier mois

---

# Méthodologie

Des nouvelles variables ont été créées pour mieux caractériser chaque client, telles que :

- Indication de s'il est parent
- Le nombre de personnes dans son ménage
- Son âge
- Son ancienneté dans l'entreprise

Des variables financières ont également été ajoutées, telles que le montant total dépensé par le client et le nombre de campagnes marketing auxquelles il a participé. Ces transformations fournissent une vue plus complète des clients, facilitant ainsi leur segmentation.

Une analyse descriptive a été effectuée pour mieux comprendre la distribution des données avant de passer à l'étape de segmentation. Les étapes de prétraitement suivantes ont été appliquées :

- Encodage des variables catégorielles
- Transformation logarithmique des variables numériques asymétriques
- Standardisation des valeurs
- Détection des valeurs aberrantes à l'aide du score Z et exclusion pour garantir la qualité des données

Une fois les données préparées, la méthode de Classification Ascendante Hiérarchique (CAH) a été utilisée pour segmenter les clients. Cette méthode a été choisie pour sa flexibilité et sa capacité à gérer des clusters de formes et de tailles inégales. Un *dendrogramme* a été utilisé pour visualiser les relations entre les clients et déterminer le nombre optimal de segments.

Cette approche a permis de découvrir des groupes homogènes, offrant ainsi une meilleure compréhension des comportements clients pour des actions marketing ciblées.

---

# Résultats

Les résultats de la segmentation ont permis d'identifier trois catégories distinctes de clients. Voici un résumé des caractéristiques principales de chaque groupe :

| **Cluster**                                | **Revenus**         | **Achats (Montant)** | **Achats (Fréquence)** | **Acceptation des Campagnes** | **Profil Familial**             |
|--------------------------------------------|---------------------|----------------------|------------------------|------------------------------|----------------------------------|
| **Familles Modestes et Réservées**         | Modestes            | Faibles              | Faibles                | < 7%                        | 90% parents, 66% en couple      |
| **Couples Haut Revenus et Opportunistes**  | Élevés              | Élevés               | Élevés                 | < 15%                       | 85% parents, 70% en couple      |
| **Professionnels Solitaires et Réactifs**  | Très élevés         | Très élevés          | Très fréquents         | ~60%                        | 82% non-parents, 64% en couple  |

### Interprétation des Résultats

- **Familles Modestes et Réservées** : Ce groupe a des revenus modestes et réalise des achats peu fréquents et de faible montant. Ils représentent un segment à prioriser pour des offres à prix abordable.
- **Couples Haut Revenus et Opportunistes** : Ce groupe, avec des revenus élevés, effectue des achats fréquents et importants. Ils sont plus réceptifs aux campagnes mais représentent une clientèle qui nécessite des produits haut de gamme.
- **Professionnels Solitaires et Réactifs** : Ce groupe réagit de manière fréquente aux campagnes marketing, avec des achats élevés. Les campagnes marketing adaptées à leurs besoins spécifiques peuvent stimuler encore plus leur engagement.

---

# Structure du Projet

Voici la structure des dossiers de ce projet :

```bash
MARKETING-CAMPAIGN/
│
├── data/                          # Données brutes
│
├── notebooks/                     # Dossiers contenant les notebooks de travail
│
├── readme.md                      # Ce fichier README
│
└── requirements.txt               # Liste des bibliothèques nécessaires pour le projet
