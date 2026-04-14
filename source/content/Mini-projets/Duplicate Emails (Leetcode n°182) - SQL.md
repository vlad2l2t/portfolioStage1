#leetcode #sql
https://leetcode.com/problems/duplicate-emails/description/

***Intitulé:***
>Write a solution to report all the duplicate emails. Note that it's guaranteed that the email field is not NULL. Return the result table in **any order**.

***Code soumis:***
```sql
SELECT email FROM Person GROUP BY email HAVING COUNT(email)>1;
```

Renvoie les emails présents plusieurs fois dans la table "Person" en regroupant par email et en filtrant ceux qui apparaissent plus d'une fois.