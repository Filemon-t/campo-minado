# Campo Minado em C

Projeto acadêmico desenvolvido em **linguagem C** como implementação do jogo **Campo Minado**, utilizando uma matriz 9x9 para representar o tabuleiro.

O projeto foi desenvolvido como um exercício de aplicação de conceitos fundamentais da linguagem C, como **matrizes, funções, estruturas condicionais e de repetição, geração de números aleatórios e recursividade**.

## Sobre o jogo

O objetivo do Campo Minado é revelar todas as posições do tabuleiro que **não possuem minas**, evitando as 10 posições que contêm bombas.

O tabuleiro possui dimensões **9x9**, totalizando 81 posições. As 10 minas são distribuídas aleatoriamente pelo programa.

Cada posição do tabuleiro pode representar:

* `-1` → uma mina;
* `0` → uma posição vazia;
* `1` a `8` → quantidade de minas presentes nas posições vizinhas.

Como o projeto não possui uma interface gráfica, a escolha de uma posição é realizada informando a **linha e a coluna** desejadas.

## Funcionamento

Ao iniciar o jogo, o programa:

1. Inicializa o tabuleiro com valores zero;
2. Distribui aleatoriamente 10 minas;
3. Verifica a quantidade de minas existentes ao redor de cada posição;
4. Exibe o tabuleiro para o jogador utilizando `X` nas posições ainda não reveladas;
5. Solicita ao jogador uma linha e uma coluna;
6. Revela a posição escolhida;
7. Caso a posição seja vazia (`0`), as posições vazias conectadas são reveladas automaticamente;
8. Caso o jogador escolha uma mina, o jogo termina e o tabuleiro completo é exibido;
9. O jogador vence quando todas as posições que não possuem minas forem reveladas.

## Principais funções

### `inicializaTela()`

Inicializa a matriz `tela`, distribui as 10 minas aleatoriamente e calcula a quantidade de minas existentes ao redor de cada posição.

### `imprimeTelaJogador()`

Exibe a visão do tabuleiro para o jogador, utilizando `X` para representar as posições que ainda não foram reveladas.

### `imprimeTelaOriginal()`

Exibe o tabuleiro completo, permitindo visualizar as minas e os valores calculados.

### `posicaoEscolhida(int linha, int coluna)`

Processa a posição escolhida pelo jogador e realiza a revelação correspondente.

### `abreZero(int i, int j)`

Realiza a abertura automática das posições vazias conectadas à posição selecionada utilizando **recursividade**.

## Conceitos utilizados

* Linguagem C;
* Matrizes bidimensionais;
* Variáveis globais;
* Funções e procedimentos;
* Estruturas `if` e `else`;
* Estruturas `for` e `while`;
* Geração de números aleatórios com `rand()`;
* Inicialização do gerador com `srand()`;
* Recursividade;
* Validação de entrada;
* Manipulação de caracteres;
* Controle de estado das posições do tabuleiro.

## Condições de término

### Derrota

O jogador perde quando escolhe uma posição que contém uma mina.

Nesse caso, todas as posições do tabuleiro são reveladas.

###  Vitória

O jogador vence quando todas as **71 posições que não possuem minas** forem reveladas, restando apenas as 10 posições das minas ocultas.


## Contexto acadêmico

Este projeto foi desenvolvido como trabalho acadêmico para praticar conceitos de programação em linguagem C e implementar a lógica do jogo Campo Minado a partir de uma matriz bidimensional.
O trabalho propõe a utilização de uma matriz `9x9`, contendo 10 minas distribuídas aleatoriamente, além da implementação das funções responsáveis pela inicialização do tabuleiro, exibição das informações e processamento das jogadas.
