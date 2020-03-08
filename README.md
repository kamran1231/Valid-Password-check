# Valid-Password-check

# Write a Python program to check the validity of a password (input from users).
#
# Validation :
#
# At least 1 letter between [a-z] and 1 letter between [A-Z].
# At least 1 number between [0-9].
# At least 1 character from [$#@].
# Minimum length 6 characters.
# Maximum length 16 characters.


import re

psw = input('Enter the Password: ')
x = True
while x:
    if len(psw) < 6 or len(psw) > 16:
        print('Your password length is not between 6 to 16 length')
        break
    elif not re.search('[0-9]',psw):
        print('you have to use atleast one digit in your password')
        break
    elif not re.search('[a-z]',psw) or not re.search('[A-Z]',psw):
        print('you have to use atleast one capital letter in your password')
        break
    elif not re.search('[@#$]',psw):
        print('you have to use atleast one special character in your password like "@#$"')
        break
    else:
        print('Password is Valid')
        x = False
        break
if x:
    print('Invalid Password')
