# Bot-and-lists
lista simples 
import time
import random

# Boas-vindas com ASCII
print("⭐" * 35)
print("🤖  ASSISTENTE VIRTUAL  🤖")
print("⭐" * 35)
time.sleep(1)

name = input("Olá! Qual é o seu nome? 😊 ")
time.sleep(1)
print("Seja bem-vindo(a), Vamos começar!")
time.sleep(1)

# Listas iniciais
filmes = ["Homem-Aranha", "Vingadores", "O Rei Leão"]
jogos = ["Minecraft", "Fortnite", "Zelda"]

while True:
    print("\n" + "-" * 40)
    print("📋 MENU DE COMANDOS")
    print("1 - Mostrar lista de filmes")
    print("2 - Mostrar lista de jogos")
    print("3 - Adicionar filme")
    print("4 - Adicionar jogo")
    print("5 - Remover filme")
    print("6 - Remover jogo")
    print("7 - Escolher filme aleatório")
    print("8 - Escolher jogo aleatório")
    print("9 - Sair")
    print("-" * 40)

    command = input("Digite o número do comando: ").strip()

    # LISTA DE FILMES
    if command == "1":
        print("\n🎬 Lista de filmes:")
        if filmes:
            for filme in filmes:
                print("-", filme)
        else:
            print("Nenhum filme cadastrado 😢")

    # LISTA DE JOGOS
    elif command == "2":
        print("\n🎮 Lista de jogos:")
        if jogos:
            for jogo in jogos:
                print("-", jogo)
        else:
            print("Nenhum jogo cadastrado 😢")

    # ADICIONAR FILME
    elif command == "3":
        novo_filme = input("Digite o nome do filme: ")
        filmes.append(novo_filme)
        print("✅ '{novo_filme}' foi adicionado à lista de filmes!")

    # ADICIONAR JOGO
    elif command == "4":
        novo_jogo = input("Digite o nome do jogo: ")
        jogos.append(novo_jogo)
        print("✅ '{novo_jogo}' foi adicionado à lista de jogos!")

    # REMOVER FILME
    elif command == "5":
        remover = input("Digite o nome do filme para remover: ")
        if remover in filmes:
            filmes.remove(remover)
            print("🗑️ '{remover}' removido com sucesso!")
        else:
            print("❌ Filme não encontrado.")

    # REMOVER JOGO
    elif command == "6":
        remover = input("Digite o nome do jogo para remover: ")
        if remover in jogos:
            jogos.remove(remover)
            print("🗑️ '{remover}' removido com sucesso!")
        else:
            print("❌ Jogo não encontrado.")

    # FILME ALEATÓRIO
    elif command == "7":
        if filmes:
            print("🎲 Filme sorteado:", random.choice(filmes))
        else:
            print("Não há filmes para sortear.")

    # JOGO ALEATÓRIO
    elif command == "8":
        if jogos:
            print("🎲 Jogo sorteado:", random.choice(jogos))
        else:
            print("Não há jogos para sortear.")

    # SAIR
    elif command == "9":
        print("👋 Até logo, {name}! Obrigado por usar o assistente.")
        break

    # COMANDO INVÁLIDO
    else:
        print("⚠️ Comando inválido! Tente novamente.")

    time.sleep(1)










  
