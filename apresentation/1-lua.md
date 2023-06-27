## Lua

1. O que é Lua?

- Lua foi criada nos anos 90 pela PUC-rio
- Foi criada inicialmente para um projeto para automatizar a simulação de poços de petróleo.
- Sintaxe simples e limpa
- Linguagem leve, flexível e fácil de integrar com outras tecnologias.
- Hoje é usada para jogos a sistemas embarcados, de servidores web a projetos de IoT

2. Similaridade com javascript

- Variaveis
```lua
-- Variáveis em Lua são dinamicamente tipadas
local nome = "João"
local idade = 25
local salario = 2500.50
```

```javascript
// Variáveis em JavaScript também são dinamicamente tipadas
var nome = "João";
var idade = 25;
var salario = 2500.50;
```

- Estrutura de controle
```lua
local temperatura = 30

if temperatura > 25 then
    print("Está quente!")
elseif temperatura > 15 then
    print("Está agradável!")
else
    print("Está frio!")
end
```

```javascript
var temperatura = 30;

if (temperatura > 25) {
    console.log("Está quente!");
} else if (temperatura > 15) {
    console.log("Está agradável!");
} else {
    console.log("Está frio!");
}
```


- Funções
```lua
function saudacao(nome)
    print("Olá, " .. nome .. "!")

    return nome
end

saudacao("Maria")  -- Output: Olá, Maria!

```

```javascript
function saudacao(nome) {
    console.log("Olá, " + nome + "!");

    return nome
}

saudacao("Maria");  // Output: Olá, Maria!

```

- Trabalhando com Arrays
```lua
local frutas = {"maçã", "banana", "laranja"}

for i, fruta in ipairs(frutas) do
    print("Eu gosto de " .. fruta)
end

```

```javascript
var frutas = ["maçã", "banana", "laranja"];

frutas.forEach(function(fruta) {
    console.log("Eu gosto de " + fruta);
});

```


- Import e Export
```lua
-- meuarquivo.lua
local function minhaFuncao()
    print("Olá, mundo Lua!")
end

return {
    minhaFuncao = minhaFuncao
}
```

```lua
-- outroarquivo.lua
local meuArquivo = require("meuarquivo")

meuArquivo.minhaFuncao() -- Output: Olá, mundo Lua!
```

```javascript
// meuarquivo.js
function minhaFuncao() {
    console.log("Olá, mundo JavaScript!");
}

module.exports = {
    minhaFuncao: minhaFuncao
};
```
```javascript
// outroarquivo.js
const meuArquivo = require("./meuarquivo");

meuArquivo.minhaFuncao(); // Output: Olá, mundo JavaScript!
```

