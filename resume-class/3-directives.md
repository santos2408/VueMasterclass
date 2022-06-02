## Directives

1 - Diretivas são atributos especiais escritos com prefixo (v-) e que são
fornecidos pelo Vue. Espera-se que os valores das diretivas sejam expressões
javascript únicas, com exceção das diretivas v-for, v-on e v-slot que veremos
mais adiante. A função de uma diretiva é aplicar atualizações no DOM de forma
reativa sempre que o valor da sua expressão mudar.

Algumas diretivas recebem argumentos, que são inseridas após o nome da diretiva
e dois pontos: v-bind:href. Podemos também utilizar shorthand para diminuir o
tamanho da declaração, com shorthand, tudo que estiver anterior ao argumento será
condensado em um único caracter, que pode ser dois pontos ou arroba.

- Normal: v-bind:href / v-on:click
- Shorthand: :href / @click

Podemos também passar uma expressão javascript como argumento de uma diretiva,
para isso basta colocar a expressão entre cholchetes.

---

v-bind: nos permite unir um valor dinâmico a um ou mais atributos, usa-se ':'
como shorthand. Pode-se unir com atributos class, style, src, href, entre outros.
Portanto os valores passados dentro do v-bind serão dinâmicos.

v-for: renderiza um elemento ou template multiplas vezes baseado nos dados do
script. Para utilizar essa diretiva precisamos passar um valor que será iterado
por ela. Deve-se passar uma sintaxe especial, que é (item in expressão) para que
os dados sejam iterado, podemos iterar sobre arrays, objetos e outros dados.

- atributo 'key': na maioria das vezes o v-for precisará ser seguido de um
  atributo 'key', esse atributo é usado para ajudar o Vue a 'rastrear' os v-nodes
  no DOM, fazendo com que sejam reorganizados ou removidos caso tenha alguma
  alteração. Para filhos do mesmo pai, o 'key' deve receber um identificador
  único como valor, caso contrário retornará um erro.
