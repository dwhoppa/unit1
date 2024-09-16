# quiz 006



## paper solution
![IMG_2673](https://github.com/user-attachments/assets/4c48293b-9cb9-4870-bf5a-6c21807aa376)

## flow diagram
<img width="380" alt="Screenshot 2024-09-17 at 0 05 24" src="https://github.com/user-attachments/assets/af1d5ce6-fd3b-46c1-911c-79b64b33972e">


## code
        import random
        
        characters = ('abcdefghijklmnopqrstuvwxyz'
            'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
            '0123456789'
            '!@#$%^&*()_+-=[]{},.<>?/|?`~')
        
        number_pass = 10
        length_pass =20
        
        for i in range(number_pass):
            password = ''
            for j in range(length_pass):
                index = random.randint(0, len(characters) - 1)
                password += characters[index]
            print(password)

## proof of work
<img width="1440" alt="Screenshot 2024-09-12 at 2 17 41" src="https://github.com/user-attachments/assets/bb518fb8-f808-46fb-93b7-fcaf4d8a2ea3">
