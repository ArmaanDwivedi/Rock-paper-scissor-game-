# Rock-paper-scissor-game-
Single player game 

import random 
   
def game(device, you):
       if device==you:
          return None
       elif device== 'r':
            if you== 'p':
               return True
            elif you== 's':
               return False
       elif device== 'p':
            if you== 's':
               return True
            elif you== 'r':
               return False
       
       elif device== 's':
            if you== 'r':
               return True
            elif you== 'p':
               return False

print("device turn : rock(r) paper(p) scissor(s)") 
randno = random.randint(1, 3)
if randno ==1:
       device= 'r'
elif randno == 2:
       device= 'p'
elif randno == 3:
       device= 's'
you = input("your turn : rock(r) paper(p) scissor(s)") 
a= game(device, you)

print(f"device chose {device}")
print(f"you chose {you}")
    
if a==None:
       print("tie")
elif a:
       print("you win")
else:
       print("you lose")
