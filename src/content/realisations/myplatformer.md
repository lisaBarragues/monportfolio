---
title: "MyPlatformer"
#  inutile
order: 4
image: "myplatformer/myplatformer.png"
---

MyPlatformer est un jeu de plateforme en 2D développé en Python sur mon temps personnel, en collaboration avec un ami. L’objectif était de créer un jeu simple mais complet, comprenant un personnage jouable, des mécaniques de saut et de déplacement, des plateformes, des ennemis et un système de collisions fonctionnel.
Contrairement à mes autres réalisations, ce projet n’était ni académique ni professionnel. Il s’agissait d’un défi personnel visant à approfondir mes compétences en Python et à apprendre à structurer un projet de jeu complet, de la conception jusqu’à un produit jouable. Cette réalisation m’a permis de développer mon autonomie, ma rigueur et ma capacité à mener un projet sur la durée sans contrainte extérieure.

Le projet avait une double ambition : produire un jeu agréable et approfondir notre maîtrise de Python et de ses bibliothèques. Nous souhaitions comprendre concrètement comment fonctionne un jeu : gestion des événements, boucle de jeu, collisions, architecture logicielle et organisation du code.

Le projet étant réalisé sur notre temps afin de conserver une progression régulière, nous avons décidé de l’aborder comme un projet structuré : réunions régulières, définition d’objectifs techniques et utilisation d’un dépôt GitLab pour versionner le code.

L’un des principaux enjeux était de maintenir la motivation sur un projet personnel sans échéance imposée. Il est en effet facile d’abandonner lorsque des difficultés techniques apparaissent. Nous devions donc faire preuve de rigueur et d’organisation afin de continuer à progresser. L’autre enjeu concernait l’apprentissage technique : comprendre les mécanismes internes d’un jeu 2D, notamment la gestion de la boucle de jeu, des événements clavier, des collisions et de l’architecture générale.

Mon ami et moi avons occupé un double rôle de développeurs et de chefs de projet. Nous avons partagé les responsabilités techniques et pris ensemble les décisions concernant l’architecture du projet et les fonctionnalités à développer. Des réunions régulières nous permettaient de discuter des choix techniques, d’organiser les prochaines étapes et de maintenir une vision commune du projet.

<img style="float:right; margin: 0 0 1rem 1.5rem; height:500px; width:750px;" src="/images/realisations/myplatformer/myplatformer.gif" alt="myplatformer"/>

Le développement a commencé par une phase de recherche sur les bibliothèques Python adaptées au développement de jeux 2D. Après comparaison de plusieurs solutions, nous avons choisi d’utiliser Pygame, qui permet de gérer le rendu graphique, les événements clavier et la boucle de jeu. Nous avons notamment utilisé pygame.Rect pour les collisions, pygame.locals pour la gestion des constantes clavier et pygame.time.Clock pour contrôler la fréquence d’exécution du jeu.

Nous avons structuré le projet autour de plusieurs modules afin de garantir un code clair et maintenable : une classe Player pour le personnage, une classe Platform pour les éléments du décor, une classe Enemy pour les ennemis, ainsi qu’un module principal contenant la game loop.

J’ai principalement travaillé sur l’implémentation du joueur et des mécaniques principales du jeu. Cela incluait la gestion des entrées clavier via pygame.event.get() et pygame.key.get_pressed(), le déplacement horizontal, le système de saut basé sur une vitesse verticale, ainsi que la simulation d’une gravité appliquée à chaque frame.
La gestion des collisions constituait une partie centrale du projet. J’ai utilisé des rectangles (pygame.Rect) pour détecter les intersections entre le joueur et les plateformes. Afin d’éviter des comportements incohérents comme la traversée d’objets ou les blocages latéraux, j’ai distingué les collisions horizontales et verticales selon le vecteur de mouvement. Cette logique permettait de repositionner correctement le joueur sur une plateforme et de réinitialiser sa vitesse verticale lors d’un atterrissage.

J’ai également travaillé sur la gestion des ennemis et de leurs comportements. Une classe Enemy a été créée pour définir différents types d’ennemis, avec des déplacements spécifiques et des vitesses différentes. Chaque ennemi possède une hitbox, une vitesse et un état (vivant, blessé ou mort).

J’ai implémenté un système d’états permettant de gérer les interactions entre le joueur et les ennemis : détection des collisions, dégâts infligés au joueur, élimination d’un ennemi lorsqu’il est attaqué et changement d’état lors de sa mort. Lors des collisions, deux cas sont distingués : une collision latérale inflige des dégâts au joueur, tandis qu’une collision par le dessus (par exemple lorsqu’il saute sur un ennemi) permet de l’éliminer.

J’ai également développé un système simple de gestion de vie pour le joueur. Les points de vie sont représentés visuellement par des coeurs affichés à l’écran. Lorsqu’un ennemi touche le joueur, un coeur devient grisé. Lorsque la vie atteint zéro, le joueur passe dans un état « mort », ce qui déclenche la fin de partie.

Sur le plan organisationnel, nous avons utilisé GitLab pour versionner le projet et travailler avec des branches afin de développer certaines fonctionnalités indépendamment. Une feuille de route progressive nous a permis de structurer le développement : implémentation du déplacement, gestion des collisions, ajout des ennemis, puis amélioration de la jouabilité et de l’esthétique.

Le projet a abouti à un jeu de plateforme simple mais fonctionnel, avec des mécaniques cohérentes et une expérience utilisateur satisfaisante. Nous avons pu faire tester le jeu à nos amis, ce qui a constitué une grande satisfaction personnelle. Au-delà du résultat, ce projet m’a permis de développer mes compétences en Python, en architecture logicielle et en gestion de projet collaboratif.

Sur le plan humain, cette réalisation a renforcé mon organisation, ma rigueur et mon autonomie. Sur un projet personnel, rien n’oblige à continuer : il faut donc savoir s’auto-discipliner et maintenir un effort régulier malgré les blocages techniques.
À court terme, ce projet m’a permis de mieux comprendre les bases du développement de jeux et de gagner en confiance en Python. À moyen terme, il m’a appris à structurer mes projets personnels avec la même rigueur qu’un projet académique ou professionnel. Aujourd’hui, MyPlatformer représente pour moi la preuve que je suis capable de mener un projet technique jusqu’à son aboutissement par motivation personnelle, et il a renforcé mon intérêt pour le développement de jeux.


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