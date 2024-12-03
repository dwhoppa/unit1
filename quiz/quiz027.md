#  quiz027

## code and task (A and B)
                def sort_dict(in_dict):
                    items = list(in_dict.items())
                    n = len(items)
                
                    for i in range(n):
                        min_index = i
                        for j in range(i + 1, n):
                            val1, val2 = items[min_index][1], items[j][1]
                
                            if (type(val1) is str and type(val2) is int) or (type(val1) is type(val2) and val2 < val1):
                                min_index = j
                
                        items[i], items[min_index] = items[min_index], items[i]
                
                    return dict(items)



                  from  matplotlib import pyplot as plt
                  import matplotlib
                  import math
                  
                  plt.style.use('ggplot')
                  matplotlib.use('MacOSX')
                  
                  x = []
                  y = []
                  
                  start = 0
                  step = 1/100
                  for i in range(100):
                      x1 = i*step + start
                      x.append(x1)
                      y.append(math.sin(2* x1 * 3.14159265))
                  
                  plt.plot(x,y, color='blue')
                  plt.title("y=sin(2*pi*x)")
                  plt.show()


## proof of work
<img width="1440" alt="Screenshot 2024-12-04 at 8 38 11" src="https://github.com/user-attachments/assets/a4472a02-c5c4-47e3-9208-370c18a4b4a0">

<img width="609" alt="Screenshot 2024-12-04 at 1 56 03" src="https://github.com/user-attachments/assets/79a3f053-ee90-45ef-9e24-0ead7b638140">
