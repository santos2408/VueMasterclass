### Creating App

- tudo começa pelo arquivo 'main.js' que irá criar a aplicação vue e irá montar
  essa aplicação diretamente no elemento raiz do index.html, ou seja, renderiza-la,
  que no caso será na div com 'id = #app' por convenção.

- No index.html teremos um 'root element', ou seja, um elemento raiz que irá
  agrupar a aplicação vue que será montada nele. Geralmente esse elemento é uma
  'div' com 'id = #app'. Na maior parte das vezes o index.html não irá renderizar
  praticamente nenhum dado, tudo será feito a partir do javascript.

- para iniciarmos uma aplicação em Vue, precisamos instanciar uma nova aplicação
  com a função 'createApp'. Essa função recebe como argumento um objeto com as
  'options' que são os dados que serão usados na aplicação ou pode-se passar
  o componente raiz diretamente

- o componente raiz que conterá todos os outros single-file components agrupados
  formando a página ao todo. A createApp só pode receber um componente e esse
  componente é chamado de 'root component' pois dentro dele contém todos os outros
  componentes da aplicação.

- quando instanciamos uma aplicação, o app é 'conectado' com o elemento raiz
  passado como 'root component', com isso ela poderá acessar os dados do app. Toda
  aplicação requer um 'root component'.

- geralmente usaremos um single-file componente e importaremos o componente raiz
  de um arquivo externo e passaremos como argumento do create app. Invocaremos
  também o método 'mount' na aplicação para montarmos o conteúdo da 'root
  component' dentro do container do DOM.

### Single-File Components

- É um componente de arquivo único com extensão (.vue) que nos permite encapsular
  o html, estilo e a lógica de um componente num só lugar. Com esse formato, isso
  nos permite importar o componente com toda sua lógica e estilo e aplica-lo em
  qualquer parte do código. Procure colocar o nome do arquivo igual ao nome do
  componente.

- Consiste de três blocos: template, script e style, mas aceitam opcionalmente
  blocos customizados adicionais.

- O componente só pode ter um bloco <template> e <script> por vez, mas para o script
  podemos ter outra tag caso ele tenha 'setup' como propriedade <script setup>. Já
  o style aceita múltiplas tags.

- Na tag script o 'export default' deve ser um vue component options object, deve
  retornar um objeto. 'export default { logica }'

- Na tag style podemos ter 'scoped' e 'module' como atributo que ajudam a
  encapsular os estilos do componente atual.

* mais sobre script setup: https://vuejs.org/api/sfc-script-setup.html
* mais sobre single-file component em: https://vuejs.org/api/sfc-spec.html
* mais sobre css scoped e module: https://vuejs.org/api/sfc-css-features.html#scoped-css
