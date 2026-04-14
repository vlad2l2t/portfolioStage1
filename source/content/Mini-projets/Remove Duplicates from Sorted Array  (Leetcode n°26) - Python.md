#leetcode #python 
https://leetcode.com/problems/remove-duplicates-from-sorted-array/description/

***Intitulé:***
>Given an integer array `nums` sorted in **non-decreasing order**, remove the duplicates [**in-place**](https://en.wikipedia.org/wiki/In-place_algorithm) such that each unique element appears only **once**. The **relative order** of the elements should be kept the **same**. Then return _the number of unique elements in_ `nums`. Consider the number of unique elements of `nums` to be `k`, to get accepted, you need to do the following things:               -Change the array `nums` such that the first `k` elements of `nums` contain the unique elements in the order they were present in `nums` initially. The remaining elements of `nums` are not important as well as the size of `nums`.  - Return `k`.

***Code soumis:***

```python
def removeDuplicates(nums):
	#ENTREE: liste nums non-décroissante
	#SORTIE: int k nombre d'éléments uniques
	#ROLE : Modifie une liste pour en enlever les doublons et renvoie le nombre d’éléments uniques k.
	  k = 1
	  for i in range(1, len(nums)):
			if nums[i] != nums[i-1]:
				 nums[k] = nums[i]
				 k += 1
	  return k
```

La fonction itère à travers la liste, et si un élément est différent de l'élément précédent, il est placé à la position `k` et `k` est incrémenté.