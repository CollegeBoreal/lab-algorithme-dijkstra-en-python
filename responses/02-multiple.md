Tu as entré {{ taille }} , j'ai trouvé :four: . C'est la taille de l'arbre `arbre` composé des noeuds, `debut`, `a`, `b` et `fin`.

- [ ] Déterminons le meilleur coût

Pour que notre algorithme fonctionne, nous allons chercher le meilleur coût à travers une liste de couts.

C'est très simple, on va créer une fonction `trouver_noeud_ayant_meilleur_cout` qui va recevoir une liste de noeux dont on a assigné des coûts.

:bulb: On va écrire notre fonction juste après la déclaration de notre arbre `parents` dans la partie déclaration des variables.

```python
def trouver_noeud_ayant_meilleur_cout(couts):
    meilleur_cout = INFINI
    noeud_au_meilleur_cout = None
    for noeud in couts:
        cout = couts[noeud]
        if cout < meilleur_cout:
            meilleur_cout = cout
            noeud_au_meilleur_cout = noeud
    return noeud_au_meilleur_cout
```

On `boucle` autour de notre dictionnaire de coûts en extirpant chaque `noeud` et en lisant son coût. Si le coût nous intéresse, on le garde dans deux variables `noeud_au_meilleur_cout` et `meilleur_cout`, dont on a pris le soin d'initialiser au préalable à `None` et à `INFINI` respectivement, pour les utiliser ultérieurement.

Pour rappel, nous recherchons le coût le plus bas, ce qui signifie de comparer le coût du noeud courant au coût sauvegardé dans la variable `meilleur_cout`

```python
        cout = couts[noeud]
        if cout < meilleur_cout:
```

Maintenant que nous avons notre cas de élémentaire de recherche de coûts, on va retourner le `noeud` trouvé et continuer la traversée.  

- [ ] Affichons notre noeud 

Dans la fonction `dijkstra`, remplace `print( len(arbre.values()) )` par la recherche du noeud et son affichage. Réécrit la fonction `dijkstra` comme ceci:

```python
def dijkstra(couts, parents):
    noeud = trouver_noeud_ayant_meilleur_cout(couts)
    print( noeud )
    return arbre
```

- [ ] Fais tourner ton programme dans ton terminal

:warning: Mets le chiffre que le programme a imprimé dans le message de ta signature `commit` à la soumission de ton programme.


**Soumets ton code** vers GitHub pour continuer:
```
git add b000000000.py
git commit --message "La taille de la queue est <mon chiffre ICI>"
git push
```
