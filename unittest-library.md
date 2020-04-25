# unittest library

file cap.py
```
def cap_text(text):
	```
	input a string
	output the capitalized string
	```

	retrun text.capitalize()
```

file test_cat.py
test in order of least to most complex function
```
import unittest
import cap

class TestCap(unittest.TestCase):
	
	def test_one_word(self):
		text = 'python'
		result = cap.cap_text(text)
		self.assertEqual(result,'Python')

	def test_multiple_words(self):
		text = 'monty python'
		result = cap.cap_text(text)
		self.assertEqual(result,'Monty Python')

if __name__=='__main__':
	unittest.main()

```

run test_cap.py in commandline

results in error because capitalize() only capitalizes first letter of string,
not first letter of each word

using title() passes multiple word test