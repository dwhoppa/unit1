#  quiz027

## code and task (A and B)
                def flip(v1):
                    new_dict={}
                    for key, value in v1.items():
                        new_dict[value] = key
                    return new_dict



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

<img width="609" alt="Screenshot 2024-12-04 at 1 56 03" src="https://github.com/user-attachments/assets/79a3f053-ee90-45ef-9e24-0ead7b638140">
