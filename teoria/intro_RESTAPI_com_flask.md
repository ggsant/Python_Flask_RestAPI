# Introdução

**Requisitos Básicos**
* windows, linux ou OSX 
* Lógica de Programação
* Possuir fundamentos em Python

# O que é uma API 

* É um conjunto de rotinas para acesso a um app/softwares/web.
* importantes quando se tem a intenção de realizar interações com outros serviços.
* Com as APIs a comunicação de software fica transparente ao usuario.
* podem ser locais, baseadas em web e baseadas em programas

API’s são heróis desconhecidos do nosso mundo online. Elas conectam bilhões de dispositivos e aplicações de forma segura e são a principal forma de integração de dados na era atual.

API significa **“Interface de programação de aplicativos”** ou “Application program interface”. A Wikipédia define uma API como *“um conjunto de definições e protocolos de subprograma para a construção de interações entre softwares”.*

As APIs são uma ferramenta maravilhosa para desenvolvedores porque eles **simplificam a programação através da abstração.** O desenvolvedor tem acesso aos **dados, objetos e ações** que eles necessitam e não precisam se preocupar com a implementação subjacente. Em suma, uma API protege o sistema que serve os dados permitindo ou negando acesso de acordo com a necessidade.

Uma API é a interface que permite que as aplicações de software se comuniquem entre si. Como um mensageiro que retransmite solicitações e respostas entre duas partes. Veja o exemplo.

Imagine que uma API é um garçom em seu restaurante favorito. Você está sentado à mesa olhando o menu decidindo o que pedir. A cozinha, também conhecida como o provedor, atenderá seu pedido. Mas como a cozinha saberá o que você quer? E como o seu pedido vai chegar até você? Por meio do garçom.

**O garçom leva o seu pedido (input), e o entrega à cozinha, que depois devolve a comida (output) de volta para você. O mesmo papel faz a API!**

Agora, vamos aplicar isso a um verdadeiro exemplo de API. Digamos que estamos reservando um hotel para uma viagem. O processo de busca de um hotel online é similar, você escolhe o dia em que deseja fazer o check-in, check-out e outras variáveis, como a preferência do quarto.

No processo de reserva do seu quarto de hotel, você está interagindo com o site de reservas que por sua vez acessa o banco de dados de diversos hotéis para verificar se há algum quarto disponível nestas datas. Da mesma forma como você interage com o site de reserva para obter as informações, o site de reservas irá interagir com a API do hotel.

**A API é a interface, que entende o que está sendo solicitado, realiza a pesquisa por meio de um comando pré-estabelecido e retorna os dados para o sistema que solicitou.**

O mesmo ocorre com todas as interações entre aplicativos, dados e dispositivos — as APIs são o que permitem que estes se conectem, obtenham dados.


# O que é REST

* É um modelo a ser utilizado para projetar arquitetuas de software baseado em comunicação via rede.
* Projeta a ideia de que todo recurso deveria responder aos mesmos métodos. 

Ao contrário de que muitos pensam, REST não tem nada haver com descansar (rest em inglês ). **REST são siglas para Representational State Transfer ou em português Transferência de Estado Representacional.**

REST não é uma arquitetura, biblioteca ou framework, é simplesmente um **modelo que é utilizado para projetar arquitetura de softwares distribuídos que fazem comunicação de dados pela rede, seja local ou a famosa Internet**.

Esse modelo foi criado por Roy Fielding um dos principais responsáveis e criadores do **protocolo HTTP,** basicamente, tudo que está online utiliza o protocolo HTTP ou o HTTPS que é a evolução do mesmo.

Quando o modelo se popularizou, desenvolvedores começaram a utiliza-lo para criar Serviços para fazer integrações com aplicações de diversos segmentos, nessa época o modelo para fazer essas integrações mais popular era o **SOAP**, o SOAP ainda é muito utilizado, principalmente no Brasil pelos órgãos governamentais, infelizmente.

**Separação de responsabilidades**

No REST a implementação do cliente (front-end) e do servidor (back-end) são feitas separadamente sem nenhuma interferência de um ou outro. Isso significa que os dois podem ser desenvolvidos e refatorados separadamente. Mas uma hora ou outra o cliente irá precisar se comunicar com a aplicação REST para poder usufruir dos dados que a mesma disponibiliza para consumo.

Aplicações em REST seguem um paradigma que é chamado de **STATELESSNESS**, ou seja, **não possui estado**, portanto o servidor não precisa saber em qual estado o cliente (front-end) está e vice-versa, cada nova comunicação é tratada de forma independente e os estados anteriores não interferem no resultado de uma futura requisição.

**Comunicação entre Front-end e Back-end**

No modelo REST, o front-end manda requisições para receber ou modificar dados, e o back-end envia respostas para cada requisição, seja ela uma resposta de sucesso, erro, os dados em si e etc…

**Fazendo requisições**

O REST precisa que o front-end faça uma requisição para o back-end para enviar ou modificar dados no servidor, onde o back-end fica. Um requisição consiste em:
**um verbo ou método HTTP, que define que tipo de operação o back-end vai realizar um header, ou seja, cabeçalho da requisição que passa informações sobre a requisição um path (caminho ou rota) para o back-end,** como por exemplo http://minhaapi.show.br/meucaminho informação no body, ou seja, no corpo da requisição, sendo essa informação opcional

# O que é REST API

* É uma API desenvolvida utilizando os principios da arquitetura REST. 
* Um REST API é utilizado na comunicação/integração entre software atraves de serviços web.
* Um REST API é consumido através de requisições HTTP.
* REST APIs são geralmente representadas em seus formatos por JSON e XML. Tambem são usados paginas HTML, PDF, e arquivos de imagens.
* Ao implementar um REST API, cada método deve ser responsavel por um tipo diferente de ação. Exemplo: Consulta, Alteração, Inclusão e Exclusão.

Considere um cenário em que você está usando o aplicativo Book My Show. Obviamente, este aplicativo precisa de muitos dados de entrada, pois os dados presentes no aplicativo nunca são estáticos. Ou são filmes sendo lançados com frequência, ou várias cidades exibindo filmes em diferentes idiomas em vários momentos do dia. **Nunca é estático, o que implica no fato de que os dados estão sempre mudando nesses aplicativos.**

Agora, de onde você acha que obtemos esses dados?
Bem, esses dados são recebidos do servidor ou mais comumente conhecidos como um servidor web. Assim, **o cliente solicita ao servidor as informações necessárias, por meio de uma API, e o servidor envia uma resposta ao cliente.**

Aqui, a resposta enviada ao cliente está na forma de uma página da Web em HTML. Mas, você acha que esta é uma resposta adequada que você esperaria ao enviar uma solicitação?

Bem, estou assumindo o fato de que você diria NÃO. Desde então, você prefere que os dados sejam retornados na forma de um formato estruturado, em vez da página da Web completa.

Portanto, por tais motivos, os dados retornados pelo servidor, em resposta à solicitação do cliente, estão no formato JSON ou XML. Os formatos JSON e XML possuem uma estrutura hierárquica adequada de dados.
Agora, isso parece bastante simples, certo?
Mas, o único problema que está presente nesta estrutura até agora é que você tem que usar muitos métodos para obter as informações necessárias. Para o fato, usar esses métodos para recuperar informações torna-se bastante complicado quando você precisa de dados complexos.

**Portanto, é aqui que a REST API entra em cena. A REST API cria um objeto e, a partir daí, envia os valores de um objeto em resposta ao cliente.**

**O que é REST API?**

REST sugere criar um objeto dos dados solicitados pelo cliente e enviar os valores do objeto em resposta ao usuário. Por exemplo, se o usuário estiver solicitando um filme em Bangalore em um determinado lugar e hora, você poderá criar um objeto no servidor.
Então, aqui, você tem um objeto e está enviando o estado de um objeto. É por isso que REST é conhecido como Transferência de Estado Representacional.

Se eu tiver que definir REST, então, Representational State Transfer, também conhecido como REST, é um estilo de arquitetura, bem como uma abordagem para fins de comunicação que é frequentemente usada no desenvolvimento de vários serviços da web.

O estilo arquitetônico do REST ajuda a alavancar o menor uso de largura de banda para tornar um aplicativo mais adequado para a internet. Muitas vezes é considerada a “ linguagem da internet ” e é totalmente baseada nos recursos.

Para entender melhor, vamos mergulhar um pouco mais fundo e ver como funciona exatamente uma REST API. Basicamente, a REST API divide uma transação para criar pequenos módulos. Agora, cada um desses módulos é usado para tratar de uma parte específica da transação. Essa abordagem fornece mais flexibilidade, mas requer muito esforço para ser construída desde o início.

Portanto, agora que você sabe o que é REST API, vamos entender as restrições ou princípios que devem ser satisfeitos para que um aplicativo seja considerado REST API.

**Princípios da REST API**

Bem, existem seis princípios básicos estabelecidos pelo Dr. Fielding, que definiu o design da REST API em 2000. Abaixo estão os seis princípios orientadores do REST:

* Sem estado
As solicitações enviadas de um cliente para um servidor conterão todas as informações necessárias para fazer o servidor entender as solicitações enviadas do cliente. Isso pode ser uma parte do URL, parâmetros de string de consulta, corpo ou mesmo cabeçalhos. O URL é usado para identificar exclusivamente o recurso e o corpo contém o estado do recurso solicitante. Assim que o servidor processa a solicitação, uma resposta é enviada ao cliente por meio de corpo, status ou cabeçalhos.

* Servidor cliente
A arquitetura cliente-servidor permite uma interface uniforme e separa os clientes dos servidores. Isso melhora a portabilidade em várias plataformas, bem como a escalabilidade dos componentes do servidor.

* Interface Uniforme

Para obter a uniformidade em todo o aplicativo, REST tem as seguintes quatro restrições de interface:
Identificação de recursos
Manipulação de recursos usando representações
Mensagens autodescritivas
Hipermídia como motor de estado do aplicativo

* Cache

Para fornecer um melhor desempenho, os aplicativos costumam ser armazenados em cache. Isso é feito rotulando a resposta do servidor como armazenável em cache ou não armazenável em cache, implícita ou explicitamente. Se a resposta for definida como armazenável em cache, o cache do cliente pode reutilizar os dados de resposta para respostas equivalentes no futuro.

* Sistema em camadas

A arquitetura do sistema em camadas permite que um aplicativo seja mais estável, limitando o comportamento do componente. Esse tipo de arquitetura ajuda a aumentar a segurança do aplicativo, pois os componentes em cada camada não podem interagir além da próxima camada imediata em que estão. Além disso, permite o balanceamento de carga e fornece caches compartilhados para promover escalabilidade.

* Código sob demanda

Esta é uma restrição opcional e é a menos usada. Ele permite que um código de cliente ou miniaplicativos sejam baixados e usados ​​dentro do aplicativo. Em essência, ele simplifica os clientes criando um aplicativo inteligente que não depende de sua própria estrutura de código.

Agora que você conhece os princípios por trás da REST API, a seguir vamos dar uma olhada nos Métodos da REST API.

**Métodos de REST API**
Todos nós que trabalhamos com a tecnologia da web, fazemos operações CRUD. Quando digo operações CRUD, quero dizer que criamos um recurso, lemos um recurso, atualizamos um recurso e excluímos um recurso. Agora, para fazer essas ações, você pode realmente usar os métodos HTTP, que nada mais são do que os métodos da REST API. Consulte abaixo.

# Metodos do protocolo HTTP

Existem 4 métodos básicos que podem ser usados para interagir com uma aplicação REST, os métodos são:

* **GET** que retorna os dados por algum identificador ou uma coleção de dados
* **POST** que cria um novo dado, em uma coleção já existente ou não
* **PUT** que edita e atualiza certo dado ou coleção de dados
* **DELETE** que como o próprio nome já diz, deleta certo dado ou coleção

**Quais tipos de informações uma requisição pode retornar?**

Uma requisição pode nos retornar vários tipos de formato de dados, como texto, vídeo, arquivo, musicas e muitas outras. Nós especificamos o formato que queremos receber pelo headers e Accept, alguns exemplos de headers e Accept que podemos passar são:

            image — image/png, image/jpeg, image/gif
            audio — audio/wav, image/mpeg
            video — video/mp4, video/ogg

        application — application/json, application/pdf, application/xml, application/octet-stream

**Onde ficam essas informações ?**

Essas informações precisam ser acessadas por um path (caminho) específico para cada tipo de informação que o desenvolvedor especificou anteriormente na hora de modelar sua aplicação REST, por exemplo:

No path http://minhaapi.show.br/usuarios contém as informações dos usuários, em http://minhaapi.show.br/usuarios/12 estamos acessando o usuário com o id 12 para obtermos mais informações sobre ele ou filtrar o usuário e assim por diante, cada requisição pode ter uma rota e parâmetros específicos para acessar os dados que o front-end envia as requisições.

**Códigos de Respostas**
Para cada resposta que a aplicação REST retornar, ela irá ser enviada com um código para ser definido o status da requisição, existem muitos, mas os principais são:

* **200** (OK), código de sucesso da requisição
* **201** (CREATED), código de sucesso na criação de um objeto
* **204** (NO CONTENT), código de sucesso ao deletar certo objeto/* informação
* **400** (BAD REQUEST), ocorreu algum erro na requisição, pode ter sido * um erro de várias naturezas
* **404** (NOT FOUND), informação, rota ou coleção não encontrada
* **500** (INTERNAL SERVER ERROR), provavelmente ocorreu algum erro no lado do servidor, como é um erro no servidor as informações sobre o erro em si é limitado, por conta que é impossível explorar esse erro

Para cada método HTTP é esperado os seguintes códigos de sucesso:

* GET, retorna 200 (OK)
* POST, retorna 201 (CREATED)
* PUT, retorna 200 (OK)
* DELETE, retorna 204 (NO CONTENT) Se a requisição falhar ao deletar, o código será específico ao problema encontrado


# XML e JSON

Entre os formatos de “uso geral” comumente usados ​​em ciência da computação, dois são XML (para eXtensible Markup Language ) e JSON ( JavaScript Object Notation ). O primeiro foi muito popular no início do novo século, enquanto o último ganhou popularidade no final desta década. Ambos têm **o objetivo de codificar informações estruturadas e, possivelmente, descrever qualquer forma de documento necessária (não necessariamente de uma forma ideal)**. 

XML é mais formal e permite uma aderência estrita a uma estrutura definida, enquanto JSON é um contêiner de dados mais simples (mas essa simplicidade resultou em uma boa popularidade em tempos posteriores, o formato BIOM 1.0 é um exemplo de formato JSON amplamente adotado).

**Formato JSON**

Um documento JSON é composto por uma lista de itens armazenados como pares de chave e valor. Os valores podem ser únicos (strings, inteiros, ponto flutuante ...) ou lista de valores (também conhecidos como matrizes).
Suponha que cada um de nós se apresente dizendo seu nome, sobrenome e alguns hobbies. A última informação é definitivamente uma lista, que pode estar vazia ou conter um ou vários valores.
Aqui está a notação JSON que eu poderia usar para me apresentar a um computador:

                    {
                    " nome " : " Gabriela " ,
                    " sobrenome " : " Santos " ,
                    " hobbies " : [
                        " Caminhada " ,
                        " Cozinhando " ,
                        " Programando "
                    ]
                    }

**De modo geral, um objeto JSON é colocado entre colchetes, cada item é um par “chave: valor” separado por vírgulas.** Matrizes (ou listas) são colocadas entre colchetes (novamente separados por vírgulas). Deve-se notar que adicionei espaços (recuo) e novas linhas para tornar o objeto mais agradável de ler, mas para um computador também esta notação é válida e totalmente equivalente:

    {"name":"Gabriela","surname":"Santos,"hobbies":["Hiking","Cooking","Graphic Design"]}

O formato é hierárquico, o que significa que as listas podem ser aninhadas em outras listas. Deve-se notar que a ordem dos itens é quase sempre irrelevante (o sobrenome é escrito após o nome, mas no mesmo nível de hierarquia).

**Formato XML**

Vamos começar a codificar o conjunto de dados anterior em uma das representações XML possíveis:

                <person>
                <name>Gabriela</name>
                <surname>Santos</surname>
                <hobbies>Hiking</hobbies>
                <hobbies>Cooking</hobbies>
                <hobbies>Develop</hobbies>
                </person>

Os dados típicos em XML são representados por tags, como <id>192</id>, o valor de uma tag é delimitado por uma abertura de tag ( <id>) e um formulário de fechamento ( </id>). Não existe uma maneira única de codificar uma lista, mas é simplesmente possível repetir a <hobbies>tag quantas vezes for necessário. Ou uma estrutura mais formal poderia usar uma tag aninhada, com quantos itens filhos forem <hobby>necessários:

            <hobbies>
            <hobby order="1">Hiking</hobby>
            <hobby order="2">Cooking</hobby>
            <hobby order="3">Develop</hobby>
            </hobbies>

A capacidade de aninhar tags torna particularmente evidente que documentos XML, como objetos JSON, são uma representação de dados em formato de árvore, com uma raiz com tantas ramificações quanto as tags de nível superior, e assim por diante.
O formato recente do Microsoft Office termina em x , como “.docx”: são todos documentos XML compactados com arquivos extras (como imagens embutidas)!


# ULR, URN e URI
* URL: uniform resource locator - localizador de recursos universal: host que sera acessado. exemplo: globallabs.academy
* URN: Uniform Resource name - nome do recurso universal: É o recurso que sera identificado. exemplo: /category/blog
* URI: Uniform Resource Identifier - Identificador de Recursos Universal: É o identificador do recurso, podendo ser uma imagem, um arquivo ou uma pagina. Exemplo http://globallabs.academy/category/blog/. A URI une o protocolo https://, Url e urn. 

# Framework Flask

* É um micro Framework para Python par adev web.
* Mantem um nucleo simples mas é estendivel.
* Não possui camadas de abstração para BD, validação de formularios, entre outros, mas é possivel estender com outras bibliotecas.


Lançado em 2010 e desenvolvido por Armin Ronacher, o Flask é um micro-framework destinado principalmente a pequenas aplicações com requisitos mais simples, como por exemplo, a criação de um site básico.

Possui um núcleo simples e expansível que permite que um projeto possua apenas os recursos necessários para sua execução (conforme surja a necessidade, um novo pacote pode ser adicionado para incrementar as funcionalidades da aplicação).

**Características do Flask**

**Simplicidade:** Por possuir apenas o necessário para o desenvolvimento de uma aplicação, um projeto escrito com Flask é mais simples se comparado aos frameworks maiores, já que a quantidade de arquivos é muito menor e sua arquitetura é muito mais simples.

**Rapidez no desenvolvimento:** Com o Flask, o desenvolvedor se preocupa em apenas desenvolver o necessário para um projeto, sem a necessidade de realizar configurações que muitas vezes não são utilizadas.

**Projetos menores:** Por possuir uma arquitetura muito simples (um único arquivo inicial) os projetos escritos em Flask tendem a ser menores e mais leves se comparados a frameworks maiores.

**Aplicações robustas:** Apesar de ser um micro-framework, o Flask permite a criação de aplicações robustas, já que é totalmente personalizável, permitindo, caso necessário, a criação de uma arquitetura mais definida.

**Exemplo de uma aplicação Flask**
Abaixo podemos ver um exemplo de uma aplicação em Flask. Podemos notar o quão simples criar uma aplicação web pode ser:

                from flask import Flask
                app = Flask(__name__)

                @app.route("/")
                def index():
                    return 'Bem-vindo a TreinaWeb!'

                if __name__ == "__main__":
                    app.run()

Podemos concluir que…
O Flask é uma excelente alternativa para o desenvolvimento de aplicações utilizando o Python. Ele é o principal concorrente do Django, apesar de ser considerado um micro-framework.
