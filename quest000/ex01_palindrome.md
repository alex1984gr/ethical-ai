Step 1 - Do it yourself
Write pseudocode for a function that checks if a string is a palindrome.

Implement your solution in Python.

Test with examples like "racecar", "hello", and "A man a plan a canal Panama".

Add comments explaining your reasoning.

# Pseudocode:
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

Implement your solution in Python

def is_palindrome(text):
    # reversed symbol line
    reversed_text == text[::-1] 
    # Compare the original text with the reversed text
    if text == reversed_text:
        return True  # It is a palindrome
    else:
        return False  # It is not a palindrome


Test with examples like "racecar", "hello", and "A man a plan a canal Panama".
