# Anotações e Dicas Gerais

## Markdown link

[Basic Syntax](https://www.markdownguide.org/basic-syntax/)

## NVM

Antes de qualquer coisa mudar para a versão do Node utilizada no curso  
<code>nvm use 16.16.0</code>  

## Comandos utilizados no curso

<code>node index.js</code>  
<code>npm init -y</code>  
<code>npm install --save-dev eslint@8.16.0 --save-exact</code>  
<code>npx eslint --init</code>  
<code>npx eslint index.js</code>  

## Para saber mais: usando o Eslint

Esse projeto utiliza o ESLint. Você pode conferir mais sobre essa ferramenta [no site do projeto](https://eslint.org/) ou [na página do pacote NPM](https://www.npmjs.com/package/eslint).

Para facilitar o uso do linter, utilizamos [essa extensão](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) para fazer a marcação de forma mais cômoda no VSCode.

Para “chamar” o Eslint no VSC e organizar seu código automaticamente, utilize o atalho <code>ctrl + shift + P</code> (Windows/Linux) ou <code>cmd + shift + P</code> (MacOs), digite Eslint e escolha a opção "Fix all auto-fixable problems" ou posicione o cursor piscante sobre alguma das linhas sublinhadas vermelhas e utilize o atalho <code>ctrl + .</code> para abrir o menu do Eslint e escolher “Fix all auto-fixable problems” se estiver disponível.

> Alguns erros de linter não são “auto-corrigíveis” (auto-fixable). Quando isso acontece, precisamos ler o tipo de erro que o Eslint está informando e, se for necessário, buscar na documentação para entender melhor qual é o problema e como podemos lidar com ele.


