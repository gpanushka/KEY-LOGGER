I created a basic keylogger program that records and logs keystrokes.

Keylogging is a malicious practice where software or hardware is used to secretly record the keys pressed on a keyboard. This stolen information can be used for various cybercrimes, making it a significant security threat.

I have used resources like Visual Studio Code as the text editor and used internet resources for debugging. This task is executed using the following steps:

<h3>Libraries:</h3>
The pynput library allows you to control and monitor/listen to your input devices such as they keyboard and mouse.

The pynput.mouse allows you control and monitor the mouse, while the pynput.keyboard allows you to control and monitor the keyboard.

We will use the pynput.keyboard module for this task.

![image](https://github.com/gpanushka/PRODIGY_CS_04/assets/167328539/3dd9bb56-48d1-43ff-9200-969a69c37119)

<h3> 'keyPressed' function:</h3>

This code defines a function keyPressed that likely captures and records keystrokes you press.


![image](https://github.com/gpanushka/PRODIGY_CS_04/assets/167328539/eedb8a3c-545f-44b2-8b84-2a5f5c3f80f3)



**The Function:**
keyPressed(key) takes a key argument, representing the pressed key.

**Showing the Key:**
It prints the key as a string, revealing which key was pressed.

**Logging Keystrokes:**
The concerning part is the file handling. It opens a file named "keyfile.txt" in append mode ('a'). This means anything written goes to the file's end, potentially creating a log of your keystrokes.

**Inside the file handling:**
It tries to get the character version of the key (e.g., 'a' for the 'a' key).
If successful, it writes that character to the open file.
If there's an error (like a key without a character), it prints an error message.

<h3>Main function:</h3>


![image](https://github.com/gpanushka/PRODIGY_CS_04/assets/167328539/8aa8f52d-7b7b-4a6c-82c9-3fb1335fe1fb)


Ensures the keyPressed function runs only when the script is directly executed.
Creates a keyboard listener that calls keyPressed whenever a key is pressed.
Pauses the program until the user presses Enter, allowing the listener to capture keystrokes.


<h2>OUTPUT:</h2>

Upon typing this in the textfile, 

![image](https://github.com/gpanushka/PRODIGY_CS_04/assets/167328539/b93be2ca-13f2-494f-b6c3-a9352c6546ff)

the terminal will give an output like this

![image](https://github.com/gpanushka/PRODIGY_CS_04/assets/167328539/a2c13453-c6ac-4717-9509-ef30ee343b90)

By clicking other keys, it detects the keys used and prints the name of the key used.

![image](https://github.com/gpanushka/PRODIGY_CS_04/assets/167328539/082d0692-6107-4900-a20e-a4f8a83ae451)
