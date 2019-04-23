# Guessing-Game
Guessing game

# secret word variable
secret_word = "chicken"
# guess input variable left blank for user input later on
guess = ""
# guess count variable to monitor how many guesses the user has input into the game
guess_count = 0
# guess limit variable to limit the use to a maximum of 10 guesses per game
guess_limit = 10
# out of guesses variable, if the limit reaches the maximum guesses the game ends
out_of_guesses = False


# != if the guess hasn't reached the secret_word the game will continue if they aren't out_of_guesses
while guess != secret_word and not(out_of_guesses):
    # if the guess count is below the limit the game continues
    if guess_count < guess_limit:
        # while the guess_count is below the limit and the user hasn't guessed the word the game continues and loops
        # adding +1 to the guess_count
        guess = input("Enter guess: ")
        guess_count += 1
        # if out_of_guesses is = to True the game ends
    else:
        out_of_guesses = True
# if out_of_guesses you print out the lose string
if out_of_guesses:
    print("You ran out of guesses, better luck next time.")
# if the user guesses the secret_word then you print out the winning string
else:
    print("YOU WIN! HOW DID YOU GUESS THAT?")
