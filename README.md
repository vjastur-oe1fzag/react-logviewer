# Instalação

Lembre que o código passa por transpilação, então instale a ferramenta como dependência de desenvolvimento:

```
npm install -D typescript
```


# Inferência de tipos

A linguagem consegue descobrir o tipo de uma variável sozinha.

![inference](images/inferencia-de-tipo.png)

E como a imagem anterior mostra, depois que o tipo é inferido ele não muda: não dá para atribuir um número a uma variável que ficou como texto, mesmo que a tipagem tenha sido inferida.


# Transpilando um arquivo

Dá para transpilar diretamente um arquivo:

```
npx tsc src/index.ts
```

O arquivo JavaScript equivalente é gerado na mesma pasta do fonte.


# Sugestão para transpilar e executar com um comando

A imagem abaixo mostra a sugestão: um comando único no manifesto que faz as duas etapas.

![reacher suggestion](images/sugestao-do-comando.png)

OBS: na imagem ele executa o comando de desenvolvimento declarado no manifesto.


# Gerando o arquivo de configuração

```
npx tsc --init
```


# Configuração mínima e limpa

![clean tscoonfig](images/configuracao-limpa.png)


# Opções recomendadas

(dentro do nó de opções do compilador):

- **target**: ES6;
- **module**: CommonJS (por compatibilidade);
- **outDir**: ./dist
- **strict**: true (tipagem estrita);
- **esModuleInterop**: true (compatibilidade com módulos ES);


# Dicas ao passar o mouse no editor

![details on mouse over](images/detalhes-ao-passar-o-mouse.png)


# Transpilando o projeto inteiro

Um exemplo citado em aula: rodando o compilador sem informar arquivo, ele lê o arquivo de configuração e aplica as opções — por exemplo a pasta de destino —, gerando **vários** arquivos JavaScript, um para cada fonte.


# Executando fontes sem etapa explícita de transpilação

A aula usou um pacote que executa a linguagem diretamente; ele foi instalado pelo gerenciador de pacotes e aparece no comando de desenvolvimento do manifesto, mostrado na imagem.

![tsx-package](images/pacote-executor.png)

Esse comando foi executado pelo script de desenvolvimento, como era de se esperar.

Também é possível deixar em modo vigia, como se faz no Node.JS.

![tsx watch](images/modo-vigia.png)


# Documentação do arquivo de configuração

A aula indicou a página oficial que lista todas as opções de configuração.


# Configuração mínima

A sugestão de configuração mínima é esta:

![tsconfig minimal](images/configuracao-minima.png)


# Dicas no editor

Passando o mouse sobre cada opção aparecem as dicas do editor:

![hints on mouse over](images/dicas-no-editor.png)


# Comparação de pacotes e alternativa de build

![npm trends and tsup](images/comparacao-de-pacotes.png)

A imagem mostra um gráfico comparando pacotes da mesma área, de transpilação. A sugestão foi usar um empacotador alternativo, que segundo a aula é mais usado pelas empresas do que o compilador padrão.


# Iniciando um projeto focado na linguagem

```sh
npm init -y typescript -D
```

Isso:

- cria o manifesto do projeto;
- instala a ferramenta de tipagem;
- cria o arquivo de configuração com o básico;
- cria o arquivo de padrões de verificação (a aula apaga esse arquivo, por não usar);
- cria o arquivo de entrada na pasta de fontes.

Além disso:

- se for usar controle de versão, crie o arquivo de exclusão para ignorar a pasta de dependências.


# Links das aulas

O código usado está num repositório público da trilha.

Existem também as folhas de consulta rápida e o ambiente de testes online da linguagem.