📂 PyFileIO---python-file-manager

This is a basic command-line application written in Python that allows users to perform common file operations within the script's execution directory. It is designed as a simple, interactive tool for practicing fundamental file I/O operations.

✨ Features

The application provides a main menu interface to handle the following five core file operations:

Create File (1): Creates a new, empty file with a specified name using the exclusive creation mode ("x"). It handles cases where the file already exists.

View All Files (2): Lists the names of all files and folders in the current working directory.

Delete File (3): Deletes a file with a specified name. It handles cases where the file is not found.

Read File (4): Reads and prints the entire content of a specified file. It handles cases where the file is not found.

Edit File (5): Appends new lines of content provided by the user to the end of a specified file. It uses the append mode ("a").

🧩 Code Structure

1. The application is modularized into several functions, each dedicated to a single operation, with a central main function for execution flow and robust error handling.

2. create_file(filename): Safely creates a new file, catching FileExistsError if the file already exists.

3. view_all_files(): Retrieves and displays all items in the current directory using the os.listdir() function.

4. delete_file(filename): Removes a specified file using os.remove(), catching FileNotFoundError if the file does not exist.

5. read_file(filename): Opens, reads, and prints the file content, catching FileNotFoundError.

6. edit_file(filename): Appends new text, gathered from user input, to the end of an existing file using append mode ("a").

7. main(): The core interactive loop that handles user input, displays the application menu, and calls the corresponding file operation functions until the user chooses to exit.

🧠 Key Concepts & Knowledge Used

This application demonstrates several essential Python programming concepts:

1. File I/O Modes: It utilizes the built-in open() function with different modes:

"x" for exclusive creation (ensuring you don't overwrite an existing file).

"r" for reading content.

"a" for appending data to the end of a file.

2. Context Management (with open(...)): The code uses the with statement, which is a best practice for file handling. This ensures that the file is automatically closed, even if errors occur, preventing resource leaks.

3. Exception Handling: Robust try...except blocks are used extensively to manage anticipated issues, specifically:

FileExistsError during file creation.

FileNotFoundError during reading, deleting, or editing.

General Exception to catch unexpected errors and provide user-friendly messages.

4. OS Module Interaction: The application uses the standard os module to interact with the underlying operating system:

os.listdir() to get a list of contents in the current directory.

os.remove() to delete a file.

5. Command Line Interface (CLI) Design: The main function demonstrates a simple, persistent menu loop (while True) for user interaction via input() and print().

🛠️ Requirements

1. Python 3.x
<br>
2. The application uses only standard built-in Python modules (os and built-in file handling), so no external libraries need to be installed.

🚀 How to Run

1. Save the Code: Save the provided Python code into a file named (for example) file_manager.py.

2. Open Terminal: Navigate to the directory where you saved the file using your command line interface.

3. Execute the Script: Run the file using the Python interpreter:

4. python file_manager.py

5. Interact: The application will launch, display the menu, and prompt you to enter a choice from 1 to 6.

<img width="1920" height="1020" alt="Screenshot 2025-11-23 211046" src="https://github.com/user-attachments/assets/d1f541cc-993b-452d-ae2c-2419fbb45266" />
<img width="1920" height="1020" alt="Screenshot 2025-11-23 211105" src="https://github.com/user-attachments/assets/d0b2f868-5eeb-4608-9ea0-b898a1ab6b96" />
<img width="1920" height="1020" alt="Screenshot 2025-11-23 211118" src="https://github.com/user-attachments/assets/5a566b71-38aa-4f25-8c59-b7f5fb44efed" />

