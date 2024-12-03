#  quiz030

## code
                  import numpy as np
                  from matplotlib import pyplot as plt
                  import matplotlib
                  import requests
                  from matplotlib.gridspec import GridSpec
                  from my_lib import moving_average
                  from datetime import datetime
                  
                  plt.style.use('ggplot')
                  matplotlib.use('MAcOSX') 
                  
                  server_ip = '192.168.4.137'
                  
                  request = requests.get(f"http://{server_ip}/readings")
                  readings =request.json()["readings"][0]
                  
                  temp=[]
                  hum=[]
                  for r in readings:
                      if r["sensor_id"]==11:
                          temp.append(r["value"])
                      if r["sensor_id"]==10:
                          hum.append(r["value"])
                  
                  average = [(temp[i] + hum[i]) / 2 for i in range(100)]
                  
                  fig, axes = plt.subplots(1, 3, figsize=(15, 5))
                  
                  axes[0].plot(temp, label="Temperature", color="red")
                  axes[0].set_ylabel("Temperature")
                  axes[0].set_title("Temperature Readings")
                  
                  axes[1].plot(hum, label="Humidity", color="blue")
                  axes[1].set_ylabel("Humidity")
                  axes[1].set_title("Humidity Readings")
                  
                  axes[2].plot(average, label="Average", color="green")
                  axes[2].set_ylabel("Average")
                  axes[2].set_title("Average of Readings")
                  
                  plt.show()

## proof of work
<img width="1440" alt="Screenshot 2024-12-04 at 1 48 39" src="https://github.com/user-attachments/assets/c11fc147-d96a-4c44-a992-399a886c430e">
