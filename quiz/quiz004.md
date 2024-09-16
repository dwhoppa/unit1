# quiz 004



## paper solution
![IMG_2671](https://github.com/user-attachments/assets/55dcfb91-657e-4f8d-aa52-3946c5bbd00d)

## flow diagram
<img width="418" alt="Screenshot 2024-09-16 at 23 58 20" src="https://github.com/user-attachments/assets/dbd0076d-0563-4755-8e95-6fc00fd80538">




## code
        number = int(input("Enter a number: "))
        n1=0
        for n in range(1, number):
            if number % n == 0:
                n1 += n
                print(n)
        
        if n1 == number:
            print('TRUE')
        else:
            print('FALSE')


## proof of work
<img width="1440" alt="Screenshot 2024-09-12 at 2 13 03" src="https://github.com/user-attachments/assets/e75e7891-d5aa-4e08-aac3-5d7997edbb27">
