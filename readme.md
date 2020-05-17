![](logo-rollup.jpeg)

# Rollup - Creating Your First Bundle

http://rollupjs.org/guide/en/#creating-your-first-bundle


Instalando Rollup de forma global.

    npm install rollup --global

Testando a instalação.

    rollup --help


## Este exemplo

Após criado os primeiros arquivos, executei...

    rollup src/main.js -f cjs

> The -f option (short for --format) specifies what kind of bundle we're creating.
> In this case, CommonJS (which will run in Node.js).

Nenhum arquivo foi criado/gerado.

> Because we didn't specify an output file, it will be printed straight to stdout:

    src/main.js → stdout...
    'use strict';

    var foo = 'hello world!';

    function main () {
        console.log(foo);
    }

    module.exports = main;


> You can save the bundle as a file like so:

    rollup src/main.js -o dist/bundle.js -f cjs

Obtive como saída:

    src/main.js → dist/bundle.js...
    created bundle.js in 42ms

> Congratulations! You've created your first bundle with Rollup.


### Try running the code:

Testando no terminal iterativo: 

    node
    > var myBundle = require('./dist/bundle.js');
    > myBundle();
    'hello world!'

Ou simplesmente...

    node test/bundle.js


## options.format

- amd
- cjs
- esm
- iief
- umd
- system