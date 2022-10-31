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

``` git ckeckout [branche]  ``` 

* Créer une branche et me positionne dessus

``` git checkout -b [branche] ```

* Quelles branches existent 

> m'affiche tous ce qui existe au dernier git fetch 

``` git [branche] -r  ```