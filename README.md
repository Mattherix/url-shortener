# Url-shortener

Projet-final du cours de delivery de projet: url-shortener

## Description du projet

Grâce à ce service l'utilisateur peut réduire la taille de son lien.

En entrant son lien dans un formulaire il optient un lien plus court qu'il peu partager à ses amis (ex: https://github.com/Mattherix/url-shortener -> https://short.com/1)

Le lien obtenue redirige vers le lien orginal. Seul le créateur du lien voie le nombre de visite. Pas de date d'expiration pour les liens.

## Fonctionnement 

Le projet est séparé en 2 parties, le front et le back.

- Le front est un single page fait avec [vue 3](https://v3.vuejs.org/) et [tailwind css](https://tailwindcss.com/)
- Le back est une api fait en python avec [FastApi](https://fastapi.tiangolo.com/) stoquant ses données sois dans une base de données sois dans un fichier [json](https://docs.python.org/fr/3/library/json.html)/[pickel](https://docs.python.org/fr/3/library/pickle.html)
