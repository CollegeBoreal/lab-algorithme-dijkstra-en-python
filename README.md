# Algorithme du BFS en Python

Salut, 

Dans ce tutoriel, tu vas créer une recherche arborescente en utilisant l'algorithme de recherche se reposant sur [Dijkstra](https://fr.wikipedia.org/wiki/Algorithme_de_Dijkstra)

```
graphe = {'debut': {}}
graphe['debut']['a'] = 6
graphe['debut']['b'] = 2
graphe['a'] = {}
graphe['a']['fin'] = 1
graphe['b'] = {}
graphe['b']['a'] = 3
graphe['b']['fin'] = 5
graphe['fin'] = {}

INFINI = float('INF')

couts = {'a': 6, 'b': 2, 'fin': INFINI}
parents = {'a': 'debut', 'b': 'debut', 'fin': None}
visite = []

def trouver_noeud_au_meilleur_cout(couts):
    meilleur_cout = INFINI
    noeud_au_meilleur_cout = None
    for noeud in couts:
        cout = couts[noeud]
        if cout < meilleur_cout and noeud not in visite:
            meilleur_cout = cout
            noeud_au_meilleur_cout = noeud
    return noeud_au_meilleur_cout

def main():
    noeud = trouver_noeud_au_meilleur_cout(couts)
    while noeud is not None:
        cout = couts[noeud]
        voisins = graphe[noeud]
        for voisin in voisins.keys():
            nouveau_cout = cout + voisins[voisin]
            if couts[voisin] > nouveau_cout:
                couts[voisin] = nouveau_cout
                parents[voisin] = noeud
        visite.append(noeud)
        noeud = trouver_noeud_au_meilleur_cout(couts)

if __name__== "__main__":
  main()
  print(couts['fin']) 
```
