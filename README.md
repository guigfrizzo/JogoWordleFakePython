# JogoWordleFakePython
Uma imitação do jogo Termo ou Wordle com bobagens feito com python 


    import random
    
    def check_word():
        word_list = ["bosta", "putao", "cu", "mijo", "fpd", "palavrao", "puta", "coco", "cuzao", "cacete", "piroca", "pica", "buceta", "bunda","virgem", "bucetuda","chulé", "peido", "gostosa","sexo","porra"]
        hidden_word = random.choice(word_list)
        attempt = 20
        while attempt > 0:
            guess = input("Adivinhe a palavra: ")
            if guess == hidden_word:
                print("Você ganhou! WIN")
                break
            else:
                attempt = attempt - 1
                print(f"você tem {attempt} tentativa(s) \n ")
                for char, word in zip(hidden_word, guess):
                    if word in hidden_word and word in char:
                        print(word + " ✔ ")
                    else:
                        print(word + " ✘ ")
    
    check_word()
    



