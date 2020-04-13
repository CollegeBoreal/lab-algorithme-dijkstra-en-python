## Utilisation de Variables

Pour faire une recherche arborescente, il nous faut un arbre qui constituera notre variable.

Dans cet exemple, on va créer un arbre que l'on appellera `élèves` qui nous permettra de naviguer à travers une classe d'étudiants. Ces étudiants ont comme relation, une relation de proximité.

La(e) premièr.e étudiant(e) assit au bout d'une table forme le groupe de l'étudiant(e) de cette table. L'étudiant(e) assis(e) à l'autre bout de table est forcément à proximité d'un(e) étudiant(e) d'une autre table.

La relation de proximité ne peux former de boucle afin de respecter la description d'un arbre [voir DAG](https://en.wikipedia.org/wiki/Directed_acyclic_graph)

- [ ] Ajoute l'arbre suivant au programme Python, juste aprés le block de commentaires ou tu as mis ton nom.

```python
eleves = {}
eleves["Boris"]=["Amir","Franck","Nathalie","Bertrand"]
eleves["Amir"]=[]
eleves["Franck"]=[]
eleves["Nathalie"]=[]
eleves["Bertrand"]=["Erna","Hassana","Abdelkrim"]
eleves["Erna"]=[]
eleves["Hassana"]=[]
eleves["Zoureni"]=["Sekou","Auriane","Corlings"]
eleves["Sekou"]=[]
eleves["Auriane"]=[]
eleves["Corlings"]=[]
eleves["Abdelkrim"]=["Souleyman","Zack","Zoureni"]
eleves["Souleyman"]=[]
eleves["Zack"]=[]
```

- [ ] Notre programme étant une recherche, on va remplacer la fonction `main` par `search` en lui donnant un paramètre en entrée `name`. Afin de lui donner le premier nom dans l'arbre, dans le block `if __name__ == "__main__"` on écrira la nouvelle fonction et son paramètre d'entrée: `search("Boris")`. Le code se présentera comme ceci.

```python
def search(name):
   print('Informatique: le rêve')

if __name__== "__main__":
   search("Boris")
```

- [ ] La fonction `search` a plutôt l'air d'avoir un effet secondaire `side effects` car toute définition de recherche devrait retourner un booléen et devrait afficher autre chose que ce que l'on a actuellement. Pour y remédier, nous allons lui donner une valeur de retour par défaut, disons toujour faux `False` car on n'a rien trouvé et temporairement afficher la taille des valeurs comprenant notre arbre `eleves`.

```python
def search(name):
   print( len(eleves.values()) )
   return False
```

Maintenant fais tourner ton code et mets le *nombre* de valeurs que tu as trouvé dans le commentaire et faisons rouler ce tutoriel!
