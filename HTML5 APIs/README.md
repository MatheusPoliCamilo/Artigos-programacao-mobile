# HTML 5 APIs

Desde a sua origem, a web como atualmente conhecemos passou por diversas modificações, principalmente em suas linguagens, ferramentas e 
arquiteturas. Como consequência, ao longo do tempo as aplicações produzidas tornaram-se mais complexas, com novas funcionalidades, 
modelos de interação e elementos visuais. Para exemplificar, no início dos anos 2000 contávamos com websites com conteúdo estático e 
layouts simples. Caso recordemos, em geral as páginas eram constituídas de uma composição de gifs, links que eram simples apontadores 
para outras páginas e várias composições de elementos `<tr>` e `<td>`, utilizados primordialmente para posicionar elementos na tela. 
Além disso, algumas delas ainda continham um conteúdo em formato de áudio mid tocando em segundo plano, o que garantia um ar de 
modernidade na época.

As páginas que queriam inovar um pouco mais e fornecer uma experiência mais rica ao usuário recorriam à utilização de plug-ins, como os 
que permitiam animações Flash (Adobe) ou applets Java (Oracle). Entre os browsers mais populares, podíamos contar com o Internet 
Explorer, em sua versão 8, e o Netscape, que mais tarde daria origem ao Firefox. O Google Chrome, por sua vez, ainda não existia, muito 
menos o Safari.

Ademais, a comunicação do cliente com o servidor funcionava através de requisições que forçavam o recarregamento completo da página, 
não explorando nenhum tipo de cache de recursos estáticos. A solução para esse problema, embora já empregada em alguns sites, só viria 
a ser oficializada cinco anos mais tarde, em 2005, através de um artigo escrito por Jesse Garrett, introduzindo o termo AJAX. Nessa 
mesma época, a arquitetura RESTful estava sendo proposta por Roy Fielding, o que seria outro grande avanço a ser adotado e que 
prevalece até os dias atuais, impulsionando as requisições AJAX. Através dessa arquitetura, pode-se realizar cache de recursos através 
da manipulação de informações nos cabeçalhos do protocolo HTTP.

Em meio a essas mudanças, notamos também a evolução dos navegadores, dos protocolos (basta lembrar que o protocolo HTTP está em sua 
segunda versão) e até mesmo das arquiteturas. A própria arquitetura cliente-servidor agora está sendo trabalhada para utilizarmos o 
servidor somente para a validação e persistência dos dados processados no cliente. Algumas vezes, no entanto, nem para esse fim ele 
será necessário, podendo ser chamado apenas no momento de carga inicial de recursos da aplicação, que rodará de forma off-line no 
cliente. Tal abordagem permite ganhos bastante significativos, uma vez que desafoga os servidores ao processar informações diretamente 
no cliente, o qual está ficando cada vez mais poderoso permitindo que essa prática se torne mais comum.

Uma vez que o servidor diminui parte do seu papel, o foco da evolução passa a ser os elementos que compõem o cliente: o browser e as 
tecnologias envolvidas, como JavaScript, HTML e CSS. O JavaScript, por exemplo, está em sua versão 1.8.5 e as engines que o interpretam 
estão ficando cada vez mais poderosas. Uma prova disso é que atualmente são encontrados mais de 15 projetos ativos de engines e um 
trabalho constante para que a experiência com a linguagem seja a mais fluída possível.

Por sua vez, o CSS atualmente está na versão 3, na qual diversas melhorias foram realizadas para facilitar a estilização e dar maior 
autonomia ao usuário, permitindo explorar também as características do dispositivo, como através da utilização de media queries, que 
permitem a utilização condicional de código CSS dependendo do tamanho da tela onde ele está sendo executado.

E, por fim, a linguagem HTML. Ela se encontra na versão 5 e constantemente recebe atualizações para simplificar a sua sintaxe, 
permitindo um maior poder de expressão e novas ferramentas para abranger os mais variados tipos de cenários, como melhorar a 
acessibilidade das páginas através dos elementos `<section>`, `<nav>`, etc. ou melhorar a visualização de elementos em uma página 
através da diretiva viewport do elemento `<meta>`.

Como vimos, JavaScript, CSS e HTML estão todos em constante evolução, e muito do que se tem feito para essa tríade está relacionado ao 
universo mobile, que trouxe mais desafios, uma vez que as aplicações agora podem trabalhar com os diversos recursos, como câmera, 
acelerômetro, etc. Além disso, agora elas são acessadas através de vários dispositivos, de características e modelos de integração 
distintos do mundo desktop. De fato, quando o universo mobile entrou em cena, deixamos de construir páginas para construirmos 
aplicativos web.

## A nova arquitetura das aplicações web

Com a chegada dos dispositivos mobile, a forma como construímos uma aplicação web teve que ser repensada. Uma vez que ela também 
precisa rodar nesses dispositivos, torna-se importante garantir a sua otimização e fluidez, assim como geralmente acontece em uma 
aplicação nativa. Para isso acontecer, é importante nos atentarmos a conceitos como rich client, single page e ao uso bem pensado de 
HTML5 e CSS3.

Uma aplicação rich client representa uma solução que possui grande parte do código executada no cliente. Tal abordagem permite alguns 
ganhos bastante significativos, pois desafoga os servidores através da redução do número de requisições, o que, por sua vez, permite 
que a aplicação se torne mais fluída, pois o tempo de resposta será encurtado.

Já a utilização de Single Page Application (ou aplicação de uma única página) sugere que a aplicação seja renderizada em apenas uma 
página web, que jamais é recarregada completamente durante as requisições. Para que a atualização do conteúdo ocorra, são utilizadas 
requisições AJAX que trazem informações para modificar apenas algumas porções da tela. No caso de uma aplicação onde apenas parte do 
conteúdo é atualizado, essa abordagem permite o reaproveitamento de várias estruturas, garantindo um cenário de otimização de recursos 
e, consequentemente, desempenho.

Unido ao conjunto de boas práticas para a construção de uma aplicação web inserida no contexto mobile, entra em cena o HTML5, que é a 
grande especificação que está tornando a web cada vez mais poderosa e funcional. Através dessa tecnologia temos acesso a APIs que fazem 
a ligação entre as funções do dispositivo nativo e a aplicação web, permitindo construir uma solução web que se comporte de forma 
semelhante a uma aplicação nativa.
