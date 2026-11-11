# quel-jeu-images

Images du pack « Vrais jeux » de [quel-jeu](https://github.com/Taumoutsh/quel-jeu), déjà téléchargées et réduites par `tools/fetch_packs.py`.

**Dépôt privé** : ce sont des captures de jeux commerciaux et des panoramas de fans, gardés ici seulement pour un jeu privé entre amis. Ne pas le rendre public.

Il sert sur un serveur qui ne peut pas télécharger certaines sources lui-même (les wikis Fandom refusent son adresse IP). Il se clone à la place de `packs/img/` :

```bash
cd ~/quel-jeu
git clone https://github.com/Taumoutsh/quel-jeu-images.git packs/img
docker compose up -d --build        # les images sont reprises au lieu d'être téléchargées
```

Mise à jour après l'ajout de jeux :

```bash
cd ~/quel-jeu
git pull && git -C packs/img pull
docker compose up -d --build
```

`sources.json` donne l'empreinte de la source de chaque image : une image n'est reprise que si elle correspond au pack de `quel-jeu`. `dispo.js` liste les vues disponibles.
