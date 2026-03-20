---
title: "Doodle Jump"
order: 1
image: "doodlejump/doodlejump.png"
---
<div style="clear:both;"></div>
<img style="float:left; margin: 0 1.5rem 1rem 0;" src="/images/realisations/doodlejump/doodlejump.gif" alt="gif-doodlejump"/>

Lors de ma L3 d’informatique générale à l’Université Paris Cité, j’ai participé à la réalisation d’un jeu en Java inspiré de Doodle Jump en équipe de cinq. L’objectif était de développer une version personnalisée du jeu tout en respectant les bonnes pratiques de développement : structuration du code, utilisation de design patterns et gestion de version avec Git.

Ce projet s’inscrivait dans un contexte académique exigeant, avec une évaluation individuelle et collective sur un semestre. Les enjeux étaient multiples : réussir à produire un jeu fonctionnel et complet, acquérir des compétences techniques durables, et collaborer efficacement en équipe. Les principaux risques concernaient la gestion du temps, la cohérence de l’architecture et les bugs en fin de développement. Nous avons su les anticiper grâce à une organisation rigoureuse, une communication régulière et une utilisation structurée de Git.

Le projet a été mené ehn suivant la méthode agile avec des réunions hebdomadaires encadrées par une enseignante. Nous échangions sur l’avancement, répartissions les tâches et ajustions nos choix techniques. Nous avons également mis en place un canal de communication dédié pour faciliter les échanges entre les réunions. Cette organisation m'a permis de développer ma capacité à exprimer mes idées, à écouter celles des autres et à collaborer de manière constructive.

Sur le plan technique, le projet reposait sur une architecture de type MVC (Modèle-Vue-Controller), avec une séparation claire entre la logique métier, les vues (menu, jeu, paramètres) et le contrôleur gérant les interactions clavier. J'ai été chargée dès le départ de poser les fondations du projet en réalisant le premier commit : mise en place de la structure des classes principales et première interface graphique avec un menu de démarrage.

J'ai ensuite implémenté plusieurs fonctionnalités clés. J'ai conçu un système de badges original, reposant sur des compteurs intégrés dans la classe Joueur (ennemis vaincus, bonus utilisés, score atteint) et une logique de déblocage dynamique affichant visuellement les succès gagnés ou encore verrouillés, afin de renforcer la rejouabilité. J'ai également travaillé sur la gestion des collisions entre le joueur, les plateformes et les ennemis, en distinguant les différents types d'interactions (rebond, chute, élimination), ainsi que sur l'intégration des entités du jeu comme les plateformes mouvantes, les ressorts et les fusées.

<img style="float:right; margin: 0 0 1rem 1.5rem; height:500px; width:520px;" src="/images/realisations/doodlejump/badge.png" alt="gif-doodlejump"/>

Pour la gestion du son, j'ai apporté mon aide à un membre de l'équipe qui rencontrait des difficultés. Nous avons ainsi travaillé ensemble pour implémenter la fonctionnalité. Nous avons développé deux classes dédiées, Son et VisualPlayer, permettant la lecture, la mise en pause et l'arrêt des sons. J'ai sélectionné les effets sonores à partir de banques libres de droit et intégré des bruitages contextuels (ressort, fusée…), ainsi qu'un contrôle de la musique dans le menu des paramètres.

Enfin, nous avons mis en place un système de persistance des données via une base SQLite : une classe de connexion permettait d'enregistrer et de récupérer les informations du joueur (score, pseudonyme, progression), assurant une continuité entre les parties. Tout au long du projet, j'ai également assuré une gestion régulière du dépôt Git : gestion de branches, résolution de conflits et revue de code entre membres.

Le projet a abouti à un jeu complet et fonctionnel, intégrant les principales mécaniques de Doodle Jump. Les résultats ont été très positifs, tant sur le plan technique (maîtrise de Java, compréhension d’une architecture logicielle, utilisation de SQL) que sur le plan humain (organisation, communication, travail en équipe).

À court terme, ce projet m'a permis d'être plus à l'aise pour aborder d'autres projets en Java, mais aussi de gagner en confiance dans la communication au sein d'un groupe : je suis désormais plus à l'aise pour donner mon avis, proposer des idées et échanger constructivement. À moyen et long terme, il m'a servi de base solide pour mon alternance, où je retrouve des problématiques similaires de structuration de projet, de collaboration et de prise de décision technique. Si le projet devait être poursuivi, je chercherais à améliorer la modularité de certaines fonctionnalités et à fluidifier la jouabilité du jeu.

Avec le recul, cette réalisation m’a appris l’importance d’une architecture bien pensée dès le départ, d’une communication régulière et d’un développement progressif accompagné de tests fréquents. J'ai également compris la valeur de la documentation, que nous avons parfois négligée sous la pression des délais. Ce sont des habitudes que j'applique aujourd'hui dans tous mes projets. Ma valeur ajoutée sur ce projet réside à la fois dans l'initiative technique en posant les fondations et en proposant des fonctionnalités originales comme le système de badges et dans ma contribution humaine, en aidant proactivement mes coéquipiers et en maintenant une dynamique de groupe positive tout au long du semestre. Ces enseignements influencent aujourd’hui ma manière de travailler et ma façon d’aborder de nouveaux projets.

<h3>Compétences associées</h3>

<div style="display:flex; gap:4rem;">
  <div>

**Technique**
- **[Java](/competences/java)**
- **[Git](/competences/git)**
- **[SQL](/competences/sql)**

  </div>
  <div>

**Humaine**
- **[Communication](/competences/)**
- **[Organisation](/competences/organisation)**
- **[Adaptabilité](/competences/adaptabilité)**
- **[Esprit d'équipe](/competences/esprit-equipe)**
  </div>
</div>
