# devine-un-nombre2
import random

def devine_le_nombre():
    nombre_a_deviner = random.randint(1, 100)
    print("J'ai choisi un nombre entre 1 et 100. Devine lequel !")

    while True:
        reponse = input("Entre un nombre : ")

        try:
            reponse_int = int(reponse)
        except:
            print("Ce n'est pas un nombre valide.")
            continue

        if reponse_int < 1 or reponse_int > 100:
            print("Le nombre doit être entre 1 et 100.")
            continue

        if reponse_int == nombre_a_deviner:
            print("Bravo, tu as deviné le nombre !")
            break
        elif reponse_int < nombre_a_deviner:
            print("Le nombre que j'ai choisi est plus grand.")
        else:
            print("Le nombre que j'ai choisi est plus petit.")

if __name__ == '__main__':
    devine_le_nombre()
