---
---

# Vamos codar




---

# Receber dados de temperatura do DHT11


```lua
-- Digital Pin Number (int)
-- returns temp string humi string
local makeDHT11 = function (pinNumber)
    local dthModule = {}
    dthModule.read = function ()
        local status, temp, humi, temp_dec, humi_dec = dht.read11(pinNumber)
        
        print(status == dht.OK)
        print(status == dht.ERROR_CHECKSUM)
        print(status == dht.ERROR_TIMEOUT)

        return temp, humi
    end

    return dthModule
end

return makeDHT11
```

---

# Controller COAP para acionar o DHT11
```lua
local function makeControllers(cs)
    local controllers = {}
    -- Getters
    -- GETTING DATA
    -- coap post -p "test" -o coap://192.168.0.114:5683/v1/f/Data
    local function readDth()
        function Data(payload)
            
            local data = modules.Dht11.read()
            print(data)
          
            return data
        end

        cs:func("Data")
    end

    controllers.readDth = readDth

    return controllers
end

```


---

- module Motor
    - Run
    - Back
    - Turn left
    - Turn Right
- Controllers COAP
    - DHT
    - Motor
    - Health

- Wifi.lua
- Init.lua


# Javascript

- Service COAP
- Controllers
    - Health
    - Save DHT
    - Run
    - Back
    - Turn left
    - Turn Right
    