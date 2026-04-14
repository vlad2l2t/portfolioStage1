#leetcode #sql 
https://leetcode.com/problems/combine-two-tables/

***Intitulé:***
>Write a solution to report the first name, last name, city, and state of each person in the `Person` table. If the address of a `personId` is not present in the `Address` table, report `null` instead. Return the result table in **any order**.

***Code soumis:***
```sql
SELECT firstName, lastName, city, state FROM Person LEFT JOIN Address USING(personId);
```

Sélectionne le prénom (firstName) et le nom (lastName) de la table Personne, ainsi que la ville (city) et l'état (state) de la table Adresse. Effectue une jointure gauche (LEFT JOIN) entre les deux tables en utilisant la colonne personId comme clé de jointure, ce qui inclut toutes les personnes même si elles n'ont pas d'adresse correspondante.