# quiz 014



## paper solution
![image](https://github.com/user-attachments/assets/2437d4ad-3636-4d34-80b8-f6e232ecb712)



## flow diagram
![image](https://github.com/user-attachments/assets/f19187c4-6026-40d4-a647-a6e4370d67a9)



## code
          def doors_opened(n):
              doors = [False] * n
          
              for student in range(1, n + 1):
                  for door in range(student - 1, n, student):
                      doors[door] = not doors[door]
          
              open_doors = [i + 1 for i in range(n) if doors[i]]
              return open_doors
          
          n = 5
          print(doors_opened(n))


## proof of work
![image](https://github.com/user-attachments/assets/76bcda15-9eee-4f87-a9ac-ca6471c25b80)
