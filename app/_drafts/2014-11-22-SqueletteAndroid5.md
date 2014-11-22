---
layout: post
title: Squelette Android 5.0
author: Benjamin
cover: android5-banner
tags: [Android, Material design]
---

## Pourquoi ?

Chez Code-Troopers, nous avons pas mal de projets __Android__. Au début du projet, on fait toujours la même chose :

 1. on lance __Android Studio__
 2. on créé un nouveau projet
 3. on choisit parmi les templates qu'il nous propose
 4. on ajoute nos librairies favorites
 5. on modifie le thème

Toutes ces étapes sont répétitives. De plus, avec l'arrivée du __Material Design__ et
les nouvelles libraires de compatibilités, les templates que propose __Android Studio__ ne sont plus d'actualités. Par exemple si l'on choisit un template avec le __NavigationDrawer__, il faut presque tout changer pour celui-ci colle au nouveau standard __Material Design__.

<!--break-->

## Le squelette

Afin de faciliter la vie des troopers, j'ai décidé de créer un squelette d'application __Android__ contenant nos librairies favorites et le minimum visuel.

<div style="text-align:center;margin:50px">
<a href="/images/postAndroid5/screen1.png" data-lightbox="group-1" title="Page d'accueil du squelette" class="inlineBoxes">
<img class="medium" src="/images/postAndroid5/screen1.png" alt="Page d'accueil du squelette"/>
</a>
<a href="/images/postAndroid5/screen2.png" data-lightbox="group-1" title="Navigation drawer" class="inlineBoxes">
<img class="medium" src="/images/postAndroid5/screen2.png" alt="Navigation drawer"/>
</a>
</div>


### Bye bye ActionBar, Hello Toolbar

Depuis l'arrivée de __Lollipop__, un nouvel élément a fait son entrée dans le SDK, la __Toolbar__. Celle-ci possède quasiment les mêmes fonctionnalités que l'__ActionBar__. Le principal avantage, c'est qu'elle n'est pas liée magiquement au layout, c'est à nous de l'inclure.

### NavigationDrawer

Si l'on se réfère au [specifications du __Material Design__](http://www.google.com/design/spec/patterns/navigation-drawer.html), le menu doit prendre toute la hauteur de l'écran et se placer sous la barre de statut. Ceci n'est pas encore bien implémenté par tout le monde. De plus, l'implémentation n'est pas si simple. J'ai donc décidé de l'inclure dans ce squelette en ajoutant par la même, l'intéraction avec la __Toolbar__ (pour pouvoir avoir l'icône hamburger sans avoir à ajouter de ressources). Je tiens au passage à remercier l'auteur de ce [post](http://stackoverflow.com/questions/26745300/navigation-drawer-semi-transparent-over-status-bar-not-working) qui m'a grandement aidé.

### Librairies

Pour l'instant, j'ai ajouté seulement trois librairies :

* __ButterKnife__ pour l'injection de view
* __Dagger__ pour l'injection du reste
* __Picasso__ pour le chargement et la gestion des images

### Le thème

Je me suis basé sur le thème par défaut de __AppCompat__, je l'ai ensuite modifié pour changer les couleurs des barres de statut et d'action lorsque le téléphone est sous __Lollipop__.

## Projet

Voilà, vous pouvez trouver ce projet sur notre [github](https://github.com/code-troopers/material-android-bootstrap). Il va sûrement évoluer avec le temps pour ajouter d'autres choses afin d'avoir des exemples d'implémentations. Vos commentaires, issues sont les bienvenues, je me ferai un plaisir d'y répondre et si vous avez d'autres idées, vous pouvez toujours forker.