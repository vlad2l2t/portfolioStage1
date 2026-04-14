#python
Projet réalisé le [[03-06]]

```python
import os

  

#Si le fichier de budget n'existe pas, initialisation

def setupBudget():

    try :

        os.remove('depenses.txt')

    except FileNotFoundError:

        pass

    budget = float(input("Quel est votre budget initial ? "))

    with open('budget.txt','w') as f:

        f.write(str(budget)+'\n')

        f.write(str(budget))

    print(f'Vous avez un budget de {budget} €.')

    return budget

  

#Ajout d'une dépense

def ajoutDepense():

    #Voir le budget restant

    with open('budget.txt','r') as f:

        lines = f.readlines()

        budgetRestant = float(lines[1].strip())

    with open('depenses.txt','a+') as f :

        #Affichage du numéro de la dépense

        f.seek(0)

        lines = f.readlines()

        nbDepenses = len(lines)

        if(len(lines)==0):

            nbDepenses = 0

        print(f"Dépense n°{nbDepenses+1} :")

        #Prompt libellé

        libelle=input("Libellé : ")

        #Prompt montant protégé contre les erreurs de valeur

        while True:

            try :

                montant= float(input("Montant : "))

                break

            except ValueError:

                print("Erreur lors de la saisie du montant.")

        #Prompt magasin

        magasin =input("Magasin : ")

        #Ecriture dans le fichier

        f.write(f"{libelle}|{montant}|{magasin}\n")

        print()

        #Affichage du budget restant

        budgetRestant = budgetRestant - montant

        print(f'Dépense de {montant}€ chez {magasin} ajoutée.')

        print(f'Budget restant : {budgetRestant}€.')

    #Actualisation du budget restant dans le fichier budget

    with open('budget.txt','r+') as f:

        lines = f.readlines()

        lines[1] = str(budgetRestant) + '\n'

        f.seek(0)

        f.writelines(lines)

    print()

    return

  

#Visionnage des dépenses

def visioDepense():

    #Exception fichier non-existant

    if not os.path.exists('depenses.txt') or os.stat("depenses.txt").st_size == 0:

        print("Vous n'avez pas de dépenses enregistrées.\n")

        return

    #Affichage du budget restant

    with open('budget.txt','r') as f:

        f.seek(0)

        lines = f.readlines()

        budgetInit = lines[0].strip()

        budgetRestant = lines[1].strip()

        print(f"Budget initial :{budgetInit}€.")

        print(f"Budget restant : {budgetRestant}€.")

    #Lecture des données du fichier

    print("Dépenses enregistrées :\n")

    with open('depenses.txt','r') as f :

        lines = f.readlines()

        for index, line in enumerate(lines, start=1):

            libelle, montant, magasin = line.strip().split('|')

            print(f"Dépense n°{index}:")

            print(f"     Libellé: {libelle}")

            print(f"     Montant: {montant}")

            print(f"     Magasin: {magasin}\n\n")

  
  

#Suppression d'une dépense

def supprDepense():

    #Affichage des dépenses

    visioDepense()

    print()

    #Exception si fichier vide

    if os.stat("depenses.txt").st_size == 0:

        print("Vous n'avez pas de dépenses enregistrées.\n")

        return

    #Prompt (protégé) du choix de la dépense à supprimer

    while True:

        try:

            aSupprimer = int(input("Quelle dépense voulez-vous supprimer ?"))

            break

        except ValueError:

            print("Choix non-valide.")

    with open('depenses.txt','r+') as f:

        f.seek(0)

        lines = f.readlines()

        nbLignes = len(lines)

        if(aSupprimer>nbLignes or aSupprimer<1):

            while True:

                try:

                    aSupprimer = int(input("Quelle dépense voulez-vous supprimer ?"))

                    break

                except ValueError:

                    print("Choix non-valide.")

        #Récupération des infos sur la dépense

        libelle, montant, magasin = lines[aSupprimer - 1].strip().split('|')

        montant = float(montant)

        #Suppression de la ligne

        del lines[aSupprimer - 1]

        #Réécriture du fichier

        with open('depenses.txt', 'w') as f:

            f.writelines(lines)

        #Actualisation du fichier de budget (remboursement)

        with open('budget.txt','r+') as f:

            lines = f.readlines()

            ancienBudgetRestant = float(lines[1].strip())

            budgetRestantUpdate = ancienBudgetRestant + montant

            lines[1] = f"{budgetRestantUpdate}\n"

            f.seek(0)

            f.writelines(lines)

        #Confirmation

        print(f'Dépense "{libelle}" supprimée. Montant remboursé : {montant}€.')

        print(f'Nouveau budget restant : {budgetRestantUpdate}')

  

#Fonction qui clear la console, + de lisibilité

def clearConsole():

    os.system('cls' if os.name == 'nt' else 'clear')

  

  

#Main

def main():

    clearConsole()

    #Bienvenue

    print("Bienvenue dans le programme de gestion de budget.")

    print('-----------\n')

    #Budget initial

    if not os.path.exists('budget.txt'):

        budget = setupBudget()

    with open('budget.txt','r+') as f:

        f.seek(0)

        lines = f.readlines()

        budget = lines[0].strip()

        budgetRestant = lines[1].strip()

        #Si pas de budget trouvé, initialisation

        if not budget:

            clearConsole()

            budget = setupBudget()

        else:

            #Si données trouvées, affichage et confirmation de récupération

            print("Nous avons résupéré des données précédentes.")

            print(f'Budget initial : {budget}€.')

            print(f'Budget restant : {budgetRestant}€.')

            print('     Est-ce bien cela ?')

            print(f"     1- Oui, continuer avec {budgetRestant}€.")

            print(f"     2- Non, recommencer à zéro.")

            #Prompt protégé

            while True :

                try:

                    choix = int(input())

                    #Si choix recommencer, initialisation

                    if(choix==2):

                        clearConsole()

                        budget = setupBudget()

                        break

                    #Sinon continuer

                    elif(choix==1):

                        break

                    else:

                        print("Choix non-valide.")

                except ValueError:

                    print("Choix non-valide.")

    while(True):

        #Affichage des choix

        print("Que souhaitez-vous faire ? ")

        print('     1- Ajouter une dépense')

        print('     2- Visionner les dépenses')

        print('     3- Supprimer une dépense')

        print('     4- Exit')

        #Choix utilisateur

        try:

            choice=int(input())

            if choice==1:

                clearConsole()

                ajoutDepense()

            elif choice == 2:

                clearConsole()

                visioDepense()

            elif choice ==3:

                clearConsole()

                supprDepense()

            elif choice==4:

                clearConsole()

                print("Goodbye.")

                exit()

            #Exception choix non-valide

            else:

                print('Choix non-valide.')

                continue

        except ValueError:

            print("Choix non-valide.")

main()
```

Ce script Python est une application de gestion de budget en ligne de commande. Il permet à l'utilisateur de suivre ses dépenses par rapport à un budget initial. Le script offre les fonctionnalités suivantes : initialiser un budget, ajouter des dépenses (avec libellé, montant et magasin), visualiser les dépenses enregistrées, et supprimer des dépenses. Les données sont stockées dans des fichiers texte (`budget.txt` pour le budget initial et restant, et `depenses.txt` pour la liste des dépenses). Le script gère les erreurs de saisie et offre une interface utilisateur simple pour interagir avec les données. Au démarrage, il vérifie si un budget a déjà été défini et permet à l'utilisateur de continuer avec le budget existant ou de recommencer à zéro.