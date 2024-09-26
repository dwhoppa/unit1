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

### Flow diagrams for algorithms

![Untitled Project (4)](https://github.com/user-attachments/assets/b88222bf-66dd-4cad-aae9-df3821f5724a)

This flow diagram explains to the user the steps of the function that presents a text-based menu to the user and asking them to select an option. It only accepts valid options from a menu set and returns the selected option as an integer.

--------------------------------------------------------------------------------------------------------

![Untitled Project (3)](https://github.com/user-attachments/assets/ddead595-e7c3-421d-9993-d6808b52098a)

This flow diagram explains to the user the steps of the function that displays the list of passwords in a masked format (where each character of the password is replaced by an *) along with the corresponding name.

--------------------------------------------------------------------------------------------------------

![Untitled Project (2)](https://github.com/user-attachments/assets/8af47a6e-a8a3-42b0-83d3-3c01e6149a90)

This flow diagram explains to the user the steps of the function that writes a list of passwords stored in a dictionary to a file.

### Data storage

### Sketches of the application (wireframe diagrams)

### Test plan

## Record of Tasks
| Task Number | Planned action                            | Planned outcome                          | Time estimated | Target Completion Date | Criterion |
|-------------|-------------------------------------------|------------------------------------------|----------------|------------------------|-----------|
| 1           | 1st part of 1st meeting with the client   | Identify the problem that the client has | 5 min          | sep 13                 | A         |
| 2           | 2nd part of first meeting with the client | Brainstorm and create the solution       | 10 min         | sep 13                 | A         |
| 3           | Plan the success criteria points          | The clear view of the requirements       | 15 min         | sep 13                 | A         |
