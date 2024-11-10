#  quiz018

## code and task
                  
              def get_truth():
              
                  a, b, c = 0, 0, 0
                  table = '|A|B|C|AB+notB+notCB|\n'
                  for i in range(8):
                      c=not c
              
                      if i%2 == 0:
                          b = not b
              
                      if i%4 == 0:
                          a = not a
              
                      eq=(a and b) and (not b) or(not(c and b))
              
                      row = f'|{int(a)}|{int(b)}|{int(c)}|{int(eq)}\n'
                      table += row
                  return table
              
              print(get_truth())

<img width="673" alt="Screenshot 2024-11-11 at 1 07 23" src="https://github.com/user-attachments/assets/305b3f48-9ff7-48bc-8457-3e90caf4e448">

## proof of work
<img width="1440" alt="Screenshot 2024-11-11 at 1 06 37" src="https://github.com/user-attachments/assets/7f8e9d8b-0c75-4a41-ad9d-de8b043966f7">
