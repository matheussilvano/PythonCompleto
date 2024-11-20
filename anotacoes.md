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

### Valores padrão para os parâmetros
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
- Nesse caso, o código foi atualizado para receber `z`, porém ele recebe um <br>valor padrão</br> `None` para poder realizar operações somente com `x` e `y`
