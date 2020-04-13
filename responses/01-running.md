Chèr.e {{ id }}, il est temps de faire de la programmation!

- [ ] Changer l'auteur du programme Python

```python
# -*- coding: utf-8 -*-
"""

@author: CollegeBoreal
"""
```

Modifier le programme Python avec l'éditeur de ton choix et changer l'auteur `CollegeBoreal` avec ton :id: Github

- [ ] Exécuter un programme Python

Voyons voir le programme Python, on peut y voir une fonction `main` qui contiendra toutes les instructions pour écrire l'algorithme:

```python
def main():
  #print('Informatique: le rêve')
```

En dessous de la fonction, on trouvera un `if` appellant cette fonction:

```python
if __name__== "__main__":
    main()
```

En faisant cela, la fonction `main` s'èxècutera tant que le programme Python est éxécuté.

Dans la fonction `main`, enlève le commentaire se trouvant sur la ligne:`#print('Informatique: le rêve')`. Cela permettra d'afficher le texte qui se trouve entre les parenthèses. Il y a un `#` devant la ligne, qui veut dire que c'est un commentaire. Enlève le commentaire par le retrait du `#` permettant à Python de lire la ligne et sauveguarde le fichier.

- [ ] Fais tourner ton programme dans ton terminal

Pour éxécuter le programme Python taper `python b000000000.py` dans le terminal. Le programme Python doit se trouver dans le même répertoire ou l'on se trouve.

* Sous Powershell (Sous windows utilise le champ recherche de ta barre d'icône et tape `Anaconda Powershell` )

```
PS > python b000000000.py
```

* Sous ZSH (Sous :apple:)

```
% python b000000000.py
```


Après l'éxécution, sur votre terminal s'affichera: "Informatique: le rêve". Nous ferons mieux dans quelques instants mais pour l'instant, il faut soumettre le code vers GitHub. 


- [ ] Soumettre les modifications

Pour chaque changement de fichiers dans ton référentiel, il faut  `ajouter` et `signer` le fichier qui te permet de formuler un message detailant ce que tu as changé. Ensuite tu peux `soumettre` une version mise à jour, en même temps que tes commentaires, vers GitHub. 

:round_pushpin: Faisons ces trois étapes:

1. Ajouter dans Git: `git add b000000000.py`
2. Signer dans Git: `git commit -m "Enlever le commentaire de la ligne 8"`
3. Soumettre à Git: `git push`
