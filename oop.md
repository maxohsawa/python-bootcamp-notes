# Object Oriented Programming

## __init__

```
class NameOfClass():
# naming convention is to capitalize and use camel casing

	def __init__(self, param1, param2):
		self.param1 = param1
		self.param2 = param 2

	def some_method(self):
		# perform some action
		print(self.param1)
```

## initialize in main

```
class Sample():
	pass

my_sample = Sample()

type(my_sample)
# __main__.Sample
```

## attributes

```
class Dog():

	def __init__(self,breed):

		self.breed = breed

my_dog = Dog()
# error, expecting parameter

my_dog = Dog(breed='Lab')

type(my_dog)
# __main__.Dog

my_dog.breed
# 'Lab'
```

```
class Dog():

	def __init__(self,mybreed):

		self.my_attribute = mybreed

my_dog = Dog(mybreed='Huskie')

my_dog.my_attribute
# 'Huskie'

# demo only. convention is to use the same naming for input param and object attribute
```

## class object attribute and methods

```
class Dog():

	species = 'mammal'
	# this is a class object attribute
	# class is a keyword we can't use so we use species

	def __init__(self,breed):
		self.breed = breed

my_dog = Dog(breed='Lab')

my_dog.breed
# 'Lab'

my_dog.species
# 'mammal'
```

```
class Dog():

	def __init__(self,breed,name):
		self.breed = breed
		self.name = name

	def bark(self,number):
		print('WOOF! My name is {} and the number is: {}'.format(self.name,number)

my_dog = Dog('Lab','Frankie')

my_dog.bark(9)
# 'WOOF! My name is Frankie and the number is 9'
```

```
class Circle():

	# Class Object Attribute
	pi = 3.14

	def __init__(self,radius=1):
	# default radius is 1
		self.radius = radius
		self.area = radius * radius * self.pi
		# self.pi or Circle.pi
		# using Circle.pi makes it clearer that it's a class object attribute

	# Method
	def get_circumference(self):
		return 2 * self.pi * self.radius

my_circle = Circle()
mycircle.get_circumference()
# 6.28
```

## inheritance

```
class Animal():

	def __init__(self):
		print('Animal Created')

	def who_am_i(self):
		print('I am an animal')

	def eat(self):
		print('I am eating')

myanimal = Animal()
# 'Animal Created'

myanimal.eat()
# 'I am eating'

myanimal.who_am_i()
# 'I am an animal'

class Dog(Animal):
	# deriving Dog class from Animal class

	def __init__(self):
		Animal.__init__(self)
		print('Dog Created')

	def who_am_i(self):
		print('I am a dog')

mydog = Dog()
# 'Animal Created'
# 'Dog Created'

mydog.eat()
# 'I am eating'

mydog.who_am_i()
# 'I am a dog'
```

## polymorphism

```
class Dog():

	def __init__(self,name):
		self.name = name

	def speak(self):
		return self.name + ' says woof!'

class Cat()

	def __init__(self,name):
		self.name = name

	def speak(self):
		return self.name + ' says meow!'

niko = Dog('niko')
felix = Cat('felix')

print(niko.speak())
# 'niko says woof!'

print(felix.speak())
# 'felix says meow!'

for pet in [niko,felix]:
	print(type(pet))
	print(pet.speak())
# <class '__main__.Dog'>
# 'niko says woof!'
# <class '__main__.Cat'>
# 'felix says meow!'

def pet_speak(pet):
	print(pet.speak())

pet_speak(niko)
# 'niko says woof!'

pet_speak(felix)
# 'felix says meow!'
```

## abstract class

```
class Animal():

	def __init__(self,name):
		self.name = name

	def speak(self):
		raise NotImplementedError('Subclass must implement this abstract method')

myanimal = Animal('fred')

myanimal.speak()
# Not Implemented Error

class Dog(Animal):
	
	def speak(self):
		return self.name + ' says woof!'

class Cat(Animal):

	def speak(self):
		return self.name + ' says meow!'

fido = Dog('Fido')

isis = Cat('Isis')

print(fido.speak())
# 'Fido says woof!'

print(isis.speak())
# 'Isis says meow!'
```

## special methods

```
class Book():

	def __init__(self,title,author,pages):
		self.title = title
		self.author = author
		self.pages = pages

	def __str__(self):
		return f'{self.title} by {self.author}'

	def __len__(self):
		return self.pages

	def __del__(self):
		print('A book object has been deleted')

b = Book('Python rocks','Jose',200)

str(b)
# 'Python rocks by Jose'

print(b)
# 'Python rocks by Jose'

len(b)
# 200

del b
b
# 'A book object has been deleted'
```













