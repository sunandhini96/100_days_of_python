# Task 1: Treasure Map

Instructions

To write a program that will mark a spot on a map with an X.

![image](https://github.com/sunandhini96/100_days_of_python/assets/63030539/58c31795-a43f-41a3-8e15-20a1dc6ffe38)


So an input of A3 should place an X at the position shown below:

![image](https://github.com/sunandhini96/100_days_of_python/assets/63030539/c87aac71-9bc4-49f6-9706-97ab7c291ca5)

## Example Input 1
B3
## Example Output 1
Hiding your treasure! X marks the spot.
```
['⬜️', '️⬜️', '️⬜️']
['⬜️', '⬜️', '️⬜️']
['⬜️️', 'X', '⬜️️']
```
## Solution : 

```
line1 = ["⬜️","️⬜️","️⬜️"]
line2 = ["⬜️","⬜️","️⬜️"]
line3 = ["⬜️️","⬜️️","⬜️️"]
map = [line1, line2, line3]
print("Hiding your treasure! X marks the spot.")
position = input() # Where do you want to put the treasure?
letter = position[0]
first =int(position[1])-1
if letter == "A":
  map[first][0] = "X"
elif letter == "B":
  map[first][1] = "X"
else:
  map[first][2] = "X"

print(f"{line1}\n{line2}\n{line3}")
```
## Output : 

TEST CASE 1

### Input   :  B3
### Output

Hiding your treasure! X marks the spot.
```
['⬜️', '️⬜️', '️⬜️']
['⬜️', '⬜️', '️⬜️']
['⬜️️', 'X', '⬜️️']
```


# Task 2: 
## Rock, Paper, Scissors game:
### Code:
```
import random
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''
game_images = [rock, paper, scissors]
our_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.\n"))

if our_choice < 0 or our_choice >= 3:
  print("invalid number ! Try again ")
else:
  print(game_images[our_choice])


  computer_choice = random.randint(0,2)
  print("computer chose: ")
  print(game_images[computer_choice])
  
  if computer_choice == our_choice:
    print("It's a tie!")
  elif computer_choice == 0 and our_choice == 2:
    print("You Lose!")
  elif computer_choice == 2 and our_choice == 0:
    print("You Win!")
  elif computer_choice > our_choice:
      print("You Lose!")  
  elif our_choice > computer_choice:
      print("You Win!")
```
### Output:
What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.

1
```
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
```
computer chose: 
```
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
```
You Win!
