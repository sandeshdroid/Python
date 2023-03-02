myCat = {'size': 'fat', 'color': 'gray', 'disposition': 'loud'} #'size' is key, 'fat' is value of key

'My cat has ' + myCat['color'] + ' fur.'
      
'My cat has gray fur.'



[1, 2, 3] == [3, 2, 1]
      
False

eggs = {'name': 'Sophie', 'species': 'cat', 'age': 8}
      
ham = {'species': 'cat', 'name': 'Sophie', 'age': 8}

eggs == ham
      
True

#dictionary doesnot care about order as lists



'name' in eggs #check if key 'name' is present in dictionary
      
True



list(eggs.keys()) #lists keys , use item for both keys and values



for k in eggs.values(): #using for loop to print dictionary value
      print(k)

Sophie
cat
8

for i in eggs.items(): #generates tuples (immutable value in small barckets)
      print(i)

('name', 'Sophie')
('species', 'cat')
('age', 8)



eggs 
      
{'name': 'Sophie', 'species': 'cat', 'age': 8}
eggs.get('age', 0)
      
8
eggs.get('color', 0)
      
0

#returns 0 if not found and avoids crashing



eggs = {'name': 'Sophie', 'species': 'cat', 'age': 8}
      
eggs.setdefault('color', 'black')
      
'black'
eggs
      
{'name': 'Sophie', 'species': 'cat', 'age': 8, 'color': 'black'}
eggs.setdefault('color', 'orange')
      
'black'
eggs
      
{'name': 'Sophie', 'species': 'cat', 'age': 8, 'color': 'black'}

#setdefault only adds item if absent



message = 'hi'

count = {}

for character in message.upper():
    count.setdefault(character, 0)
    count[character] = count[character] + 1

print(count)

#count number of each character