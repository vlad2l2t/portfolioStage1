#leetcode #python 
https://leetcode.com/problems/palindrome-number/description/

***Intitulé :***
> Given an integer `x`, return `true` if `x` is a palindrome, and `false` otherwise.

***Code soumis :***
```python
class Solution(object):
    def isPalindrome(self, x):
		#ENTREE: int x
		#SORTIE: True ou False
		#ROLE: détermine si x peut se lire dans les deux sens
	 
		  #Convertir x en chaîne de caractères
        x = str(x)
		  #Renverse la chaîne de caractères dans une nouvelle variable
        rev = x [::-1]

			#Si la nouvelle variable est identique à x, alors x est un palindrome
        if(x == rev):
            return True
        else:
            return False
```

La fonction détermine si un entier est un palindrome. Elle convertit l'entier en chaîne, inverse cette chaîne, et compare l'original avec l'inverse. Si elles sont identiques, l'entier est un palindrome et la fonction retourne `True`; sinon, elle retourne `False`.