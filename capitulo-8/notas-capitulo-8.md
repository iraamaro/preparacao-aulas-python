# 8 - Funções

Blocos de códigos para fazer uma tarefa em especial. Bem usual para não manter o comportamento de repetir a si (do not repeat yourself - D.R.Y.).

## Definição e informações

**Exemplo simples de função:**

```python
def greet_user():
    """Exibe uma saudação simples."""
    print("Hello!")
 
 greet_user()
```

**Exemplo de função com parâmetro:**

```python
def greet_user(username):
    """Exibe uma saudação simples."""
    print("Hello, " + username.title() + "!")
    
greet_user('jesse')
```

### Exercício 8.1 - Mensagem

Escreva uma função chamada **display_message()** que mostre uma frase informando a todos o que você está aprendendo neste capítulo. Chame a função e certifique-se de que a mensagem seja exibida corretamente.

```python
def display_message():
    print("Aprendendo sobre funções em Python3!")
    
display_message()
```
### Exercício 8.2 - Livro favorito

Escreva uma função chamada **favorite_book()** que aceite um parâmetro title. A função deve exibir uma mensagem como: *Um  dos  meus livros favoritos é Alice no país das maravilhas*. Chame a função e não se esqueça de incluir o título do livro como argumento na chamada da função.

```python
def favorite_book(title):
    print("Um dos meus livros favoritos é: {}.\n".format(title))
    
favorite_book("A arte da guerra")
```

## Argumentos e argumentos posicionais

**Posicionamento, quantidade de chamadas e ordenação**

```python
def describe_pet(animal_type, pet_name):
    """Exibe informações sobre um animal de estimação."""
    print("\nI have a " + animal_type + ".")
    print("My " + animal_type + "'s name is " + pet_name.title() + ".")
 
describe_pet('hamster', 'harry')
describe_pet('dog', 'willie')
```
**Nomeação**

```python
def describe_pet(animal_type, pet_name):
    """Exibe informações sobre um animal de estimação."""
    print("\nI have a " + animal_type + ".")
    print("My " + animal_type + "'s name is " + pet_name.title() + ".")
    
describe_pet(animal_type='hamster', pet_name='harry')
```

**Valores dfault**

Atenção quanto a posição do argumento ao chamar a função.

```python
def describe_pet(pet_name, animal_type='dog'):
    """Exibe informações sobre um animal de estimação."""
    print("\nI have a " + animal_type + ".")
    print("My " + animal_type + "'s name is " + pet_name.title() + ".")
 
describe_pet(pet_name='willie')
describe_pet('totó')

```
### Exercício 8.3 - Camisetas

Escreva  uma  função  chamada  **make_shirt()**  que  aceite  um tamanho e o texto de uma mensagem que deverá ser estampada na camiseta. A função deve exibir uma frase que mostre o tamanho da camiseta e a mensagem estampada. Chame  a  função  uma  vez  usando  argumentos  posicionais para  criar  uma camiseta. Chame a função uma segunda vez usando argumentos nomeados.


### Exercício 8.4 - Camisetas grandes

Modifique a função **make_shirt()**  de  modo  que  as camisetas sejam grandes por default, com uma mensagem Eu  amo  Python.  Crie uma camiseta grande e outra média com a mensagem default, e uma camiseta de qualquer tamanho com uma mensagem diferente.

### Exercício 8.5 - Cidades

Escreva  uma  função  chamada  **describe_city()**  que  aceite  o nome de uma cidade e seu país. A função deve exibir uma frase simples, como Reykjavik  está  localizada  na  Islândia.  Forneça  um  valor  default  ao parâmetro que representa o país. Chame sua função para três cidades diferentes em que pelo menos uma delas não esteja no país default.