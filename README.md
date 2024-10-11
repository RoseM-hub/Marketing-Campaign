#Marketing-Campaign

**Énoncé du Problème**

L'analyse de la personnalité des clients est une analyse détaillée des clients idéaux d'une entreprise. Elle aide une entreprise à mieux comprendre ses clients et facilite la modification des produits en fonction des besoins, des comportements et des préoccupations spécifiques de différents types de clients.

L'analyse de la personnalité des clients aide une entreprise à modifier ses produits en fonction de ses clients cibles issus de différents segments de clients. Par exemple, au lieu de dépenser de l'argent pour commercialiser un nouveau produit auprès de tous les clients de la base de données de l'entreprise, une entreprise peut analyser quel segment de clients est le plus susceptible d'acheter le produit et ensuite commercialiser le produit uniquement auprès de ce segment particulier.

**Contenu**

**Attributs**

*Personnes*

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

*Produits*

- **MntWines** : Montant dépensé en vin au cours des 2 dernières années
- **MntFruits** : Montant dépensé en fruits au cours des 2 dernières années
- **MntMeatProducts** : Montant dépensé en viande au cours des 2 dernières années
- **MntFishProducts** : Montant dépensé en poisson au cours des 2 dernières années
- **MntSweetProducts** : Montant dépensé en sucreries au cours des 2 dernières années
- **MntGoldProds** : Montant dépensé en or au cours des 2 dernières années

*Promotion*

- **NumDealsPurchases** : Nombre d'achats effectués avec une réduction
- **AcceptedCmp1** : 1 si le client a accepté l'offre lors de la 1ère campagne, 0 sinon
- **AcceptedCmp2** : 1 si le client a accepté l'offre lors de la 2ème campagne, 0 sinon
- **AcceptedCmp3** : 1 si le client a accepté l'offre lors de la 3ème campagne, 0 sinon
- **AcceptedCmp4** : 1 si le client a accepté l'offre lors de la 4ème campagne, 0 sinon
- **AcceptedCmp5** : 1 si le client a accepté l'offre lors de la 5ème campagne, 0 sinon
- **Response** : 1 si le client a accepté l'offre lors de la dernière campagne, 0 sinon

*Lieu*

- **NumWebPurchases** : Nombre d'achats effectués sur le site web de l'entreprise
- **NumCatalogPurchases** : Nombre d'achats effectués en utilisant un catalogue
- **NumStorePurchases** : Nombre d'achats effectués directement en magasin
- **NumWebVisitsMonth** : Nombre de visites sur le site web de l'entreprise au cours du dernier mois

**Cible**

Il est nécessaire de réaliser un clustering pour résumer les segments de clients.


Le jeu de données pour ce projet est fourni par le Dr. Omar Romero-Hernandez.
