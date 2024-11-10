#  quiz017
## code and task
                        def get_truth():
                        
                            a, b, c = 0, 0, 0
                            table = '|A|B|C|\n'
                            for i in range(8):
                                row=f'|{int(a)}|{int(b)}|{int(c)}|\n'
                                table+=row
                                c=not c
                        
                                if i%2 == 0:
                                    b = not b
                        
                                if i%4 == 0:
                                    a = not a
                            return table
                        
                        print(get_truth())

<img width="1202" alt="Screenshot 2024-11-11 at 1 04 53" src="https://github.com/user-attachments/assets/398858c3-8a87-4aa3-afe0-25c49a7d6054">

## proof of work
<img width="1440" alt="Screenshot 2024-11-11 at 1 01 15" src="https://github.com/user-attachments/assets/0160e011-534e-4a78-8f0c-e984e81d2ebf">
