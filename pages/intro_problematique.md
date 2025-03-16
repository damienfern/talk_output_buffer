---
layout: image
image: /disneyland-bg.jpg
---

<img 
  v-click v-motion
  :initial="{ x: -100 }"
  :enter="{ x : 0, y : 0 }"
  src="/disneyland-mickey-mouse-jumping-kids.jpg"
  width="500" height="500"
/>
<img
  v-click v-motion
  :initial="{ x: 900, y: 900 }"
  :enter="{ x : 0, y : 0 }"
  style="position: fixed; bottom: 50px; right: 50px;"
  src="/space-mountain.jpg"
  width="250" height="250" 
/>

<!--

En Octobre dernier, j'ai eu la chance de partir à Disneyland Paris.
Mais pas pour profiter du parc, mais pour assister au Forum PHP 2024. 

-->

--- 
layout: image
image: /hotel-marvel.jpg
---

<img v-click src="/forum-php.png" width="300" height="300" style="position: fixed; right: 20px; top: 20px;" />
<img v-click src="/conference-hall-1.jpg" width="600" height="600" />


---

# Qu'est-ce qu'on fait pendant 2 heures de train ? 

<div class="image-container">
  <img v-click src="/netflix.webp" class="image-train" />
  <img v-click src="/gamer.png" class="image-train" />
  <img v-click src="/coding.webp" class="image-train" />
</div>

<style>
.image-container {
  display: flex;             /* Utilise Flexbox pour aligner les images horizontalement */
  justify-content: center;   /* Aligne les images au centre */
  gap: 80px;                 /* Espacement entre les images (ajuste selon tes besoins) */
}

.image-train {
  width: 200px;              /* Ajuste la largeur des images */
  height: auto;              /* Garde la proportion des images */
}
</style>

<!-- 

On part avec 3 collègues et pour ce genre d'event, on prend le train (ça tombe bien y a un direct de lyon pour aller à Marne La Vallée). Et pendant le voyage, pour m'occuper, pendant les 2 petites heures, j'ai plusieurs choix :

- Netflix
- Games
- Faire du dev (perso ou open source)

Bon la wifi/partage de co pour Netflix, pas fou fou, games j'ai rien sur le PC donc lets goooo

-->

---

<div class="container">
  <img src="/alex_no_mouth.png" class="image" />
  <img src="/alex_mouth.png" class="image"  :class="$clicks >= 1 ? 'mouth':''" />
  <div v-click></div>
</div>

<!-- "Eh, si tu veux contribuer, notamment Symfony, tu peux check les issues sur Github et regarder les bugs ou les features." -->

<style>
.container {
  position: relative;
  width: 500px; /* Exemple de taille */
  height: 500px; /* Exemple de taille */
}

.image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%; /* Assure-toi que les images couvrent la taille du conteneur */
  height: 100%; /* Assure-toi que les images couvrent la taille du conteneur */
}

.mouth {
    animation: speak 0.5s infinite; /* Animation pour simuler la parole */
}
/* Animation de la bouche */
@keyframes speak {
  0% {
    transform: translate(0%, 0%); /* Position initiale */
  }
  30% {
    transform: translate(0%, 2%); /* Ouvrir la bouche */
  }
  50% {
    transform: translate(0%, 0%); /* Ouvrir la bouche */
  }
  70% {
    transform: translate(0%, 3%); /* Ouvrir la bouche */
  }
  90% {
    transform: translate(0%, 0%); /* Ouvrir la bouche */
  }
  100% {
    transform: translate(0%, 0%); /* Fermer la bouche */
  }
}
</style>

---

<v-clicks>

# Le WebProfilerBundle

<img src="/web-profiler.png" height="600" width="600" />
<img src="/webprofiler-bar.png" height="200" />


</v-clicks>

<!-- Un de mes composants/bundle préférés c'est le webProfilerBundle.
Rappelez à quoi sert le WebProfiler

Il m'a sauvé la vie plus d'une fois donc lets gooo pour lui. [INSERER SCREEN WEB PROFILER] -->

---

<img src="/symfony_issue.png"  width="600" height="600"  />

<!-- Donc je cherche dans les issues et je tombe sur ce ticket -->

<!-- Bon c'est un souci d'intégration de la barre de débug lors qu'on stream une réponse. C'est parti ! -->
