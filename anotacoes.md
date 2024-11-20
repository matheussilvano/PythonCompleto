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
