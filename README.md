import random
import sys
import time
from colorama import Fore, init
import os
def clearConsole():
    os.system('cls' if os.name == 'nt' else 'clear')
clearConsole()
init()
def restart_program():
    print("Restarting script...")
    os.execv(sys.executable, ['python'] + sys.argv)

money = int(10)
print ("   _____     ")
print ("  /  1  \     ")
print (" | 4   2 |    ")
print ("  \__3__/     ")
while True:
    print (f"$$$ = ({money})")
    bid = int(input("how much do you want to bid?\n"))
    if bid > money:
        print("you're too broke to bid that much")
        continue
    else:
        money -= bid    
    roulette = ["1","2","3","4"]
    ans = random.choice(roulette)
    choice = input("What number do you want to bet on? (1,2,3,4)\n")
    clearConsole()
    for i in range(5):
        print ("   _____     ")
        print ("  /  o  \     ")
        print (" | 4 | 2 |    ")
        print ("  \__3__/     ")

        time.sleep(.1)
        clearConsole()

        print ("   _____     ")
        print ("  /  1  \     ")
        print (" | 4 / 2 |    ")
        print ("  \__3__/     ")

        time.sleep(.1)
        clearConsole()

        print ("   _____     ") 
        print ("  /  1  \     ")
        print (" | 4 - o |    ")
        print ("  \__3__/     ")

        time.sleep(.1)
        clearConsole()

        print ("   _____     ")
        print ("  /  1  \     ")
        print (" | 4 \ 2 |    ")
        print ("  \__3__/     ")

        time.sleep(.1)
        clearConsole()

        print ("   _____     ")
        print ("  /  1  \     ")
        print (" | 4 | 2 |    ")
        print ("  \__o__/     ")

        time.sleep(.1)
        clearConsole()

        print ("   _____     ")
        print ("  /  1  \     ")
        print (" | 4 / 2 |    ")
        print ("  \__3__/     ")

        time.sleep(.1)
        clearConsole()

        print ("   _____     ") 
        print ("  /  1  \     ")
        print (" | o - 2 |    ")
        print ("  \__3__/     ")

        time.sleep(.1)
        clearConsole()

        print ("   _____     ")
        print ("  /  1  \     ")
        print (" | 4 \ 2 |    ")
        print ("  \__3__/     ")

        time.sleep(.1)
        clearConsole()
    rand = random.randint(1,4)
    
    if ans == choice:
        print("Win :D")
        bid *=4
    else:
        print("Lose :(")
        bid *=0 
    money += bid
    if money == 0:
        print("you're out of money :(")
        break
while True:
    choice2 = input("type 'r' to restart\n")
    clearConsole()
    if choice2 == "r":
        restart_program()
