# Variáveis

*Guia feito usando Ubuntu, outros sistemas operacionais podem conter mudanças sutis na sintaxe.*

---
Em Python **variáveis** são **identificadores que fazem referência a objetos armazenados na memória**.
O Python possui uma tipagem **dinâmica e forte**, o que isso quer dizer:

**tipagem dinâmica**:
a variável é o nome que referência o objeto buscado na memória, não o valor do objeto.
```sh
Ex.
x = 10
x = 5
print(x) # 5

y = x
print(y) # 5

Python lê o código de cima para baixo e como a variável no caso é global, ele pega o último "nome" associado ao valor na memória.

x -> identificador
10/5 -> objeto (int)
= -> operador de atribuição

Essa característica é muito importante pois ela permite atribuir um objeto ou dado sem definir seu "tipo na memória", uma vez que o python usa ponteiros para referências objetos na memória ao invés de uma memória estática e pré-definida. A desvantagem é perda de velocidade de execução.

em C:
int x = 5
x = "oi"
printf(x) # erro

em Python:
x = 5
x = "oi"
print(x) # oi
```

**tipagem forte**:
o python não faz coerções implícitas e perigosas como soma entre **tipos** diferentes (str, bool, int, float, etc).
```sh
Ex.
"10" + 5 # TypeError
int("10") + 5 # 15

Em JS que tem uma tipagem fraca, o primeiro exemplo ficaria:
console.log("10" + 5) # 105
```

Isso influencia na forma como as variáveis funcionam na linguagem.

---
#### Regras de nomenclatura

Variáveis em python são **case-sensitive**(letras maiúsculas e minúsculas tem diferença).

Temos algumas formas de escrever variáveis em python:
```sh
snake_case -> palavras separadas por _:
	Ex. exemplo_de_variavel_snakecase = "snake case"

camel Case -> primeira letra minúscula, demais iniciais maiúsculas:
	Ex. variavelCamelCase = "camel Case"

Pascal Case -> todas as iniciais maiúsculas:
	Ex. VariavelPascalCase = "Pascal Case"

kebab-case -> separas por -:
	Ex. variavel-kebab-case = "kebab case"

CONSTANTE -> em python, variáveis constantes (não devem ser modificadas), são atribuidas por convenção com todas as letras maiúsculas, apesar de que, de fato, ela podem ser modificadas, então é uma convenção não alterar o valor de variáveis atribuídas dessa forma:
	Ex. CONSTANTE = "Valor constante"
```

---
#### Formas de atribuição

**Atribuição Múltipla**
```sh
a, b, c = 1, 2, 3
```

**Atribuição Encadeada**
```sh
x = y = z = 0 # todos os nomes apontam para o mesmo objeto na memória
```

---
#### Variáveis como referência

```sh
a = [1, 2, 3, 4]
b = a
b.append(4)

print(a) # 1, 2, 3, 4
```

