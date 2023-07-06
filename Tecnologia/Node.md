Node é um runtime enviroment, não é uma linguagem de programação nem um frame work
Node is asynchronous by default, 
Node is ideal for I/O Intensive apps
Node is **not** ideal for CPU intensive apps

node --version
node arquivo.js (executa o arquivo)

setTimeout()
clearTimeout()

setInterval()
clearInterval()

Toda aplicação node possui um modulo principal
(toda vez que inicia uma aplicação do node ele cria esse módulo principal baseado no arquivo inicial de execução e um módulo para cada arquivo importado?)
durante a execução de uma aplicação node, o código do arquivo a ser executado é envolvido em uma função funtion(exports, require, module, __filename, __dirname){ código }

module.exports.nome = item;  // Vai como objeto
module.exports = item;   // Vai como o próprio item

exports = item;


ex. pode-se utilizar parte dos dados desse módulo para algo
const path = require('path'); // os, fs, events
let pathObj = path.parse(__filename);
console.log(pathObj);

Boa prática para não ter o risco de sobrescrever
const variavel = require('url.arquivo.js')