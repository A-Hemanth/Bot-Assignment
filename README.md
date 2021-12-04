# Bot-Assignment 
Q.7 Password Code
import re
password= input("Input your password :")
x = True
while x:  
    if (len(password)<6 or len(password)>16):
        break
    elif not re.search("[a-z]",password):
        break
    elif not re.search("[0-9]",password):
        break
    elif not re.search("[A-Z]",password):
        break
    elif not re.search("[!\"#$%&'()*+,-./:;<=>?@[\]^_`{|}~]",password):
        break
    elif re.search("\s",password):
        break
    else:
        print("Valid Password")
        x=False
        break

if x:
    print("Not a Valid Password")
