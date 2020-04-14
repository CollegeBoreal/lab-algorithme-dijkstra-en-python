## Utilisation de Variables

Pour faire une recherche arborescente, il nous faut un arbre qui constituera notre variable.

Dans cet exemple, on va créer un arbre que l'on appellera `arbre` qui nous permettra de naviguer à travers des noeuds ayant un poids à chaque arc (symbolisé par un flèche). 

Le but étant de traverser l'arbre du début jusqu'à la fin en prenant le chemin le moins couteux, dans notre cas le tracé indiqué en rouge :crayon:. Les coût peuvent indiqués des kilomètres, des vitesses de débit Internet. Pour notre exemple, nous allons choisir des kilomètres.

Pour rappel, le graphe ne peux former de boucle afin de respecter la description d'un arbre [voir DAG](https://en.wikipedia.org/wiki/Directed_acyclic_graph)

<img src="https://user-images.githubusercontent.com/62551735/79170355-2027ed80-7dbd-11ea-8a80-3871a0d40ab0.png" width="384" height="512"></img>

- [ ] Ajoute l'arbre suivant au programme Python, juste aprés le block de commentaires ou tu as mis ton nom.

```python
arbre = {}
arbre['debut'] = {}
arbre['debut']['a'] = 6
arbre['debut']['b'] = 2
arbre['a'] = {}
arbre['a']['fin'] = 1
arbre['b'] = {}
arbre['b']['a'] = 3
arbre['b']['fin'] = 5
arbre['fin'] = {}
```

- [ ] Ajoute ensuite, le dictionnaire `hastable` de coûts qui nous permettra de définir le coût du chemin optimal. Tu remarqueras que l'on a initialisé une variable `INFINI` de type `float` qui nous servira de `bouche trou` le temps que l'on trouve la valeur recherchée. On assignera au coût de départ, les couts de `début` de l'arbre et au final `couts['fin']` qui est le coût que nous recherchons à l'`INFINI`.

```
INFINI = float('inf')

couts = {}
couts = arbre['debut']
couts['fin'] = INFINI
```

- [ ] Enfin, afin de remonter dans l'arbre, ajoute le dictionnaire `parents` qui nous guidera vers le haut de la hiérarchie si besoin.

```
parents = {}
parents['a'] = 'debut'
parents['b'] = 'debut'
parents['fin'] = None
```

- [ ] Notre programme étant une recherche sur l'algorithme de l'informaticien hollandais [Dijkstra](https://fr.wikipedia.org/wiki/Edsger_Dijkstra), on va remplacer la fonction `main` par son nom `dijkstra` en lui donnant deux paramètres en entrée `couts` et `parents` qui évolueront au fil de la recherche. Dans le block `if __name__ == "__main__"` on écrira la nouvelle fonction et ses paramètres d'entrée: `dijkstra(couts, parents)`. Le code se présentera comme ceci.

```python
def dijkstra(couts, parents):
   print('Informatique: le rêve')

if __name__== "__main__":
   dijkstra(couts, parents)
```

- [ ] La fonction `dijkstra` a plutôt l'air d'avoir un effet secondaire `side effects` car toute définition de recherche devrait retourner une valeur et pourrait afficher autre chose que ce que l'on a actuellement. Pour y remédier, nous allons lui donner une valeur de retour par défaut, notre arbre `arbre`.

```python
def dijkstra(couts, parents):
    print( len(arbre.values()) )
    return arbre
```

Maintenant fais tourner ton code et mets le *nombre* de valeurs que tu as trouvé dans le commentaire et faisons rouler ce tutoriel!
