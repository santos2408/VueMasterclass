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

v-bind: une um ou mais atributos dinamicamente, usa-se ':' como shorthand.
Pode-se unir com atributos class, style, src, href, entre outros.
