## Directives

1 - Diretivas são atributos especiais escritos com prefixo (v-) e que são
fornecidos pelo Vue. Espera-se que os valores das diretivas sejam expressões
javascript únicas, com exceção das diretivas v-for, v-on e v-slot que veremos
mais adiante. A função de uma diretiva é aplicar atualizações no DOM de forma
reativa sempre que o valor da sua expressão mudar.

No vue as diretivas serão 'tags' especiais que serão incluídas nos elementos
HTML como se fossem attributos e que irão aplicar algum comportamento especial
a esse atributo.

Algumas diretivas recebem argumentos, que são inseridos após o nome da diretiva
e dois pontos: v-bind:href. Podemos também utilizar shorthand para diminuir o
tamanho da declaração, com shorthand, tudo que estiver anterior ao argumento será
condensado em um único caracter, que pode ser dois pontos ou arroba. Vale lembrar
que nem todas as diretivas contém um shorthand.

- Normal: v-bind:href / v-on:click
- Shorthand: :href / @click

Podemos também passar uma expressão javascript como argumento de uma diretiva,
para isso basta colocar a expressão entre cholchetes.

---

v-bind: nos permite unir um valor dinâmico a um ou mais atributos, usa-se ':'
como shorthand. Pode-se unir com atributos class, style, src, href, entre outros.
Portanto os valores passados dentro do v-bind serão dinâmicos. Resumidamente o
v-bind torna o atributo dinâmico, podendo receber valores através de uma API ou
banco de dados.

podemos passar valores normais, bem como arrays e objetos com algum valor
booleano que nos retornará o nome da classe. Em objetos as 'keys' serão os nomes
das classes e o 'valor' será a expressão que retorna um booleano. Nos arrays
cada item é o nome da classe, podendo receber também objetos.

v-for: renderiza um elemento ou template multiplas vezes baseado nos dados do
script. Para utilizar essa diretiva precisamos passar um valor que será iterado
por ela. Deve-se passar uma sintaxe especial, que é (item in expressão) para que
os dados sejam iterados, podemos iterar sobre arrays, objetos e outros dados.

Podemos passar como argumento o item atual que está sendo iterado e também
receber o seu index, o que é opcional. Por padrão o v-for não move o elemento de
local, para forçarmos ele a organizar os elementos, o vue precisa de uma diretiva
'v-bind:key' para que ele possa identificar cada item iterado.

- atributo 'key': na maioria das vezes o v-for precisará ser seguido de um
  atributo 'key', esse atributo é usado para ajudar o Vue a 'rastrear' os v-nodes
  no DOM, fazendo com que sejam reorganizados ou removidos caso tenha alguma
  alteração. Para filhos do mesmo pai, o 'key' deve receber um identificador
  único como valor, caso contrário retornará um erro.

v-show: essa diretiva alterna a visilidade do elemento baseado no valor booleano
da expressão passada como 'argumento' dela. Ela funciona inserindo uma propriedade
'display: none' no elemento em questão, portanto o elemento continua existindo
na árvore do DOM, mas está apenas invisível.

v-if / v-if-else / v-else: semelhante a v-show, alterna a visilidade do elemento,
no entanto ela não adiciona a propriedade 'display: none' quando a expressão
resulta false, e sim remove totalmente o elemento da árvore do DOM. Ou seja, o
elemento é destruído ou reconstruído dependendo do seu retorno booleano. Use-as
em ordem de declaração.

Vale lembrar que v-if tem maior prioridade do que v-for, não é recomendado
utilizar estas duas diretivas num mesmo elemento. Vale lembrar que essa diretiva
consome também mais poder de processamento do vue, já que ela destrói o elemento
e cria novamente. Das três diretivas, a v-else não espera uma expressão como
'argumento'.

v-model: cria uma associação bi-direcional em uma formulário ou componente, é
limitado a input, select, textarea e componentes.

basicamente conseguimos passar um valor padrão para um campo, mas se o usuário
modificar esse campo, com o v-model nós poderemos atualizar dinamicante o valor
deste campo sem precisar mexer no código. Ele define o valor do formulário com
base no que o usuário coloca.

com isso podemos capturar o valor que está sendo digitado pelo usuario e armazenar
num array, objeto, variável ou banco de dados. Em alguns blocos como radio e checkbox
é necessário inserir o 'value' do formulário.
