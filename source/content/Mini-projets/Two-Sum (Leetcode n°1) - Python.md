#leetcode #python 
https://leetcode.com/problems/two-sum/description/

***Intitulé :*** 
> Given an array of integers `nums` and an integer `target`, return _indices of the two numbers such that they add up to `target`_. You may assume that each input would have **_exactly_ one solution**, and you may not use the _same_ element twice. You can return the answer in any order.

***Code soumis :*** 
```python
class Solution(object):
    def twoSum(self, nums, target):
        #ENTREE: Liste nums, int target
		  #SORTIE: tuple de coordonnées dans la liste nums
		  #ROLE: retourne l'indice de deux éléments distincts qui en s'additionannt valent 'target'

		  #Double boucle de parcours 
        for i in range (0, len(nums)):
            for j in range (0, len(nums)):
					#Test d'addition et vérification si les deux nombres sont bien distincts
                if (nums[j]+nums[i] == target and j!=i):
                    return [i,j]
```

La fonction trouve deux indices distincts dans une liste dont les éléments correspondants s'additionnent à une cible donnée. Elle utilise une double boucle pour tester toutes les paires possibles et retourne les indices si la somme correspond à la cible.