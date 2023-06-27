# Lua
<!-- todo: add lua bg -->

Lua é uma linguagem de script poderosa, eficiente, leve e incorporável. Ele suporta programação procedural, programação orientada a objetos, programação funcional, programação orientada a dados e descrição de dados.s

- 🔬 **Brazil** -  criada nos anos 90 pela PUC-Rio.
- 🚀 **Alta performance** -  conhecida por sua eficiência e velocidade em aplicações com baixo consumo de recursos.
- ⚙️ **Customizáve** -  permite aos desenvolvedores estender a linguagem e criar novos recursos de acordo com suas necessidades.
- 💻  **Plataformas Diversasy** -  suportada em uma ampla gama de sistemas operacionais, como Windows, macOS, Linux, iOS e Android.
- 📝 **Documentação Abundante** -  a comunidade Lua oferece uma extensa documentação, tutoriais e exemplos para facilitar o aprendizado e uso da linguagem.

<br>
<br>




---
layout: default
---



# Variáveis

<br>

**Lua**

```lua
-- Variáveis em Lua são dinamicamente tipadas
local nome = "João"
local idade = 25
local salario = 2500.50
```

**Javascript**

```javascript 
// Variáveis em JavaScript também são dinamicamente tipadas
var nome = "João";
var idade = 25;
var salario = 2500.50;
```

---
layout: two-cols
---

# Estrutura de controle

<br>

**Lua**
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
::right::

<br>
<br>
<br>
<br>

**Javascript**

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

---

# Funções

<br>

**Lua**

```lua
function saudacao(nome)
    print("Olá, " .. nome .. "!")
    return nome
end

saudacao("Maria")  -- Output: Olá, Maria!
```

**Javascript**

```javascript 
function saudacao(nome) {
    console.log("Olá, " + nome + "!");
    return nome;
}

saudacao("Maria");  // Output: Olá, Maria!
```

---

# Arrays

<br>

**Lua**

```lua
local frutas = {"maçã", "banana", "laranja"}

for i, fruta in ipairs(frutas) do
    print("Eu gosto de " .. fruta)
end

```

**Javascript**

```javascript 
var frutas = ["maçã", "banana", "laranja"];

frutas.forEach(function(fruta) {
    console.log("Eu gosto de " + fruta);
});

```

---


# Import e Export

<br>

**Lua**

```lua
-- meuarquivo.lua
local function minhaFuncao()
    print("Olá, mundo Lua!")
end

return {
    minhaFuncao = minhaFuncao
}


-- outroarquivo.lua
local meuArquivo = require("meuarquivo")

meuArquivo.minhaFuncao() -- Output: Olá, mundo Lua!

```

**Javascript**

```javascript 
// meuarquivo.js
function minhaFuncao() {
    console.log("Olá, mundo JavaScript!");
}

module.exports = {
    minhaFuncao: minhaFuncao
};


// outroarquivo.js
const meuArquivo = require("./meuarquivo");

meuArquivo.minhaFuncao(); // Output: Olá, mundo JavaScript!

```

---

# Aprenda mais sobre Lua

<br>

## Documentação oficial

- Visite o site oficial do Lua para acessar a documentação completa.

## Tutoriais online

- [Lua Tutorial](https://www.lua.org/pil/): Tutorial abrangente sobre Lua.
- [Lua Crash Course](https://learnxinyminutes.com/docs/lua/): Guia rápido e conciso de Lua.
- [Lua Programming](https://www.tutorialspoint.com/lua/): Tutoriais abrangentes de Lua.

