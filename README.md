- 👋 Hi, I’m ahmed khalid
- project name "Menu-Driven"


 "Menu-Driven"

 description:

  Dining Decision Assistant is an interactive, easy-to-use program that provides options for lunch and dinner


********

مساعد اتخاذ القرارات في تناول الطعام" هو برنامج تفاعلي وسهل الاستخدام يوفير خيارات لتناول الغداء والعشاء

The Menu-Driven Assembly Program is a simple interactive application designed to provide users with options to choose between lunch, dinner,
or exit.
Developed in assembly language, this program offers a basic structure that can be expanded with specific functionality in each section.



Menu-Driven Assembly Program

Overview:

The Menu-Driven Assembly Program is a simple interactive application designed to provide users with options to choose between lunch, dinner, or exit. Developed in assembly language, this program offers a basic structure that can be expanded with specific functionality in each section.

Features:

-Menu Options:

Users are presented with a menu, including options for lunch, dinner, and exiting the program.
-User Interaction:

The program accepts user input, allowing users to make a selection based on the presented menu.
-Modular Structure:

The program is organized into sections for lunch, dinner, exit, and handling invalid input, providing a modular and extensible framework.
-Result Display:

After each user selection, the program displays a result, providing feedback to the user.
-Error Handling:

The program gracefully handles invalid user input, ensuring a user-friendly experience.

usage Instructions:

-Run the Program:

Execute the program to initiate the menu-driven application.
-Input Selection:

Enter the numeric value corresponding to the desired option:
1 for lunch
2 for dinner
3 to exit
-View Result:

The program processes the user's choice, displays a result, and provides further instructions.

-the code:
<.data
    prompt1 db 13, 10, "Enter a choice for Lunch: $"
    prompt2 db 13, 10, "Enter a choice for Dinner: $"
    prompt3 db 13, 10, "Enter a choice for Exit: $"
    result db 13, 10, "Result: $"

    ; Add more prompts and results as needed

_start:
    ; Initialization
    mov ah, 9
    lea dx, prompt1
    int 21h

    ; Get user input
    mov ah, 1
    int 21h
    sub al, '0' ; Convert ASCII to numeric value

    ; Handle user input
    cmp al, 1
    je Lunch

    cmp al, 2
    je Dinner

    cmp al, 3
    je Exit

    jmp Invalid

Lunch:
    ; Code for Lunch section
    ; ...

    ; Display result
    mov ah, 9
    lea dx, result
    int 21h

    ; Exit or go back to the main menu
    jmp ExitOrMainMenu

Dinner:
    ; Code for Dinner section
    ; ...

    ; Display result
    mov ah, 9
    lea dx, result
    int 21h

    ; Exit or go back to the main menu
    jmp ExitOrMainMenu

Exit:
    ; Code for Exit section
    ; ...

    ; Display result
    mov ah, 9
    lea dx, result
    int 21h

    ; Exit the program
    int 20h

Invalid:
    ; Code for handling invalid input
    ; ...

    ; Display result
    mov ah, 9
    lea dx, result
    int 21h

ExitOrMainMenu:
    ; Display options for Exit or Main Menu
    ; ...

    ; Get user input
    mov ah, 1
    int 21h
    sub al, '0' ; Convert ASCII to numeric value

    ; Handle user input
    cmp al, 1
    je Exit

    cmp al, 2
    je _start ; Go back to the main menu

    jmp Invalid>


thank you!
