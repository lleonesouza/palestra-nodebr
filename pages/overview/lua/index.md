---
layout: image-right
image: pages/overview/coap/imgs/lua-background.jpg
---
# Lua
<!-- todo: add lua bg -->

Lua é uma linguagem de programação

- 🔬 **Brasil** - Criada nos anos 90 pela PUC-Rio
- 🚀 **Alta Performance** - Eficiênte e baixo consumo de recursos
- ⚙️ **Customizável** - Criar novos recursos de acordo com suas necessidades
- 💻  **Diversas Plataformas** -  Windows, macOS, Linux, iOS e Android
- 📝 **Documentação Abundante** -  Boas documentação, tutoriais e exemplos

<br>
<br>


---
layout: default
---


# Variáveis

<br>

<div>

**Javascript**

```javascript 
// Variáveis em JavaScript também são dinamicamente tipadas
var nome = "João";
var idade = 25;
var salario = 2500.50;
```

</div>

**Lua**

```lua 
-- Variáveis em Lua são dinamicamente tipadas
local nome = "João"
local idade = 25
local salario = 2500.50
```




---
layout: two-cols
---

# Estrutura de controle

<div>

**Javascript**
```javascript  {all|1|3,4|5,6|7,8|all}
var temperatura = 30;

if (temperatura > 25) {
    console.log("Está quente!");
} else if (temperatura > 15) {
    console.log("Está agradável!");
} else {
    console.log("Está frio!");
}
```

</div>

::right::

<br>
<br>

<div>

**Lua**

```lua {all|3,4|5,6|7,8|all}
local temperatura = 30

if temperatura > 25 then
    print("Está quente!")
elseif temperatura > 15 then
    print("Está agradável!")
else
    print("Está frio!")
end
```
</div>

<style>
    div {
        padding: 5px;
        margin-top: 30px;
    }
</style>
---

# Funções

<br>

**Javascript**

```javascript {all|2,3|6|all}
function saudacao(nome) {
    console.log("Olá, " + nome + "!");
    return nome;
}

saudacao("Maria");  // Output: Olá, Maria!
```



**Lua**

```lua {all|2,3|6|all}
function saudacao(nome)
    print("Olá, " .. nome .. "!")
    return nome
end

saudacao("Maria")  -- Output: Olá, Maria!
```

---

# Arrays

<br>


**Javascript**

```javascript 
var frutas = ["maçã", "banana", "laranja"];

frutas.forEach(function(fruta) {
    console.log("Eu gosto de " + fruta);
});

```


**Lua**

```lua
local frutas = {"maçã", "banana", "laranja"}

for i, fruta in ipairs(frutas) do
    print("Eu gosto de " .. fruta)
end

```


---
layout: two-cols
---

# Import e Export

--


*myFunction.js*



```javascript 
function myFunction() {
    console.log("world, hello");
}

export default myFunction
```


*otherFile.js*

```javascript 
const myFunction = require("./myFunction");

...

```

::right::

<br>
<br>
<br>


*myFunction.lua*

```lua
local function myFunction()
    print("world, hello")
end

return myFunction
```

*otherFile.lua*

```lua
local myFunction = require("myFunction")

...

```

---
layout: image-right
image: pages/overview/coap/imgs/lua-logo.png
---

# Aprenda mais sobre Lua

<br>

## Documentação oficial

- Visite o site oficial do Lua para acessar a documentação completa.

## Tutoriais online

- [Lua Tutorial](https://www.lua.org/pil/): Tutorial abrangente sobre Lua.
- [Lua Crash Course](https://learnxinyminutes.com/docs/lua/): Guia rápido e conciso de Lua.
- [Lua Programming](https://www.tutorialspoint.com/lua/): Tutoriais abrangentes de Lua.

