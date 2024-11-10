#  quiz019

## code and task
              import random
              
              random.seed(1)
              def produce(n=5,m=3,s=2):
                  x, y = [], []
                  table = '|' + 'x'.center(20, ' ') + '|' + 'y(x)'.center(20, ' ') + '|\n'
              
                  for i in range(n):
                      rx = random.randint(0, 100)
                      ry=rx**(0.5*((m/s)**2))
                      x.append(rx)
                      y.append(ry)
              
                      table += '|' + str(rx).center(20, ' ') + '|' + str(round(ry, 2)).center(20, ' ') + '|\n'
              
                  return table
              
              print(produce(n=5, m=3, s=2))

<img width="496" alt="Screenshot 2024-11-11 at 1 09 30" src="https://github.com/user-attachments/assets/532a1d32-4073-4fb5-8b0b-3a3de250dffb">

## proof of work
<img width="1440" alt="Screenshot 2024-11-11 at 1 08 40" src="https://github.com/user-attachments/assets/a0625560-5735-4730-8a1d-ea14d0c12edd">
