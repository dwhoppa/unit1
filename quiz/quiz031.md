#  quiz031

## code
                  import numpy as np
                  from matplotlib import pyplot as plt
                  import matplotlib
                  
                  plt.style.use('ggplot')
                  matplotlib.use("MacOSX")
                  
                  start= -2
                  step=4/100
                  
                  x=[]
                  y=[]
                  x1=[]
                  y1=[]
                  x2=[]
                  y2=[]
                  x3=[]
                  y3=[]
                  
                  for i in range(100):
                      x+=[i*step+start]
                      y+=[x[i]**2]
                  
                  for i in range(100):
                      x1+=[i*step+start]
                      y1+=[-(x1[i]**2)]
                  
                  for i in range(100):
                      y2+=[i*step+start]
                      x2+=[y2[i]**2]
                  
                  for i in range(100):
                      y3+=[i*step+start]
                      x3+=[-(y3[i]**2)]
                  
                  plt.plot(x, y, color='green')
                  plt.plot(x1, y1, color='green')
                  plt.plot(x2, y2, color='green')
                  plt.plot(x3, y3, color='green')
                  
                  plt.xlabel('X-axis')
                  plt.ylabel('Y-axis')
                  plt.title("Four Parabolas Aligned with Axes")
                  plt.show()

## proof of work
<img width="640" alt="Screenshot 2024-12-04 at 1 50 35" src="https://github.com/user-attachments/assets/86a980f8-a992-47b5-9827-55662b30ba67">
