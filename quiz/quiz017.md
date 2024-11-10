#  quiz017
## code
            word=input('Enter a word:')
            if  len(word)>2:
                middle_count = len(word) - 2
                result = f"{word[0]}{middle_count}{word[-1]}"
            else:
                result = word
            print(f"{word} -> {result}")

## proof of work
<img width="1440" alt="Screenshot 2024-09
