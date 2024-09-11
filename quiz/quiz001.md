# quiz 001



## paper solution
![image](https://github.com/user-attachments/assets/416904b1-fd77-4e9b-9a92-35f2d545d553)

## code
word=input('Enter a word:')
if  len(word)>2:
    middle_count = len(word) - 2
    result = f"{word[0]}{middle_count}{word[-1]}"
else:
    result = word
print(f"{word} -> {result}")

## proof of work
Enter a word:localization
localization -> l10n
