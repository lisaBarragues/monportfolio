---
title: "Catan"
order: 3
image: "catan.png"
---

Dans le cadre du premier semestre de ma L2 informatique, nous devions développer une version informatique complète de Catan en Java. Le projet devait proposer deux modes de jeu : une version textuelle entièrement jouable dans le terminal et une version graphique avec interface utilisateur. Il fallait implémenter les principales mécaniques du jeu : gestion des ressources, construction de routes, colonies et villes, échanges entre joueurs et ports, cartes développement, déplacement du voleur et conditions de victoire. Le projet demandait une véritable modélisation orientée objet ainsi qu’une réflexion sur l’architecture logicielle.

Ce projet a été l’un des plus marquants de mes débuts en programmation orientée objet. Il m’a confrontée pour la première fois à la modélisation d’un système complexe : le jeu de société Catan, avec son plateau, ses règles et ses nombreuses interactions entre les joueurs. Travailler sur ce projet m’a poussée à structurer ma réflexion, à collaborer efficacement et à persévérer malgré des difficultés techniques. Avec le recul, il a renforcé ma confiance dans ma capacité à mener un projet de développement conséquent.

Les objectifs étaient à la fois techniques et pédagogiques : implémenter fidèlement les règles du jeu, concevoir une architecture claire et maintenable, et développer une expérience de jeu cohérente dans les deux versions. Ce projet devait également nous permettre d’approfondir notre maîtrise de Java, de la programmation orientée objet et de la gestion de version avec GitLab.

Le projet s’est déroulé sur tout le semestre et a été réalisé en binôme dans le cadre d’un module dédié à la programmation orientée objet. Nous devions produire un programme fonctionnel ainsi qu’un rapport expliquant nos choix techniques et les difficultés rencontrées. La charge de travail était importante et devait être conciliée avec les autres matières.

Plusieurs enjeux accompagnaient ce projet. Sur le plan académique, il représentait une part importante de la note finale. Sur le plan technique, la richesse des mécaniques du jeu rendait le développement particulièrement ambitieux pour des étudiantes en début de L2. Il fallait concevoir une architecture solide, anticiper les interactions entre classes et gérer les nombreux cas particuliers liés aux règles du jeu. Les difficultés se manifestaient notamment par des bugs comme des null pointer ou des stack overflow. Enfin, l’enjeu humain était également important : maintenir une bonne communication et rester motivées tout au long du semestre.

Pour la modélisation du jeu, j’ai commencé par identifier les principales entités : tuiles, ressources, constructions, joueurs et plateau. J’ai conçu une classe Tuile avec plusieurs classes héritées selon le type de ressource, une classe Plateau représentée sous forme de matrice 2D, ainsi qu’une hiérarchie de classes pour les constructions (routes, colonies et villes). Des interfaces et classes abstraites ont également été utilisées pour structurer le modèle objet.

Nous avons ensuite développé progressivement les différentes fonctionnalités du jeu. Dans la version textuelle, cela incluait la gestion des ressources par joueur, le placement des constructions (route, ville etc..), les échanges entre joueurs et ports, un système de cartes développement ainsi qu’une intelligence artificielle simple. Dans la version graphique, nous avons modélisé le plateau avec des classes internes représentant les cases, routes et intersections. Les interactions se faisaient via des clics souris, et certaines actions utilisaient des fenêtres dédiées.

Certaines règles du jeu se sont révélées particulièrement complexes à implémenter. Par exemple, la construction de routes ou de colonies nécessitait de nombreuses vérifications pour respecter les règles du jeu. La gestion des cartes développement ou des bonus comme le plus long chemin demandait également une logique plus avancée. L’intelligence artificielle, basée sur des choix aléatoires, provoquait parfois des erreurs de type stack overflow, que nous avons corrigées en limitant le nombre de tentatives.

Une grande partie de la fin du semestre a été consacrée à la stabilisation du jeu et à la correction des bugs, notamment les erreurs de null pointer.

Le projet a été réalisé en binôme, avec une collaboration étroite tout au long du semestre. Nous organisions régulièrement des réunions pour discuter de l’architecture du programme, répartir les tâches et résoudre les problèmes techniques. Cette collaboration a été essentielle pour confronter nos idées, améliorer la conception du projet et maintenir un rythme de travail régulier.

Le résultat final a été très positif. Nous avons réussi à développer une version complète de Catan jouable à la fois en texte et en interface graphique, respectant les principales règles du jeu. Malgré la complexité du projet, nous avons livré un programme stable et fonctionnel. Cette réalisation a considérablement renforcé mes compétences en Java et en programmation orientée objet.

Ce projet m’a également permis de développer des compétences importantes en gestion de projet et en travail d’équipe. Sur le plan technique, j’ai approfondi ma maîtrise de Java, notamment l’utilisation de l’héritage, des interfaces et des classes internes. Sur le plan humain, il m’a appris à m’organiser sur la durée, à communiquer efficacement avec ma binôme et à résoudre des problèmes techniques de manière collaborative.
À court terme, ce projet m’a permis de gagner en confiance dans mes compétences en Java. À moyen terme, il a posé les bases de ma manière de concevoir des architectures logicielles et d’aborder les projets complexes. Aujourd’hui encore, cette expérience influence ma façon de développer : elle m’a appris à structurer mes projets, à anticiper les difficultés et à persévérer face aux obstacles techniques.
Avec le recul, ce projet a joué un rôle important dans mon parcours. Il m’a montré que j’étais capable de mener à bien un projet ambitieux et de progresser rapidement face à des défis techniques importants.

<h3>Compétences associées</h3>

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
