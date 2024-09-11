# quiz 001



## paper solution
![IMG_2668](https://github.com/user-attachments/assets/34bcc5db-33bc-495e-adee-b8a621fc3550)


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
