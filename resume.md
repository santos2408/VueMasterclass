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
excetuando-se o 'script setip'. Geralmente veremos dentro dele uma declaração
"export default" que exportará um objeto de opções do componente e digamos que
esse objeto conterá as configurações do componente.

Esse objeto recebe algumas propriedades, a primeira será a 'name', onde iremos
declarar o nome formal do nosso componente, pois apenas com o nome do arquivo o
vue não consegue identificar qual componente é, portanto, com a propriedade
'name' estamos "confirmando" essa nomenclatura e isso nos permitirá chamá-lo
em outros locais do projeto.
