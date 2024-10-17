# Brute-Force-Attack-
This project simulates a Brute Force Attack using Python to demonstrate how a brute force algorithm attempts to crack a password by trying every possible combination. The script randomly generates a 4-character password and then tries to guess it using brute force until the correct combination is found.

Project Overview
Features:
Random Password Generation: A 4-character password consisting of random ASCII characters is generated.
Brute Force Algorithm: The algorithm attempts to guess the password by generating random combinations of characters until the correct one matches.
Security Awareness: This project illustrates how brute force attacks work and highlights the importance of strong passwords in cybersecurity.
Prerequisites:
Python 3.x
random module (built-in to Python)
How It Works:
Password Generation: A random 4-character password is created using ASCII characters between 60 and 70.
Brute Force Attack: The program generates random 4-character combinations until it matches the generated password.
Result: The program informs whether the password is hacked or not after each attempt, and stops when the correct password is found.


import random as ran  # Import the random module to generate random numbers

# Step 1: Create the original password
original_password = []  # Initialize an empty list to store the password

# Generate a 4-character password
for i in range(4):
    a = chr(ran.randint(60,70))  # Generate a random ASCII character between 60 and 70
    b = str(a)  # Convert the character to a string
    c = original_password.append(b)  # Append the character to the original_password list
    length = len(original_password)  # Check the length of the password
    print(length)  # Print the current length
    if length == 4:
        pass  # Once the password has 4 characters, exit the loop
        break

# Step 2: Brute Force Attack
while True:
    brute_Force_Attack = []  # Initialize an empty list for the brute force attempt

    # Generate a random 4-character password guess
    for i in range(4):
        Simple_password = (chr(ran.randint(60,70)))  # Randomly select a character between 60 and 70
        string_con = str(Simple_password)  # Convert the character to a string
        brute_Force_Attack.append(string_con)  # Add the guessed character to the brute_Force_Attack list
        length_ = len(brute_Force_Attack)  # Check the length of the guessed password
        if length_ == 4:
            print()  # If it's 4 characters, stop generating more characters

    # Step 3: Compare the brute force attempt with the original password
    if brute_Force_Attack != original_password:
        print(brute_Force_Attack, '*===*', original_password)  # Print both passwords for comparison
        print("Password is not hacked.")  # Inform that the password has not been hacked yet

    else:
        brute_Force_Attack == original_password  # If the guess matches the original password
        print(brute_Force_Attack, '*===*', original_password)  # Print both passwords
        print('PASSWORD IS HACKED')  # Inform that the password has been hacked
        break  # Exit the loop once the password is hacked

Conclusion:
This project provides a basic understanding of how brute force attacks work by generating a random password and attempting to guess it through multiple iterations. It demonstrates why using strong, complex passwords is crucial to avoid vulnerabilities in security systems.
