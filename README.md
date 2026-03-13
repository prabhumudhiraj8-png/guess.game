

import random


print("1.Computer guess game with no limit and 10 highest integer number\n")

def guess(num):
    low=1
    high=num
    feedback=""
    while feedback!="c" and not(low==high):
        guess=random.randint(1,num)
        feedback=input(f"system guess {guess} low/high,correct(l/h/c):   ")
        if feedback=="h":
             low=guess-1
        elif feedback=="l":
            high=guess+1
        elif feedback not in("c","h","l"):
            print("An a error invalid letter")
    print(f"correct guess which is {guess}\n")

guess(10)


print("4.Player's guess game of limit 10 highest 1000 integer number\n")

random_number=random.randint(1,1000)
guess=0
count_guess=1
limit_guess=11
out_of_guess=False

while random_number!=guess and not(out_of_guess):
    if(count_guess<limit_guess):
        print(f"S.NO {count_guess}:")
        guess = int(input("Enter the integer number that system guessing:   "))
        count_guess+=1
    else:
        out_of_guess=True

    if(random_number>guess and not(out_of_guess)):
        print("increases the integer number")
    elif(random_number<guess and not(out_of_guess)):
        print("decreases the integer number")
    elif(random_number==guess):
        print(f"right guess {random_number}\n")
    elif(out_of_guess):
        print(f"out of guess well correct guess is {random_number}\n")


print("2.Computer guess game with limit 5 and 10 highest integer number\n")


for i in range(1,6):
    low = 1
    high = 11
    random_number = random.randint(1, 10)
    print(f"S.NO {i}:")
    correct_or_wrong = input(f"System guess {random_number} low,high or correct (l/h/c):    ")
    guess=random_number
    if correct_or_wrong == "h":
        low = guess - 1
    elif correct_or_wrong == "l":
        high = guess + 1
    elif correct_or_wrong=="c":
        print(f"Correct guess of number {random_number}\n")
        break
    elif correct_or_wrong not in("h","l","c"):
        print("Error invalid word")
    if i==5:
        print("out of guess\n")

print("3.player's guess game with noo limit highest 10 integer number\n")

def guess_computter(x):

    random_number=random.randint(1,x)
    guess=0
    while random_number!=guess:

        guess=int(input("Enter the integer number that system guessing:    "))
        if random_number>guess:
            print("increases the integer number")
        elif random_number<guess:
            print("decreases the integer number")
    print(f"CONGRATULATION right guess which is {random_number}\n")

guess_computter(10)


print("4.Player's guess game of limit 10 highest 1000 integer number\n")

random_number=random.randint(1,1000)
guess=0
count_guess=1
limit_guess=11
out_of_guess=False

while random_number!=guess and not(out_of_guess):
    if(count_guess<limit_guess):
        print(f"S.NO {count_guess}:")
        guess = int(input("Enter the integer number that system guessing:   "))
        count_guess+=1
    else:
        out_of_guess=True

    if(random_number>guess and not(out_of_guess)):
        print("increases the integer number")
    elif(random_number<guess and not(out_of_guess)):
        print("decreases the integer number")
    elif(random_number==guess):
        print(f"right guess {random_number}\n")
    elif(out_of_guess):
        print(f"out of guess well correct guess is {random_number}\n")


print("5.Your guess with 5 limit and 10 integer number\n")

random_number = random.randint(1, 10)

for i in range(1,6):
    print(f"S.NO {i}:")
    guess=int(input("Enter the random integer number:    "))

    if random_number<guess:
        print("decreases the random integer number")
    elif random_number>guess:
        print("increases the random integer number")
    elif random_number==guess:
        print(f"correct guess {random_number}\n")
        break

    if i==5:
        print(f"out of guesses and the correct guess is {random_number}\n")
