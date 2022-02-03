# Python-built-in-modules-problems
Python built-in modules like random and there types problems
'''
#1. Write a Python program to generate a random color hex,
#a random alphabetical string, random value between two integers (inclusive) and a random multiple of 7 between 0 and 70. Use random.randint()
#sol:

import  random
import string
# case 1
print('generate a random colour hex: ', end = ' ')
print('#{:06x}'.format(random.randint(0,0xFFFFFFFFF)))
#case2
print('\ngenerate a random alphabetical string:')
max_length = 255
s = ''
for i in range(random.randint(1,max_length)):
    s += random.choice(string.ascii_letters)
print(s)
#case 3
print('generate a random value between two integers, inclusive: ')
print(random.randint(0,10))
print(random.randint(-7,7))
print(random.randint(1,1))
#case 4
print('generate a random multiple of 7 between 0 and 70: ')
print(random.randint(0,10)*7)
####
___________________________________________________________________________________________________
#2. Write a Python program to select a random element from a list, set,
#dictionary (value) and a file from a directory. Use random.choice()
#sol:
import  random
import os
#case 1
print('random elements from a list: ')
elements = [1,2,3,4,5,6,7,8,9]
print(random.choice(elements))
print(random.choice(elements))
print(random.choice(elements))

# case 2
print('\nselect a random alue from a set:')
elements = set([1,2,3,4,5,6,7,8,9])
#sets are inalid input so convert it into tuple
print(random.choice(tuple(elements)))
print(random.choice(tuple(elements)))
print(random.choice(tuple(elements)))

#case 3
print('select random value from dict: ')
d = {'a':1, 'b':2, 'c':3, 'd':4}
key = random.choice(list(d))
print(d[key])
key = random.choice(list(d))
print(d[key])

print(' select a random file from directory:')
print(random.choice(os.listdir('/')))
___________________________________________________________________________________________________

#3. Write a Python program to generate a random
# alphabetical character, alphabetical string and alphabetical string
# of a fixed length. Use random.choice()
#sol:
import random
import string

#case 1
print('generate random alphabet char:')
print(random.choice(string.ascii_letters))

#case2
print('generate a random alphabet string: ')
max_len = 255
s=''
for i in range(random.randint(1,max_len)):
    s += random.choice(string.ascii_letters)
print(string)

#csae 3
print('generate a random alphabet string of fixed length')
s = ''
for i in range(10):
    s += random.choice(string.ascii_letters)
print(s)
___________________________________________________________________________________________________

#4. Write a Python program to construct a seeded random number generator,
# also generate a float between 0 and 1, excluding 1. Use random.random()
#sol:
import random
#case 1
print('constructed a random no. generator: ')
print(random.Random().random())
print(random.Random(0).random())

# case 2
print('generate a float bet 0 and 1, excluding 1:')
print(random.random())

___________________________________________________________________________________________________

#5. Write a Python program to generate a random integer between 0 and 6
# - excluding 6, random integer between 5 and 10 - excluding 10, random
# integer between 0 and 10, with a step of 3 and random date
# between two dates. Use random.randrange()
#sol
import random
#case1
print('generate random int no. bet 0 and 6: ')
print(random.randrange(5))
print('generate random int no. bet 5 and 10: ')
print(random.randrange(start=5, stop=10))
print('generate random int no. bet 0 and 10 with a step of 3: ')
print(random.randrange(start=0, stop=10, step=3))

#case2
import datetime
print('random date bet two dates:')
start_dt = datetime.date(2021, 5, 7 )
end_dt= datetime.date(2022, 5, 2)
time_between_dates = end_dt - start_dt
days_betweens_dates = time_between_dates.days
random_number_of_days = random.randrange(days_betweens_dates)
random_date = start_dt + datetime.timedelta(days=random_number_of_days)
print(random_date)

_______________________________________________________________________________________

#6. Write a Python program to shuffle the elements of a given list. Use random.shuffle()
#sol

import random
n = [ 1,2,3,4,5,6]
print('origional no.')
print(n)
random.shuffle(n)
print('shuffle no.')
print(n)

words = ['red', 'black', 'green', 'blue']
print("Original list:")
print(words)
random.shuffle(words)
print("Shuffle list:")
print(words)

_______________________________________________________________________________________

#7. Write a Python program to generate a float between 0 and 1, inclusive
# and generate a random float within a specific range. Use random.uniform()

#sol
import random
print('generate a float bet 0 and 1 ')
print(random.uniform(0,1))

print('generate a random float within a sp. range ')
random_float= random.uniform(1.0,3.0)
print(random_float)

__________________________________________________________________________________________________

#8. Write a Python program to create a list of random integers
# and randomly select multiple items from the said list. Use random.sample()
# sol

import random
print('create a list of random int')
population = range(0,100)
num_list = random.sample(population, 10 )
print(num_list)

n_elements = 4
print('list : ')
result = random.sample(num_list, n_elements)
print(result)

_________________________________________________________________________________

#9. Write a Python program to set a random seed
#and get a random number between 0 and 1. Use random.random.

#sol
import  random
print('random seed and get a random number between 0 and 1')
random.seed(0)
new_random_value = random.random()
print(new_random_value)

random.seed(1)
new_random_value = random.random()
print(new_random_value)

_______________________________________________________________
########module-- types###################################
#1. Write a Python program to check if a function is a
# user-defined function or not. Use types.FunctionType, types.LambdaType()

#sol:
import random
import types


def fun():
    return 1

print(isinstance(fun, types.FunctionType))
print(isinstance(fun, types.LambdaType))
print(isinstance(lambda x: x, types.FunctionType))
print(isinstance(lambda x: x, types.LambdaType))
print(isinstance(max, types.FunctionType))
print(isinstance(abs, types.FunctionType))
print(isinstance(max, types.LambdaType))
print(isinstance(abs, types.LambdaType))

_______________________________________________________________________________________
'''
