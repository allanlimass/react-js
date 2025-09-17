# Componentes e JSX Avançado

## Use JSX Multilinha em um Componente

- JSX multilinha devem ser colocados entre parênteses

```js
import React from 'react'

function QuoteMaker() {
    return (
        <blockquote>
            <p>
                The world is full of objects, more or less interesting
            </p>
            <cite>
                <a 
                    target="_blank"
                    href="https://en.wikipedia.org/wiki/Douglas_Huebler">
                        Douglas Huebler
                </a>
            </cite>
        </blockquote>
    );
};

export default QuoteMaker;
```

## Use um Atributo Variável em um Componente

```js
import React from 'react';

const redPanda = {
    src: 'https://upload.wikimedia.org/wikipedia/commons/b/b2/Endangered_Red_Panda.jpg',
    alt: 'Red Panda',
    width: '200px'
};

fuction RedPand() {
    return (
        <div>
            <h1>Cute Red Panda</h1>
            <img 
                src={redPanda.src}
                alt={redPanda.alt}
                width={redPanda.width}
            />
        </div>
    );
};

export default RedPanda;
```

## Colocando Logica em um Componente de Função
- É possível realizar cálculos simples dentro do componente de função

```js
function RandomNumber() {
    const n = Math.floor(Math.random() * 10 + 1);
   
    return <h1>{n}</h1>
};
```

## Use um Condicional em um Componente de Função
```js
import React from 'react';

const fiftyFifty = Math.random() < 0.5;

function TonightsPlan() {
  if (fiftyFifty) {
    return <h1>Tonight I'm going out WOOO</h1>
  } else {
    return <h1>Tonight I'm going to bed WOOO</h1>
  }
}

export default TonightsPlan;
```

## Ouvinte de Eventos e Manipuladores de Eventos em um Componente
