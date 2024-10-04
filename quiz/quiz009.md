# quiz 009



## paper solution
![image](https://github.com/user-attachments/assets/b814c85f-0949-41ae-bf5d-639749cd7f42)


## flow diagram
![image](https://github.com/user-attachments/assets/05a916f5-8587-425d-bc80-8e6fc4b50162)



## code
            def secure(text, shift):
                result = ""
                for char in text:
                    if char.isalpha():
                        shifted = ord(char) + shift
                        if char.islower() and shifted > ord('z'):
                            shifted -= 26
                        elif char.isupper() and shifted > ord('Z'):
                            shifted -= 26
                        result += chr(shifted)
                    else:
                        result += char
                return result
            
            print(secure("hello world!", 13))


## proof of work
![image](https://github.com/user-attachments/assets/44f1d912-8adb-40bd-9018-7b52f3710aea)

