# formation_git

## Mise en place

Le plus simple est de créer la remote, puis de la cloner 

```
$ git clone https://github.com/MarjorieRomeo/formation_git.git
Cloning into 'formation_git'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

```

## Modifier un fichier

Ajouter au staging : 

```git add FICHIER```

Ajouter a un commit local :

```git commit -m FICHIER```

Envoyer le commit local sur la remote... ***Mais n'oubliez pas de vous mettre à jour avant !***

```git push -u origin BRANCHE ```


## Gestion des branches 

* changer de branche 

``` git ckeckout BRANCHE  ``` 

* Créer une branche et me positionne dessus

``` git checkout -b BRANCHE ```

* Quelles branches existent 

> m'affiche tous ce qui existe au dernier git fetch 

``` git branch -r  ```

* Merger une branche 

```
git fetch 
git branch -r # liste les branches accessibles
git merge origin/BRANCHE_SOURCE BRANCHE_COURANTE
```


# Formulaires des commandes

***git command -h :*** permet d'obtenir de l'aide sur une commande

***git init :*** cree le dossier caché .git qui contient l'historique des versions

***git clone [url] :*** permet de copier un répertoire git sur une machine locale (ainsi que l'adresse du serveur distant)

***git remote :*** permet de connaitre (-v) et de set l'adresse du serveur distant (add origin [url])

***git fetch origin :*** permet de ***charger l'état du serveur distant sur l'arbre local :*** c'est le git pull des branches

***git status :*** permet de connaitre l'état des fichiers par rapport au dernier commit en local (modification, addition, suggestion de fichier à suivre)

***git add :*** permet d'ajouter un fichier à l'arbre local (lequel ne contient que les fichiers ajoutés de cette manière)

***git diff --staged :*** permet de visaliser en ligne de commande les modifications présentes dans le staging (= commit en préparation) courant

***git remove [file1 file2...] :*** supprime le fichier des arbres distant et local. Ne supprime pas le fichier dans l'arborescence

***git commit :*** enregistre l'état des fichiers ajoutés dans l'arbre local avec un message (-m)

***git push :*** permet d'envoyer un commit sur une branche de l'arbre distant

***git pull :*** permet de merge l'arbre distant sur l'arbre local, équivalent à git fetch && git rebase