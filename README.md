# tuto
cv html/ css sur docker
# Créer un nouveau projet ici nommé: moncvhtmlcss
# Créer un fichier Dockerfile à la racine puis  ajouter:
#Les lignes de code suivantes  représentent l’image que nous allons
 utiliser avec la copie du contenu du répertoire actuel dans le conteneur.

FROM nginx:alpine
COPY . /usr/share/nginx/html

# Faire le build du projet:
docker build -t html-server-image .
# Exécuter le serveur du conteneur HTML
docker run --name html-serveur-container -d -p 8080:80 html-server-image
