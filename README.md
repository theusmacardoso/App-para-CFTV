class Visitante:
    nome: str
    idade: int

    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    def __repr__(self):
        representacao = f"Nome: {self.nome}\n"
        representacao += f"Idade: {self.idade}\n"

        return representacao

class Visita:
    visitante: Visitante
    hora_entrada: int
    hora_saida: int

    def __init__(self, visitante, hora_entrada, hora_saida):
        self.visitante = visitante
        self.hora_entrada = hora_entrada
        self.hora_saida = hora_saida



LISTA_VISITANTES: list[Visitante] = [  # instâncias
    Visitante("Matheus 1", 19),
    Visitante("Gustavo 1", 24),
    Visitante("Matheus 2", 19),
    Visitante("Gustavo 2", 30),
    Visitante("Matheus 3", 19),
    Visitante("Gustavo 3", 24),
    Visitante("Matheus 4", 19),
    Visitante("Gustavo 4", 24)
]
LISTA_VISITAS: list[Visita] = []




def exibir_menu():
    print('\n === Sistema de Gestão de Visitantes CFTV ===')
    print('As etapas são:')
    print('1. Cadastrar visitante')
    print('2. Registrar entrada visita')
    print('3. Registrar saída visita')
    print('4. Consultar visitantes')
    print('5. Consultar visitas')
    print('6. Sair')


def exibir_visitantes():
    print("\n Lista Visitantes:")

    for visitante in LISTA_VISITANTES:
        print(visitante)


def cadastro_visitante():
    nome_novo = input("Insira o nome do novo visitante: ")
    idade_novo = int(input("Insira a idade do novo visitante: "))

    novo_visitante = Visitante(nome_novo, idade_novo)

    LISTA_VISITANTES.append(novo_visitante)

    exibir_visitantes()



def main():
    cadastro_visitante()

main()
