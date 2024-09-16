# quiz 003



## paper solution
![IMG_2670](https://github.com/user-attachments/assets/ffb12cad-e398-41f3-a08a-fbe695ecb7ee)

## flow diagram
<img width="869" alt="Screenshot 2024-09-16 at 23 44 37" src="https://github.com/user-attachments/assets/4d981ae6-3f9b-4494-a41e-4048ec8bcc8c">


## code
            def translated_dna(dna_chain):
                translated_chain = ""
            
                for x in dna_chain:
                    if x == 'A':
                        translated_chain +='T'
                    elif x == 'G':
                        translated_chain +='C'
                    elif x == 'T':
                        translated_chain +='A'
                    elif x == 'C':
                        translated_chain +='G'
                    else:
                        print('The symbol is not defined')
                return translated_chain
            
            print('Enter a DNA chain: ')
            dna_chain = input()
            translated_chain = translated_dna(dna_chain)
            print('Translated DNA chain: ')
            print(translated_chain)

## proof of work
<img width="1440" alt="Screenshot 2024-09-12 at 2 06 02" src="https://github.com/user-attachments/assets/6367cb2c-78b4-49d7-b32d-458d24924a8a">

