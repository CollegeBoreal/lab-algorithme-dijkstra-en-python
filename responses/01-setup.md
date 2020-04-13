  Bienvenue dans ce laboratoire qui te guidera à écrire un programme dans le language [Python](https://www.python.org). Le programme se concentrera sur l'étude de l'algorithme permettant l'étude de la recherche binaire basée sur le [BFS](https://en.wikipedia.org/wiki/Breadth-first_search). Avant de commencer, nous allons nous assurer que l'environnement de développement est prêt. 

## :a: Installer Python 

:zero: Présence de Python

Ouvrir un terminal et vérifier la version de Python avec la commande suivante

```
% python --version
```

Si Python est installé, le résultat de la commande donnera une version. Cette version doit être superieure à `3.x.x`

:one: installer Python avec un `Package manager`

Si Python n'est pas installé, utiliser un gestionnaire de librairies.

:computer: Windows avec [choco](https://chocolatey.org/install)

```
PS > choco install anaconda3
```

:apple: MacOS avec [HomeBrew](https://docs.brew.sh/Installation)

```
% brew cask install anaconda 
% echo 'export PATH="/usr/local/anaconda3/bin:$PATH"' >> ~/.zshrc 
```

:warning: Ce laboratoire n'utilise pas Python **2**

## :b: Installer [Git](https://git-scm.com/downloads)

:two: Présence de Git

Ouvrir un terminal et vérifier la version de Git avec la commande suivante

```
% git --version
```

Si le résultat donne un numéro de version. C'est parfait sinon

:four: installer Git avec un `Package manager`

Si Git n'est pas installé, utiliser un gestionnaire de librairies.

:computer: Windows avec [choco](https://chocolatey.org/install)

```
PS > choco install git.install
```

:apple: MacOS avec [HomeBrew](https://docs.brew.sh/Installation)

```
% brew install git
```

## :ab: Cloner le référentiel

Maintenant que nous avons Git, nous pouvons cloner le référentiel contenant block d'assemblage du code quer tu vas écrire. Dans un terminal tapes `git clone {{ repoUrl }}`, la version `SSH` est également recommandée

Dans le référentiel, il y a deux fichiers:

- `README.md`: un fichier `markdown` donnant des informations sur le laboratoire
- `b000000000.py`: un fichier Python contenant le code à construire

Maintenant que tout est en place, nous pouvons commencer.

Laisses un commentaire avec ton *:id:* github pour continuer.