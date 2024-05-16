# Descrição

Esse projeto foi criado para propor um desafio técnico para os estudantes de Computação, para analisarem a proposição, aqui presente, do problema da solução do jogo Campo Minado.

## Problema

O problema do Campo-Minado é considerado um problema NP-completo. Aqui está o porquê:

1. **Definição do problema**: No jogo do Campo-Minado, você tem um tabuleiro parcialmente preenchido. O objetivo é encontrar uma distribuição de minas que seja consistente com o estado atual do tabuleiro¹.

2. **Verificação em tempo polinomial**: Se você tiver uma solução candidata para o problema (ou seja, uma distribuição proposta de minas), você pode verificar rapidamente se essa solução é válida. Basta verificar se todas as dicas no tabuleiro (os números que indicam quantas minas adjacentes existem) correspondem ao número de minas na solução proposta¹. Isso pode ser feito em tempo polinomial, o que significa que o problema do Campo-Minado está na classe NP.

3. **Redução em tempo polinomial**: Um problema é NP-completo se for um problema NP e se todo problema NP puder ser reduzido a ele em tempo polinomial². Isso significa que se você tiver um algoritmo eficiente para resolver o problema do Campo-Minado, você poderia usar esse algoritmo para resolver qualquer problema NP. Acredita-se que o problema do Campo-Minado tem essa propriedade, embora a prova seja complexa¹.

4. **Dificuldade de encontrar uma solução**: Embora seja fácil verificar uma solução para o problema do Campo-Minado, encontrar uma solução a partir de um tabuleiro parcialmente preenchido é um processo complexo. Não se conhece nenhum algoritmo que possa resolver o problema do Campo-Minado em tempo polinomial¹.

Portanto, o problema do Campo-Minado é um problema NP-completo porque satisfaz todas as condições necessárias: está na classe NP, acredita-se que todos os problemas NP possam ser reduzidos a ele, e encontrar uma solução é um processo complexo¹².

Origem: conversa com o Bing, 16/05/2024
(1) Problemas NP-completos - IME-USP. <https://www.ime.usp.br/~pf/analise_de_algoritmos/aulas/NPcompleto.html>.
(2) O que é um problema NP completo? - Stack Overflow em Português. <https://pt.stackoverflow.com/questions/34104/o-que-%C3%A9-um-problema-np-completo.>
(3) NP-completo – Wikipédia, a enciclopédia livre. <https://pt.wikipedia.org/wiki/NP-completo.>

## Desafio

O desafio proposto é pesquisar e implementar um algoritmo que resolva o problema do Campo-Minado. O algoritmo deve receber um tabuleiro parcialmente preenchido e retornar uma distribuição de minas que seja consistente com o estado atual do tabuleiro.

Após a proposta do algoritmo, o estudante deve classificar o algoritmo por sua complexidade de tempo e apontar a estratégia utilizada, bem como os desafios.

## Entrada

A entrada é composta por um tabuleiro parcialmente preenchido. O tabuleiro é uma matriz de tamanho N x M, onde N é o número de linhas e M é o número de colunas. Cada célula do tabuleiro pode estar vazia (indicada por '.') ou conter uma mina (indicada por '*'). Além disso, cada célula do tabuleiro pode conter um número de 0 a 8, que indica quantas minas adjacentes existem.

## Saída

A saída é uma distribuição de minas que seja consistente com o estado atual do tabuleiro. A distribuição de minas é representada por uma matriz de tamanho N x M, onde N é o número de linhas e M é o número de colunas. Cada célula da matriz pode conter uma mina (indicada por '*') ou estar vazia (indicada por '.').

## Exemplo

### Exemplo de Entrada

```plaintext
4 4
. . . .
. 1 1 .
. 1 1 .
. . . .
```

### Exemplo de Saída

```plaintext
* * . .
* 1 1 .
. 1 1 .
. . . .
```
