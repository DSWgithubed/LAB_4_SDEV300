'''This program will allow the user to enter a a phone
number and a zipcode with an additonal 4 digits attached.

'''
#David Warren SDEV 300 April 12
import numpy as np

def welcome():
    '''This is the welcome message.

    This function prints a welcome message to the user'''
    print("********** Welcome to the Python Matrix Application **********")

def menu_option():
    '''This is for the first menu option for the user.

    This function prints out the first menu option'''
    print ("Do you want to play the Matrix Game? ")
    game_option =""
    while game_option not in ["Y","N"]:
        game_option = input("Enter Y for Yes or N for No: ").upper()
    return game_option

def menu_phone():
    '''This funciton will allow the user to input phone number

    If the user's phone number does not match the format it will reject'''
    phone_number = input("Enter your phone number (XXX-XXX-XXXX): ")
    valid_phone_number(phone_number)

def valid_phone_number(phone_number):
    '''Function to validate phone number.

    Validates the format of the function.'''
    valid = False
    while valid == False:
        while len(phone_number) != 12:
            print("Phone number needs to be in (XXX-XXX-XXXX) format")
            phone_number = input("Enter your phone number (XXX-XXX-XXXX): ")
        try:
            if phone_number[3] != '-' or phone_number[7] != "-":
                phone_number = input("Phone number is not in the correct format. Please re-enter: ")

            if phone_number[:3].isalpha() or phone_number[4:7].isalpha()\
                 or phone_number[8:12].isalpha():
                print("Invalid format. ")
                phone_number = input("Phone number is not in the correct\
                 format. Please re-enter: ")
            elif phone_number[:3].isdigit() and phone_number[4:7].isdigit() and phone_number[8:12].isdigit():
                valid = True
        except IndexError:
            print("Try a valid number and format! ")
            phone_number = input("Phone number is not in the correct format. Please re-enter: ")
def zip_code ():
    '''This function collect zip codes.

    Zip codes are passed here.'''
    z_code = input("Enter your zip code+4 (XXXXX-XXXX) :")
    valid_zip_code(z_code)

def valid_zip_code(z_code):
    '''This function validates zip codes.

    Take in zip code to validate.'''
    valid = False
    while valid == False:
        while len(z_code) != 10:
            z_code = input ("Zip code is not in the correct format. Please re-enter: ")
        try:
            if z_code[5] != '-':
                z_code = input ("Zip code is not in the correct format. Please re-enter: ")

            if z_code[:5].isalpha() or z_code[5:9].isalpha():
                print("Invalid format. ")
                z_code = input ("Zip code is not in the correct format. Please re-enter: ")
            elif z_code[:5].isdigit() and z_code[6:9].isdigit():
                valid = True

        except IndexError:
            print("Try a valid number and format! ")
            z_code = input ("Zip code is not in the correct format. Please re-enter: ")

def matrix_1():
    '''Collects number for 1st matrix

    Numbers ge put inside for collection.'''
    print ("Enter your first 3x3 matrix: ")
    ac = []
    matrix1 = []
    first = None

    for i in range(3):
        for j in range(3):
            while True:
                try:
                    first= int(input (""))
                    if first in [0,1,2,3,4,5,6,7,8,9]:
                        ac.append(first)
                        break
                        print(end = "")
                except ValueError:
                    print("Enter a numerical value. ")

    matrix1.append(ac)
    matrix1 = np.array(matrix1)
    matrix1 = matrix1.reshape(3,3)
    print (matrix1)
    return matrix1

def matrix_2 ():
    '''Collects info for matrix.

    Collects all infor for second matrix.'''
    print ("Enter your second 3x3 matrix: ")
    ac = []
    matrix2 = []
    first = None

    for i in range(3):
        for j in range(3):
            while True:
                try:
                    first= int(input (""))
                    if first in [0,1,2,3,4,5,6,7,8,9]:
                        ac.append(first)
                        break
                        print(end = "")
                except ValueError:
                        print("Enter a numerical value. ")

    matrix2.append(a)
    matrix2 = np.array(matrix2)
    matrix2 = matrix2.reshape(3,3)
    print (matrix2)
    return matrix2

def menu_2():
    '''Second menu options.

    Dsiplays second menu.'''
    print("Select a Matrix Operation from the list below: ")
    print("")
    print("a. Addition")
    print("b. Subraction")
    print("c. Matrix Multiplication")
    print("d. Element by element multiplication\n")

    menu_2_selection = input("").lower()
    while menu_2_selection not in ["a","b","c","d"]:
        menu_2_selection = input("Invalid menu selection, try again.")
    return menu_2_selection

def menu_2_valid(menu_2_selction, matrix1, matrix2):
    '''Validates menu options.

    Validates options.'''
    if menu_2_selction == "a":
        addition_matrix(matrix1, matrix2)
    elif menu_2_selction == "b":
        subraction_matrix(matrix1,matrix2)
    elif menu_2_selction == "c":
        matrix_muliplication(matrix1,matrix2)
    elif menu_2_selction == "d":
        element_multiplication(matrix1,matrix2)

def addition_matrix(matrix1, matrix2):
    '''Addition matrix.

    Addition matrix.'''
    print("You selected Addition. The results are: ")
    added = np.array(matrix1 + matrix2)
    print(added)
    transpose(added)

def subraction_matrix(matrix1, matrix2):
    '''Subraction matrix collect.

    Collects subraction matrix info.'''
    print("You have selected Subraction. The results are: ")
    minus = np.array(matrix1- matrix2)
    print(minus)
    transpose(minus)

def goodbye_message():
    '''Display goodbye.

    Displays goodbye to user. '''
    print("*********** Thanks for playing Python Numpy ***********")

def transpose(action):
    '''Transposes matrix.

    Transposes matrixs.'''
    print("The Transpose is: ")
    action = np.array(action)
    action = action.transpose()
    print(action)
    print("The row and column mean values of the results are: ")
    print("Row: ",   action.mean(axis= 1))
    print("Column: ",  action.mean(axis= 0))

def matrix_muliplication(matrix1, matrix2):
    '''Performs multiplication.

    Does the mulitplication on the matrix'''
    print("You have selected Matrix Multiplication. The results are: ")
    matrix_multi = np.matmul(matrix1,matrix2)
    print(matrix_multi)
    transpose(matrix_multi)

def element_multiplication(matrix1, matrix2):
    '''Does elemental multiplication on elements.

    Completes element multiplication.'''
    print("You have selected Element by Element multiplication ")
    element_multi = np.array(matrix1 * matrix2)
    print(element_multi)
    transpose(element_multi)
def main():
    '''This is the main function.

    Main function to execute.'''
    welcome()
    game_option = "Y"
    while game_option == "Y":
        game_option = menu_option()

        if game_option == "Y":
            menu_phone()
            zip_code()
            matrix1 = matrix_1()
            matrix2 = matrix_2()
            menu_2_selection = menu_2()
            menu_2_valid(menu_2_selection,matrix1, matrix2)
    goodbye_message()

main()
