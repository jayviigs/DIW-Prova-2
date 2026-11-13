 Questão 1 

a) O window.location.search pega os parâmetros que aparecem na URL
depois do ?. Nesse caso, ele retorna id=3. O get("id") pega o
valor do parâmetro, que inicialmente é uma string. Por isso, o
Number() é usado para transformar o valor em número e conseguir comparar com o
ID dos heróis.

b) O find() percorre o array procurando um item que atenda à
condição informada. Quando encontra um herói com o ID correspondente,
retorna o objeto dele. Caso não encontre, retorna uma mensagem de erro.

c) Sem o Number(), o ID seria uma string 3, enquanto o ID do
herói seria um número 3. Como o === compara também os tipos dos
valores, eles não seriam considerados iguais e apareceria a mensagem
"Item não encontrado".

d) O return serve para interromper a função caso o herói não seja
encontrado. Sem ele, o código continuaria tentando acessar as
propriedades de um objeto que não existe (`undefined`), causando um
erro.

 Questão 2

a) O querySelector() procura um elemento na página usando um
seletor. Ele retorna o primeiro elemento encontrado ou null caso
não encontre nenhum.

b) Essas linhas verificam se determinado elemento existe antes de
executar uma função. Isso permite utilizar o mesmo arquivo JavaScript em
páginas diferentes, sem causar erros quando algum elemento não estiver
presente. Quando o elemento existe, a condição é verdadeira; quando
retorna null, é falsa.

c) Quando a URL possui ?tipo=Mangá, o código pega esse valor e
seleciona a opção correspondente no campo de categoria. Se o parâmetro
não existir, o get() retorna null e o campo continua com sua opção
padrão.

d) Ao abrir o index.html, a parte do catálogo será executada
normalmente. Porém, depois o código também chamará renderDetalhes(),
mesmo que o elemento #detalhe não exista nessa página. Quando tentar
executar alvo.innerHTML, ocorrerá um erro, porque alvo será null.

 Questão 3 

a) O código utiliza o operador % para identificar quando deve
criar um novo slide. Como existem 12 filmes e cada slide comporta 5
cards, serão criados 3 slides: dois com 5 filmes e um com os 2
restantes.

b) O matchMedia() verifica se a tela possui largura de até 767
pixels. A função atualizar() é executada inicialmente e também quando
o tamanho da tela muda. A linha 5 limpa o carrossel antes de montar os
slides novamente, evitando que os cards antigos continuem aparecendo ou
sejam duplicados.

c) Como o filme de ID 1 foi removido, o primeiro filme agora possui
ID 2. A condição "(2 - 1) % 5 === 0" será falsa, então nenhum slide será
criado e slideAtual continuará como null. Quando o código tentar
executar slideAtual.appendChild(card), ocorrerá um erro.

 Questão 4 

a) O trim() remove os espaços do começo e do final do texto. O
toLowerCase() transforma tudo em letras minúsculas, facilitando a
comparação. Já !lista.length verifica se a lista está vazia, ou seja,
se nenhum livro foi encontrado.

b) O filter() seleciona os livros que atendem às condições,
enquanto o includes() verifica se o título contém o texto pesquisado.
O && exige que duas condições sejam verdadeiras ao mesmo tempo,
enquanto o || permite que uma das condições seja verdadeira. Os
parênteses organizam essas comparações para que a categoria "Todas"
funcione corretamente.

As linhas 17 e 18 fazem a busca ser atualizada quando o usuário digita
algo ou muda a categoria.

c) (1) o ID exibido é 3. (2) os IDs exibidos são 1 e 5 (3) os IDs exibidos são 4 e 6.

d) Um exemplo seria pesquisar "xyz" com a categoria Romance. Com os
parênteses, nenhum livro apareceria, porque nenhum título contém esse
termo. Sem os parênteses, os livros da categoria Romance poderiam
aparecer mesmo sem corresponder à busca, por causa da prioridade dos
operadores && e ||.

 Questão 5

a) O id obtido pelo get() é uma string, enquanto f.id é um
número. O operador == consegue comparar os dois fazendo uma conversão
automática de tipo. Se fosse utilizado ===, o filme não seria
encontrado porque os tipos são diferentes.

b) Ao acessar detalhe.html?id=99, o find() não encontra nenhum
filme e retorna indefinido. O erro acontece quando o código tenta
acessar filme.poster, já que o filme não existe. No console,
apareceria uma mensagem semelhante a
Cannot read properties of undefined (reading 'poster').
