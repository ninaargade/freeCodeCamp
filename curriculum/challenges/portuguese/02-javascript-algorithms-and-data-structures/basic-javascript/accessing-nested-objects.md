---
id: 56533eb9ac21ba0edf2244cc
title: Acessar objetos aninhados
challengeType: 1
videoUrl: 'https://scrimba.com/c/cRnRnfa'
forumTopicId: 16161
dashedName: accessing-nested-objects
---

# --description--

As subpropriedades de objetos podem ser acessadas ao encadear a notação de ponto e de colchetes.

Aqui está um objeto aninhado:

```js
const ourStorage = {
  "desk": {
    "drawer": "stapler"
  },
  "cabinet": {
    "top drawer": { 
      "folder1": "a file",
      "folder2": "secrets"
    },
    "bottom drawer": "soda"
  }
};

ourStorage.cabinet["top drawer"].folder2;
ourStorage.desk.drawer;
```

`ourStorage.cabinet["top drawer"].folder2` seria a string `secrets` e `ourStorage.desk.drawer` seria a string `stapler`.

# --instructions--

Acesse o objeto `myStorage` e atribua o conteúdo da propriedade `glove box` para a variável `gloveBoxContents`. Use notação de ponto para todas as propriedades sempre que possível, caso contrário, use a notação de colchetes.

# --hints--

`gloveBoxContents` deveria ser igual à string `maps`.

```js
assert(gloveBoxContents === 'maps');
```

Your code should use dot notation, where possible, to access `myStorage`.

```js
assert.match(code, /myStorage\.car\.inside/);
```

`gloveBoxContents` ainda deve ser declarada com `const`.

```js
assert.match(code, /const\s+gloveBoxContents\s*=\s*myStorage\.car\.inside\[\s*("|')glove box\1\s*\]|const\s*{\s*('|")glove box\2:\s*gloveBoxContents\s*}\s*=\s*myStorage\.car\.inside;/);
```

# --seed--

## --after-user-code--

```js
(function(x) { 
  if(typeof x != 'undefined') { 
    return "gloveBoxContents = " + x;
  }
  return "gloveBoxContents is undefined";
})(gloveBoxContents);
```

## --seed-contents--

```js
const myStorage = {
  "car": {
    "inside": {
      "glove box": "maps",
      "passenger seat": "crumbs"
     },
    "outside": {
      "trunk": "jack"
    }
  }
};

const gloveBoxContents = undefined;
```

# --solutions--

```js
const myStorage = {
  "car":{
    "inside":{
      "glove box":"maps",
      "passenger seat":"crumbs"
    },
    "outside":{
      "trunk":"jack"
    }
  }
};
const gloveBoxContents = myStorage.car.inside["glove box"];
```
