# Contexte



Les données disponibles en téléchargement dans ce dossier sont issues des travaux de recherche réalisés dans le cadre de l'ANR [MApUCE.](http://www.cnrm.meteo.fr/spip.php?article787)

Elles sont fournies en accès libre, licence [ODbL](https://opendatacommons.org/licenses/odbl/1.0/).

Les données sont diffusées à deux echelles spatiales : les Unités Spatiales de Référence (USR) et l'Ilot de Chaleur Urbain (ICU).



# Contenu des dossiers



Dans chacun dossier USR (.zip), vous trouverez :                

- un fichier "USR_MAPUCE_xxx.geojson", couvrant l'unité urbaine "xxx" traitée,
- un fichier "[readme.pdf](http://mapuce.orbisgis.org/data/usr/readme.pdf)" décrivant le jeu de donnée,
- un fichier "[usr_mapuce_agglo_villes.pdf](http://mapuce.orbisgis.org/data/usr/usr_mapuce_agglo_villes.pdf)" contenant la liste des unités urbaines et communes traitées pendant le projet,
- un fichier de style "[usr_typo.sld](http://mapuce.orbisgis.org/data/usr/usr_typo.sld)" permettant de cartographier le champ "typo_maj".



Dans chacun dossier ICU (.zip), vous trouverez :                

- un fichier "xxx_icu_hot_summer_1.shp", couvrant l'unité urbaine "xxx" traitée pour la configuration de temps n°1,

- un fichier "xxx_icu_hot_summer_2.shp", couvrant l'unité urbaine "xxx" traitée pour la configuration de temps n°2,

- un fichier "[ICU_Description.pdf](http://mapuce.orbisgis.org/data/icu/ICU_Description.pdf)" décrivant le jeu de donnée ainsi que l'ensemble des configurations de temps en fonction des unités urbaines,

- un fichier de style "[icu_hot_summer.sld](http://mapuce.orbisgis.org/data/icu/icu_hot_summer.sld)" permettant de cartographier le champ "temp".

  

# Définitions



**Termes**

- USR : Unité Spatiale de Référence,  définie par un ensemble de parcelles cadastrales qui se touchent et  auxquelles sont adjointes les demi-surfaces de routes entourant cet  ensemble,
- Bloc : ensemble de bâtiments ayant au  moins un point de contact (ou une façade) en commun. Les bâtiments qui  se touchent sont alors fusionnés afin de générer une nouvelle "super"  géométrie : le bloc.

------

**Indicateurs par îlots**

- Surfaces

- - Pourcentage de surface de bâtiments : Rapport entre la somme des surfaces au sol des bâtiments et la surface de l'USR,
  - Pourcentage de surface de plancher : Rapport entre la somme des surfaces de plancher et la surface de  l'USR. La surface de plancher d'un bâtiment est égale à la surface au  sol multipliée par le nombre de niveaux du bâtiment,
  - Pourcentage de surface de végétation : Rapport entre la somme des surfaces de végétation et la surface de l'USR,
  - Pourcentage de surface de routes : Rapport entre la somme des surfaces de routes et la surface de l'USR,
  - Pourcentage de surface en eau : Rapport entre la somme des surfaces en eau et la surface de l'USR,

- Formes

- - Hauteur moyenne des bâtiments : Moyenne des hauteurs des bâtiments présents dans l'USR,
  - Volume moyen des bâtiments : Moyenne des volumes des bâtiments présents dans l'USR,
  - Compacité moyenne des bâtiments : Moyenne des compacité des bâtiments présents dans l'USR,
  - Compacité moyenne des blocs : Moyenne des compacités des blocs présents dans l'USR,

- Autres

- - Nombre de bâtiments : Nombre de bâtiments présents dans l'USR,
  - Distance moyenne entre bâtiments : Pour chaque bâtiment, nous calculons la moyenne des distances aux  autres bâtiments présents dans l'USR. Ensuite, nous calculons la moyenne de ces distances moyennes.

------

**Typologies**

- Bâtiment majoritaire par ilôts : dans  chaque USR, les bâtiments sont statistiquement classés sur la base d'une soixantaine d'indicateurs morphologiques (en partie présentés  ci-dessus). Cette classification (supervisée, avec la méthode du "Random Forest") permet de faire ressortir les types majoritaire et secondaire  de bâti dans l'USR. Ici, nous présentons le type majoritaire.

------

**Ilôt de Chaleur Urbain (ICU)**

- ICU - Scénario ETE 1 et 2 : Ces deux  couches représentent l'îlot de chaleur urbain (ICU) calculé sur une  Unité Urbaine (UU) d'étude. Il s'agit ici d'une modélisation faite à  l'aide du modèle [TEB](http://www.umr-cnrm.fr/spip.php?article199&lang=fr) et dont le résultat, exprimé en kelvin, montre l'effet de l'UU sur la  température nocturne pendant une situation estivale propice à un fort  îlot de chaleur urbain. Deux configurations de temps (scénarios) sont  proposées pour chacune des UU. Pour en savoir plus, reportez vous à la  documentation disponible [ICI](http://mapuce.orbisgis.org/data/icu/ICU_Description.pdf) (voir l'onglet "[Données ICU](http://mapuce.orbisgis.org/#data_icu)").



# Bibliographie

- Bocher E., Petit G., Bernard J., Palominos S. *"A geoprocessing framework to compute urban indicators: The MApUCE tools chain"*. Urban Climate, Elsevier, 2018, 24, pp.153-174. [10.1016/j.uclim.2018.01.008](http://dx.doi.org/10.1016/j.uclim.2018.01.008)
- Bocher E., Petit G., Fortin N., Palominos S. *"H2GIS a spatial database to feed urban climate issues"*. 9th International Conference on Urban Climate ([ICUC9](http://www.meteo.fr/icuc9/index.html)), Jul 2015, Toulouse, France. 2015. [(Référence)](https://halshs.archives-ouvertes.fr/halshs-01179756)



# Mention légale

**Données**

Les données distribuées en open data sont le fruit  de calculs scientifiques. II n'est reconnu aucune valeur juridique  particulière au contenu des données mises à disposition. Les auteurs  déclinent toute responsabilité concernant l'interprétation qui pourrait  en être faite.

------

**Outils**

L'écosystème d'outils utilisés pour  stocker, traiter et diffuser les données du projet MApUCE est composé uniquement de logiciels libres dont notamment la base de données spatiale [H2GIS](http://h2gis.org/). 

------

**Auteurs & Contact**

Groupe SIG de l'équipe [DECIDE](http://www.lab-sticc.fr/en/teams/m-570-decide.htm) du [Lab-STICC](http://www.lab-sticc.fr/en/index/) (CNRS UMR 6285).             

Pour toutes questions ou demandes d'informations complémentaires, veuillez envoyer un e-mail à "info" *arobase* "orbisgis.org"
