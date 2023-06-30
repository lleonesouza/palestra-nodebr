<template>
    <Slide>
        <h1>Uma ponte entre NodeMCU e NodeJS</h1>
        
        <div class="image-container">
            <div>
                <v-click at="2">
                    <img src="./imgs/lua-logo.png" class="logo-lua">
                </v-click>
                <v-click at="1">
                    <img src="./imgs/esp8266.png" class="logo-esp8266">
                </v-click>
                <v-click at="0">
                    <img src="./imgs/nodemcu-logo.png" class="logo-nodemcu">
                </v-click>
            </div>

            <div>
                <v-click at="3">
                    <img src="./imgs/ponte.png" class="ponte">
                </v-click>
                <v-click at="6">
                    <img src="./imgs/coap-rfc.png" class="logo-coap">
                </v-click>
            </div>
     
            <div>
                <v-click at="4">
                    <img src="./imgs/js-logo.png" class="logo-js">
                </v-click>
                <v-click at="5">
                    <img src="./imgs/nodejs-logo.png" class="logo-nodejs">
                </v-click>
            </div>
          
        </div>
    </Slide>
</template>
  
<style>
h1 {
    text-align: center;
}

.image-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo-nodemcu {
    position: absolute;
    bottom: 5%;
    width: 150px;
    height: auto;
}

.logo-esp8266 {
    position: absolute;
    bottom: 25%;
    width: 170px;
    height: auto;
}

.ponte {
    position: absolute;
    bottom: 0%;
    left: 22%;
    width: 550px;
    height: auto;
}

.logo-lua {
    position: absolute;
    bottom: 7%;
    left: 22%;
    width: 100px;
    height: auto;
}

.logo-js {
    position: absolute;
    right: 5%;
    top: 35%;
    width: 120px;
    height: auto;
}

.logo-nodejs {
    position: absolute;
    right: 10%;
    top: 15%;
    width: 160px;
    height: auto;
}

.logo-coap {
    position: absolute;
    right: 30%;
    top: 45%;
    width: 250px;
    height: auto;
}

</style>
  