#  quiz023

## code and task
              
                    import numpy as np
                    from matplotlib import pyplot as plt
                    import matplotlib
                    
                    plt.style.use('ggplot')
                    matplotlib.use("MacOSX")
                    
                    x=[]
                    h=[57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
                    
                    for i in range(32):
                        x.append(i)
                    
                    m, b = np.polyfit(x,h, 1)
                    print(f"The linear model for the data is y={m:.2f}x+({b:.2f})")
                    def model(x, m, b):
                        return m*x+b
                    
                    x_model=[min(x),max(x)]
                    y_model=[model(min(x), m, b), model(max(x), m, b)]
                    
                    plt.plot(x_model, y_model, color='green')
                    
                    plt.scatter(x, h, linewidth=2, color='#fb8500')
                    plt.xlabel('x')
                    plt.ylabel('$h=mx+b$')
                    plt.show()
<img width="408" alt="Screenshot 2024-11-11 at 1 18 44" src="https://github.com/user-attachments/assets/cce6a92a-29d0-4c37-8d02-b8119a02a4c8">

## proof of work
<img width="1440" alt="Screenshot 2024-11-11 at 1 18 09" src="https://github.com/user-attachments/assets/3c73bef4-f752-4525-b1b7-d82f2a7f4476">


