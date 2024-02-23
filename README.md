Create a basic keylogger program that records and logs keystrokes. Focus on logging the keys pressed and saving them to a file. Note: Ethical considerations and permissions are crucial for projects involving keyloggers.
from pynput import keyboard
This line imports the keyboard module from the pynput library, which is used for monitoring and controlling input devices, such as keyboards and mice.
def keyPressed(key):
    print(str(key))
    with open("keylog.txt", 'a') as logkey:
        try:
           char = key.char
           logkey.write(char)
        except:
            print("Error getting char")

This block defines a function named keyPressed that takes a key parameter. Inside the function, it prints the string representation of the key to the console.
It then opens a file named "keyfile.txt" in append mode ('a') and attempts to get the character representation of the key (key.char).
If successful, it writes the character to the file. If there's an exception (error) during this process, it prints an error message.

The input() function is included to keep the script running indefinitely until the user manually terminates it.

In summary, the code sets up a keylogger using the pynput library, defining a callback function to handle key presses and logging them to a file named "keylog.txt".
The script continues running until the user manually stops it.
