# decorators

## returning functions as a variable
```
def hello(name="Jose"):
	print("The hello() function has been executed")

	def greet():
		return "\t This is greet() inside hello"

	def welcome():
		return "\t This is welcome() inside hello"

	print(greet())
	print(welcome())

	if name == "Jose":
		return greet

	else:
		return welcome

my_new_func = hello("Jose")

print(my_new_func())

# 	This is greet() inside hello
```

## passing in a function as a variable
```
def hello():
	return "Hi Jose"

def other(some_defined_function):
	print("Other code runs here")
	print(some_defined_function())

other(hello)

# Other code runs here
# Hi Jose
```

## function wrapping
```
def new_decorator(original_func):

	def wrap_func():

		print("Some extra code, before original function")

		original_function()

		print("Some extra code, after original function")

	return wrap_func


def function_that_needs_decorator():

	print("I want to be decorated")


decorated_function = new_decorator(function_that_needs_decorator)

decorated_function()

# Some extra code, before original function
# I want to be decorated
# Some extra code, after original function
```

## decorator
```
@new_decorator
def function_that_needs_decorator():
	print("I want to be decorated")
