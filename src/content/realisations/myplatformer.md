---
title: "MyPlatformer"
#  inutile
order: 4
image: "myplatformer/myplatformer.png"
---

## Présentation du projet

**MyPlatformer** est un jeu de plateforme en 2D développé en **[Python](/competences/python)** sur mon temps personnel, en collaboration avec un ami. L’objectif était de créer un **jeu simple** mais **complet**, comprenant un personnage jouable, des mécaniques de saut et de déplacement, des plateformes, des ennemis et un système de collisions fonctionnel.
Contrairement à mes autres réalisations, ce projet n’était **ni académique ni professionnel**. Il s’agissait d’un **défi personnel** visant à approfondir mes compétences en **[Python](/competences/python)** et à apprendre à structurer un projet de jeu complet, de la conception jusqu’à un produit jouable. Cette réalisation m’a permis de **développer mon autonomie**, ma **rigueur** et ma capacité à mener un projet sur la durée sans contrainte extérieure.

## Objectifs, enjeux et risques

Le projet avait une **double ambition** : produire un jeu agréable et approfondir ma maîtrise de **[Python](/competences/python)** et de ses **bibliothèques**. Je souhaitais comprendre concrètement comment fonctionne un jeu avec la gestion des événements, la boucle de jeu, les collisions, l'architecture logicielle et l'organisation du code.

Le projet étant réalisé sur mon **temps personnel**, j'ai décidé de l'aborder comme un projet structuré afin de conserver une **progression régulière**. J'ai donc mis en place des réunions régulières, une définition d’objectifs techniques et un dépôt **[Git](/competences/git)** pour versionner le code.

Pour nous en tant que développeurs, les **enjeux** étaient multiples. Le premier était de maintenir la **motivation** sur un projet personnel sans échéance imposée. Il est en effet facile d’abandonner lorsque des difficultés techniques apparaissent. Nous devions donc faire preuve de **rigueur** et d’**organisation** afin de continuer à progresser. Le second enjeu concernait l’**apprentissage technique** : maîtriser les mécanismes internes d’un jeu 2D. Le risque principal était de s'éparpiller en voulant trop en faire.

Pour les **utilisateurs finaux**, dans mon cas, mes amis qui ont testé le jeu, l'enjeu était d'obtenir une **expérience de jeu fluide et agréable**, **sans bugs bloquants** ni **comportements incohérents** (traversée de plateformes, collisions erratiques). Un jeu injouable ou frustrant aurait rendu l'ensemble de mon travail peu gratifiant. Le **risque** pour eux était donc de se retrouver face à un jeu instable, ce qui nous a poussés à travailler avec sérieux la **robustesse des mécaniques de base** avant d'ajouter de nouvelles fonctionnalités.

## Les acteurs 

Mon ami et moi avons occupé un **double rôle** de **développeurs** et de **chefs de projet**. Nous avons partagé les responsabilités techniques et pris ensemble les décisions concernant l’**architecture du projet** et les **fonctionnalités à développer**. Des réunions régulières nous permettaient de discuter des choix techniques, d’organiser les prochaines étapes et de maintenir une vision commune du projet.

## Étapes de réalisation

Le développement a commencé par une **phase de recherche** sur les bibliothèques [Python](/competences/python) adaptées au développement de jeux 2D. Après comparaison de plusieurs solutions, j'ai choisi d’utiliser **Pygame**, qui permet de gérer le rendu graphique, les événements clavier et la boucle de jeu. Nous avons notamment utilisé `pygame.Rect` pour les collisions, `pygame.locals` pour la gestion des constantes clavier et `pygame.time.Clock` pour contrôler la fréquence d’exécution du jeu.

J'**ai structuré** le projet autour de **plusieurs modules** afin de garantir un code clair et maintenable : une classe `Player` pour le **personnage**, une classe `Platform` pour les **éléments du décor**, une classe `Enemy` pour les **ennemis**, ainsi qu’un **module principal** contenant la game loop.

J’ai principalement travaillé sur l’**implémentation du joueur** et des mécaniques principales du jeu. Cela incluait la **gestion des entrées clavier** via `pygame.event.get()` et `pygame.key.get_pressed()`, le **déplacement horizontal**, le système de saut basé sur une vitesse verticale, ainsi que la simulation d’une gravité appliquée à chaque frame.
La **gestion des collisions** constituait une partie **centrale** du projet. J’ai utilisé des rectangles (`pygame.Rect`) pour détecter les intersections entre le joueur et les plateformes. Afin d’éviter des comportements incohérents comme la traversée d’objets ou les blocages latéraux, j’ai **distingué** les collisions horizontales et verticales selon le vecteur de mouvement. Cette logique permettait de **repositionner correctement le joueur** sur une plateforme et de réinitialiser sa vitesse verticale lors d’un atterrissage.

<img style="float:center; margin: 0 0 1rem 1.5rem; height:500px; width:750px;" src="/images/realisations/myplatformer/myplatformer.gif" alt="myplatformer"/> 

J’ai également travaillé sur la **gestion des ennemis** et de **leurs comportements**. Une classe `Enemy` a été créée pour définir **différents types d’ennemis**, avec des déplacements **spécifiques** et des vitesses **différentes**. Chaque ennemi possède une hitbox, une vitesse et un état (vivant, blessé ou mort).

J’ai implémenté un **système d’états** permettant de gérer les interactions entre le joueur et les ennemis : détection des collisions, dégâts infligés au joueur, élimination d’un ennemi lorsqu’il est attaqué et changement d’état lors de sa mort. Lors des collisions, deux cas sont distingués : une collision latérale inflige des dégâts au joueur, tandis qu’une collision par le dessus (par exemple lorsqu’il saute sur un ennemi) permet de l’éliminer.

J’ai aussi développé un **système simple de gestion de vie** pour le joueur. Les points de vie sont représentés visuellement par des coeurs affichés à l’écran. Lorsqu’un ennemi touche le joueur, un coeur devient grisé. Lorsque la vie atteint zéro, le joueur passe dans un état « mort », ce qui déclenche la fin de partie. Tout cela est géré via des **variables** propre à l'objet `Joueur`.

Sur le **plan organisationnel**, nous avons utilisé **[Git](/competences/git)** pour versionner le code et travailler avec des branches afin de développer certaines fonctionnalités indépendamment. Une **feuille de route** nous a permis de structurer le développement : implémentation du déplacement, gestion des collisions, ajout des ennemis, puis amélioration de la jouabilité et de l’esthétique.

## Résultats

Le projet a abouti à un jeu de plateforme simple mais **pleinement fonctionnel**, avec des mécaniques cohérentes et une expérience utilisateur satisfaisante. 

Le résultat a été concluant **pour les utilisateurs**, les amis qui ont pu tester le jeu ont joué sans rencontrer de bugs. Les retours ont été positifs sur la fluidité des déplacements et le visuelle du jeu. Voir des personnes extérieures au projet prendre du plaisir à jouer a représenté une grande satisfaction personelle.

**Pour nous**, au-delà du jeu en lui-même, ce projet a été une réussite, j'ai acquéri une meilleure maîtrise de **[Python](/competences/python)** et de la librairie **Pygame**, une compréhension approfondie de l'architecture logicielle d'un jeu 2D, et la capacité à **mener un projet collaboratif jusqu'à sa fin**. 

## Les lendemains du projet

À court terme, ce projet m’a permis de consolider mes connaissances en **[Python](/competences/python)** et m'a montré que j'étais capable de m'engager dans un projet et m'y tenir. J'ai su allouer du temps et maintenir un effort régulier malgré les blocages techniques.

À moyen terme, **MyPlatformer** m’a appris à traiter un projet personnel avec la même rigueur qu'un projet académique. Cette discipline m'a ensuite servi dans mes projets suivants, où j'ai pu appliquer ces mêmes méthodes.

Aujourd’hui, cette réalisation représente pour moi la preuve que je suis capable de mener un projet technique jusqu’à son aboutissement par motivation personnelle. Il a également renforcé mon intérêt pour **[Python](/competences/python)**, un langage **très polyvalent** qui peut aussi bien être utilisé pour le développement de jeux que pour l'analyse de données ou l'entraînement de modèles d'intelligence artificielle.

## Mon regard critique

Ma principale valeur ajoutée sur ce projet a été la **conception** et l'**implémentation des mécaniques de jeu côté joueur** avec la gestion des entrées, la physique du saut et le système de collisions. J'ai dû **résoudre des problèmes concrets**, comme la distinction entre collisions horizontales et verticales, qui m'ont forcé à réfléchir à la **logique du programme plutôt qu'à simplement écrire du code**.

En revanche, avec le recul, nous aurions pu aller plus loin en ajoutant une **génération procédurale de niveaux**, ce qui nous aurait permis de proposer davantage de contenu sans avoir à concevoir chaque niveau manuellement.

Ce projet m'a également montré l'**importance des tests utilisateurs**. Les retours de nos amis ont permis d'identifier des problèmes que nous ne remarquions plus à force d'être plongés dans le code. Cette expérience m'a appris qu'impliquer des testeurs tôt dans le développement est **essentiel** et c'est quelque chose que je compte appliquer dans mes futurs projets.

<h3>Compétences associées</h3>

<div style="display:flex; gap:4rem; ">
  <div>

**Technique**
- **[Python](/competences/python)**
- **[Git](/competences/git)**

  </div>
  <div>

**Humaine**
- **[Rigueur](/competences/rigueur)**
- **[Autonomie](/competences/autonomie)**
- **[Organisation](/competences/organisation)**

  </div>
</div>