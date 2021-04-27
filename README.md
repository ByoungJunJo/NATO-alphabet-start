# NATO-alphabet-start
## TODO 1. Create a dictionary in this format: {"A": "Alfa", "B": "Bravo"}
```
import pandas as pd

df = pd.read_csv("nato_phonetic_alphabet.csv")
nato_dict = {row.letter: row.code for (index, row) in df.iterrows()}
print(nato_dict)
```
## TODO 2. Create a list of the phonetic code words from a word that the user inputs.

```
word = input("Enter a word: ").upper()
user_input = [nato_dict[letter] for letter in word]
print(user_input)
```
# Lessons
1. List comprehension: `[new_item for item in list if test]`
2. Dictionary comprehension if there's a list: `{new_key:new_value for item in list}`
3. Dictionary comprehension if there's a dictionary: `{new_key:new_value for (key, value) in dict.items if test}`
