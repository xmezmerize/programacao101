# Introdução a algoritmos

*Guia feito usando Ubuntu, outros sistemas operacionais podem conter mudanças sutis na sintaxe.*

---
Um **algoritmo** é uma sequência de passos/instruções estruturadas de forma lógica para a implementação de uma solução ou resolução de um problema.

Temos 3 formas de estruturar um algoritmo:
```sh
- Descrição narrativa
- Fluxograma
- Pseudo-código
```

---
#### Descrição narrativa

Essa é a forma mais primitiva e talvez a mais fundamental no processo de aprendizado em lógica de programação. Ele consiste em descrever usando a linguagem natural estruturada. O foco está exclusivamente no **raciocínio**, **ordem das decisões** e na **clareza causal** entre ações.

Em algoritmos mais complexos, a descrição narrativa passa a incorporar **estruturas condicionais**, **repetições implícitas**, **excessões**, **fluxos** e **subprocessos**, mantendo sempre uma linha **objetiva**, **sequencial** e **não ambígua**.

Outro princípio fundamental é a **noção de estado**, esse princípio surge ao lidarmos com informações dinâmicas ao longo do algoritmo.

```sh
achar o dobro de um número:

- armazenar o número que o usuário inputar(via terminal, formulário, etc.) em uma variável;
- criar uma variável que some esse número da primeira variável por 2;
- retornar esse novo valor(via terminal, API, etc.)
```

Essa é uma forma de escrever esse algoritmo que retorne o resultado esperado, em programação há várias formas de escrever um mesmo algoritmo, essa designação ou forma de programar é denominado de **paradigma**.

---
#### fluxograma

Essa é a **representação gráfica de um algoritmo** onde símbolos específicos possuem um papel semântico bem definido. Ele descreve o **controle do fluxo**.

Os símbolos fundamentais são:
```sh
- Terminal(início/fim): representa os pontos de entrada e saída do algoritmo.
- Processo(retângulo): representação determinística -> cálculo, atribuição, atualização de variável, transformação de dados, etc.
- Entrada/saída(paralelograma): Interação com meio externo -> leitura de dados, raspagem ou exibição de resultados.
- Decisão(losango): símbolo lógico onde o fluxo se bifurca com base em uma condição booleana.
