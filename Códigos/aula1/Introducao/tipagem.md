# Tipagem - Python


Python utiliza tipagem **dinâmica**, o que quer dizer que o **tipo** (int, str, float, etc) é inferido pelo interpretador em tempo de execução (isso é conhecido como **Duck Typing**). No momento em que uma variável é criada através de atribuição (`atribuição = objeto`), o interpretador define um tipo para a variável.

```sh
Em python (dinâmica):
	num = 15 # quando eu executar será int
	num = float(15) # troquei o tipo do objeto para float, ao dar print o retorno será "15.0"
	
Em C (estática):
	str nome = 'Pedro' # tipo definido na declaração da variável e não pode ser alterado depois.
```

Python também possui uma tipagem **forte** o que significa que ele não faz coerção automática entre tipos:

```sh
Em python (tipagem forte):
	num1 = "50" # str
	num2 = 5 # int
	soma = num1 + num2 # TypeError
	
Em JS (tipagem fraca):
	let num1 = "50" # str
	let num2 = 5 # int
	let soma = num1 + num2 # 505
```

