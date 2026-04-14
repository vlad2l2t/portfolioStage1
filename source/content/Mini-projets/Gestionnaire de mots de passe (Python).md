#python 
Projet réalisé les [[02-06]] et [[03-06]]

```python
from cryptography.fernet import Fernet

import os

  

#------------

# Keys / Setup

#------------

  

# Generate key if not already created

def gen_key():

    key = Fernet.generate_key()

    with open('key.key', 'wb') as f:

        f.write(key)

  

# Load encryption key

def load_key():

    with open('key.key', 'rb') as f:

        return f.read()

  

# Set the master password

def set_master_pwd():

    master_pwd = input("Set the master password: ")

    encrypted_pwd = fer.encrypt(master_pwd.encode())

    with open('masterPwd.txt', 'wb') as f:

        f.write(encrypted_pwd)

    print("Master password set.\n")

  

# Verify the master password

def verify_master_pwd():

    with open('masterPwd.txt', 'rb') as f:

        stored = f.read()

    attempts = 3

    while attempts > 0:

        guessed = input("What's the master password? ")

        try:

            if fer.decrypt(stored).decode() == guessed:

                return True

        except:

            pass

        print("Password incorrect.")

        attempts -= 1

    print("Too many incorrect attempts. Quitting.")

    return False

  

#----------

# Password management

#----------

  

def view():

    if not os.path.exists('passwords.txt'):

        print("You don't have any registered passwords.\n")

        return

  

    with open('passwords.txt','r') as f:

        lines = f.readlines()

        print("Here are your registered passwords:\n")

        for index, line in enumerate(lines, start=1):

            platform, user, pwd = line.strip().split(' ')

            print(f"Account n°{index}: {platform}")

            print(f"     Username: {user}")

            print(f"     Password: {fer.decrypt(pwd.encode()).decode()}\n")

  

def add():

    platform = input("For what platform is it? ")

    user = input("What's the username? ")

    pwd = input("What's the password? ")

    encrypted_pwd = fer.encrypt(pwd.encode()).decode()

    with open('passwords.txt', 'a') as f:

        f.write(f"{platform} {user} {encrypted_pwd}\n")

    print(f"Password for {platform} has been added.\n")

  

#-----

# Main

#-----

  

# Create key if missing

if not os.path.exists('key.key'):

    gen_key()

  

# Load encryption key

key = load_key()

fer = Fernet(key)

  

# Set master password if missing

if not os.path.exists('masterPwd.txt'):

    set_master_pwd()

  

# Verify master password

if not verify_master_pwd():

    exit()

  

# Main loop

while True:

    mode = input("What do you want to do? (add/view/q): ").lower()

    if mode == "q":

        print("Goodbye.")

        break

    elif mode == "view":

        view()

    elif mode == "add":

        add()

    else:

        print("Invalid mode. Use 'add', 'view', or 'q'.\n")
```

Ce script Python est un gestionnaire de mots de passe sécurisé. Il utilise la bibliothèque `cryptography` pour chiffrer les mots de passe. Le script commence par générer une clé de chiffrement unique si elle n'existe pas déjà, puis la charge. Il permet ensuite à l'utilisateur de définir un mot de passe maître, qui est également chiffré et stocké. Avant d'accéder aux fonctionnalités de gestion des mots de passe, l'utilisateur doit vérifier son mot de passe maître. Le script offre deux fonctionnalités principales : l'ajout de nouveaux mots de passe pour différentes plateformes (qui sont chiffrés avant d'être stockés) et la visualisation des mots de passe enregistrés (qui sont déchiffrés avant d'être affichés). Les mots de passe sont stockés dans un fichier texte, mais ils sont chiffrés pour protéger leur confidentialité. Le script utilise le chiffrement Fernet pour assurer la sécurité des mots de passe stockés.