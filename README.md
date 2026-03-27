# exercicio-tictactoe-ATR

# Jogo da Velha Concorrente (C++ Threads)

Este repositório contém a solução para um problema de **Programação Concorrente**: gerenciar o acesso a um recurso compartilhado (tabuleiro) e coordenar a alternância de turnos entre dois agentes (threads) utilizando C++.

## Descrição do Projeto

O objetivo é simular um jogo da velha onde dois jogadores controlados pelo computador (com estratégias "Sequencial" e "Aleatória") jogam simultaneamente. Sem sincronização, o código original apresentava condições de corrida (*race conditions*), permitindo que um jogador jogasse no lugar do outro ou que ambos acessassem o tabuleiro ao mesmo tempo.

## Tecnologias Utilizadas

* **Linguagem:** C++
* **Biblioteca:** `<thread>` para execução paralela.
* **Sincronização:** * `std::mutex`: Para garantir exclusão mútua no acesso ao tabuleiro.
    * `std::condition_variable`: Para coordenar a alternância de turnos (Jogador X -> Jogador O).
    * `std::unique_lock`: Para gerenciamento flexível do bloqueio de recursos.
