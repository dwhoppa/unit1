#  quiz024

## code and task
              
                      from matplotlib import pyplot as plt
                      import matplotlib
                      
                      plt.style.use('ggplot')
                      matplotlib.use("MacOSX")
                      
                      data =  {
                      'x': [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19],
                      'y': [24, 1, 2, 25, 26, 21, 23, 34, 49, 2, 19, 32, 7, 17, 36, 7, 45, 28, 40, 46]
                      }
                      
                      x=data['x']
                      y=data['y']
                      
                      plt.plot(x, y, color='green')
                      
                      plt.scatter(x, y, linewidth=2, color='#fb8500')
                      plt.xlabel('x')
                      plt.ylabel('$h=mx+b$')
                      plt.show()


## proof of work
<img width="1440" alt="Screenshot 2024-11-11 at 1 20 57" src="https://github.com/user-attachments/assets/9b445a6a-f9bf-492a-a128-ca709742de6d">
