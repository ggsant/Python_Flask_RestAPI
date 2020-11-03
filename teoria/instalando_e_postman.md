# instalação 

# PIP

* Sistema de gerenciamento de pacotes.
* Utilizado para instalar e gerenciar pacotes/bibliotecas em python
* Já vem empacotado com python desde a versão 3.4 

# Virtualenv

* Ferramenta para criar ambientes python isolados.
* Vem integrado com o Python desde a versao 3.3
* Extremamente útil para se trabalhar com projetos que utilizam bibliotecas com versoes diferentes.

# POSTMAN 

* Ferramenta utilizada para realizar requisições HTTP.
* Com ela é possivel chamar qualquer método e tambem enviar parametros.

# Usando no VsCode

**Pré-requisitos**

Para concluir este tutorial do Flask, você deve fazer o seguinte (que são as mesmas etapas do tutorial geral do Python ):

* 1 - Instale a extensão Python .

* 2 - Instale uma versão do Python 3 (para a qual este tutorial foi escrito). As opções incluem:

* (Todos os sistemas operacionais) Um download de python.org ; normalmente use o botão Baixar Python 3.6.5 que aparece primeiro na página (ou qualquer que seja a versão mais recente).
* (Linux) A instalação embutida do Python 3 funciona bem, mas para instalar outros pacotes do Python você deve executar sudo apt install python3-pipno terminal.
* (macOS) Uma instalação através do Homebrew no macOS usando brew install python3(a instalação do sistema do Python no macOS não é compatível).
* (Todos os sistemas operacionais) Um download do Anaconda (para fins de ciência de dados).

* 3 - No Windows, certifique-se de que a localização do seu interpretador Python esteja incluída na sua variável de ambiente PATH. Você pode verificar o local executando pathno prompt de comando. Se a pasta do interpretador Python não estiver incluída, abra as Configurações do Windows, pesquise "ambiente", selecione Editar variáveis ​​de ambiente para sua conta e edite a variável de caminho para incluir essa pasta.

# Crie um ambiente de projeto para o tutorial Flask 

Nesta seção, você cria um ambiente virtual no qual o Flask é instalado. Usar um ambiente virtual evita a instalação do Flask em um ambiente Python global e oferece controle exato sobre as bibliotecas usadas em um aplicativo. Um ambiente virtual também facilita a criação de um arquivo requirements.txt para o ambiente .

* 1 - Em seu sistema de arquivos, crie uma pasta de projeto para este tutorial, como hello_flask.

* 2 - Nessa pasta, use o seguinte comando (conforme apropriado para seu computador) para criar um ambiente virtual nomeado com envbase em seu intérprete atual:

**macOS/Linux**

            sudo apt-get install python3-venv    # If needed
            python3 -m venv env

**Windows**

            python -m venv env

**Nota:** Use uma instalação Python padrão ao executar os comandos acima. Se você usar a python.exepartir de uma instalação do Anaconda, verá um erro porque o módulo garantirpip não está disponível e o ambiente é deixado em um estado inacabado.

* 3 - Abra a pasta do projeto no VS Code executando code .ou executando o VS Code e usando o comando Arquivo > Abrir pasta .

* 4 - No código do VS, abra a Paleta de comandos ( Exibir > Paleta de comandos ou ( Ctrl + Shift + P )). Em seguida, selecione o Python: Selecione o comando Interpreter 

* 5 - O comando apresenta uma lista de interpretadores disponíveis que o VS Code pode localizar automaticamente (sua lista irá variar; se você não vir o interpretador desejado, consulte Configurando ambientes Python ). Na lista, selecione o ambiente virtual na pasta do seu projeto que começa com ./envou .\env:


* 6 - Executar Terminal: Criar Novo Terminal Integrado ( Ctrl + Shift + ` )) a partir da Paleta de Comandos, que cria um terminal e ativa automaticamente o ambiente virtual executando seu script de ativação.

**Nota:** No Windows, se o seu tipo de terminal padrão for PowerShell, você poderá ver um erro informando que ele não pode executar activate.ps1 porque a execução de scripts está desabilitada no sistema. O erro fornece um link para informações sobre como permitir scripts. Caso contrário, use Terminal: Selecione Shell Padrão para definir "Prompt de Comando" ou "Git Bash" como seu padrão.

* 7 - O ambiente selecionado aparece no lado esquerdo da barra de status do VS Code e observe o indicador "(venv)" que informa que você está usando um ambiente virtual.

* 8 - Instale o Flask no ambiente virtual executando um dos seguintes comandos no Terminal de código VS:

**macOS/Linux**

            pip3 install flask

**Windows**

            pip install flask

Agora você tem um ambiente independente pronto para escrever o código do Flask. O VS Code ativa o ambiente automaticamente quando você usa o Terminal: Criar Novo Terminal Integrado . Se você abrir um prompt de comando ou terminal separado, ative o ambiente executando source env/bin/activate(Linux / macOS) ou env\scripts\activate(Windows). Você sabe que o ambiente está ativado quando o prompt de comando mostra (env) no início.

# Crie e execute um aplicativo Flask mínimo

* 1 - No VS Code, crie um novo arquivo na pasta do seu projeto nomeado app.pyusando Arquivo > Novo no menu, pressionando Ctrl + N , ou usando o ícone do novo arquivo na Visualização do Explorer.

* 2 - Em app.py, adicione o código para importar o Flask e crie uma instância do objeto Flask. Se você digitar o código abaixo (em vez de usar copiar e colar), poderá observar o IntelliSense e as autocomplicações do VS Code :

                    from flask import Flask
                    app = Flask(__name__)

* 3 - Além disso app.py, adicione uma função que retorne conteúdo, neste caso uma string simples, e use o app.routedecorador do Flask para mapear a rota do URL /para essa função:

                    @app.route("/")
                    def home():
                        return "Hello, Flask!"

**Dica:** você pode usar vários decoradores na mesma função, um por linha, dependendo de quantas rotas diferentes você deseja mapear para a mesma função.

* 4 - Salve o app.pyarquivo ( Ctrl + S ).

* 5 - No terminal, execute o aplicativo digitando python3 -m flask run(macOS / Linux) ou python -m flask run(Windows), que executa o servidor de desenvolvimento Flask. O servidor de desenvolvimento procura app.pypor padrão. Ao executar o Flask, você verá uma saída semelhante a esta:

        (env) D:\py\\hello_flask>python -m flask run
        * Environment: production
        WARNING: Do not use the development server in a production environment.
        Use a production WSGI server instead.
        * Debug mode: off
        * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)

Se você vir um erro de que o módulo Flask não pode ser encontrado, certifique-se de ter executado pip3 install flask(macOS / Linux) ou pip install flask(Windows) em seu ambiente virtual, conforme descrito no final da seção anterior.

Além disso, se você deseja executar o servidor de desenvolvimento em uma porta ou endereço IP diferente, use os argumentos de linha de comando host e port, como em --host=0.0.0.0 --port=80.

* 6 - Para abrir seu navegador padrão na página renderizada, Ctrl + clique no http://127.0.0.1:5000/URL no terminal.

* 7 - Observe que quando você visita um URL como /, uma mensagem aparece no terminal de depuração mostrando a solicitação HTTP:

        127.0.0.1 - - [11/Jul/2018 08:40:15] "GET / HTTP/1.1" 200 -
        
* 8 - Pare o aplicativo usando Ctrl + C no terminal.

Dica : Se você deseja usar um nome de arquivo diferente de app.py, como program.py, defina uma variável de ambiente chamada FLASK_APP e defina seu valor para o arquivo escolhido. O servidor de desenvolvimento do Flask então usa o valor de FLASK_APP em vez do arquivo padrão app.py. Para obter mais informações, consulte a interface de linha de comando do Flask .