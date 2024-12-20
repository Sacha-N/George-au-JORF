# George-au-JORF
## Motivation
Qui, de George ou d'Enzo, d'Emilie ou de Mélanie, composent les cabinets ministériels ? Ce projet, réalisé à l'occasion du cours de Python pour la data science (automne 2024) à l'Ensae, vise à rendre compte des structures de classe et de genre parmi les conseiller·ères ministériel·les. 

En l'absence de données sur l'origine sociale des membres des cabinets, nous employons le prénom comme proxy, au travers notamment de la moyenne prédite au Baccalauréat (*Sociologie des prénoms*, Coulmont 2011).

## Données
Dans le cadre de ce projet, deux principales sources sont mobilisées : les nominations publiées au Journal officiel de la République française (JORF), récupérées grâce à l'API Légifrance du portail public PISTE, et les listes de bacheliers 2024 comprenant nom, prénom, mention, récupérées par webscraping. 

Ces deux sources nous permettent de faire preuve de concept pour l'année 2024, puis sont complétées pour les années précédentes par la base constituée par Nathann Cohen via son outil Jorfsearch [https://www.steinertriples.ch/ncohen/data/nominations_JORF/] comprenant les nominations depuis 1990, ainsi que par les données des éditions précédentes du Baccalauréat conservées par Baptiste Coulmont, que nous avons contacté. Nous avons également créé notre propre algorithme de scraping pour récupérer les données 2024 sur le site *Le Parisien*. Malheureusement, il nous a été impossible de réaliser cela pour plusieurs années du fait de la délétion des données à chaque itération du bac.

Nous avons par ailleurs utilisé d'autres données annexes. La première est le répertoire des prénoms de l'Insee [https://www.insee.fr/fr/statistiques/7635552]. La deuxième est le fichier géo-data des académies en France, fournit par le ministère de l'éducation nationale [https://www.data.gouv.fr/fr/pages/donnees-geographiques/].

## Méthode 
Ce projet a une portée principalement descriptive et diachronique : comment a évolué l'ouverture sociale et la composition genrée des cabinets ? A quelle(s) région(s) correspond la géographie des prénoms plébiscités par les ministres ?

Ces statistiques descriptives sont complétées par un travail de modélisation : Nous avons réalisé une série de régressions linéaires. Celles-ci représentaient une *probabilité* pour un *prénom* d'accéder à un cabinet ministériel, en fonction du *score* ou du *sexe*. Nous avons utilisé plusieurs définitions du *score* et de cette *probabilité* ce qui nous a permis de tirer différentes conclusions. 

## Principaux résultats
(**à compléter**)

En termes spatiaux, nous avons mis en valeur l'hétérogénéité des résultats au bac des différentes académies. L'académie de Strasbourg sortant en tête.

La modélisation nous a permis de mettre en valeur la corrélation positive entre le *score social* et la *probabilité* pour un *prénom* d'être en cabinet ministériel. Elle nous a également permis de mettre en avant que toutes choses égales par ailleurs, les hommes ont une probabilité plus grande de rentrer en cabinet ministériel.

## Organisation du repository 
Il nous faudra : un main, puis le script de scraping et le script d'API à côté