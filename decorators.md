# decorators

```
def hello(name="Jose"):
	print("The hello() function has been executed")

	def greet():
		return "\t This is greet() inside hello"

	def welcome():
		return "\t This is welcome() inside hello"

	print(greet())
	print(welcome())
	print("This is the end of the hello function")