# python game
import random

print("welcome to rock paper scissor game")

while True:
   print("Enter choice: \n 1. Rock \n 2. Paper \n 3. Scissor ")

   choice = int(input("Users turn: "))

   while choice > 3 or choice < 1:
      choice = int(input("Enter valid choice: "))

   if choice == 1:
      choice_name = 'Rock'
   elif choice == 2:
      choice_name = 'Paper'
   else:
      choice_name = 'Scissor'

   print("user choice is: " + choice_name)
   print("\n Now it's computer turn..")

   comp_choice = random.randint(1, 3)

   while comp_choice == choice:
      comp_choice == random.randint(1, 3)
   
   if comp_choice == 1:
      comp_choice_name = 'Rock'
   elif comp_choice == 2:
      comp_choice_name = 'Paper'
   else:
      comp_choice_name = 'Scissor'

   print("computer choice is: " + comp_choice_name)
   print(choice_name + "vs" + comp_choice_name)

   if ((choice == 1 and comp_choice == 2) or 
   (choice == 2 and comp_choice == 1)):
       print("Paper wins => ", end = "")
       result = "Paper"
   elif ((choice == 1 and comp_choice == 3) or
   (choice == 3 and comp_choice == 1)):
       print("Rock wins =>", end = "")
       result = "Rock"
   else:
      print("Scissor wins =>", end = "")
      result = "Scissor"

   if result == choice_name:
      print("user wins")
   else:
      print("computer wins")

   print("do you want to play again? (Y/N)")
   ans = input()

   if ans == 'n' or ans == 'N':
      break

print("\n Thanks for playing") 











