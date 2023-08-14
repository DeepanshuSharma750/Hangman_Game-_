import random

word = ["apple", "mango", "orange", "pineapple", "watermelon", "banana", "graves", "gauva", "lychee"]
lives = 10
choice_word = random.choice(word)
 print(choice_word)
list = []
for blanks in choice_word:
    list += "_"
print(list)
game_over = False
while not game_over:
    guesses_word = input("guesses the word:-")
    guesses_word = guesses_word.lower()
    for position in range(len(choice_word)):
        letter = choice_word[position]
        if letter == guesses_word:
            list[position] = guesses_word
            print(list)
            print("You are amazing")
    if guesses_word not in choice_word:
        lives -= 1

        print("You have only %s chance" % lives)
        if lives == 0:
            game_over = True
            print("You lose the game!!")
            print("please try again")
    if "_" not in list:
        game_over = True
        print("You win the game!!")
# Hangman_Game-_
Games make your life easy and funny
