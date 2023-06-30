---
layout: image-right
image: pages/coding/nodejs/imgs/esquerda.gif
---
# Virar Esquerda

<br>
<br>
<br>

```lua {all|3,4|6,7|all}
local turnLeft = function()
        -- motor 1
        gpio.write(pin1, gpio.LOW)
        gpio.write(pin2, gpio.LOW)
        -- motor 2
        gpio.write(pin4, gpio.LOW)
        gpio.write(pin5, gpio.HIGH)
end
``` 


---
layout: image-right
image: pages/coding/nodejs/imgs/direita.gif
---

# Virar Direita

<br>
<br>
<br>

```lua {all|3,4|6,7|all}
local turnRight = function()
        -- motor 1
        gpio.write(pin1, gpio.LOW)
        gpio.write(pin2, gpio.HIGH)
        -- motor 2
        gpio.write(pin4, gpio.LOW)
        gpio.write(pin5, gpio.LOW)
end
``` 


---
layout: image-right
image: pages/coding/nodejs/imgs/reto.gif
---

# Frente



<br>
<br>
<br>

```lua {all|3,4|6,7|all}
local run = function()
        -- motor 1
        gpio.write(pin1, gpio.LOW)
        gpio.write(pin2, gpio.HIGH)
        -- motor 2
        gpio.write(pin4, gpio.LOW)
        gpio.write(pin5, gpio.HIGH)
end
``` 


---
layout: image-right
image: pages/coding/nodejs/imgs/ré.gif
---

# Ré



<br>
<br>
<br>

```lua {all|3,4|6,7|all}
local back = function()
        -- motor 1
        gpio.write(pin1, gpio.HIGH)
        gpio.write(pin2, gpio.LOW)
        -- motor 2
        gpio.write(pin4, gpio.HIGH)
        gpio.write(pin5, gpio.LOW)
end
``` 



---
layout: image-right
image: pages/coding/nodejs/imgs/ré.gif
---

# Parar

<br>
<br>
<br>

```lua {all|3,4|6,7|all}
local stop = function()
        -- motor 1
        gpio.write(pin1, gpio.LOW)
        gpio.write(pin2, gpio.LOW)
        -- motor 2
        gpio.write(pin4, gpio.LOW)
        gpio.write(pin5, gpio.LOW)
end
``` 

---
layout: image-right
image: pages/coding/nodejs/imgs/velocidade.gif
---

# Velocidade

<br>
<br>
<br>

```lua {all|1,2|4|5,6|all}
pwm.setup(pin0, 1000, 0)
pwm.setup(pin3, 1000, 0)

local setSpeed = function(speed) -- 0 ~ 1000
    pwm.setduty(pin0, speed)
    pwm.setduty(pin3, speed)
end
```

