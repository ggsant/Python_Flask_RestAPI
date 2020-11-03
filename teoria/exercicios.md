**Qual das características abaixo não faz parte do PyCharm?**

- [ ] Dentre suas funções, o PyCharm faz formatação automática e complementação do código.
- [ ] É um ambiente de desenvolvimento integrado usado na programação em linguagem Python.
- [ ] Ele pode ser trabalhado juntamente com a ferramenta Django.
- [x] O PyCharm otimiza tarefas no Python mas não faz integração com outros sistemas.
- [ ] Todas estão corretas.

**O trecho do código @app.route() permite especificar o método de leitura do código Python. Avalie as afirmativas abaixo para inclusão tanto do método GET quanto POST.**

- [ ] @app.route("/", methods=['GET'; 'POST'])
- [ ] @app.route("/", methods=('GET', 'POST'))
- [ ] @app.route("/", methods=[GET, POST])
- [x] @app.route("/", methods=['GET', 'POST'])
- [ ] @app.route("/", methods=[GET; POST])

**Ao visualizar o retorno no navegador foi apresentado o seguinte texto de erro:**

                Method Not Alowed
                The method is not allowed for the requested URL.

**Mediante isso, qual linha de código abaixo seria a responsável por isso?**

- [ ] @app.route("/<gorduras>")
- [ ] @app.route("/<carboidratos>", methods=[POST])
- [ ] @app.route("/<minerais>", methods=['GET', 'POST'])
- [x] @app.route("/<vitaminas>", methods=['POST'])
- [ ] @app.route("/<proteinas>", methods=['GET'])

**Qual a finalidade do comando import_name?**

- [ ] Nenhuma das alternativas.
- [ ] Para importar projetos antigos de outras linguagens para o Flask.
- [x] Este comando define o que pertence ao projeto.
- [ ] Faz com que o Flask inicie seu servidor interno.
- [ ] O comando é para delimitar que o projeto está contido em um pacote.

**Qual a finalidade do Virtualenv?**

- [ ] Nenhuma das alternativas.
- [ ] É uma funcionalidade da linguagem Python que cria diferentes ambientes para desenvolvimento de aplicações.
- [x] É uma ferramenta para criar ambientes Python isolados e muito útil também para criar projetos que utilizam bibliotecas com diferentes versões.
- [ ] É uma ferramenta que deve ser usada exclusivamente na linguagem Python para que seja utilizada uma única biblioteca.
- [ ] É uma plataforma que deve ser utilizada quando se deseja instalar dependências de um projeto específico em Python.

**O trecho do código @app.route() permite a transferência de parâmetros através da URI. Sendo assim, qual das opções abaixo pega corretamente o nome de vocalistas de bandas de rock através do método GET?**

I - @app.route("/<StevenTyler>", methods=['GET'])
II - @app.route("</MickJagger>")
III - @app.route("/<DavidBowie>")
IV - @app.route("/<DebbieHarry")

- [x] Apenas I e III.
- [ ] Apenas I.
- [ ] Todas.
- [ ] Todas, exceto II.
- [ ] Apenas III.

**Na aula foi ensinado o comando utilizado para que o arquivo Python execute o código. Assinale a opção correta com a justificativa correta.**

- [ ] app.run, porque run é o nome do arquivo, tal como run.py
- [ ] app(run), porque run é o parâmetro do Python que irá acessar o comando do aplicativo.
- [x] app.run(), porque run é um comando associado à variável app que recebeu Flask(__name__)
- [ ] run.app(), porque run é um comando associado à variável app que recebeu Flask(__name__)
- [ ] app.run(), porque run é o nome do arquivo, tal como run.py

**Analise o código abaixo e assinale o comando que está faltando:**

                    app = Flask(__name__)

                    @app.route("/")
                    def hello():
                    return "Hello World!"

- [ ] open = Flask
- [x] from flask import Flask
- [ ] import flask from Flask
- [ ] FLASK_APP=hello.py flask run
- [ ] from Flask

**O Flask permite mudança e atualização constante no arquivo, evitando que você precise fazê-lo manualmente para checar as mudanças. O comando correto que permite esse processo é:**

- [ ] debug.run(True)
- [x] app.run(debug=True)
- [ ] app.debug(True)
- [ ] app.run(true)
- [ ] app.debug(=True)

**Qual a finalidade do comando import_name?**

- [ ] O comando é para delimitar que o projeto está contido em um pacote.
- [x] Este comando define o que pertence ao projeto.
- [ ] Para importar projetos antigos de outras linguagens para o Flask.
- [ ] Nenhuma das alternativas.
- [ ] Faz com que o Flask inicie seu servidor interno.


**Em qual das alternativas abaixo é usada a ferramenta Postman?**

- [ ] Para facilitar o teste e depuração de frameworks.
- [x] Para realizar requisições HTTP por uma interface simples.
- [ ] Para otimizar o tempo de desenvolvimento de projetos back-end.
- [ ] Para pode testar qualquer serviço Pycharm.
- [ ] Para testar aplicações da interface gráfica.