# Step 1 - Do it yourself
Write pseudocode for a function that checks if a string is a palindrome.

Implement your solution in Python.

Test with examples like "racecar", "hello", and "A man a plan a canal Panama".

# Add comments explaining your reasoning.

# Pseudocode:
'''
FUNCTION is_palindrome(text):
    # 1. Read the original text and split each character into a separate element
    letters = split_into_characters(text)

    # 2. Put the letters in reverse order
    reversed_letters = reverse(letters)

    # 3. Compare the original letters with the reversed ones
    IF letters == reversed_letters:
        RETURN True  # It is a palindrome
    ELSE:
        RETURN False  # It is not a palindrome
'''

# Implement your solution in Python

## my Python implementation 

def is_palindrome(text):
    # remove spaces and lowercase
    cleaned = "".join(text.lower().split())
    reversed_text = cleaned[::-1]
    return cleaned == reversed_text

# Test with examples like "racecar", "hello", and "A man a plan a canal Panama".

# Tests

print(is_palindrome("racecar"))                     # True
print(is_palindrome("hello"))                       # False
print(is_palindrome("A man a plan a canal Panama")) # True 

# Add comments explaining your reasoning

The function is_palindrome checks if a given string is a palindrome.
It first cleans the input by removing spaces and converting it to lowercase.
Then, it reverses the cleaned string and compares it to the original cleaned string.
If they are the same, it returns True indicating that the string is a palindrome.
