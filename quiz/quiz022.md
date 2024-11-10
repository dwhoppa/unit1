#  quiz022

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
                  y.append(abs(x[-1]))
              
              plt.plot(x, y, color='blue')
              plt.xlabel('x')
              plt.ylabel("y(x)")
              plt.show()
<img width="362" alt="Screenshot 2024-11-11 at 1 16 55" src="https://github.com/user-attachments/assets/e14b157a-9ed2-487b-8a7f-8648a31146d0">

## proof of work
<img width="1440" alt="Screenshot 2024-11-11 at 1 16 30" src="https://github.com/user-attachments/assets/43ae2e51-7c9e-4366-a70d-611cc8939069">
