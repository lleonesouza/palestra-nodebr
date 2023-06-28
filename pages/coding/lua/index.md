---
---

# Código LUA

- Código que vai ser feito upload no nodemcu
- Apenas realiza ações
- Chamada HTTP
- Usa o template do Toolkit


---

# Temperatura e Umidade
```lua
local status, temp, humi, temp_dec, humi_dec = dht.read11(pin0)

-- Check the status and print any errors
if status == dht.OK then
    print("Read successful")
elseif status == dht.ERROR_CHECKSUM then
    print("Checksum error")
elseif status == dht.ERROR_TIMEOUT then
    print("Timeout error")
end

local data = {
    temperature = temp,
    humidity = humi
}

return sjson.encode(data)
```



---
layout: two-cols
---

# Motor
```lua
gpio.mode(pin1, gpio.OUTPUT)
gpio.mode(pin2, gpio.OUTPUT)
gpio.mode(pin3, gpio.OUTPUT)
gpio.mode(pin4, gpio.OUTPUT)

local direction = {}

-- Para Esquerda
direction["left"] = function ()
    gpio.write(pin1, gpio.HIGH)
    gpio.write(pin2, gpio.LOW)
end

-- Para Direita
direction["right"] = function ()
    gpio.write(pin1, gpio.LOW)
    gpio.write(pin2, gpio.HIGH)
end


```

::right::

<br>
<br>



```lua
-- Reto
direction["up"] = function ()
    gpio.write(pin1, gpio.HIGH)
    gpio.write(pin2, gpio.HIGH)
end


-- Ré
direction["down"] = function ()
    gpio.write(pin1, gpio.LOW)
    gpio.write(pin2, gpio.LOW)
end

-- Para
direction["stop"] = function ()
    gpio.write(pin3, gpio.LOW)
    gpio.write(pin6, gpio.LOW)
end
```
