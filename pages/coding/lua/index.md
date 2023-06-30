---
---

# temperatura e umidade
```lua {all|1,2|4,5,6,7,8|all}
-- reading DHT11
local temp, humi = dht.read11(pin)

-- json encodig
local data = sjson.encode({
    temperature = temp,
    humidity = humi
})

return data
```



---
layout: two-cols
---

# Motor
```lua {all|1,2,3,4|4,5,6,7,8|all}
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
