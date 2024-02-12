import random
import time

def jeu_de_lettre():
    lettres = "azertyuiopqsdfghjklmwxcvbn"
    lettre_a_deviner = random.choice(lettres)

    print("Bienvenue dans le jeu de devinette de lettre!")
    print("Une lettre a été choisie au hasard. Devinez quelle est cette lettre.")

    while True:
        essai = input("Devinez une lettre : ")

        if essai == lettre_a_deviner:
            print("Bravo! Vous avez deviné la lettre correctement.")
            choix = input("Voulez-vous rejouer? (oui/non) : ")
            if choix.lower() == "oui":
                jeu_de_lettre()
            else:
                print("Merci d'avoir joué!")
            break

        else:
            print("Dommage! Essayez encore.")
            time.sleep(3)

if __name__ == "__main__":
    jeu_de_lettre()
