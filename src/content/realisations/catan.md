---
title: "Catan"
order: 3
image: "catan/catan.png"
---

## Présentation du projet

Dans le cadre du premier semestre de ma L2 informatique, j'ai développé une version jouable du jeu de société **Catan** en **[Java](/competences/java)**. Le projet devait proposer **deux modes de jeu** : une **version textuelle** dans le terminal et une **version graphique** avec une interface utilisateur. 
<img style="float:right; margin: 0 0 0 1.5rem;border-radius: 8px; height:400px; width:500px;" src="/images/realisations/catan/boardgame.jpg" alt="boardgame"/>

Il fallait implémenter les principales mécaniques du jeu : gestion des ressources, construction de routes, colonies et villes, échanges entre joueurs et ports, cartes développement, déplacement du voleur et conditions de victoire. Ce projet demandait une véritable **modélisation orientée objet** ainsi qu’une réflexion sur l’**architecture logicielle**.


Ce projet a marqué mes débuts en **programmation orientée objet (POO)**. Il m’a confrontée pour la première fois à la **modélisation** d’un système complexe : le jeu **Catan**, avec son plateau, et ses nombreuses règles. Travailler sur ce projet m’a poussée à structurer ma réflexion, à collaborer efficacement et à persévérer malgré des difficultés techniques. Avec le recul, il a renforcé ma confiance dans ma capacité à mener un projet de développement conséquent.
## Objectifs, enjeux et risques

Les objectifs étaient à la fois **techniques** et **pédagogiques** : implémenter fidèlement les règles du jeu, concevoir une **architecture claire et maintenable**, et développer une expérience de jeu cohérente dans les deux versions. Ce projet devait également me permettre d'approfondir ma maîtrise de **[Java](/competences/java)**, de la **POO** et de la gestion de version avec **[Git](/competences/git)**.
Il s’est déroulé sur tout le semestre dans le cadre d’un module dédié à la POO, avec une charge de travail importante à concilier avec les autres matières.

Plusieurs enjeux accompagnaient ce projet. Pour l'enseignant, le livrable devait démontrer une maîtrise réelle des concepts de la **POO** (**héritage**, **interfaces**, **encapsulation**) et une **architecture cohérente**, un programme fonctionnel mais mal structuré n'aurait pas répondu aux attentes pédagogiques. Pour moi, il représentait une part importante de la note finale, mais aussi un premier **vrai défi de développement**. Le principal **risque technique** résidait dans la modélisation, en effet une mauvaise conception en amont pouvait rendre le code rapidement ingérable, provoquer des erreurs en cascade et compromettre la livraison du projet dans son ensemble.

## Étapes de réalisation

### Modélisation et architecture

J'ai débuté le projet par une phase d'**analyse fonctionnelle** des règles du jeu, visant à **identifier les entités** et **leurs relations**, cela a permis de définir une **hiérarchie de classes**. Pour les tuiles (du plateau), j'ai créé une **classe abstraite** `Tuile` **étendue** par des **sous-classes** typées selon la ressource produite (`TuileForet`, `TuileMontagne`, `TuileChamp`, etc.) et une `TuileDesert` sans production (de ressources). 
Le plateau est constitué d'un ensemble de tuiles, chaque tuile a un **nom**, un **numéro** et un **tableau de quatre** `Arete`  représentant ses côtés, c'est-à-dire les emplacements où les constructions peuvent être posées.
Pour les **constructions**, j'ai défini une **classe abstraite** `Construction` dont héritaient `Route`, `Colonie` et `Ville`, chacune **encapsulant** sa propre logique de validation de placement et de calcul de coût. Des **interfaces** ont structuré les comportements partagés, notamment pour les entités participant au cycle de production et de consommation de ressources.


### Implémentation de la version textuelle

J'ai choisi de prioriser la version jouable dans le terminal avant d'aborder l'interface graphique, afin de valider la **logique métier** indépendamment de la présentation visuelle.
Cette version englobait l'**ensemble du cycle du jeu**, c'est-à-dire la distribution des ressources au lancer de dé, le placement des constructions avec vérification des contraintes d'adjacence, les échanges maritimes et entre joueurs, l'activation des cartes développement et leurs effets, ainsi qu'une **IA** basique basée sur des choix aléatoires. Ce dernier point a généré un **bug significatif**, des erreurs de types `stack overflow` causées par les tentatives **répétées** d'action invalide de l'IA. Pour remédier à ce souci, j'ai ajouté un **compteur de tentatives**. Au-delà d'un certain seuil, plutôt que de laisser l'IA tourner indéfiniment, je recherchais automatiquement un coup valide parmi les actions disponibles et le jouais à sa place, avant de passer au joueur suivant.

### Implémentation de la version graphique

La **version graphique** a été construite en surcouche de la **logique métier** existante. J'ai modélisé le plateau (tuiles carrés, intersections et routes) avec des **classes internes** représentant chaque entité graphique. La gestion des interactions reposait sur des écouteurs d'événements souris (`MouseListener`), et les actions nécessitant un choix de la part du joueur, comme la sélection d'une ressource lors d'un échange ou la désignation de la case voleur s'affichaient dans des **boîtes de dialogue** dédiées.
<img style="float:left; margin: 1rem 1.5rem 1rem 0;border-radius: 8px; height:490px; width:690px;" src="/images/realisations/catan/catangameplay.png" alt="catangameplay"/>

À l'approche de la date de rendu, je me suis consacrée à la **stabilisation du jeu** et à la **correction des bugs**, notamment des `NullPointerException` dues à une mauvaise initialisation de certaines variables lors de séquences d'actions peu fréquentes. 


Certaines règles du jeu se sont révélées particulièrement **complexes** à implémenter. Par exemple, la construction de routes ou de colonies nécessitait de nombreuses vérifications d'adjacence pour respecter les règles du jeu. La gestion des cartes développement et des bonus comme le **plus long chemin** demandait également une logique plus avancée, notamment un **algorithme de parcours** de routes pour en déterminer le détenteur à chaque tour.

## Les acteurs

Plusieurs personnes ont joué un rôle dans ce projet. L'**enseignant** responsable du module fixait le cahier des charges et était disponible pour répondre aux questions techniques pendant les travaux pratiques. Ses retours m'ont parfois poussée à revoir certains choix d'architecture que je pensais bons au départ.
Ma **binôme** était évidemment l'actrice centrale au quotidien. Nous organisions régulièrement des réunions pour **discuter de l’architecture**, **se répartir les tâches** et **résoudre les problèmes techniques** ensemble. Cette **collaboration** a été **essentielle** pour confronter nos idées, améliorer la conception du projet et maintenir un rythme de travail constant.

## Résultats

Le résultat final a été **très positif**. Le projet répondait aux exigences du cahier des charges, une version complète de **Catan** jouable à la fois dans le terminal et dans interface une graphique, respectant les règles du jeu, accompagnée d'un **rapport de conception** documentant les choix techniques retenus. 

Pour l'enseignant, ce projet constituait avant tout une preuve de maîtrise des concepts vus en cours. Le projet démontrait une **application concrète** des principes de la **POO** et le rapport de conception témoignait également d'une **capacité à justifier nos choix techniques**, compétence tout aussi importante dans le cadre de l'évaluation.

Pour moi, cette réalisation a considérablement renforcé mes notions en **[Java](/competences/java)** et m'a également permis de développer des compétences importantes en **gestion de projet** et en **[travail d'équipe](/competences/esprit-equipe)**. Sur le plan technique, j'ai approfondi ma maîtrise de **Java**, notamment l'utilisation de l'**héritage**, des **interfaces** et des **classes internes**. Sur le plan humain, elle m'a appris à m'**[organiser](/competences/organisation)** sur la durée, à **[communiquer](/competences/communication)** efficacement avec ma binôme et à résoudre des problèmes techniques de manière collaborative.

## Les lendemains du projet

À court terme, ce projet m'a permis de gagner en confiance dans mes compétences en **[Java](/competences/java)** et d'aborder les projets suivants avec une **méthodologie** solide. 
À moyen terme, il a beaucoup influencé ma manière de concevoir une **architecture logicielle** et d'aborder les **projets complexes**. En effet, il est préférable d'identifier les règles métiers,  modéliser les entités et leurs relations avant d'implémenter. C'est un principe que j'ai appliqué sur ce projet et qui m'a servi lorsque j'ai abordé les **patterns de conception** dans les semestres suivants.
Aujourd'hui encore, cette expérience influence ma façon de développer, elle m'a appris à structurer mes projets, à anticiper les difficultés et à persévérer face aux obstacles techniques.
Avec le recul, ce projet a joué un rôle important dans mon parcours. Il m’a montré que j’étais capable de mener à bien un projet ambitieux et de progresser rapidement face à des défis techniques.

## Mon regard critique
En relisant ce projet aujourd'hui, je vois clairement ce que j'aurais fait différemment. La modélisation du plateau via des tableaux d'`Arete` était fonctionnelle, mais les relations de voisinage entre tuiles sont devenues compliquées à gérer au fur et à mesure, notamment pour implémenter le calcul du **plus long chemin**. Une structure en **graphe** aurait été plus adaptée.
L'IA est fonctionnelle mais ce n'est pas agréable de jouer avec, j'aurais aimé avoir le temps de développer une **vraie intelligence artificielle**.
Et surtout, j'ai testé manuellement tout au long du projet, mettre en place des **tests unitaires** sur les règles métier dès le début aurait rendu la détection des bugs plus rapide.

## Compétences associées

<div style="display:flex; gap:4rem;">
  <div>

**Technique**
- **[Java](/competences/java)**
- **[Git](/competences/git)**

  </div>
  <div>

**Humaine**
- **[Organisation](/competences/organisation)**
- **[Esprit d'équipe](/competences/esprit-equipe)**
- **[Communication](/competences/communication)**
- **[Autonomie](/competences/autonomie)**
  </div>
</div>
