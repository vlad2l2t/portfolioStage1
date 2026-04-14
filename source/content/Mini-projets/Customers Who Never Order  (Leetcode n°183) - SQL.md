#leetcode #sql 
https://leetcode.com/problems/customers-who-never-order/

***Intitulé:***
>Write a solution to find all customers who never order anything. Return the result table in **any order**.

***Code soumis:***
```sql
SELECT name AS Customers FROM Customers WHERE id NOT IN(SELECT customerId FROM Orders);
```

Sélectionne les noms des clients qui n'ont pas d'entrées correspondantes dans la table `Orders`. Elle utilise une sous-requête pour récupérer tous les `customerId` de la table `Orders`, puis filtre les clients de la table `Customers` dont l'`id` n'est pas présent dans les résultats de cette sous-requête, indiquant ainsi qu'ils n'ont pas passé de commande. Le résultat est une liste des noms de ces clients, renommée `Customers`.
