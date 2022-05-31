## Rendering Data to View

1 - Ao criarmos um componente, devemos nomeá-lo de forma consistente, nesse caso
utilizando a chamada "pascal case" que consiste em colocar letra maiúscula na
primeira letra de cada palavra do componente, similar ao "capitalize" do CSS. Um
componente é composto por três tags: template, script e style

2 - A tag 'template' representa o HTML do nosso componente e que será renderizado
por ele no final. Um componente contém no máximo apenas uma tag template

3 - A tag 'script' é onde poderemos adicionar qualquer código javascript para
este componente. Podemos inserir nela as funcionalidades desse componente e como
ele irá funcionar na aplicação. Cada componente contém no máximo uma tag script,
excetuando-se o 'script setup'. Geralmente veremos dentro da tag 'script' uma
declaração "export default" que exportará um objeto de opções do componente
e digamos que esse objeto conterá as configurações do componente.

- Esse objeto recebe algumas propriedades, a primeira será a 'name', onde iremos
  declarar o nome formal do nosso componente, pois apenas com o nome do arquivo o
  vue não consegue identificar qual componente é, portanto, com a propriedade
  'name' estamos "confirmando" essa nomenclatura e isso nos permitirá chamá-lo
  em outros locais do projeto.

- Em seguida declaramos a propriedade 'components', que registra os componentes
  a serem usados pela instância do componente que importarmos. Caso o nome da
  propriedade seja igual ao nome do componentes podemos utilizar a sintaxe o s
  horthand property name.

4 - Quando inserimos o nosso componente dentro da tag 'template', devemos
inserir o nome do componente como se fosse uma tag HTML normal, utilizando de
'pascal case' com abertura e fechamento de tag. Podemos também adicionar o mesmo
componente quantas vezes quisermos; Existem outras maneiras se renderizar o
componente e que o Vue aceita também, são elas:

- podemos usar a sintaxe de 'kbob case' que consiste na inserção de hífen em
  todo momento de capitalize do nome do componente. Ex: MainNav / main-nav.
  Portanto, podemos escolher entre as nomentaclaturas de <MainNav> ou <main-nav>
  para o componente. No entatno, vale lembrar que o nome do componente dentro da
  propriedade 'name' continua sendo do mesmo formato, em pascal case.

- caso nosso componente não receba nenhum conteúdo dentro dele, não precisamos
  adicionar a tag de fechamento, basta adicionar uma única tag com fechamento
  implícito que o componente será renderizado normalmente. Ex: <main-nav />

5 - Dentro do nosso componente, na parte onde se encontra nosso script, além
de propriedade 'name' que vimos anteriormente, podemos adicionar também um
método "data" que permitirá nos "conectarmos" com o HTML de forma dinâmica.
Essa é uma parte da "reatividade" do Vue, com o método data podemos realizar
mudanças no nosso DOM dinamicamente. Ele retorna um estado inicial de reatividade
do nosso componente.

O método "data" deve retornar um objeto com propriedades disponíveis para uso
dentro do HTML. Dentro desse objeto serão passadas as propriedades que serão
"adicionados/injetadas/interpoladas" no nosso HTML. Esses dados podem ser
strings, números, arrays, objetos, requisições de api,entre outros.

Para inserirmos a nossa informação dinâmica dentro do documento HTML, devemos
adicionar uma interpolação chamada também de "mustache". {{ exemplo }}.
Essa interpolação nos permite unir o DOM renderizado com as informações da
instância de data do componente criando assim um dado reativo.
