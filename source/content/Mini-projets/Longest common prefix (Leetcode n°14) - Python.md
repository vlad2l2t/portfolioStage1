#leetcode #python
https://leetcode.com/problems/longest-common-prefix/description/

***Intitulé:***
> Write a function to find the longest common prefix string amongst an array of strings. If there is no common prefix, return an empty string `""`.

***Code soumis:***
```python
class Solution(object):
    def longestCommonPrefix(self, strs):
        #ENTREE: liste de strings 'strs'
        #SORTIE: String 'longestPre'
        #ROLE:Renvoie le préfixe commun le plus long d'une liste donnée
  
        #Le préfixe le plus long est par défaut le premier mot de la liste en entier
        longestPre = strs[0]

        #Boucle qui parcours toutes les valeurs de la liste
        # '[1:]' fait que la boucle commence au deuxième élément
        for word in strs[1:]:
            #Réduire le préfixe si le mot ne commence pas par celui ci
            while not word.startswith(longestPre):
                longestPre = longestPre[:-1]
                #Si le préfixe est complètement coupé, alors on vide la chaîne de caractères
                if not longestPre:
                    return ""
        return longestPre
```

La fonction 'longestCommonPrefix' identifie le plus long préfixe commun d'une liste de chaînes. Elle initialise le préfixe avec le premier mot, puis le réduit itérativement tant qu'il n'est pas un préfixe des autres mots. Si le préfixe devient vide, il n'y a pas de préfixe commun. Sinon, elle retourne le préfixe commun trouvé.
