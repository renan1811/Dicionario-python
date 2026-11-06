# Dicionario-python

Neste README reuni os principais comandos e conceitos de Python que vimos nas aulas. Coloquei uma explicação curta para cada um e exemplos para mostrar como funcionam.

## 1. Começando: entrada e saída

### `print()`

Usamos para mostrar alguma coisa no terminal, como um texto ou o valor de uma variável.

```python
curso = "Informática"
print("Curso:", curso)
print("Bom dia!")
```

**Resultado:**
```text
Curso: Informática
Bom dia!
```

### `input()`

Pede para o usuário digitar um valor. O Python recebe esse valor como texto (`str`), mesmo que a pessoa digite um número.

```python
cidade = input("Qual é sua cidade? ")
print("Você mora em", cidade)
```

**Exemplo:**
```text
Qual é sua cidade? Joinville
Você mora em Joinville
```

## 2. Variáveis e tipos

### Variáveis

Uma variável guarda uma informação que podemos usar depois.

```python
produto = "Caderno"
quantidade = 3
valor = 12.50
print(produto, quantidade, valor)
```

**Resultado:**
```text
Caderno 3 12.5
```

### Tipos de dados

| Tipo | O que guarda | Exemplo |
| --- | --- | --- |
| `int` | Números inteiros | `25` |
| `float` | Números com decimal | `8.5` |
| `str` | Textos | `"Olá"` |
| `bool` | Verdadeiro ou falso | `False` |

### `type()`

Serve para descobrir o tipo de um valor.

```python
print(type(25))
print(type(8.5))
print(type("Olá"))
print(type(False))
```

**Resultado:**
```text
<class 'int'>
<class 'float'>
<class 'str'>
<class 'bool'>
```

### `int()`, `float()`, `str()` e `bool()`

São funções para converter um valor para outro tipo, quando a conversão é possível.

```python
print(int("20") + 5)
print(float("7.25"))
print(str(15) + " pontos")
print(bool(0))
```

**Resultado:**
```text
25
7.25
15 pontos
False
```

## 3. Operadores

### Contas: operadores aritméticos

| Símbolo | Operação | Exemplo e resultado |
| --- | --- | --- |
| `+` | Adição | `8 + 3` → `11` |
| `-` | Subtração | `8 - 3` → `5` |
| `*` | Multiplicação | `8 * 3` → `24` |
| `/` | Divisão | `8 / 3` → `2.666...` |
| `//` | Divisão inteira | `8 // 3` → `2` |
| `%` | Resto da divisão | `8 % 3` → `2` |
| `**` | Potência | `8 ** 2` → `64` |

```python
print(12 + 4)
print(12 // 5)
print(12 % 5)
```

**Resultado:**
```text
16
2
2
```

### Comparações: operadores relacionais

Usamos para comparar dois valores. A resposta será `True` ou `False`.

| Operador | Significado |
| --- | --- |
| `==` | É igual a |
| `!=` | É diferente de |
| `>` | É maior que |
| `<` | É menor que |
| `>=` | É maior ou igual a |
| `<=` | É menor ou igual a |

```python
pontos = 12
print(pontos == 10)
print(pontos >= 10)
print(pontos != 12)
```

**Resultado:**
```text
False
True
False
```

### Operadores lógicos: `and`, `or` e `not`

- `and`: as duas condições precisam ser verdadeiras.
- `or`: basta uma condição verdadeira.
- `not`: troca verdadeiro por falso e vice-versa.

```python
nota = 8
presenca = 80
print(nota >= 6 and presenca >= 75)
print(nota == 10 or presenca == 100)
print(not (nota < 6))
```

**Resultado:**
```text
True
False
True
```

### Atribuição

O `=` coloca um valor na variável. Já `+=`, `-=`, `*=`, `/=`, `//=`, `%=` e `**=` fazem uma operação e atualizam o valor dela.

```python
saldo = 20
saldo += 10
print(saldo)
saldo -= 5
print(saldo)
```

**Resultado:**
```text
30
25
```

### `in` e `not in`

Verificam se determinado valor aparece em uma sequência, como uma lista ou um texto.

```python
materias = ["Python", "Banco de Dados", "Redes"]
print("Python" in materias)
print("Matemática" not in materias)
```

**Resultado:**
```text
True
True
```

## 4. Tomando decisões no código

### `if`

Faz uma verificação. Se a condição for verdadeira, executa o bloco indentado.

```python
temperatura = 30
if temperatura > 28:
    print("Está quente")
```

**Resultado:**
```text
Está quente
```

### `else`

Define o que acontece quando a condição do `if` for falsa.

```python
numero = 14
if numero % 2 == 0:
    print("Número par")
else:
    print("Número ímpar")
```

**Resultado:**
```text
Número par
```

### `elif`

É útil quando temos mais de duas possibilidades para verificar.

```python
media = 6.5
if media >= 8:
    print("Ótima média")
elif media >= 6:
    print("Aprovado")
else:
    print("Abaixo da média")
```

**Resultado:**
```text
Aprovado
```

## 5. Repetições

### `range()`

Cria uma sequência de números, muito usada junto com `for`. O limite final não entra na sequência.

```python
print(list(range(4)))
print(list(range(3, 7)))
print(list(range(2, 11, 2)))
```

**Resultado:**
```text
[0, 1, 2, 3]
[3, 4, 5, 6]
[2, 4, 6, 8, 10]
```

### `for`

Repete um trecho de código passando pelos itens de uma sequência.

```python
for dia in range(1, 4):
    print("Dia", dia)
```

**Resultado:**
```text
Dia 1
Dia 2
Dia 3
```

### `while`

Repete enquanto uma condição continuar verdadeira. É importante atualizar a variável usada na condição para o laço não ficar infinito.

```python
tentativas = 1
while tentativas <= 3:
    print("Tentativa", tentativas)
    tentativas += 1
```

**Resultado:**
```text
Tentativa 1
Tentativa 2
Tentativa 3
```

### `break`

Interrompe um laço antes de chegar ao final.

```python
for numero in range(1, 7):
    if numero == 4:
        break
    print(numero)
```

**Resultado:**
```text
1
2
3
```

### `continue`

Pula apenas a repetição atual e segue para a próxima.

```python
for numero in range(1, 6):
    if numero == 2:
        continue
    print(numero)
```

**Resultado:**
```text
1
3
4
5
```

## 6. Funções úteis para números

### `abs()`

Retorna o valor absoluto, sem o sinal negativo.

```python
print(abs(-23))
```

**Resultado:** `23`

### `round()`

Arredonda um número. Também podemos informar quantas casas decimais queremos.

```python
print(round(9.876, 1))
print(round(4.7))
```

**Resultado:**
```text
9.9
5
```

### `pow()`

Calcula uma potência.

```python
print(pow(3, 4))
```

**Resultado:** `81`

### `min()` e `max()`

Encontram, respectivamente, o menor e o maior valor.

```python
notas = [7, 9, 5, 8]
print(min(notas))
print(max(notas))
```

**Resultado:**
```text
5
9
```

## 7. Trabalhando com textos (`str`)

### `upper()` e `lower()`

O primeiro deixa todas as letras maiúsculas, e o segundo deixa minúsculas.

```python
print("bom dia".upper())
print("ESCOLA".lower())
```

**Resultado:**
```text
BOM DIA
escola
```

### `strip()`

Retira os espaços que sobrarem nas pontas do texto.

```python
nome = "  Renan  "
print(nome.strip())
```

**Resultado:** `Renan`

### `replace()`

Substitui um trecho de uma string por outro.

```python
mensagem = "Hoje tem prova de redes"
print(mensagem.replace("redes", "Python"))
```

**Resultado:**
```text
Hoje tem prova de Python
```

### `split()`

Divide um texto em partes, formando uma lista. Podemos escolher o separador.

```python
print("azul;verde;amarelo".split(";"))
```

**Resultado:**
```text
['azul', 'verde', 'amarelo']
```

### `find()`

Procura um trecho e retorna a posição onde ele começa. Se não encontrar, retorna `-1`.

```python
palavra = "computador"
print(palavra.find("puta"))
print(palavra.find("xyz"))
```

**Resultado:**
```text
3
-1
```

## 8. Listas

### Criando e acessando uma lista

Uma lista reúne vários valores. Para acessar um item, usamos seu índice, começando pelo `0`.

```python
jogos = ["Minecraft", "Terraria", "Stardew Valley"]
print(jogos)
print(jogos[1])
```

**Resultado:**
```text
['Minecraft', 'Terraria', 'Stardew Valley']
Terraria
```

### `append()`

Coloca um novo item no fim.

```python
cores = ["azul", "verde"]
cores.append("vermelho")
print(cores)
```

**Resultado:**
```text
['azul', 'verde', 'vermelho']
```

### `insert()`

Adiciona um item na posição informada.

```python
numeros = [10, 30]
numeros.insert(1, 20)
print(numeros)
```

**Resultado:**
```text
[10, 20, 30]
```

### `remove()`

Remove um item procurando pelo valor dele.

```python
nomes = ["Ana", "Bruno", "Lucas"]
nomes.remove("Bruno")
print(nomes)
```

**Resultado:**
```text
['Ana', 'Lucas']
```

### `pop()`

Retira um elemento pela posição. Sem informar o índice, retira o último. O valor retirado também pode ser guardado.

```python
fila = ["A", "B", "C", "D"]
print(fila.pop())
print(fila.pop(0))
print(fila)
```

**Resultado:**
```text
D
A
['B', 'C']
```

### `sort()`

Organiza a lista em ordem crescente. Com `reverse=True`, organiza em ordem decrescente.

```python
valores = [12, 4, 18, 7]
valores.sort()
print(valores)
valores.sort(reverse=True)
print(valores)
```

**Resultado:**
```text
[4, 7, 12, 18]
[18, 12, 7, 4]
```

### `reverse()`

Inverte a ordem atual dos elementos, sem necessariamente colocar em ordem numérica ou alfabética.

```python
letras = ["x", "y", "z"]
letras.reverse()
print(letras)
```

**Resultado:**
```text
['z', 'y', 'x']
```

### `len()`

Conta quantos elementos existem em uma lista ou quantos caracteres há em um texto.

```python
print(len([4, 8, 12, 16]))
print(len("Escola"))
```

**Resultado:**
```text
4
6
```

## 9. Lendo e salvando arquivos

### `open()`

Abre um arquivo. Os modos principais são `"r"` (leitura), `"w"` (escrita, substitui o conteúdo anterior) e `"a"` (adiciona conteúdo ao final).

```python
arquivo = open("anotacoes.txt", "w", encoding="utf-8")
arquivo.close()
```

### `write()` e `close()`

O `write()` grava texto em um arquivo aberto para escrita. O `close()` fecha o arquivo depois do uso.

```python
arquivo = open("anotacoes.txt", "w", encoding="utf-8")
arquivo.write("Estudar Python\n")
arquivo.write("Revisar listas\n")
arquivo.close()
```

Depois desse código, o arquivo `anotacoes.txt` terá duas linhas.

### `read()`

Lê todo o texto que está no arquivo.

```python
arquivo = open("anotacoes.txt", "r", encoding="utf-8")
print(arquivo.read())
arquivo.close()
```

**Resultado:**
```text
Estudar Python
Revisar listas
```

### `readline()`

Lê uma linha por vez. Aqui usei `strip()` para tirar a quebra de linha no `print()`.

```python
arquivo = open("anotacoes.txt", "r", encoding="utf-8")
print(arquivo.readline().strip())
print(arquivo.readline().strip())
arquivo.close()
```

**Resultado:**
```text
Estudar Python
Revisar listas
```

### `with`

É uma forma mais prática de trabalhar com arquivos, porque o Python fecha o arquivo automaticamente ao sair do bloco.

```python
with open("tarefas.txt", "w", encoding="utf-8") as arquivo:
    arquivo.write("Fazer atividade\n")
    arquivo.write("Enviar no GitHub\n")

with open("tarefas.txt", "r", encoding="utf-8") as arquivo:
    print(arquivo.read())
```

**Resultado:**
```text
Fazer atividade
Enviar no GitHub
```

---

Esses são os comandos e estruturas que organizei para consultar quando estiver fazendo exercícios em Python.
