# Bonnes pratiques SEO / Mise en prod

## .htaccess

Mettre en place le protocol https sur notre site grâce au fichier .htaccess à la racine du site.<br>
Dans ce fichier nous pouvons forcer la réécriture de notre url en https://

Exemple OVH :

`RewriteEngine On
RewriteCond %{SERVER_PORT} 80
RewriteRule ^(.*)$ https://www.votredomaine.fr/$1 [R,L]`

Doc OVH du mod_rewrite https://docs.ovh.com/fr/hosting/htaccess-reecriture-url-mod-rewrite/

## Open Graph protocol

http://ogp.me/

Permet de définir tout un tas d'informations via des Metada og: dans le head, important pour Facebook ou Linkedin par exemple.<br>
 Voir le lien ci-dessus.

## Metadata

Metadata tels que Keywords, Description (indispensable)

## Liens 

Tous les liens doivent être en https:// ou en chemin relatif

## Google Search Console

https://search.google.com/search-console/about?hl=fr&utm_source=wmx&utm_medium=wmx-welcome

Ajouter la Google Search Console sur votre domaine afin d'être en mesure d'indexer les pages sur google.<br>
1 - Ajouter la propriété <br>
2 - Entrer le nom de domaine <br>
3 - Se connecter sur son hébergeur <br>
4 - Dans le domaine en question, allez dans les configuration DNS (Zone DNS sur OVH) <br>
5 - Ajouter une entrée TXT <br>
6 - Copier coller l'enregistrement TXT généré dans la search console en tant que valeur de la nouvelle entrée TXT de votre zone DNS <br>
7 - Valider la nouvelle entrée sur votre hébergeur puis valider la propriété du domaine sur la search console <br>
8 - Il n'y a plus qu'a séléctionner le domaine que vous souhaitez (si vous en avez ajouté plusieurs) dans la Google Search Console et effectuer certaines actions tel qu'envoyer le Sitemaps ou inspecter les URL pour voir si elles sont bien indexé dans google (si non, google indexera l'url inspecté)
