# quiz 016



## paper solution
![image](https://github.com/user-attachments/assets/4b4114aa-cb99-400c-afd0-c81cc760294f)



## flow diagram
![image](https://github.com/user-attachments/assets/d92e288f-3b49-47b7-be2f-33aae68c329d)



## code
                def replace(input_string):
                    vowel_map = {
                        'a': '4',
                        'e': '3',
                        'i': '1',
                        'o': '0',
                        ' ': '_'
                    }
                
                    output_string = ''
                
                    for char in input_string:
                        if char.lower() in vowel_map:
                            output_string += vowel_map[char.lower()]
                        else:
                            output_string += char
                
                    return output_string
                
                input_str = "Hello!"
                print(replace(input_str))



## proof of work
![image](https://github.com/user-attachments/assets/3f58ce7f-c973-41e1-a5c8-fc213a85a77e)
