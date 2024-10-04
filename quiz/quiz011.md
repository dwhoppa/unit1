# quiz 011



## paper solution
![image](https://github.com/user-attachments/assets/45ff9c76-8c12-47aa-85b0-3562b02b74a5)



## flow diagram
![image](https://github.com/user-attachments/assets/8eb4de4f-2eac-4471-8888-33c4157b71d3)



## code
           def show_days_of_august():
               days_of_week = ["Mo", "Tu", "We", "Th", "Fr", "Sat", "Su"]
           
               output = []
           
               for day in range(1, 32):
                   day_of_week = days_of_week[(day + 2)%7]
                   output.append(f"{day_of_week} {day}")
           
               return '  '.join(output)
           
           print(show_days_of_august())

## proof of work
![image](https://github.com/user-attachments/assets/f5b8512a-d410-4c10-a1ad-aaa753659a44)
