from ast import literal_eval
import random

#Generate random number

def falsche_nummer(lives, count):
    lives -= 1
    count += 1
    print(f"Falsche Nummer. Verbleibende Leben: {lives}")
    return lives, count

def main():

    min = 1
    max = '50'
    number_to_be_guessed = random.randint( min, max )
    lives = 5
    count = 0

    print(f"Die kleinst mögliche Zahl ist {min} und die höchste ist {max}")

    while lives > 0:

        guess = input("Nummer eingeben: ")

        if int(guess) > int(min) or int(guess) < int(max):


            if int(guess) == int(number_to_be_guessed):
                count += 1
                print(f"Richtig. Du hast {count} Versuch/e gebraucht.")
                break
                
            elif int(guess) < int(number_to_be_guessed):
                lives, count = falsche_nummer(lives, count)
                print("Tipp: Die Gesuchte Zahl ist höher.")

            elif int(guess) > int(number_to_be_guessed):
                lives, count = falsche_nummer(lives, count)
                print("Tipp: Die Gesuchte Zahl ist niedriger.")


        elif guess < min or guess > max:
            print("Gewählte Zahl nicht im gültigen Bereich.")

    
    neues_spiel(lives, number_to_be_guessed, count)
            
    
def neues_spiel(lives, number, count):

    #Check if Player won or not
    if lives == 0:
        string_for_new_game = f"Du hast leider alle deine Leben verloren. Die gesuchte Zahl war {number}."
    else:
        string_for_new_game = f"------------Gewonnen!!!----------- \n Du hast {count} Versuche gebraucht."

    #New Game?
    new_game = input(f"{string_for_new_game} Erneut spielen? y/n: ")    
    if new_game.lower() == 'y':
        main()
    else:
        quit    




if __name__ == '__main__':
    main()    
