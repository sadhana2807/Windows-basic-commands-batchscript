# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
<img width="887" height="111" alt="image" src="https://github.com/user-attachments/assets/dbe01196-07dc-4a59-8f77-129aa05a7c94" />


Remove the directory "my-folder"
## COMMAND AND OUTPUT


Create the file Rose.txt

## COMMAND AND OUTPUT

<img width="767" height="107" alt="image" src="https://github.com/user-attachments/assets/51272f60-c782-4e9d-8ac6-6479a250e932" />

<img width="827" height="258" alt="image" src="https://github.com/user-attachments/assets/da08de66-9af1-490c-9de5-d012ea50e9bf" />

Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="819" height="107" alt="image" src="https://github.com/user-attachments/assets/ff1e4a6f-a267-4b61-a658-8189100dc53f" />


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="671" height="62" alt="image" src="https://github.com/user-attachments/assets/2980c81b-f9d1-4e8c-91c7-4fea4bd03396" />


Remove the file hello1.txt

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="658" height="171" alt="image" src="https://github.com/user-attachments/assets/0a564d49-d027-467a-a586-855abb6c355a" />


List out all the associated file extensions 

## COMMAND AND OUTPUT
<img width="614" height="218" alt="image" src="https://github.com/user-attachments/assets/37b1a96a-b22f-438d-824d-3e3f1011bbbe" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="574" height="613" alt="image" src="https://github.com/user-attachments/assets/8aa73f02-8362-406b-a8f6-f2c36138fe17" />


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
~~~
@echo off
set name=John
echo Hello, %name%!
pause
~~

## OUTPUT
<img width="506" height="80" alt="image" src="https://github.com/user-attachments/assets/6de5779c-bfe2-479d-9d82-8bd5348dcedc" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

~~~
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
~~~

## OUTPUT
<img width="664" height="159" alt="image" src="https://github.com/user-attachments/assets/a02b5bab-8812-4fbc-9e9e-0f16c12fdfd2" />


Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
~~~
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
~~~

## OUTPUT

<img width="550" height="204" alt="image" src="https://github.com/user-attachments/assets/6a113f0b-76f9-4d54-84b4-4f2e3c20eb3d" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
~~~
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
~~~

## OUTPUT
<img width="488" height="80" alt="image" src="https://github.com/user-attachments/assets/07f2ac7a-785a-466a-9d39-7725ae1cb060" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
~~~
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause
~~~


## OUTPUT

<img width="466" height="298" alt="image" src="https://github.com/user-attachments/assets/e6581a23-a4d2-4818-98b8-8cf3ed936f87" />


# RESULT:
The commands/batch files are executed successfully.

