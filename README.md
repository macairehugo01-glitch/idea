# RaiseFX — Site vitrine R&D (proposition interne)

Site de présentation pour lancer le département R&D chez RaiseFX. Node.js/Express, statique côté contenu.

## Lancer en local

npm install
npm start

Puis ouvrir http://localhost:3000

## Ajouter ta vidéo (page webinaire)

1. Crée le dossier public/video/ et dépose ton fichier, par exemple pitch.mp4.
2. Dans public/webinaire.html, remplace le bloc <div class="video-placeholder">…</div> par :

<video controls poster="/img/video-poster.jpg">
  <source src="/video/pitch.mp4" type="video/mp4">
</video>

## Déploiement GitHub → Railway

1. git init && git add . && git commit -m "init site R&D"
2. Crée un repo GitHub et push :
   git remote add origin <url-du-repo>
   git push -u origin main
3. Sur railway.app : New Project → Deploy from GitHub repo → sélectionne le repo.
4. Railway détecte package.json et lance npm start automatiquement.
5. Chaque git push redéploie automatiquement.
