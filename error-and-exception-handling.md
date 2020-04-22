# errors and exception handling

```
def add(n1,n2):
	print(n1+n2)

add(10,20)
# 30

number1 = 10

number2 = input('Please provide a number: ')
# 20

add(number1,number2)
# TypeError: unsupported operant type(s) for +: 'int' and 'str'
```

```
try:
	result = 10 + '10'

except:
	print("Hey it looks like you aren't adding correctly.")
```

```
try:
	result = 10 + 10

except:
	print("Hey it looks like you aren't adding correctly.")

else:
	print("Add went well!")
	print(result)

# "Add went well"
# 20
```

write mode creates a new file, no errors:
```
try:
	f = open("testfile","w")
	f.write("Write a test line")

except TypeError:
	print("There was a type error")

except OSError:
	print("Hey you have an OS Error")

finally:
	print("I always run")

# "I always run"
```

trying to read from a file you don't have permission for:
```
try:
	f = open("testfile","r")
	f.write("Write a test line")

except TypeError:
	print("There was a type error")

except OSError:
	print("Hey you have an OS Error")

finally:
	print("I always run")

# "Hey you have an OS Error"
# "I always run"
```

```
def ask_for_int():
	try:
		result = int(input("Please provide nubmer: "))
	except:
		print("Whoops! That is not a number")
	finally:
		print("End of try, except, finally")

ask_for_int()

# Please provide number:
# word
# Whoops! That is not a number
# End of try, except, finally
```

```
def ask_for_int():
	while True:
		try:
			result = int(input("Please provide nubmer: "))
		except:
			print("Whoops! That is not a number")
			continue
		else:
			print("Yes thank you")
			break
		finally:
			print("End of try, except, finally")

ask_for_int()

# Please provide number:
# word
# Whoops! That is not a number
# End of try, except, finally
# Please provide number:
# 10
# Yes thank you
# End of try, except, finally
```