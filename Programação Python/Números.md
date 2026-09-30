Os números são usados com muita frequência em programação para ==armazenar pontuações em jogos, representar dados em visualizações, guardar informações em aplicações web e assim por diante.== Python trata números de várias maneiras diferentes, de acordo com o modo como são usados. Vamos analisar inicialmente como Python trata inteiros, pois eles são os dados mais simples para trabalhar.

#### Inteiros 
Você pode somar (+), subtrair (-), multiplicar (*) e dividir (/) inteiros em Python.
>>> 2 + 3
>>>  5 
>>>  >>> 3 - 2
>>>  >>>  1
>>>  >>>   >>> 2 * 3
>>>  >>>   >>>  6
>>>  >>>   >>>   >>> 3 / 2 
>>>  >>>   >>>   >>> 1.5

 Em uma sessão de terminal, Python simplesmente devolve o resultado da operação. Dois símbolos de multiplicação são usados em Python para representar exponenciais:
  >>> 3 ** 2 
  >>> 9
  >>>  >>> 3 ** 3
  >>>  >>>  27
  >>>  >>>   >>> 10 ** 6
  >>>  >>>   >>>  1000000

A linguagem Python também aceita a ordem das operações, portanto você pode fazer várias operações em uma expressão. Também podemos usar parênteses para modificar a ordem das operações para que Python possa avaliar sua expressão na ordem que você especificar. Por exemplo:
>>> 2 + 3*4 
>>> 14
>>>  >>> (2 + 3) * 4 
>>>  >>> 20 

Os espaços nesses exemplos não têm nenhum efeito no modo como Python avalia as expressões: eles simplesmente ajudam a identificar mais rapidamente as operações que têm prioridade quando lemos o código.

#### Números de ponto flutuante
Python chama qualquer número com um ponto decimal de número de ponto flutuante (float). Esse termo é usado na maioria das linguagens de programação e refere-se ao fato de ==um ponto decimal poder aparecer em qualquer posição em um número.== Toda linguagem de programação deve ser cuidadosamente projetada para lidar de modo adequado com números decimais de modo que eles se comportem de forma apropriada, não importa em que lugar o ponto decimal apareça. Na maioria das ocasiões, podemos usar decimais sem nos preocupar com o modo como eles se comportam. Basta fornecer os números que você quer usar, e Python provavelmente fará o que você espera:
>>> 0.1 + 0.1
>>>  0.2 
>>>  >>> 0.2 + 0.2 
>>>  >>> 0.4
>>>  >>>  >>> 2 * 0.1 
>>>  >>>  >>> 0.2 
>>>  >>>  >>> >>> 2 * 0.2 
>>>  >>>  >>> >>> 0.4 

 No entanto, tome cuidado, pois, às vezes, você poderá obter um número arbitrário de casas decimais em sua resposta: 
 >>> 0.2 + 0.1 
 >>> 0.30000000000000004 
 >>> >>> 3 * 0.1 
 >>> >>> 0.30000000000000004 

Isso acontece em todas as linguagens e não é motivo para muita preocupação. Python tenta encontrar uma forma de representar o resultado do modo mais exato possível, o que, às vezes, é difícil, considerando a maneira como os computadores devem representar os números internamente. Basta ignorar as casas decimais extras por enquanto; você aprenderá a lidar com casas extras quando for necessário nos projetos da Parte II.

#### Evitando erros de tipo com a função str()
Com frequência, você vai querer usar o valor de uma variável em uma mensagem. Por exemplo, suponha que você queira desejar feliz aniversário a alguém. Você poderia escrever um código como este:
`birthday.py` 
`age = 23`
`message = "Happy " + age + "rd Birthday!"`
`print(message)`

Você esperaria que esse código exibisse a seguinte saudação simples de feliz aniversário: Happy 23rd birthday!.

Contudo, se executar esse código, verá que ele gera um erro: 
`Traceback (most recent call last):` 
`File "birthday.py", line 2, in message = "Happy " + age + "rd Birthday!"`
`u TypeError: Can't convert 'int' object to str implicitly` 

É um erro de tipo. ==Significa que Python não é capaz de reconhecer o tipo de informação que você está usando==. Nesse exemplo, Python vê que você está usando uma variável em u cujo valor é um inteiro (int), mas não tem certeza de como interpretar esse valor. O interpretador sabe que a variável poderia representar um valor numérico 23 ou os caracteres 2 e 3. Quando usar inteiros em strings desse modo, você precisará especificar explicitamente que quer que Python utilize o inteiro como uma string de caracteres. ==Podemos fazer isso envolvendo a variável com a função str();== essa função diz a Python para representar valores que não são strings como strings:
`age = 23` 
`message = "Happy " + str(age) + "rd Birthday!"`
`print(message)`

Com isso, Python sabe que você quer converter o valor numérico 23 em uma string e exibir os caracteres 2 e 3 como parte da mensagem de feliz aniversário. Agora você obterá a mensagem esperada, sem erros: Happy 23rd Birthday! Trabalhar com números em Python é simples na maior parte do tempo. Se você estiver obtendo resultados inesperados, verifique se Python está interpretando seus números da forma desejada, seja como um valor numérico, seja como um valor de string.