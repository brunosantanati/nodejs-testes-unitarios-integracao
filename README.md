# Anotações e Dicas Gerais

## Markdown link

[Basic Syntax](https://www.markdownguide.org/basic-syntax/)

## NVM

Instalar versões do Node usadas no curso  
<code>nvm install 16.16.0</code>  
<code>nvm install 16.14.2</code>  

Antes de qualquer coisa mudar para uma das versões do Node utilizada no curso  
<code>nvm use 16.16.0</code>  
<code>nvm use 16.14.2</code>  

## Comandos utilizados no curso

Comandos usados no primeiro projeto:

<code>node index.js</code>  
<code>npm init -y</code>  
<code>npm install --save-dev eslint@8.16.0 --save-exact</code>  
<code>npx eslint --init</code>  
<code>npx eslint index.js</code>  
<code>npm install --save-exact jest@28.1.0 --save-dev</code>  
<code>npm run test</code>  
<code>npm run test:watch</code>  
<code>npm run test:coverage</code>  

Comandos usados no projeto API ([README](https://github.com/brunosantanati/nodejs-testes-unitarios-integracao/blob/main/my-source-code/node-api/README.md)):  

<code>npm install</code>  
<code>npm run dev</code>  

Comandos relacionados ao SQLite:

<code>sudo apt update</code>  
<code>sudo apt install sqlite3</code>  
<code>sqlite3 --version</code>  
<code>sqlite3 ./src/db/livraria.sqlite</code>  

Comandos para rodar via SQLite client:

<code>PRAGMA foreign_keys;</code>  
<code>PRAGMA foreign_keys = ON;</code>  
<code>.tables</code>  
<code>SELECT * FROM autores;</code>  
<code>SELECT * FROM livros;</code>  
<code>SELECT * FROM editoras;</code>  

## Como debugar

[How To Debug Node.js with the Built-In Debugger and Chrome DevTools](https://www.digitalocean.com/community/tutorials/how-to-debug-node-js-with-the-built-in-debugger-and-chrome-devtools)  

Usar inspect para iniciar em modo debug:  
<code>node inspect index.js</code>  

Para colocar um breakpoint no código usar:  
<code>debugger;</code>  

Enquanto debuga pode usar isso para ver o conteúdo das variáveis:  
<code>watch('nomeVariavel')</code>  

E também essas letras:

    c or cont: Continue execution to the next breakpoint or to the end of the program.  
    n or next: Move to the next line of code.  
    s or step: Step into a function. By default, we only step through code in the block or scope we’re debugging. By stepping into a function, we can inspect the code of the function our code calls and observe how it reacts to our data.  
    o: Step out of a function. After stepping into a function, the debugger goes back to the main file when the function returns. We can use this command to go back to the original function we were debugging before the function has finished execution.  
    pause: Pause the running code.  

## Para saber mais: usando o Eslint

Esse projeto utiliza o ESLint. Você pode conferir mais sobre essa ferramenta [no site do projeto](https://eslint.org/) ou [na página do pacote NPM](https://www.npmjs.com/package/eslint).

Para facilitar o uso do linter, utilizamos [essa extensão](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) para fazer a marcação de forma mais cômoda no VSCode.

Para “chamar” o Eslint no VSC e organizar seu código automaticamente, utilize o atalho <code>ctrl + shift + P</code> (Windows/Linux) ou <code>cmd + shift + P</code> (MacOs), digite Eslint e escolha a opção "Fix all auto-fixable problems" ou posicione o cursor piscante sobre alguma das linhas sublinhadas vermelhas e utilize o atalho <code>ctrl + .</code> para abrir o menu do Eslint e escolher “Fix all auto-fixable problems” se estiver disponível.

> Alguns erros de linter não são “auto-corrigíveis” (auto-fixable). Quando isso acontece, precisamos ler o tipo de erro que o Eslint está informando e, se for necessário, buscar na documentação para entender melhor qual é o problema e como podemos lidar com ele.

## Coverage

Para ver a cobertura podemos executar: <code>npm run test:coverage</code>.  
Isso irá em última instância executar esse comando:  
<code>node --experimental-vm-modules node_modules/jest/bin/jest.js --detectOpenHandles --coverage</code>  

O Jest também fornece o relatório de cobertura de forma mais visual. Quando utilizamos a flag coverage, além de exibir o relatório no terminal, o Jest também cria a pasta coverage na raiz do projeto. Dentro desta pasta, você pode acessar a subpasta lcov-report para ver o relatório (report) e interagir com os arquivos, abrindo o arquivo index.html e navegando pelos arquivos.

> Se estiver usando o Visual Studio Code, você pode abrir o arquivo index.html direto no navegador clicando com o botão direito no arquivo e selecionando a opção Open with Live Server [Alt+L Alt+O], que normalmente abre o arquivo HTML direto no navegador, no endereço http://localhost:5500/coverage/lcov-report/

## Links Jest

[Iniciando](https://jestjs.io/pt-BR/docs/getting-started)  
[Expect e matchers](https://jestjs.io/pt-BR/docs/expect)

## Async/await

Artigo [Async/await no JavaScript: o que é e quando usar a programação assíncrona?](https://www.alura.com.br/artigos/async-await-no-javascript-o-que-e-e-quando-usar)