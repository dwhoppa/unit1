# quiz 001



## paper solution
![IMG_2668](https://github.com/user-attachments/assets/34bcc5db-33bc-495e-adee-b8a621fc3550)

## flow diagram
<img width="462" alt="Screenshot 2024-09-16 at 23 17 52" src="https://github.com/user-attachments/assets/e4173075-eadd-474c-92a2-6ddad355356c">


## code
            word=input('Enter a word:')
            if  len(word)>2:
                middle_count = len(word) - 2
                result = f"{word[0]}{middle_count}{word[-1]}"
            else:
                result = word
            print(f"{word} -> {result}")

## proof of work
<img width="1440" alt="Screenshot 2024-09-12 at 2 02 24" src="https://github.com/user-attachments/assets/13350684-c680-463c-95d9-b81bfe24db69">

