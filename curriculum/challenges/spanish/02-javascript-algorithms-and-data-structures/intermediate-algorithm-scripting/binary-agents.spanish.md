---
id: a8d97bd4c764e91f9d2bda01
title: Binary Agents
localeTitle: Agentes binarios
isRequired: true
challengeType: 5
---

## Description
<section id='description'>
Devuelve una frase traducida al inglés de la cadena binaria pasada.
La cadena binaria estará separada por espacios.
Recuerda usar <a href='http://forum.freecodecamp.org/t/how-to-get-help-when-you-are-stuck/19514' target='_blank'>Read-Search-Ask</a> si te atascas. Trate de emparejar el programa. Escribe tu propio código.
</section>

## Instructions
<section id='instructions'>

</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: ' <code>binaryAgent(&quot;01000001 01110010 01100101 01101110 00100111 01110100 00100000 01100010 01101111 01101110 01100110 01101001 01110010 01100101 01110011 00100000 01100110 01110101 01101110 00100001 00111111&quot;)</code> &#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; &#39;&#39; '
    testString: 'assert.deepEqual(binaryAgent("01000001 01110010 01100101 01101110 00100111 01110100 00100000 01100010 01101111 01101110 01100110 01101001 01110010 01100101 01110011 00100000 01100110 01110101 01101110 00100001 00111111"), "Aren"t bonfires fun!?", "<code>binaryAgent("01000001 01110010 01100101 01101110 00100111 01110100 00100000 01100010 01101111 01101110 01100110 01101001 01110010 01100101 01110011 00100000 01100110 01110101 01101110 00100001 00111111")</code> should return "Aren&#39;t bonfires fun!?"");'
  - text: <code>binaryAgent(&quot;01001001 00100000 01101100 01101111 01110110 01100101 00100000 01000110 01110010 01100101 01100101 01000011 01101111 01100100 01100101 01000011 01100001 01101101 01110000 00100001&quot;)</code> 0011.
    testString: 'assert.deepEqual(binaryAgent("01001001 00100000 01101100 01101111 01110110 01100101 00100000 01000110 01110010 01100101 01100101 01000011 01101111 01100100 01100101 01000011 01100001 01101101 01110000 00100001"), "I love FreeCodeCamp!", "<code>binaryAgent("01001001 00100000 01101100 01101111 01110110 01100101 00100000 01000110 01110010 01100101 01100101 01000011 01101111 01100100 01100101 01000011 01100001 01101101 01110000 00100001")</code> should return "I love FreeCodeCamp!"");'

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='js-seed'>

```js
function binaryAgent(str) {
  return str;
}

binaryAgent("01000001 01110010 01100101 01101110 00100111 01110100 00100000 01100010 01101111 01101110 01100110 01101001 01110010 01100101 01110011 00100000 01100110 01110101 01101110 00100001 00111111");
```

</div>



</section>

## Solution
<section id='solution'>


```js
function binaryAgent(str) {
  return str.split(' ').map(function(s) { return parseInt(s, 2); }).map(function(b) { return String.fromCharCode(b);}).join('');
}
```

</section>