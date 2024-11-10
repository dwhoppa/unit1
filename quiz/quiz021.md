#  quiz021

## code and task

              import matplotlib
              import matplotlib.pyplot as plt
              
              plt.style.use('ggplot')
              matplotlib.use("MacOSX")
              
              start=-10
              step=0.01
              x,y=[],[]
              
              for i in range(int(20/step)):
                  x.append(start+step*i)
                  y.append(2*(x[-1]+5)**2)
              
              plt.plot(x, y, color='blue')
              plt.xlabel('x')
              plt.ylabel("$y = (2*(x[-1]+5)**2)$")
              plt.title("Graph for parabola $y = (2*(x[-1]+5)**2)$")
              plt.show()
              
<img width="282" alt="Screenshot 2024-11-11 at 1 15 14" src="https://github.com/user-attachments/assets/ea2bce96-c3c4-4d38-9d91-af8b7b0b6c86">

## proof of work
<img width="1440" alt="Screenshot 2024-11-11 at 1 14 43" src="https://github.com/user-attachments/assets/7d5ffc33-9acf-428b-beb3-3d4a329418e5">
