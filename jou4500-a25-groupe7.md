**7 novembre 2025**<br>
**CMN4500/JOU4500 Journalisme numérique II**<br>
**Alice Rosange Mbela Ebele, Catherine Brideau, Mackenzie Moffatt**<br>
**Présenté à Jean-Sébastien Marier**<br>

# Analyse exploratoire de données (AED) et proposition

## Avant-propos

Ce projet s’appuie sur le jeu de données « Questionnaire détaillé du recensement de 2021 – Données par quartier » publié par la Ville d’Ottawa. En analysant ces données, l’objectif est d’explorer (...) des quartiers d’Ottawa afin de mieux comprendre les dynamiques locales. Cette analyse exploratoire servira à analyser les données en profondeur pour le projet final.

**Voici quelques ressources utiles pour ce travail :**

* [Page *Syntaxe de base pour l’écriture et la mise en forme* de GitHub](https://docs.github.com/fr/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [Le répertoire modèle pour ce projet au cas où vous effaceriez quelque chose par accident](https://github.com/jsmarier/jou4100_jou4500_mpad2003_project2_template)

Avez-vous remarqué comment créer un hyperlien? En langage Markdown, on met le texte cliquable entre une paire de crochets et l'adresse URL entre parenthèses.

Pour créer une liste non ordonnée, il suffit de mettre une étoile (`*`) devant chaque item.

## 1. Introduction

Le projet s’appuie sur les données du recensement 2021 pour Ottawa, compilées par Statistique Canada. Elles incluent des variables clés telles que l’âge, le revenu, les langues, le statut matrimonial, le logement et l’emploi. Les données ont été nettoyées et structurées afin de permettre une analyse comparative entre les quartiers riches et défavorisés d’Ottawa. Les différentes sections de ce travail sont les suivantes: l’obtention des données suivi par la compréhension de celles-ci, une analyse VIMA, le nettoyage des données par l’entremise des outils de Google Feuille de Calcul, le logiciel OpenRefine, etc., Analyse exploratoire des données (AED) et finalement la possibilité d’un récit potentiel et/ou un angle pour la suite du travail.

* [Lien vers le jeu de données original sur Ottawa ouverte](https://ouverte.ottawa.ca/datasets/ottawa::questionnaire-d%C3%A9taill%C3%A9-du-recensement-de-2021-donn%C3%A9es-par-quartier/about)
* [Lien vers la version CSV sur du portail GitHub du prof](https://raw.githubusercontent.com/jsmarier/files-for-course-assignments/refs/heads/main/Questionnaire_d%C3%A9taill%C3%A9_du_recensement_de_2021_Donn%C3%A9es_par_quartier.csv)

## 2. Obtenir les données

![](capture_initiale.png)<br>
###### *Figure 1 : La capture d'écran Intiale lors de l'importation du Jeu de Données dans Excel.*

Pour importer les données dans Google Feuille de Calcul, nous avons commencé par télécharger le fichier CSV dans mon ordinateur. Prochainement, nous avons été dans Google Feuille de calcul et créé une nouvelle feuille de calcul. Nous avons continué par cliquer sur fichier et importé le fichier CSV.

#### Nombre de Colonnes:
Il y a 26 colonnes dans le jeu de données.
Il y a 2248 lignes dans le jeu de données. (Incluant la ligne de titres)

#### Est-ce que les données semblent-elles propres?
À première vue, l’alignement de certaines cases est à droite au lieu d’être à gauche. Il y a quelques espaces avant certains mots. Par exemple, sur le ligne 532 (langues autochtones). Un manque de majuscules pour certains mots dans la colonne caractéristiques. Par exemple, sur la ligne 2, le mot taux n’a pas de majuscule, alors qu’il l’est plus loin dans le jeu de données.

###### Colonne A
Dans la colonne A, les données sont nominales. Ces données nominales représentent des catégories représentatives sur les quartiers. Par exemple, le total de groupes d’âge de la population et en dessous, chaque groupes d’âge individuel séparés. 

###### Colonne B
Dans la colonne B, les données sont numériques. Ce sont des nombres qu’on peut additionner ou soustraire, ou pour des comparaisons pour des calculs statistiques.

###### Colonne C
Dans la colonne C jusqu'à la fin, ce sont des données quantitatives discrètes parce qu’on compte des individus et parce que des comptages de personnes ne peuvent pas prendre une infinité de valeurs.

##### Angle Potentiel
Comparer les revenus moyens entre les quartiers riches et défavorisés.

##### Question ou hypothèse
Pourquoi certains quartiers d’Ottawa ont un salaire plus élevé que d’autres?




Utilisez deux croisillons (`##`) pour créer un intertitre de niveau 2 comme celui-ci.

Utilisez le modèle de code ci-dessous pour insérer une capture d'écran. Vos images doivent être sauvegardées dans le même dossier que votre fichier `.md`.

![]()<br>
*Figure 1 : La fenêtre d'importation d'un fichier de Google Feuilles de calcul.*

**Voici quelques exemples de fonctions et de lignes de code mises dans des boîtes grises :**

1. Si vous nommez une fonction, mettez là à l'intérieur de guillemets « inclinés » comme ceci : `IMPORTHTML`.
1. Si vous voulez inclure une ligne de code complète, faites la même chose, mais avec tout le code : `=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)`.
1. Alternativement, vous pouvez mettre le code dans une boîte indépendante en utilisant le modèle de code ci-dessous :

``` r
=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)
```
C'est aussi comme ça qu'on crée une liste ordonnée. Il suffit de mettre `1.` devant chaque item.

## 3. Comprendre les données

### 3.1. Analyse VIMA

La colonne C, soit celle du quartier Orléans Est-Cumberland, ne présente aucune donnée invalides. À première vue, pour donner un exemple, le Total - Répartition (%) de la population par grands groupes d'âge - Données-échantillon (25 %), équivaut à 100%. Chaque colonne vis à vis cette rangée présente la même chose. Ensuite, aucune des rangées dans la colonne C ne comporte des données vides (à part, pour les gens âgés de 100 et plus pour ce quartier en particulier, mais qui ne me semble pas impossible) ou bien la rangée 29 à 32 de cette colonne (soit le pourcentage divisé du Total - Répartition (%) de la population par grands groupes d'âge - Données-échantillon (25 %)), qui est bel et bien divisé pour avoir un total de 100%. Il n’y a pas de valeurs manquantes dans cette colonne. Finalement, je ne vois pas de données aberrantes. 

Appuyez vos affirmations en citant les sources appropriées. Veuillez suivre les [normes APA en matière d'attribution dans le corps du texte](https://apastyle.apa.org/style-grammar-guidelines/citations).

**Par exemple :**

Comme l'affirme Cairo (2016), une visualisation de données doit être véridique...

### 3.2. Nettoyage des données

Insérez votre texte ici.

### 3.3. Analyse exploratoire des données (AED)

Insérez votre texte ici.

**Cette section doit inclure une capture d'écran de votre tableau croisé dynamique, comme ceci :**

![](pivot-table-screen-capture.png)<br>
*Figure 2 : Ce tableau croisé dynamique montre...*

**Cette section doit aussi inclure une capture d'écran de votre graphique exploratoire, comme ceci :**

![](chart-screen-capture.png)<br>
*Figure 3 : Ce graphique exploratoire montre...*

## 4. Récit potentiel

Insérez votre texte ici.

## 5. Conclusion

Insérez votre texte ici.

## 6. Références

Veuillez inclure une liste de vos références ici. Assurez-vous de suivre les [normes APA pour les références](https://apastyle.apa.org/style-grammar-guidelines/references). Les retraits négatifs (*hanging paragraphs*) ne sont pas nécessaires. Le [guide sur l'adaptation APA](https://arts.uottawa.ca/lettres/sites/arts.uottawa.ca.lettres/files/cartu-outils-de-redaction-adaptation-apa.pdf) de l'Université d'Ottawa pourrait également vous être utile.

**Voici un exemple :**

Bounegru, L., & Gray, J. (Eds.). (2021). *The Data Journalism Handbook 2: Towards A Critical Data Practice*. Amsterdam University Press. [https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153](https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153)
