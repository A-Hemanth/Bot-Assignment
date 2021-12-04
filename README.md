#Q.6  Unique-dictionaries


dict_list=[{'name': 'affirm', 'confidence': 0.9448149204254}, {'name': 'affirm', 'confidence': 0.944814920425415}, {'name': 'inform', 'confidence': 0.9842240810394287}, {'name': 'inform', 'confidence': 0.9842240810394287}] 
dict_list_uniq = []
for data in dict_list:
    if data not in dict_list_uniq:
        dict_list_uniq.append(data)
print(dict_list_uniq)

#OR


dict_list=[{'name': 'affirm', 'confidence': 0.9448149204254}, {'name': 'affirm', 'confidence': 0.944814920425415}, {'name': 'inform', 'confidence': 0.9842240810394287}, {'name': 'inform', 'confidence': 0.9842240810394287}] 
dict_list_updated = [ str(item) for item in dict_list]
unique_set = set(dict_list_updated)
print(unique_set)

-----------------------------------------------------------------------------------------------------------------------
#Q.7 Password Code

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

---------------------------------------------------------------------------------------------------------
#Q.8  Combine two dictionary


d1 = {'a': 100, 'b': 200, 'c':300}
d2 = {'a': 300, 'b': 200, 'd':400}
for key in d2:
    if key in d1:
        d1[key] = d2[key] + d1[key]
    else:
        d1[key]= d2[key]
print(d1)
