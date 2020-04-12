# Web Components

Como desenvolvedores, sabemos que é uma boa ideia reutilizar o código o máximo que pudermos. Tradicionalmente, isso não tem sido fácil 
quando o assunto são estruturas de marcação customizadas, pense no complexo HTML (e estilo e script associados) que, às vezes, deve ser 
escrito para renderizar controles UI customizados e em como utilizá-los repetidas vezes pode tornar sua página uma bagunça se você não 
tomar cuidado.

**Web Components** buscam resolver esses problemas, são formados por três tecnologias principais, que podem ser usadas em conjunto para 
criar elementos customizados versáteis, com funcionalidade encapsulada, que podem ser reutilizados onde você quiser sem preocupação com 
conflito de código.

* **Elementos customizados**: Um conjunto de APIs JavaScript que permite definir elementos customizados e seus respectivos comportamentos, 
podendo ser utilizados de diferentes formas na interface da aplicação.
* **Shadow DOM**: Um conjunto de APIs JavaScript para incorporar uma árvore DOM "fantasma" encapsulada a um elemento — que é renderizada 
separadamente do DOM do documento principal — e controlar a funcionalidade associada. Nesse caso, você pode manter os recursos de um 
elemento privados, fazendo com que seu comportamento e estilo possam ser escritos sem medo de causar conflito com outras partes do 
documento.
* **Templates HTML**: Os elementos <template> e <slot> permitem que você escreva templates de marcação que não são exibidas na página. Elas 
podem então ser reutilizadas várias vezes como modelo de estrutura de um elemento customizado.
