---
title: "Doodle Jump"
order: 1
image: "doodlejump/doodlejump.png"
---

## Présentation du projet

Lors de ma L3 d’informatique générale à l’<a href="https://u-paris.fr" target="_blank">Université Paris Cité</a>, j’ai participé à la réalisation d’un jeu en **Java** inspiré de **Doodle Jump** en équipe de cinq. L’objectif était de **développer une version personnalisée du jeu** tout en respectant les bonnes pratiques de développement : structuration du code, utilisation de **design patterns** et gestion de version avec **[Git](/competences/git)**.

<img style="float:left; margin: 0 1.5rem 1rem 0; border-radius: 8px" src="/images/realisations/doodlejump/doodlejump.gif" alt="gif-doodlejump"/>

## Objectifs, enjeux et risques

Ce projet s’inscrivait dans un **contexte académique exigeant**, avec une évaluation à la fois **individuelle** et **collective**. 
L'objectif technique était de **produire un jeu fonctionnel**, jouable et bien structuré, en **appliquant les concepts vus en cours**. Mais aussi de démontrer une capacité à **[travailler en équipe](/competences/esprit-equipe)** pendant un semestre entier. 

Le principal enjeu pour moi était de réussir à m'**intégrer efficacement** dans une équipe de cinq. Il fallait aligner les visions techniques, éviter les incohérences entre les parties développées séparément et rester force de proposition sans empiéter sur le travail des autres. C'était ma première expérience de développement dans une équipe aussi grande.

Plusieurs **risques** existaient, le premier était la **coordination**, cinq personnes travaillant en parallèle sur une même base de code augmentent les risques de conflits Git, de duplications ou d'incompatibilités de code. Un autre risque était le potentiel **déséquilibre** dans la **contribution** des membres, certains plus à l'aise techniquement pouvaient prendre plus de tâches et laisser d'autres en retrait, impactant la **cohésion du groupe**.

## Étapes de réalisation

Le projet a été mené en suivant la **méthode agile** avec des **réunions hebdomadaires** encadrées par une enseignante. Ces points réguliers nous permettaient d'**échanger sur l’avancement**, de nous **répartir** les tâches et d'**ajuster** nos choix techniques. J'ai également mis en place un **canal de communication** dédié pour **faciliter les échanges** en dehors des réunions. Cette **[organisation](/competences/organisation)** m'a permis de développer ma **capacité à exprimer mes idées**, à écouter celles des autres et à collaborer de manière constructive.

### Mise en place du projet

J'ai été chargée dès le départ de poser les **fondations du projet** en réalisant le **premier commit**, il incluait la mise en place de la **structure des classes principales**, l'organisation des packages et le développement de la **première interface graphique** avec un **menu de démarrage**.  Ce rôle m'a demandé de faire des **choix** d'architecture décisifs notamment la séparation entre la logique métier, les vues (menu, jeu, paramètres) et le contrôleur gérant les interactions clavier.

<img style="float:right; margin: 0 0 1rem 1.5rem; border-radius: 10px;height:500px; width:520px;" src="/images/realisations/doodlejump/badge.png" alt="gif-doodlejump"/>

### Gestion des collisions

J'ai travaillé sur la **gestion des collisions** entre le joueur, les plateformes et les ennemis. Cela impliquait de distinguer **plusieurs types d'interactions** comme le rebond sur une plateforme, la chute en cas de contact avec un ennemi, ou encore l'élimination d'un ennemi par un saut. Pour cette partie, j'ai beaucoup travaillé sur la **précision des hitboxes** et l'**ordre de traitement** des événements dans la boucle de jeu, pour éviter des comportements incohérents.
J'ai également participé à l'intégration de plusieurs entités : les **plateformes mouvantes**, les **ressorts** et les **fusées**, chacune avec des comportements et des effets distincts sur le joueur. J'ai fait en sorte que leur implémentation reste cohérente avec l'architecture **MVC** (Modèle, Vue, Controleur) déjà en place.

### Contribution à la gestion du son

Pour la **gestion du son**, j'ai apporté mon **[aide](/competences/esprit-equipe)** à un membre de l'équipe qui rencontrait des difficultés. Nous avons ainsi travaillé **ensemble** pour implémenter la fonctionnalité. Nous avons développé deux classes dédiées, `Son` et `VisualPlayer`, permettant la lecture et la mise en pause des sons. J'ai sélectionné les effets sonores à partir de banques libres de droit et **intégré des bruitages contextuels** (ressort, fusée), ainsi qu'un contrôle de la musique dans le menu des paramètres.

### Système de badge

J'ai aussi conçu un **système de badges** original, reposant sur des **compteurs** intégrés dans la classe `Joueur` (ennemis vaincus, bonus utilisés, score atteint) et une logique de **déblocage dynamique** affichant visuellement les succès obtenus ou encore verrouillés. L'objectif était de renforcer la **rejouabilité** du jeu en donnant au joueur des objectifs à long terme. Pour que ce système soit vraiment utile, il fallait que la progression du joueur soit sauvegardée entre les parties. J'ai donc mis en place une **persistance des données** via une base **[SQLite](/competences/sql)** : une classe de connexion permettait d'enregistrer et de récupérer les informations du joueur (score, nom, badges débloqués), assurant une **continuité** entre les parties.

## Les acteurs 

L'enseignante encadrant le module fixait le **cadre du projet** et **animait** les réunions hebdomadaires.
Les **quatre membres de l'équipe** étaient les autres acteurs de cette réalistion. Chacun avait ses **points forts**, et j'ai essayé de m'**[adapter](/competences/adaptabilité) aux profils de chacun**, que ce soit pour **expliquer** un choix d'architecture, **débloquer** un problème technique ou maintenir une ambiance positive au sein de l'équipe. J'ai notamment pris l'initiative d'**[aider](/competences/esprit-equipe) proactivement** les membres en difficulté.

## Résultats

Le projet a abouti à un **jeu complet** et **fonctionnel**, intégrant les principales mécaniques de Doodle Jump. Pour l'enseignante, le projet **répondait aux attentes du cours** et pour mes camarades, avoir posé une architecture claire dès le départ **a facilité l'intégration** de chacun dans le projet. De manière générale, le **[travail en équipe](/competences/esprit-equipe)** s'est bien passé et chacun a pu contribuer à sa façon.

Cette réalisation a consolidé mes compétences en **[Java](/competences/java)** et en **conception logicielle**, et m'a permis de progresser sur des aspects que je maîtrisais moins comme la **gestion de conflits [Git](/competences/git)** à plusieurs, **intégrer du son** dans un développement ou encore penser à une fonctionnalité d'un **point de vue du joueur** plutôt que d'un point de vue uniquement technique. 

## Les lendemains du projet

À court terme, ce projet m'a surtout appris à mieux **travailler en groupe**, et m'a encouragé à davantage **proposer mes idées**. J'ai également beaucoup progressé en **[Java](/competences/java)**, cette réalisation m'a donné l'occasion de développer des fonctionnalités encore jamais vu. 

À moyen terme, il m'a servi de **base solide** pour mon alternance, où je retrouve des problématiques similaires de **structuration de projet**, de **collaboration** et de **prise de décision technique**. 

Si le projet devait être poursuivi, je chercherais à améliorer la **modularité** de certaines fonctionnalités et à **fluidifier** la jouabilité du jeu, en effet il reste un peu lent et contient encore quelques bugs.

## Mon regard critique

Avec le recul, ce projet m’a vraiment appris l’importance de partir sur une **base claire** dès le début. Nous avons vu que certains choix faits rapidement pouvaient compliquer la suite du développement, notamment quand il fallait ajouter de nouvelles fonctionnalités. J’ai aussi pris conscience qu'échanger **régulièrement** permet d’éviter les incompréhensions et de se tenir au courant sur l'avancement de chacun. Enfin, travailler sur des **tâches spécifiques** avec des objectifs simples m’a permis de **mieux développer** et d’éviter l'accumulation d'erreurs difficiles à corriger.

Ma **valeur ajoutée** sur ce projet se situe à la fois sur le plan **technique** et **humain**. Dès le début, j’ai pris l’initiative de poser les fondations du projet, ce qui a aidé à **structurer** le travail de l’équipe. J’ai aussi proposé et développé des fonctionnalités comme le système de badges, qui ont apporté un aspect plus personnalisé au jeu. Sur le plan humain, j’ai essayé d’être disponible pour les autres, en aidant lorsque quelqu’un rencontrait des difficultés et en **participant activement** aux échanges.

Ce projet m’a donc permis de **mieux comprendre** ma façon de travailler, mes points forts mais aussi les points à améliorer. Aujourd’hui, ces enseignements me servent **dans tous mes projets**, notamment dans ma manière de m’**organiser** et de **collaborer** avec les autres.

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
