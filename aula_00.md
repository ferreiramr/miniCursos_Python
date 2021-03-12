# AULA 01 - REVISÃO

## 1. COMO COMEÇAR

- Instalando ou acessando o seu ambiente de desenvolvimento
- Visual Studio Code e suas extensões
- Anaconda e Jupyter Notebook
- Google Colaboratory

## 2. REVISÃO

 - Revisão dos principais conceitos e estruturas da linguagem Python por meio do desenvolvimetno do jogo: [Adinhe em que número pensei.](https://repl.it/@ferreira_mr/adivinhe-em-que-numero-pensei#main.py)


### 2.1 QUE VOCÊ JÁ SABE
 
 Comente o código do jogo [Adinhe em que número pensei.](https://repl.it/@ferreira_mr/adivinhe-em-que-numero-pensei#main.py), linha a lina da maneira mais descritiva que você conseguir.

 ```python
"""
ADIVINHE EM QUE NÚMERO PENSEI
Clique em Run para iniciar o jogo (Botão no topo da página, no meio)
"""

from random import randint

inicio_do_intervalo = 0
fim_do_intervalo = 100
numero_secreto = randint(0, 100)
jogo_terminou = False

MENSAGEM_DE_INICIO_DO_JOGO = 'PENSEI EM UM NÚMERO DE {} A {}. ADIVINHE QUAL!' 
MENSAGEM_DE_UM_CHUTE = 'Dê um chute: '
MENSAGEM_DE_CHUTE_CORRETO = 'PARABÉNS VOCË GANHOU'
MENSAGEM_DE_CHUTE_ERRADO = 'Errou! Tente novamente!'
MENSAGEM_DE_CHUTE_ALTO = 'Você chutou alto.'
MENSAGEM_DE_CHUTE_BAIXO = 'Você chutou baixo'

def pegar_o_chute(MENSAGEM_DE_UM_CHUTE):
	MENSAGEM_DE_ERRO = 'O CHUTE DEVE SER UM NÚMERO INTEIRO! TENTE NOVAMENTE'
	chute = None
	while not chute:
		chute = input(MENSAGEM_DE_UM_CHUTE)
		try:
			return int(chute)
		except:
			print(MENSAGEM_DE_ERRO)
			chute = None


print(MENSAGEM_DE_INICIO_DO_JOGO.format(inicio_do_intervalo, fim_do_intervalo))

while not jogo_terminou:

	chute = pegar_o_chute(MENSAGEM_DE_UM_CHUTE)

	acertou = chute == numero_secreto
	chutou_alto = chute > numero_secreto
	chutou_baixo = chute < numero_secreto

	if acertou:
		print(MENSAGEM_DE_CHUTE_CORRETO)
		break
	else:
		print(MENSAGEM_DE_CHUTE_ERRADO)
		if chutou_alto:
			print(MENSAGEM_DE_CHUTE_ALTO)
		else:
			print(MENSAGEM_DE_CHUTE_BAIXO)
 ```

 
 ### 2.2. ENTENDENDO E APRENDENDO COM O CÓDIGO 

 1. Qual a finalidade do trecho de código `from random import randint`

 1. Qual a finalidade das variáveis `inicio_do_intervalo` e `fim_do_intervalo`.

 1. Qual será o valor da variável `numero_secreto` no inico de cada rodada

 1. Qual a finalidade da variável `jogo_terminou`, que tipo de dado ele armazena

 1. Qual a finalidade das variáveis: `MENSAGEM_DE_INICIO_DO_JOGO`, `MENSAGEM_DE_UM_CHUTE`, `MENSAGEM_DE_CHUTE_CORRETO`, `MENSAGEM_DE_CHUTE_ERRADO`, `MENSAGEM_DE_CHUTE_ALTO` e `MENSAGEM_DE_CHUTE_BAIXO`. Por que elas estão em letras maiúsculas?

 1. Que valor a variável `chute` armazena?

 1. O que é a estrutura `pegar_o_chute`?

 1. O que faz o trecho de código `pegar_o_chute(MENSAGEM_DE_UM_CHUTE)`

 1. Qual a finalidade das extruturs `try` e `except`.

 1. Que tipo de dado armazena as variáveis `acertou`, `chutou_alto` e `chutou_baixo`?

 1. O que tem de errado com a variável `chutou_baixo`?

 1. Qual trecho de código matémm o jogo em execução?

 1. Qual trecho de código termina o jogo?

 1. Descreva qual foi sua experiência e sensações realizando esta atividade.

## LISTA DE EXERCÍCIOS

## DESAFIOS

- Modificar o jogo [Adinhe em que número pensei.](https://repl.it/@ferreira_mr/adivinhe-em-que-numero-pensei#main.py) tornando-o mais completo e divertido.

- Realizar o *commit* da sua lista de exercícios no [**Github**](https://github.com/).

## REFERÊNCIAS

1. [Ambientes para desenvolvimento](ambientes_de_desenvolvimento.md)
2. [Materiais de apoio](referencias.md)
