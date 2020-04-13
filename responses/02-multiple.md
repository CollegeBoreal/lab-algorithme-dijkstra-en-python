Tu as entré {{ taille }} , j'ai trouvé :one::four: . Cela n'a pas trop d'importance pour l'instant, continuons!.

- [ ] Déterminons la personne élue

Pour que notre algorithme fonctionne, nous allons assigner une personne qui nous permettra d'arrêter notre recherche.

Notre recherche consiste à trouver la personne dans la classe qui possède un ordinateur Apple :apple:. Pour cela, on va poser la question à tous les étudiants, trouver la première personne qui correspond à notre critère d'élection et stopper notre recherche en retournant `vrai` sinon aller jusqu'au bout de l'arbre et ramener `faux`. Créons une fonction, à part, que l'on nommera `personne_elue` et posons la question si la personne courante `name` est bien l'élue.

:bulb: On va écrire notre fonction juste après la déclaration de notre arbre `eleves`

```python
def personne_elue(name):
    return name == 'Zoureni'
```

Maintenant que nous avons notre cas de base `base case`, penser à la récursion, on va utiliser une autre `structure de données` pour ordonner notre recherche.  

- [ ] Soyons ordonné

Pour cela, nous allons demander à nos étudiants qui sont à proximiter de se mettre en ligne comme quand on prend le bus. Nous allons placer nos étudiants en ligne appellé `Queue`, en Python cela s'appelle `deque` pour [Double Ended Queue](https://en.wikipedia.org/wiki/Double-ended_queue). On peut dépiler la queue, soit du coté gauche, soit du coté droit, d'oû son nom `double ended` Queue.

Juste après la fonction `personne_elue`, écrire la ligne suivante permettant d'aller chercher `(importer)` le code de la `queue` dans une autre librairie appelée `collections`

```python
from collections import deque
``` 

Donnons à la queue le nom d'une variable que l'on pourrait appeller `search_queue`. Pour initialiser `search_queue`, c'est à dire la créer en mémoire, on utilise la fonction `deque()` en Python. 

```python
search_queue = deque()
```

Pour placer des personnes à la file, on utilise `l'affectation` suivante 

```python
search_queue += eleves[name]
```

Nous n'avons pas encore placé l'initialisation et l'affectation de notre variable `search_queue`. Pour cela, nous allons placer `search_queue` dans la fonction `search()` comme montré ci-dessous:

```python
def search(name):
   search_queue = deque()
   search_queue += eleves[name]
   print( len(search_queue) )
   return False
```

Maintenant, le code de la fonction `search()` place les premières personnes à la queue leu leu et le nom de cette personne est donné par le paramètre de la fonction `search()` qui est `name`. La fonction détermine également la taille de la première série de la queue `search_queue` en affichant sa taille avec la fonction `len()`

- [ ] Fais tourner ton programme dans ton terminal

:warning: Mets le chiffre que le programme a imprimé dans le message de ta signature `commit` à la soumission de ton programme.


**Soumets ton code** vers GitHub pour continuer:
```
git add b000000000.py
git commit --message "La taille de la queue est <mon chiffre ICI>"
git push
```
