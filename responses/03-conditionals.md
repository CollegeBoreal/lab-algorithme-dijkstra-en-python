Continuons maintenant dans une recherche arborescente plus approfondie.

Pour naviguer dans la queue, on va demander aux personnes de sortir par la gauche `(du bus)` et tant qu'il y a une personne dans la queue, on continue. Le mouvement s'arrete quand la queue est vide. Ceci est représenté par le code ci-dessous:

```python
   while search_queue:
      personne = search_queue.popleft()
```

Ce code ne fait que faire sortir les premières personnes entrées dans le bus. Il ne tient pas compte des `autres stations de bus`, dans notre cas le lien de proximité de nos étudiants.

Pour se faire, nous allons rajouter une ligne `search_queue += eleves[personne]` nous permettant de faire le lien entre tous les étudiants, remplir la queue au fur et à mesure et finalement `traverser` l'arbre entièrement.

- [ ] Remplace la ligne `print( len(search_queue) )` qui imprime la taille des premiers entrés par la traversée de l'arbre suivante

```python
   while search_queue:
      personne = search_queue.popleft()
      search_queue += eleves[personne]
```

La traversée de l'abre est presqu'inutile car nous l'avons traversé dans son entier sans avoir trouvé l'élu. Nous devons donc revenir sur nos pas et :

* insérer la fonction définie plus tôt `personne_elue()`

* trouver au plus vite l'élu(e) 

* et sortir de l'arbre dés que l'on peut. 


- [ ] L'insertion de ce nouvel élément se fera juste à la sortie du bus `popleft()` et avant que la personne `rameute` ses amis `search_queue += eleves[personne]`.

```python
      if personne_elue(personne):
         print(personne + " a le fameux Mac")
         return True
```

:bulb: Le code final de notre algorithme devrait ressembler à ceci, vérifie que le code ci dessous correspond à celui de ton programme:

```python
   while search_queue:
      personne = search_queue.popleft()
      if personne_elue(personne):
         print(personne + " a le fameux Mac")
         return True
      search_queue += eleves[personne]
```

- [ ] Exécute ton code et ajoute en commentaire l'impression que tu as obtenu. On passera ensuite au code suivant.
