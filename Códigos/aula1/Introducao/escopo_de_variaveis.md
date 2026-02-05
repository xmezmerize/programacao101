# Escopo de Variáveis

*Guia feito usando Ubuntu, outros sistemas operacionais podem conter mudanças sutis na sintaxe.*

---
Em Python, o escopo de variáveis é um conceito importante para entendermos o
comportamento de um código, tornando simples e legível.

Quando o Python encontra um nome, ele procura nessa ordem:

1. L - Local
2. E - Enclosing (não local)
3. G - Global
4. B - Built-in

---
#### Local

No escopo local, variáveis pertencem a um contexto, uma parte do código com uma função, por exemplo.

```sh
x = 10

def local():
	x = 2
	return x

print(x) # 10 -> escopo global
print(local()) # 2 -> escopo local
```

---
#### Enclosing (não local)

Enclosing é o elo entre funções aninhadas, compartilhando estado sem usar variáveis globais.

```sh
def externa():
	x = 10
	
	def interna():
		return x
		
	def soma_interna(f: int = interna()) -> int:
		soma = f + 10
		return soma
		
	return soma_interna()
	
print(externa()) # 20
```
  
Tanto a variável `x` quanto `soma` funcionam apenas dentro do escopo inicial `externa()`. O python tem uma característica essencial que é o `nonlocal`, sem essa propriedade o `x` de fora de `interna()` e o `x` dentro de `interna()` teriam outro valor.

---
#### Global

Variáveis globais podem ser acessadas por todo código.

```sh
aqui eu não defino no escopo local nenhum valor associado a n:

n = 10

def f():
	return n 
	
print(f()) # 10


também é possível alterar o valor de uma variável global:

r = 10

def t():
	global r
	r = 5
	
t()
print(r) # 5
```

---
#### Cuidados

**UnboundLocalError** - Ocorre quando o python **interpreta uma variável como local**, mas ela é **lida antes de receber valor** dentro de um função.

**Design de Código** - Tome cuidado com identação e atribuição de variáveis durante a criação de um programa pois pode se tornar um produto de difícil manutenção e muito aninhado. O ideal é evitar variáveis globais e usar sempre contexto nas variáveis.
