# quiz 015



## paper solution
![image](https://github.com/user-attachments/assets/046a324c-7f0a-4866-a9b2-3ed3780d2e34)




## flow diagram
![image](https://github.com/user-attachments/assets/5ab1fa8b-7262-4f98-a0e8-d2112704c04d)


## code
              def average_word_length(word_list):
                  total_length = 0
                  total_words = 0
              
                  for word in word_list:
                      stripped_word = word.strip()
                      total_length += len(stripped_word)
                      total_words += 1
              
                  if total_words == 0:
                      return 0
              
                  average_length = total_length / total_words
                  return average_length
              
              words = [" Hello ", " world "]
              print(average_word_length(words))


## proof of work
![image](https://github.com/user-attachments/assets/3724ceb3-eb96-4970-bf94-eba4022c4c92)
