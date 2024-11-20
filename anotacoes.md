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
#### Escopo global: Escopo onde todo o código é alcançável
```python
x = 1
def escopo():
    print(x)

escopo()
```
#### Escopo local: Escopo onde apenas nomes dentro do mesmo local podem ser alcançados
```python
def escopo():
    x = 1
    print(x)

escopo()
```
- A variável `x` existe apenas dentro do escopo da função `escopo`, caso eu tente acessar `x` fora da função, terei o retorno: `x is not defined`

```python
x = 1
def funcao1():
    y = 2
    print(y)
    def funcao2():
        z = 3
        print(z)
    
```
- Nesse caso, a variável `x` está no escopo do módulo, podendo ser acessada em qualquer lugar, a variável `y` pode ser acessada tanto na `funcao1` quanto na `funcao2` e a variável `z` só pode ser acessada no escopo da `funcao2`
- Caso uma variável `x` seja declarada duas vezes em escopos separados, funcionarará como duas variáveis diferentes, possuindo um valor em cada escopo
- `global`: Transforma uma variável de escopo local em uma variável de escopo global:
```python
def escopo():
    global x
    x = 10    # esse x funcionará fora do escopo da função
```

### Return
- Caso não haja um `return`, a variável retornará `none` por padrão
- Exemplo de função com retorno:
```python
def soma(x, y):
    return x + y

soma1 = soma(2, 2)
soma2 = soma(3, 3)
print(soma1 + soma2)
```
- Caso não fosse usado o `return`, o Python tentaria somar `none` + `none`, o que acarretaria em um erro
- Não se pode colocar nada em uma função após o `return`, pois será um código **inalcansável**

### \*args
