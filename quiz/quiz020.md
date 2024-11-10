#  quiz020

## code and task

              import matplotlib
              import matplotlib.pyplot as plt
              import numpy as np
              
              plt.style.use('ggplot')
              matplotlib.use("MacOSX")
              
              def plot_function(m=3, s=2, x_max=100):
                  x_values = np.linspace(1, x_max, 100)
                  y_values = x_values ** (0.5 * ((m / s) ** 2))
              
                  plt.plot(x_values, y_values, color='blue')
                  plt.title(f'Graph of y(x) with m = {m} and s = {s}')
                  plt.xlabel('x')
                  plt.ylabel("$x_values ** (0.5 * ((m / s) ** 2))$")
                  plt.show()
              
              plot_function(m=3, s=2, x_max=100)

<img width="199" alt="Screenshot 2024-11-11 at 1 13 05" src="https://github.com/user-attachments/assets/1d60f059-a80d-4e30-b92c-b736f29daf34">

## proof of work
<img width="1440" alt="Screenshot 2024-11-11 at 1 11 18" src="https://github.com/user-attachments/assets/e5497bb2-f9ab-400b-b8a9-9337b9de1f5f">
