# Curso Python 3 completo

## Funções (def)
- São trechos de código para replicar determinada ação
- Podem receber valores para parâmetros (argumentos)
- Por padrão, retornam `none`
- Como criar uma função:
```python
def saudacao(nome):
    print(f"Olá, {nome}!")

saudacao("Mundo")
```

### Argumentos nomeados e não nomeados
- Argumentos não nomeados (ou posicionais), ecebem apenas o argumento (valor)
```python
def soma(x, y):
    print(x + y)

soma(1, 2)
```

- Argumentos nomeados possuem nome e um sinal de igual `=`
```python
def soma(x, y):
    print(x + y)

soma(y=2, x=1)
```

### Valores padrão
- Ao definir uma função, os parâmetros podem ter valores padrão
- Caso nenhum valor seja enviado ao parâmetro, o padrão será usado
```python
def soma(x, y, z=None):
    if z is not None:
        print(x + y + z)
    else:
        print(x + y)
soma(1, 2)
```
- Nesse caso, o código foi atualizado para receber `z`, porém ele recebe um **valor padrão** `None` para poder realizar operações somente com `x` e `y`

### Escopo de funções
- O escopo é o local que o código pode atingir
- Por exemplo, se um determinado código está dentro do escopo de uma função específica, não vai afetar o restante do código
#### __Escopo global__: Escopo onde todo o código é alcançável
```python
x = 1
def escopo:
    print(x)

escopo()
```
#### __Escopo local__: Escopo onde apenas nomes dentro do mesmo local podem ser alcançados
```python
def escopo:
    x = 1
    print(x)

escopo()
```
    - A variável `x` existe apenas dentro do escopo da função `escopo`, caso eu tente acessar `x` fora da função, terei o retorno: `x is not defined`

