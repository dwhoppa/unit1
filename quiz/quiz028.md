#  quiz028

## code
                      from datetime import datetime
                      import requests
                      from my_lib import moving_average
                      import matplotlib
                      import matplotlib.pyplot as plt
                      import numpy as np
                      
                      server_ip="192.168.4.137"
                      
                      r = requests.get(f"http://{server_ip}/readings")
                      data=r.json()
                      readings=data['readings'][0]
                      
                      sensor_data = []
                      for r in readings:
                          if r ['sensor_id']==11:
                              sensor_data.append(r['value'])
                      
                      x=[]
                      for i in range(0,1000):
                          x.append(i)
                      
                      y=sensor_data[600:1600]
                      
                      
                      plt.style.use('ggplot')
                      plt.subplot(2, 1, 1)

                      plt.plot(y, color='blue')
                      plot_smoothed = moving_average(windowSize=5, x=y)
                      plt.plot(plot_smoothed, color = "red")
                      
                      m, b = np.polyfit(x,y, 1)
                      print(f"The linear model for the data is y={m:.2f}x+({b:.2f})")
                      def model(x, m, b):
                          return m*x+b
                      
                      x_model=[min(x),max(x)]
                      y_model=[model(min(x), m, b), model(max(x), m, b)]
                      
                      plt.plot(x_model, y_model, color='green')
                      
                      a, b, c = np.polyfit(x, y, deg=2)
                      model = []
                      for i in x:
                          model +=[a*i**2+b*i+c]
                      
                      plt.plot(x, y, color = "black")
                      plt.show()

## proof of work
<img width="1440" alt="Screenshot 2024-12-04 at 1 38 44" src="https://github.com/user-attachments/assets/770a1e32-2f98-46cd-8cc3-62a84ea8578e">

