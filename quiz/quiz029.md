#  quiz029

## code
                        import matplotlib.pyplot as plt
                        import numpy as np
                        
                        server_ip = "192.168.4.137"
                        
                        r = requests.get(f"http://{server_ip}/readings")
                        data = r.json()
                        readings = data['readings'][0]
                        
                        temperature_data=[]
                        pressure_data=[]
                        
                        for r in readings:
                            if r['sensor_id'] == 11:
                                temperature_data.append(r['value'])
                            elif r['sensor_id'] == 12:
                                pressure_data.append(r['value'])
                        
                        min_length = min(len(temperature_data), len(pressure_data))
                        temperature_data = temperature_data[0:min_length]
                        pressure_data = pressure_data[0:min_length]
                        
                        sensor_sum = [t + p for t, p in zip(temperature_data, pressure_data)]
                        sensor_average = [(t + p) / 2 for t, p in zip(temperature_data, pressure_data)]
                        
                        plt.style.use('ggplot')
                        fig, axs = plt.subplots(3, 1, figsize=(10, 12))
                        
                        axs[0].plot(temperature_data, color='red')
                        axs[0].set_title("Temperature Sensor (ID=11)")
                        axs[0].set_xlabel("Time")
                        axs[0].set_ylabel("Temperature")
                        
                        axs[1].plot(pressure_data, color='blue')
                        axs[1].set_title("Pressure Sensor (ID=12)")
                        axs[1].set_xlabel("Time")
                        axs[1].set_ylabel("Pressure")
                        
                        axs[2].plot(sensor_sum, color='purple')
                        axs[2].set_title("Sum of Temperature and Pressure")
                        axs[2].set_xlabel("Time")
                        axs[2].set_ylabel("Sum")
                        
                        plt.show()

## proof of work
<img width="1440" alt="Screenshot 2024-12-04 at 1 44 26" src="https://github.com/user-attachments/assets/f48cb408-951e-4007-aa31-ed05eb49fae8">


