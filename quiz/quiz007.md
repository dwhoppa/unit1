# quiz 007



## paper solution
![IMG_2675](https://github.com/user-attachments/assets/50870bbd-61ea-4ef6-a54f-788e008024ad)
![IMG_2674](https://github.com/user-attachments/assets/95a248a3-76d6-4131-b2df-836591513f33)



## code
        numbers = input("Enter a list of numbers: ")
        n = [int(item) for item in numbers.split(',')]
        M= -1
        for i in range(len(n)):
            if n[i]>M:
                M=n[i]
        print(M)

## proof of work
<img width="1440" alt="Screenshot 2024-09-12 at 2 23 26" src="https://github.com/user-attachments/assets/38968696-1f95-4a79-81ff-61cf66268023">
