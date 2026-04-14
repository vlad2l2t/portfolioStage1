#leetcode #python 
https://leetcode.com/problems/roman-to-integer/

***Intitulé :*** 
> Roman numerals are represented by seven different symbols: `I`, `V`, `X`, `L`, `C`, `D` and `M`. For example, `2` is written as `II` in Roman numeral, just two ones added together. `12` is written as `XII`, which is simply `X + II`. The number `27` is written as `XXVII`, which is `XX + V + II`. Roman numerals are usually written largest to smallest from left to right. However, the numeral for four is not `IIII`. Instead, the number four is written as `IV`. Because the one is before the five we subtract it making four. The same principle applies to the number nine, which is written as `IX`. There are six instances where subtraction is used:
	- `I` can be placed before `V` (5) and `X` (10) to make 4 and 9. 
	- `X` can be placed before `L` (50) and `C` (100) to make 40 and 90. 
	- `C` can be placed before `D` (500) and `M` (1000) to make 400 and 900.
 Given a roman numeral, convert it to an integer.

***Code soumis :*** 
```python
def romanToInt(s)
	#ENTREE: string s (chiffre romain)
	#SORTIE: int valueInt (chiffre arabe)
	#ROLE: Convertit un chiffre romain en chiffre arabe

	#Convertit la chaîne de caractères en une liste avec un caractère par index
	listRoman = list(s)
   valueInt = 0
	#Boucle parcourant chaque caractère
	for i in range(0,len(listRoman)):

		#Variable 'NextChar' contient le prochain caractère
		#(utile pour 'IV' qui donne '4' par exemple)
		#Si i est le dernier caractère, alors nextChar ne sera pas utile.
	  if (i==len(listRoman)-1):
			nextChar = None
	  else:
			nextChar = listRoman[i+1] 
		#Si le caractère est un 'I', on ajoute 1 au total
	  if listRoman[i] =='I':
		  #Si le caractère d'après est un V ou un X, on retire 1 au total
			if nextChar in ('V','X'):
				 valueInt-=1
			else:
				 valueInt+=1*
		#Etc etc...
	  elif listRoman[i] =='V':
			valueInt+=5
	  elif listRoman[i]=='X':
			if nextChar in ('L','C'):
				 valueInt-=10
			else : 
				 valueInt+=10
	  elif listRoman[i]=='L':
			valueInt+=50
	  elif listRoman[i]=='C':
			if nextChar in('D','M'):
				 valueInt-=100
			else:
				 valueInt+=100
	  elif listRoman[i]=='D':
			valueInt+=500
	  elif listRoman[i]=='M':
			valueInt+=1000
	 #Retourne le total
	 return valueInt
```

La fonction convertit un chiffre romain en entier. Elle itère sur la chaîne du chiffre romain, ajustant une valeur entière en fonction de chaque symbole et de sa relation avec le symbole suivant, gérant ainsi les cas de soustraction (comme IV ou IX). Finalement, elle retourne la valeur entière résultante.