De modo abstrato, o compilador é um programa que converte código de uma
linguagem para outra. Como se fosse uma função do tipo `compilador(str) -> str`.
No caso de compiladores que emitem código de máquina ou bytecode, seria mais
preciso dizer `compilador(str) -> bytes`, mas a idéia básica é a mesma.

De forma geral o processo é dividido em etapas como abaixo

```python
def compilador(x1: str) -> str | bytes:
    x2 = lex(x1)        # análise léxica
    x3 = parse(x2)      # análise sintática
    x4 = analysis(x3)   # análise semântica
    x5 = optimize(x4)   # otimização
    x6 = codegen(x5)    # geração de código
    return x6
```

Defina brevemente o que cada uma dessas etapas realizam e marque quais seriam os
tipos de entrada e saída de cada uma dessas funções. Explique de forma clara o
que eles representam. Você pode usar exemplos de linguagens e/ou compiladores
conhecidos para ilustrar sua resposta. Salve sua resposta nesse arquivo.

# lex(x1: str) -> list[token]
Transforma o codigo fonte em uma lista de tokens.
 
# parse(x2: list[token]) -> ast
Organiza os tokens em uma estrutura hierarquica (ast).

# analysis(x3: ast) -> ast
Verifica a semantca do codigo e anota a ast com informaçoes.

# optimize(x4: ast) -> ast
Transforma a ast em uma versão mais enfciente e com mesma semantica

# codegen(x5: ast) -> bytes
Converte a ast em código de maquinna.