---
title: "Automatisation de tâches"
order: 2
image: "alternance/alternance.png"
---

## Présentation du projet

Mon alternance de deux ans chez <a href="https://www.easybourse.com" target="_blank">Easybourse</a>, un courtier en ligne filiale de **La Banque Postale**, m’a permis de passer d’un cadre académique à un environnement professionnel réel, avec des enjeux concrets pour l’entreprise. **EasyBourse** propose une plateforme permettant aux particuliers d’investir en bourse de manière **sécurisée** et **accessible**. Durant cette expérience, j’ai travaillé sur plusieurs projets liés à l’analyse de données, au reporting et à l’automatisation de processus internes.

Ma **mission principale** était la **mise en place de rapports** réglementaires et business, ainsi que la **création de dashboards** destinés à améliorer la connaissance des clients et la vision globale de l’activité de l’entreprise. Cette mission s'installait aussi dans un contexte d'**automatisation** et de **réduction de la dette technique** très présente dans l'entreprise. J'ai donc mis en place de nouveaux rapports mais aussi repris des actuels mais encore générés manuellement.

## Objectifs, enjeux et risques

Cette **mission** avait différents objectifs, pour l’entreprise, il s’agissait de fournir à la direction et aux équipes métiers des reporting **fiables** et **exploitables**, permettant d’avoir une **vision claire** sur les clients et leur activité. Les reportings réglementaires étaient également **indispensables** pour garantir la **conformité** de l’entreprise avec les obligations légales. La partie automatisation de certains traitements permettait quant à elle de **réduire les tâches manuelles chronophages**, d’améliorer la fiabilité des données et surtout d'avoir un contrôle sur ces processus. Autrement dit, la mise en place de la **méthode ARC**, acronyme pour **Automatisation**, **Régulation**, **Contrôle**, qui consiste à s'assurer que chaque traitement s'est bien exécuté, d'être alerté rapidement en cas d'anomalie et de pouvoir intervenir sans délai pour corriger le problème.

Pour moi, cette mission était celle que je devais mener à bien pour valider ma mission en entreprise, l'objectif était d'appliquer les procédures enseignées et d'être efficace. 

Les **enjeux** pour l’entreprise étaient importants. Avant la mise en place de certains reportings, il n’existait pas toujours de **vision centralisée de l’activité**, ce qui limitait l’efficacité des analyses marketing et la prise de décision. Les projets d’automatisation visaient également à **réduire les risques d’erreurs humaines** et à améliorer la **qualité des traitements**. Pour moi, l’enjeu était de réussir mon intégration dans un environnement professionnel, de gagner en crédibilité et de démontrer ma capacité à contribuer à des projets ayant un impact réel pour l’entreprise.

Le risque était de ne pas atteindre les attentes de l'entreprise et de mon maître d'apprentissage. Pour l'entreprise, c'était de voir ce projet stagner, et de continuer à perdre du temps sur des tâches qui pourrait être automatisée.

## Les acteurs 

Ma mission s'est donc déroulée dans un environnement professionnel structuré impliquant plusieurs équipes : **développeurs**, **équipes métiers**, **marketing** et **direction**. 

J’ai travaillé en étroite collaboration avec mon **maître d’apprentissage**, qui m’accompagnait sur les aspects techniques et fonctionnels des développements. Il m’a aidée à comprendre les enjeux métiers et à structurer mes solutions. J’ai également collaboré avec les autres **développeurs** lors des reprises de code, des mises en production et des échanges sur les bonnes pratiques. Les interactions avec les autres services cités précédemment étaient également essentielles pour comprendre les besoins et concevoir des solutions adaptées.

## Étapes de réalisation

### Prise d'information

Mon travail consistait à **répondre aux demandes de reporting**, qu’elles soient **réglementaires** ou liées aux **besoins métiers**. Je devais analyser chaque demande, comprendre sa finalité et déterminer si elle pouvait être automatisée. Il était important de comprendre l'**objectif du rapport**, surtout si il contenait des **données à caractère personnel** (**DCP**), c'est-à-dire toute information permettant d'identifier **directement** ou **indirectement** une personne comme un nom de famille ou un numéro client. Ces données étant **sensibles**, il était important de bien comprendre leur usage avant de commencer le développement.

### Développement Python et DAG Airflow

Une fois les **besoins clarifiés**, j'explorais les bases de données de l’entreprise pour identifier les **tables** et les **relations pertinentes**, puis je construisais des requêtes **[SQL](/competences/sql)** capables de produire les données attendues.
Certaines se sont d'ailleurs révélées **complexes** à optimiser, notamment sur des **volumes de données importants**.
Ces requêtes étaient ensuite intégrées dans les scripts **[Python](/competences/python)** que je développais, accompagné de l'algorithme nécessaire lorsqu'une phase de vérification ou de contrôle des données était demandé. 

Ensuite, j'utilisais <a href="https://airflow.apache.org" target="_blank">Airflow</a>, un outil d'**orchestration de workflows**, pour **planifier** et **automatiser** l'exécution de ces traitements. Cela impliquait de rédiger un **DAG** (Directed Acylic Graph), qui consiste en un code **Python** afin de définir l'ordre et la fréquence d'exécution des différentes tâches. Tous les lundis à 8h ou bien tous les 1er du mois par exemple. Cet outil nous permet de mettre en place la méthode **ARC**.

<div style="float: center; margin: 1rem 0 1rem 1.5rem;">
  <img style="display:block; margin: 1rem auto; border-radius: 8px; width:100%; height:100%;" src="/images/realisations/alternance/airflow_interface.png" alt="airflow"/>
  <p style="text-align: center; font-size: 0.85rem; opacity: 0.7;margin-bottom: 0px;">
    Une capture d'écran de l'interface Airflow, montrant un DAG qui permet d'exécuter un dashboard quotidiennement.
  </p>
</div>

### Tests en recette

Une fois le **développement finalisé**, je le testais en recette afin de vérifier son **bon fonctionnement** avant la mise en production.  Cet **environnement isolé** permettait de s'assurer que le rapport généré était **correct** sans risquer d'impacter les données de production.

### Validation par le demandeur

Une fois le **test concluant**, je sollicitais la personne à l'origine de la demande pour qu'elle **valide le rapport**, autrement dit la cohérence des données, la structure des colonnes et bien sûr le respect du besoin initial. Cette étape est essentielle pour s'assurer que le travail réalisé correspond bien aux attentes.

### Mise en production

Après avoir obtenue **toutes les validations nécessaires**, je passais à la **mise en production** du développement. Pour cela, je créais une **merge request** afin de soumettre l’intégration du code, permettant à mon maître d'apprentissage de relire les modifications et de garantir la qualité du code avant son **déploiement**. Cette organisation facilitait la **collaboration** et **assurait un suivi clair** des évolutions du projet. Par la suite, les **DevOps**, administrateurs des infrastructures informatiques et **responsable** de la gestion de la production, prenaient ensuite le relais en **acceptant ma merge request**. Je collaborais également avec eux pour **planifier** la mise à disposition des fichiers générés via **SecureTransport**, l’**outil de transfert de fichier sécurisé** utilisé par l’entreprise.

<img style="display:block; margin: 1.5rem auto; border-radius: 8px; height:90px; width:650px;" src="/images/realisations/alternance/dashboardglob.png" alt="dashglob"/>
  <p style="text-align: center; font-size: 0.85rem; opacity: 0.7;margin-bottom: 0px;">
    Un exemple de rapport que j'ai réalisé, représentant le chiffre d'affaires de l'entreprise (les données présentées ici sont fictives).
  </p>

## Résultats

Les résultats ont été **très positifs**. Les reporting développés ont permis d’apporter une vision plus claire de l’activité de l’entreprise, ce qui a facilité la prise de décision pour le marketing, le service client et la direction. L’automatisation de certains traitements a également permis de **réduire les tâches manuelles** et d’améliorer la fiabilité des données produites.

Pour moi, cette mission a été une **vraie montée en compétences**. J'ai appris à travailler pour la première fois dans un environnement professionnel. J'ai pu **collaborer avec des équipes non techniques** et aux profils très différents. J'ai livré des **développements de qualité** dans des délais impartis et voir mes rapports utilisés en production et **présentés en comité de direction** a été une grande fierté.

## Mon regard critique

Ma **principale valeur ajoutée** sur ce projet a été mon **autonomie** et ma **rigueur**. Dès le début j'ai pris les devants en explorant les bases de données, en proposant des solutions et en revenant vers mon maître d'apprentissage avec des questions précises plutôt que des blocages. Cette façon de travailler m'a permis d'avancer **efficacement** et de montrer que j'étais capable de gérer des développements de **manière indépendante**.

Ce que je retiens surtout de cette expérience, c'est l'importance de la communication. J'ai appris à **[adapter](/competences/adaptabilite) mon discours** selon mon interlocuteur, qu'il soit développeur, ou bien qu'il fasse partie de la direction, j'ai **reformulé** des besoins techniques en termes compréhensibles et inversement. 

## Les lendemains du projet

À court terme, cette mission m'a permis de **consolider mes compétences** en **[SQL](/competences/sql)**, **[Python](/competences/python)** et **[Git](/competences/git)**, mais surtout de comprendre comment le développement informatique peut avoir un impact concret sur le fonctionnement d'une entreprise et lui être bénéfique.

À moyen terme, elle m'a appris à **[communiquer](/competences/communication) avec des équipes non techniques**, à **comprendre** les besoins métiers et à y **répondre de manière adaptée**. Être **capable de vulgariser** des termes techniques et d'expliquer pourquoi une demande n'est pas possible est une vraie compétence que j'ai pu apprendre.

Aujourd’hui, cette expérience constitue un **socle essentiel** de mon parcours professionnel et a confirmé mon envie d’évoluer dans des environnements techniques exigeants et collaboratifs.

<h3>Compétences associées</h3>
<div style="display:flex; gap:4rem;">
<div>

**Technique**
- **[Python](/competences/python)**
- **[SQL](/competences/sql)**
- **[Git](/competences/git)**

</div>
<div>

**Humaine**
- **[Esprit d'équipe](/competences/esprit-equipe)**
- **[Adaptabilité](/competences/adaptabilite)**
- **[Communication](/competences/communication)**
- **[Rigueur](/competences/rigueur)**
  </div>
</div>
