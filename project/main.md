# project Unit 1

## Criterion A: Planning

## Problem definition

My client Mr N, is the owner the owner of a web design company. Аs the company is small the employees did not think about keeping all the passwords of their deisgn software that they use in one place under protection. At the moment they store all passwords in a shared document in Google Docs, which has only one level of protection, it implies that there is a very high risk that anyone can gain access to the document and steal all the data. The owner predicts that the company will expand in the very near future, so they want to be prepared in advance and keep all the passwords safe.

## Proposed solution

After I spoke with my client, we came up with a solution to this problem. Create a calculator program that will perform basic functions such as (addition, subtraction, multiplication, division). Also the calculator can give feedback on basic errors (e.g. division by 0). However, if user enters a secret password (for example: 1234), the program will turn into a password manager. It will be able to perform such functions as: Create, Replace, Update, Delete passwords.  This program will keep all passwords safe. 

## Success criteria

1. The calculator should accept user input to perform basic operations (addition, subtraction, multiplication, division).
1. The calculator can handle typical errors (e.g., division by zero) and give appropriate feedback.
1. If the user enters the secret code ("open123") for the first number input, the program will change modes and act as a password manager.
1. In password manager mode, the user should be able to perform CRUD operations (Create, Replace, Update, Delete):
   * Add a password (for example, for a website).
   * View the stored passwords (only if they re-enter the secret code).
1. Save passwords permanently and securely
1. Use the terminal to interact with the user.

# Criterion B: Design

### System diagram
![Untitled presentation](https://github.com/user-attachments/assets/997ed749-8fb8-4d80-a64d-787a997d3e35)
System Diagram showing the minimal requirement for the hardware and software used for proposed solution. The lock indicates encryption.

### Flow diagrams for algorithms

![Untitled Project (4)](https://github.com/user-attachments/assets/b88222bf-66dd-4cad-aae9-df3821f5724a)

This flow diagram explains to the user the steps of the function that presents a text-based menu to the user and asking them to select an option. It only accepts valid options from a menu set and returns the selected option as an integer.

--------------------------------------------------------------------------------------------------------

![Untitled Project (3)](https://github.com/user-attachments/assets/ddead595-e7c3-421d-9993-d6808b52098a)

This flow diagram explains to the user the steps of the function that displays the list of passwords in a masked format (where each character of the password is replaced by an *) along with the corresponding name.

--------------------------------------------------------------------------------------------------------

![Untitled Project (2)](https://github.com/user-attachments/assets/8af47a6e-a8a3-42b0-83d3-3c01e6149a90)

This flow diagram explains to the user the steps of the function that writes a list of passwords stored in a dictionary to a file.

### Test plan

## Criterion C: The code
1. Calculator.py
     
  from settings import *
  from password_manager import password_manager
  
  
  while True:
      num1 = input('Enter the 1st number ')
  
      if num1.lower() in ('quit', 'exit'):
          break
  
      if num1 == secretphrase:
          # go to password manager mode
          password_manager()
          continue
      a = float(num1)
      b = float(input('Enter the 2nd number '))
      op = input('Choose an operation (+-*/) ')
  
      if op == '+':
          r = a + b
      elif op == '-':
          r = a - b
      elif op == '*':
          r = a * b
      elif op == '/':
          if b == 0:
              print("Error. Division by zero is not allowed.")
              continue
          r = a / b
      else:
          print("Invalid operation. Please try again.")
          continue
  
      print(f'{a}{op}{b} = {r}')
  
2. password_manager
   from settings import *
   from os.path import exists
  
  
  def menu():
      text_menu = '''
      1. List all of the passwords
      2. Check the password in open view 
      3. Create new password
      4. Change the existing password
      5. Remove the password from list
      0. Return back to calculator mode
  Please, select one option: '''
      while True:
          print(text_menu)
          opt = input()
          if opt in '012345':
              return int(opt)
  
  def encrypt(password):
      return password[::-1]
  
  def decrypt(encrypted_password):
      return encrypted_password[::-1]
  
  def read_password_file():
      passwords = {}
      if exists(password_file_name):
          with open(password_file_name) as pf:
              for s in pf:
                  name, psw = s.split(':')
                  name = name.strip()
                  psw = psw.strip()
                  passwords[name] = decrypt(psw)
      return passwords
  
  
  def write_password_file(passwords):
      with open(password_file_name, 'w') as pf:
          for name in passwords:
              encrypted_psw = encrypt(passwords[name])
              pf.write(f'{name}:{encrypted_psw}\n')
  
  
  def print_passwords(passwords):
      if not passwords:
          print('No password')
          return False
      i = 0
      print('All passwords:')
      for name in passwords:
          psw = passwords[name]
          i += 1
          print(f'{i}. {name}: {"*" * len(psw)}')
      return True
  
  def password_manager():
      print('Welcome to Password Manager!')
      passwords = read_password_file()
      while True:
          opt = menu()
  
          if opt == 1:
              print_passwords(passwords)
  
          elif opt == 2:
              secret_input = input('Please enter the secret phrase to view passwords: ')
              if secret_input != secretphrase:
                  print("Incorrect secret phrase. Access denied.")
                  continue
              if print_passwords(passwords):
                  psw_num = int(input(f'Enter a number of password to view (1 - {len(passwords)}) '))
                  name = list(passwords)[psw_num - 1]
                  psw = passwords[name]
                  print(f'{name}: {psw}')
  
          elif opt == 3:
              name = input('Enter the name of new password ')
              psw = input('Enter the new password ')
              passwords[name] = psw
              write_password_file(passwords)
  
          elif opt == 4:
              if print_passwords(passwords):
                  psw_num = int(input(f'Enter a number of password to change (1 - {len(passwords)}) '))
                  name = list(passwords)[psw_num - 1]
                  psw = input('Enter the new password ')
                  passwords[name] = psw
                  write_password_file(passwords)
  
          elif opt == 5:
              if print_passwords(passwords):
                  name = input('Enter the name to remove from list ')
                  del passwords[name]
                  write_password_file(passwords)
  
          else:
              print('Return to calculator mode')
              return
  
3. settings.py
    secretphrase = "open123"
    password_file_name = "passwords.txt"

## Record of Tasks
| Task Number | Planned action                                                     | Planned outcome                                                                                                                                                                                | Time estimated | Target Completion Date | Criterion |
|-------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------------------|-----------|
| 1           | 1st part of 1st meeting with the client                            | Identify the problem that the client has                                                                                                                                                       | 5 min          | sep 13                 | A         |
| 2           | 2nd part of first meeting with the client                          | Brainstorm and create the solution                                                                                                                                                             | 10 min         | sep 13                 | A         |
| 3           | Plan the success criteria points                                   | The clear view of the requirements                                                                                                                                                             | 15 min         | sep 13                 | A         |
| 4           | Plan the program architecture                                      | A detailed system design for both the calculator and password manager                                                                                                                          | 1 week         | sep 17                 | B         |
| 5           | Create the flow diagrams which explain functions used in a program | The clear view for the user of how the program works                                                                                                                                           | 2 hours        | sep 19                 | B         |
| 6           | Create a system diagram                                            | System Diagram showing the minimal requirement for the hardware and software used for proposed solution                                                                                        | 1 hour         | sep 19                 | B         |
| 7           | Develop a simple calculator and hidden password manager program    | A fully functioning password manager that allows users to create, replace, update, and delete passwords which is hidden  in the calcilator and opens only when the user enters the secret code | 1 week         | sep 26                 | C         |
| 8           | Insert basic encryption                                            | Passwords are securely stored using encryption, preventing unauthorized access even if the storage is compromised                                                                              | 1 day          | sep 26                 | C         |
| 9           | Test of the program                                                | 1) A tested and reliable calculator module that performs accurate calculations and handles errors gracefully (e.g., division by zero)                                                          | 1 hour         | sep 26                 | C         |
|             |                                                                    | 2) A password manager that has been tested, ensuring that all the CRUD operations work correctly                                                                                               | 1 hour         | sep 26                 | C         |
|             |                                                                    | 3) A secure system where unauthorized users cannot access or view passwords. Passwords are encrypted                                                                                           | 1 hour         | sep 26                 | C         |
