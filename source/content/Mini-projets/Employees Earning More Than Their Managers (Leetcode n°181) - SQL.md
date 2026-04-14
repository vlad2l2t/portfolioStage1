#leetcode #sql 
https://leetcode.com/problems/employees-earning-more-than-their-managers/description/

***Intitulé:***
> Write a solution to find the employees who earn more than their managers. Return the result table in **any order**.

***Code soumis:***
```sql
SELECT t1.name AS Employee FROM Employee t1 WHERE salary>(SELECT salary FROM Employee WHERE id = t1.managerId);
```

Sélectionne le nom des employés de la table Employee (alias t1) dont le salaire est supérieur au salaire de leur manager. Le manager est identifié par l'ID (managerId) dans la même table Employee par le biais d'une sous-requête.