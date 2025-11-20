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


# Step 2 - Use AI to learn

Now that your function works, use AI to go deeper:

"I wrote a palindrome function. Here's my code: 
def is_palindrome(text):
    # remove spaces and lowercase
    cleaned = "".join(text.lower().split())
    reversed_text = cleaned[::-1]
    return cleaned == reversed_text
'''


What's the time complexity?
What edge cases might I miss?
Are there better approaches?"
# AI answer
1️⃣ Time Complexity

Η συνάρτηση σου:

cleaned = "".join(text.lower().split())
reversed_text = cleaned[::-1]
return cleaned == reversed_text


text.lower() → O(n)

text.split() → O(n)

"".join(...) → O(n)

cleaned[::-1] → O(n)

cleaned == reversed_text → O(n)

Συνολικό Time Complexity: O(n), όπου n = μήκος του αρχικού string.

2️⃣ Edge Cases που μπορεί να χάσεις

Σημεία στίξης: A man, a plan, a canal: Panama → η συνάρτηση θα δώσει False χωρίς να αφαιρέσεις κόμματα, άνω/κάτω τελείες κλπ.

Διαφορετικοί χαρακτήρες Unicode: τόνους, ειδικά ελληνικά ή emojis.

Empty string: αυτή επιστρέφει True, που συνήθως είναι αποδεκτό.

Strings με μόνο κενά: " " → θα βγει True.

3️⃣ Better Approaches

Ignore punctuation

import string

def is_palindrome(text):
    cleaned = "".join(c.lower() for c in text if c.isalnum())
    return cleaned == cleaned[::-1]


isalnum() κρατάει μόνο γράμματα και αριθμούς

Αγνοεί σημεία στίξης και κενά

Επίσης κάνει lowercase

Two-pointer method (χωρίς να αντιστρέφεις ολόκληρο το string)

def is_palindrome(text):
    s = [c.lower() for c in text if c.isalnum()]
    i, j = 0, len(s)-1
    while i < j:
        if s[i] != s[j]:
            return False
        i += 1
        j -= 1
    return True


Εξοικονομεί μνήμη, ειδικά για πολύ μεγάλα strings

# Step 3 - Reflection

# What did you learn from solving it before asking AI?

By solving the palindrome problem on my own, I reinforced my understanding of string manipulation and basic algorithm design. I learned how to break down the problem into smaller steps, such as cleaning the input and reversing the string. This process helped me appreciate the importance of clear logic and step-by-step reasoning in coding.

# How is your understanding different now?

After consulting AI, my understanding has deepened significantly. I learned about the time complexity of my solution, which is O(n), and I became aware of potential edge cases that I hadn't initially considered, such as punctuation and Unicode characters. Additionally, I discovered more efficient approaches, like using the two-pointer method, which optimizes memory usage. This experience highlighted the value of considering various perspectives and techniques to enhance my coding skills.

# Could you now write similar functions (e.g., reverse a string) without help?

Yes, I feel confident that I could now write similar functions, such as reversing a string, without help. The process of breaking down the palindrome problem and learning from AI has equipped me with a stronger foundation in string manipulation and algorithmic thinking. I understand the importance of considering edge cases and optimizing solutions, which will be beneficial in writing other related functions.

